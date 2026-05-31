# General Workflow SOP: FDS, Smokeview, Python, Git, And VS Code

## 1. Purpose

This standard operating procedure defines the repeatable workflow for the 6-month fire engineering and FDS portfolio project.

It is intended to cover most portfolio cases, including:

- simple FDS room fire examples
- smoke and tenability studies
- evacuation / ASET-RSET studies
- smoke control sensitivity studies
- battery or equipment fire risk studies
- industrial liquid spill or pool fire studies
- model credibility, sensitivity, and validation exercises

The goal is to create a traceable engineering workflow:

```text
brief -> assumptions -> model input -> simulation -> visual review -> data processing -> interpretation -> report -> QA -> git commit
```

This portfolio is a self-directed learning and professional development project. It is not a certified fire engineering design, fire risk assessment, regulatory submission, or safety approval.

## 2. Tool Roles

| Tool | Main role | Typical outputs |
|---|---|---|
| VS Code | Main working environment | Edited `.fds`, `.py`, `.md`, `.csv` files |
| Git | Version control and project history | Commits, branches, tags, change history |
| FDS | Fire/smoke simulation solver | `.out`, `.smv`, `.csv`, binary result files |
| Smokeview | Visual inspection and selected figures | screenshots, visual checks, animations if needed |
| Python | Repeatable post-processing | plots, summary tables, comparison figures |
| Markdown | Technical documentation and reports | briefs, assumptions, reports, logs |

Use VS Code as the control room. Use Git as the safety net. Use FDS to solve. Use Smokeview to inspect. Use Python to quantify. Use Markdown to explain.

## 3. Standard Case Folder Structure

Each case study should use a consistent structure.

```text
03_case_studies/
  case_XX_short_case_name/
    README.md
    brief.md
    assumptions_register.md
    design_fire_register.md
    risk_register.md
    model_log.md
    qa_checklist.md
    report.md
    website_summary.md
    fds/
      case_XX_baseline.fds
      case_XX_variant_01.fds
    scripts/
      case_specific_processing.py
    figures/
      selected_for_report/
    data_processed/
    notes/
```

Large raw simulation results should stay local unless they are small and intentionally selected for public evidence.

Recommended local-only folders:

```text
99_local_results_placeholder/
local_results/
run_outputs/
raw_outputs/
```

## 4. Git Tracking Policy

Commit files that explain, reproduce, or communicate the work:

- `.fds` input files
- Python scripts
- Markdown reports and notes
- selected final figures
- small example CSV files
- templates and checklists
- README files
- assumptions and decision logs

Do not normally commit heavy or temporary result files:

- `.s3d`
- `.sf`
- `.bf`
- large `.csv` result files
- large Smokeview exports
- temporary run folders
- generated cache files
- local virtual environments

Recommended `.gitignore` categories:

```gitignore
# FDS heavy outputs
*.s3d
*.sf
*.bf
*.prt5
*.smoke3d
*.sz

# Large/local results
local_results/
run_outputs/
raw_outputs/
99_local_results/

# Python
.venv/
__pycache__/
*.pyc

# OS/editor
.DS_Store
Thumbs.db
```

## 5. Standard Daily Workflow

Use this for normal 2-hour evening sessions.

| Time | Activity |
|---|---|
| 17:00-17:10 | Open VS Code, review previous notes, choose one task |
| 17:10-18:00 | Main technical work: input file, script, reading, or report |
| 18:00-18:10 | Short break |
| 18:10-18:50 | Run/check/process/write the day's output |
| 18:50-19:00 | Update log, QA notes, next step, and commit if useful |

If 3 hours are available, use the extra hour for report writing, QA, or Python post-processing rather than uncontrolled model changes.

## 6. Standard Case Workflow

### Step 1: Define The Case Question

Start each case with a short `brief.md`.

The brief should answer:

- What is the learning or engineering question?
- What is the simplified scenario?
- What is in scope?
- What is explicitly out of scope?
- What outputs will demonstrate success?

Good example:

```text
This case develops a simple FDS room fire model to demonstrate geometry setup, fire source definition, Smokeview inspection, device output extraction, Python plotting, and limitations reporting.
```

Poor example:

```text
Run an FDS model.
```

### Step 2: Record Assumptions Before Modelling

Create or update `assumptions_register.md`.

Minimum columns:

```markdown
| ID | Assumption | Reason | Evidence / source | Impact if wrong |
|---|---|---|---|---|
| A01 |  |  |  |  |
```

Record assumptions about:

- geometry
- fire source
- materials
- ventilation
- mesh resolution
- occupants, if relevant
- tenability criteria, if relevant
- software versions
- simplifications

### Step 3: Create Or Update The FDS Input

Create the `.fds` file inside the case `fds/` folder.

For every FDS input, check:

- `&HEAD` has a clear `CHID`
- `&MESH` dimensions and cell counts are intentional
- geometry is simplified but documented
- fire source is documented
- vents/open boundaries are documented
- output devices are useful
- slice files support visual interpretation
- `&TIME` is appropriate for the learning goal
- file ends with `&TAIL /`

Use clear names:

```text
case_00_baseline.fds
case_01_baseline.fds
case_01_door_open.fds
case_01_hrr_sensitivity_high.fds
```

### Step 4: Run FDS

Run from the relevant case folder or FDS folder.

Example:

```powershell
cd 03_case_studies\case_00_first_fds_room_fire\fds
fds case_00_baseline.fds
```

For parallel runs, use MPI/OpenMP only when the model is large enough and structured for it.

Example:

```powershell
fds_local -p 4 -o 1 case_01_baseline.fds
```

General rule:

- one small mesh will not use many CPU cores efficiently
- multiple meshes can use MPI processes
- OpenMP can help within a mesh, but speedup is not guaranteed
- test performance before assuming more cores means faster runtime

### Step 5: Read The FDS Output Log

Always inspect the `.out` file before trusting results.

Check for:

- FDS version
- number of MPI processes
- mesh dimensions and total cells
- warnings or errors
- pressure iteration behaviour
- maximum CFL number
- simulation completion status
- abnormal termination

Record key run information in `model_log.md`.

Suggested format:

```markdown
| Run ID | Input file | Date | FDS version | Runtime | Status | Notes |
|---|---|---|---|---|---|---|
| R01 | case_00_baseline.fds |  |  |  | Completed / failed |  |
```

### Step 6: Inspect In Smokeview

Open the `.smv` file:

```powershell
smokeview case_00_baseline.smv
```

Use Smokeview to check:

- geometry is correct
- obstructions are in the expected places
- vents and openings are correct
- fire source is in the expected location
- smoke movement is plausible
- slices are useful
- visual outputs support the report question

Do not treat Smokeview images alone as proof. They are visual evidence, not the full analysis.

Save selected figures only when they support the report.

Suggested figure naming:

```text
fig_01_geometry_overview.png
fig_02_temperature_slice_60s.png
fig_03_smoke_layer_view.png
```

### Step 7: Process Results With Python

Use Python for quantitative and repeatable analysis.

Common FDS files to process:

- `*_devc.csv`
- `*_hrr.csv`
- `*_steps.csv`
- selected summary CSV files

Typical Python outputs:

- HRR vs time plots
- device temperature plots
- visibility or smoke-layer plots
- comparison plots between cases
- sensitivity summary tables

Example command:

```powershell
python 04_shared_scripts/fds_devc_plotter.py path\to\case_devc.csv --out figures
```

Python scripts should:

- read input paths from command-line arguments
- create output folders if needed
- label axes with units
- save figures with clear names
- report missing or unclear columns
- avoid hard-coded local paths where possible

### Step 8: Interpret Results

Write interpretation after visual and numerical review.

Separate:

- what the model shows
- what the model does not show
- what is uncertain
- what assumptions control the result
- what would be needed for a real project

Use cautious language:

```text
The simplified model indicates...
Under the stated assumptions...
This result should not be interpreted as a design conclusion...
Further work would require...
```

Avoid overclaiming:

```text
This proves the building is safe.
This design complies.
This result can be used for approval.
```

### Step 9: Write Or Update The Report

Each serious case should have a `report.md`.

Recommended structure:

```markdown
# Case Title

## Document Control
## Disclaimer
## Executive Summary
## Client / Study Question
## Scope And Exclusions
## Scenario Description
## Assumptions
## Method
## Results
## Interpretation
## Limitations
## Recommendations Or Learning Points
## QA Checklist
## References
## Appendix
```

Every report should include:

- disclaimer
- assumptions
- limitations
- software versions
- figure captions
- standards labels
- reproducibility notes

### Step 10: QA Before Committing

Use `qa_checklist.md` before each milestone commit.

Minimum QA checklist:

```markdown
- [ ] Disclaimer included
- [ ] Case question is clear
- [ ] Assumptions are recorded
- [ ] FDS input file is named clearly
- [ ] FDS output log checked
- [ ] Smokeview geometry reviewed
- [ ] Python plots are reproducible
- [ ] Figures have clear names and captions
- [ ] Limitations are stated
- [ ] References are labelled
- [ ] Large raw outputs are excluded from Git
- [ ] Git status checked before commit
```

### Step 11: Commit To Git

Check status:

```powershell
git status
```

Review changes:

```powershell
git diff
```

Add specific files:

```powershell
git add README.md
git add 03_case_studies\case_00_first_fds_room_fire
git add 04_shared_scripts
```

Commit with a clear message:

```powershell
git commit -m "Add case 00 baseline FDS workflow"
```

Push:

```powershell
git push
```

Good commit messages:

```text
Add case 00 baseline FDS input
Document case 01 assumptions
Add FDS device CSV plotter
Add Smokeview figures for case 01
Draft case 02 ASET-RSET report
```

## 7. Weekly Workflow

At the end of each week:

- update `learning_log.md`
- update `skills_matrix.md`
- update `decision_log.md`
- review open tasks
- check whether reports contain disclaimers and limitations
- check that large raw outputs are not staged
- push completed work to GitHub

Suggested weekly reflection:

```markdown
## Week X Reflection

### What I completed

### What I learned technically

### What I learned about fire engineering judgement

### What needs more work

### Next week's priority
```

## 8. Standards And References Rule

Because the portfolio is UK-prioritised but broad, label references clearly:

| Label | Meaning |
|---|---|
| `[UK]` | UK-specific or England/Wales-specific context |
| `[International / US]` | US-origin or internationally referenced |
| `[International / industrial]` | Industrial, insurance, or multinational practice |
| `[Tool / model]` | Modelling documentation |
| `[General engineering]` | Physics or engineering fundamentals |

Do not imply that an international or US standard automatically applies to a UK project. If a non-UK reference is used, explain whether it is background learning, comparison, or tool guidance.

## 9. Software Version Recording

Record software versions in `00_project_management/software_setup.md` and in serious case reports.

Suggested table:

```markdown
| Tool | Version | Notes |
|---|---|---|
| FDS |  |  |
| Smokeview |  |  |
| Python |  |  |
| Git |  |  |
| VS Code |  |  |
| Operating system |  |  |
```

Useful checks:

```powershell
python --version
git --version
fds
smokeview
```

Adjust commands if the local installation uses different executable names or full paths.

## 10. Troubleshooting Routine

When something fails, do not immediately change many things.

Use this order:

1. Read the exact error message.
2. Check the `.out` file.
3. Confirm the input file path and working directory.
4. Confirm the FDS file ends correctly with `&TAIL /`.
5. Check recent edits with `git diff`.
6. Make one small change.
7. Rerun.
8. Record the issue and fix in `model_log.md` or `decision_log.md`.

Common issues:

| Symptom | First check |
|---|---|
| FDS does not start | command path, file path, syntax error |
| Smokeview does not open expected model | correct `.smv` file and working directory |
| CPU usage is low | mesh count, model size, MPI/OpenMP settings |
| Python script fails | CSV path, column names, virtual environment |
| Git wants to add huge files | `.gitignore` and raw output folders |
| Report feels weak | missing question, assumptions, or limitations |

## 11. Milestone Definitions

Use these milestones for each case.

| Milestone | Meaning |
|---|---|
| M1 Brief complete | Case question, scope, and exclusions are written |
| M2 Baseline input complete | FDS input is ready for first serious run |
| M3 Baseline run reviewed | `.out` and Smokeview checks are complete |
| M4 Data processed | Python plots and tables are generated |
| M5 Report drafted | Results, interpretation, and limitations are written |
| M6 QA complete | Checklist complete and public outputs reviewed |
| M7 Published | Relevant files committed and pushed |

## 12. Final Rule

For every case, preserve the chain of reasoning:

```text
question -> assumptions -> input file -> run log -> visual review -> processed data -> interpretation -> limitations -> commit
```

If that chain is clear, the portfolio will show professional judgement even while the case studies remain simplified learning exercises.
