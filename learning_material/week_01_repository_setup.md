# Week 1 Learning Material: Repository Setup And Professional Framework

This workbook supports Week 1 of the advanced fire engineering and modelling portfolio. It is based on the local planning files `first_3_months_fire_portfolio_plan.md` and `advanced_fire_portfolio_codex_context.md`.

The aim of Week 1 is to build the professional framework before doing any modelling. By the end of the week, the portfolio should have a clear public purpose, disclaimer, standards-labelling approach, reusable templates, software setup notes, and a basic QA routine.

> This is self-directed learning material for a portfolio project. It is not certified fire engineering design advice, a fire risk assessment, a regulatory submission, or a safety approval.

## Weekly Working Rhythm

Use this rhythm for each 2-hour evening block:

| Time | Activity |
|---|---|
| 17:00-17:10 | Review today's task and previous notes |
| 17:10-18:00 | Main learning or technical setup |
| 18:00-18:10 | Short break |
| 18:10-18:50 | Exercise, writing output, or setup task |
| 18:50-19:00 | QA notes, learning log, and next step |

## Week 1 Outputs

By the end of Week 1, aim to have:

- Repository skeleton defined
- Public disclaimer prepared
- README purpose paragraph drafted
- Standards map created
- Knowledge-base structure planned
- Case-study template planned
- Report template drafted
- Software setup notes created
- Python shared scripts folder planned
- FDS device CSV plotter brief written
- Portfolio QA checklist created
- Decision log started
- Week 1 reflection written

---

## Day 1: Project Brief And Repository Skeleton

### Learning Objectives

- Understand what the portfolio is meant to prove.
- Separate the roles of GitHub, a final PDF portfolio, and a website.
- Establish the non-certified design disclaimer from the start.

### Key Concepts

A professional portfolio is not only a collection of outputs. It should show how you think, document assumptions, manage uncertainty, and communicate technical work.

For this project:

- GitHub shows reproducible workflow, inputs, scripts, templates, and documentation.
- The final PDF shows polished evidence for job applications and interviews.
- The website shows visual communication and project storytelling.
- The disclaimer prevents overclaiming and makes clear that the work is educational.

The intended professional identity is:

> A general fire engineering consultant candidate with advanced modelling strength, strong thermal-fluid background, and practical engineering/reporting capability.

### Reading Notes

Read the project purpose and disclaimer in your planning files. The most important point is that the portfolio should demonstrate learning, judgement, reproducible workflows, and professional communication without presenting the work as certified fire engineering design.

### Practical Exercise

Create or plan these top-level files:

```text
README.md
portfolio_plan.md
disclaimer.md
learning_log.md
skills_matrix.md
standards_map.md
references.md
.gitignore
```

Create or plan these top-level folders:

```text
00_project_management/
01_knowledge_base/
02_templates/
03_case_studies/
04_shared_scripts/
05_website/
06_final_outputs/
99_local_results_placeholder/
```

### Writing Task

Draft the first paragraph for `README.md`:

```markdown
This repository is a self-directed advanced fire engineering and modelling portfolio. It demonstrates fire engineering learning, FDS/Smokeview workflow development, Python post-processing, technical reporting, and professional documentation for consultancy-style case studies.
```

Then add a short status note:

```markdown
The work in this repository is educational and portfolio-based. It is not a certified fire engineering design, fire risk assessment, regulatory submission, or safety approval.
```

### Done Criteria

- The top-level structure is clear.
- The disclaimer exists or is ready to add.
- The README explains the learning purpose without claiming professional certification.

### Reflection Prompts

- What should a recruiter or consultant learn about me in 60 seconds?
- What must I avoid implying?
- Which outputs belong on GitHub, and which should stay local?

### Optional Stretch Task

Write three portfolio success statements, for example:

- I can document assumptions clearly.
- I can process model outputs reproducibly.
- I can explain modelling limitations.

---

## Day 2: Standards Map And Knowledge Base Structure

### Learning Objectives

- Separate UK, international, industrial, tool, and general engineering references.
- Understand why standards must be labelled carefully.
- Start a knowledge base that grows alongside case studies.

### Key Concepts

The portfolio is UK-prioritised but broad. Fire physics may be similar across jurisdictions, but regulation, terminology, approval routes, and acceptance criteria are not interchangeable.

Use labels whenever standards, guidance, or references are mentioned:

| Label | Meaning | Example |
|---|---|---|
| `[UK]` | UK-specific or England/Wales-specific context | Approved Document B, BS 9999, BS 7974 |
| `[International / US]` | US-origin or internationally referenced | NFPA guidance |
| `[International / industrial]` | Industrial, insurance, or multinational practice | FM Global-style risk engineering |
| `[Tool / model]` | Modelling documentation | FDS User Guide, Smokeview User Guide |
| `[General engineering]` | Physics and engineering principles | Heat transfer, combustion, fluid mechanics |

### Reading Notes

Approved Document B is published on GOV.UK as statutory guidance for fire safety matters within and around buildings in England. GOV.UK records updates and amendments, so check the current page before citing version-specific details in public work.

GOV.UK workplace fire safety guidance introduces the idea of a responsible person for non-domestic premises and the need to carry out and review fire risk assessments. Use this as broad UK context, not as a substitute for detailed professional guidance.

### Practical Exercise

Create or plan `standards_map.md` with this structure:

```markdown
# Standards And Guidance Map

## Labelling Convention

| Label | Meaning | Example |
|---|---|---|
| [UK] | UK-specific or England/Wales-specific context | Approved Document B, BS 9999, BS 7974 |
| [International / US] | US-origin or internationally referenced | NFPA guidance |
| [International / industrial] | Industrial, insurance, or multinational practice | FM Global-style risk engineering |
| [Tool / model] | Modelling documentation | FDS User Guide, Smokeview User Guide |
| [General engineering] | Physics and engineering principles | Heat transfer, combustion, fluid mechanics |

## Rule

International or US guidance must not be presented as automatically applicable to a UK project. Where non-UK references are used, their role must be explained.
```

Create or plan the first layer of the knowledge base:

```text
01_knowledge_base/
  01_fire_dynamics/
  02_fire_engineering_practice/
  03_international_and_industrial_practice/
  04_fds_modelling/
  05_evacuation_modelling/
  06_consultancy_skills/
```

### Writing Task

Add three initial entries to `references.md`:

```markdown
# References

## FDS And Smokeview

- [Tool / model] NIST FDS-SMV homepage: https://pages.nist.gov/fds-smv/
- [Tool / model] NIST FDS-SMV manuals: https://pages.nist.gov/fds-smv/manuals.html

## UK Fire Safety Context

- [UK] Approved Document B: https://www.gov.uk/government/publications/fire-safety-approved-document-b
- [UK] Workplace fire safety responsibilities: https://www.gov.uk/workplace-fire-safety-your-responsibilities
```

### Done Criteria

- Standards labels are defined.
- The UK vs international distinction is explicit.
- The knowledge-base folder structure is ready.

### Reflection Prompts

- Why is "physics is similar" not the same as "regulation is transferable"?
- Which labels will I use most in Month 1?
- What should I check before citing a standard or guidance document?

### Optional Stretch Task

Write a short note comparing these two statements:

```text
Poor: NFPA guidance applies to this UK case.
Better: NFPA guidance is used here as an international comparison only; UK applicability would require project-specific review against UK statutory guidance and relevant British Standards.
```

---

## Day 3: Case Study And Report Templates

### Learning Objectives

- Learn the shape of a consultancy-style technical report.
- Understand assumptions, exclusions, QA, and client questions.
- Build reusable case-study templates before modelling.

### Key Concepts

A case study is not just a model. It includes a brief, assumptions, method, results, limitations, references, and QA.

A good case study starts with a clear question. For example:

> What does this simplified FDS room fire model show about basic smoke and temperature output workflow?

That is much better than:

> Run a fire model.

The first version can be answered, documented, limited, and reviewed.

### Practical Exercise

Create or plan this reusable template folder:

```text
02_templates/case_study_template/
  README.md
  brief.md
  assumptions_register.md
  design_fire_register.md
  risk_register.md
  model_log.md
  qa_checklist.md
  report.md
  report_appendix.md
  website_summary.md
  figures/
  fds/
  pathfinder/
  pyrosim/
  scripts/
```

### Writing Task

Use this structure in `report.md`:

```markdown
# Report Title

## Document Control

| Field | Value |
|---|---|
| Project |  |
| Case study |  |
| Author |  |
| Date |  |
| Version |  |
| Status | Draft |

## Disclaimer

This case study is a simplified self-directed learning exercise. It is not a certified fire engineering design, fire risk assessment, regulatory submission, or safety approval.

## Executive Summary

## Client Question

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

### Done Criteria

- A future case can be created by copying the template.
- Report structure includes disclaimer, assumptions, limitations, and references.
- The template does not imply certified design approval.

### Reflection Prompts

- What makes a model result trustworthy enough to discuss?
- Where should uncertainty appear in a report?
- What is the difference between a client question and a modelling task?

### Optional Stretch Task

Draft a one-paragraph fictional brief for Case 00:

```markdown
This case study develops a simple single-room FDS model to demonstrate the basic workflow from input file preparation to Smokeview inspection and Python post-processing. The purpose is to learn model setup, output extraction, figure generation, and limitations reporting. The model is simplified and is not intended to represent a real building or design scenario.
```

---

## Day 4: Tool Installation And Version Recording

### Learning Objectives

- Understand the toolchain: FDS, Smokeview, Python, Git, and VS Code.
- Record software versions like a professional report would.
- Separate solver, visualisation, and post-processing roles.

### Key Concepts

FDS is the solver. Smokeview is the visualisation tool. Python is used for post-processing, plotting, summaries, and repeatable analysis. Git records the development history of the portfolio.

NIST describes FDS as a large-eddy simulation code for low-speed flows, with emphasis on smoke and heat transport from fires. Smokeview is the companion visualisation program for FDS and CFAST outputs.

Software versions matter because model behaviour, input syntax, and output formats can change. A report should make it possible to understand what toolchain produced the results.

### Practical Exercise

Create or plan `00_project_management/software_setup.md`:

```markdown
# Software Setup

| Tool | Version | Install path / command | Notes |
|---|---:|---|---|
| Operating system |  |  |  |
| FDS |  |  |  |
| Smokeview |  |  |  |
| Python |  |  |  |
| Git |  |  |  |
| VS Code |  |  |  |
```

Add this explanatory note:

```markdown
FDS is the solver. Smokeview is the visualisation tool. Python is used for post-processing, plotting, summaries, and repeatable analysis. Git records the development history of the portfolio.
```

### Writing Task

Record installation notes in this format:

```markdown
## Installation Notes

- FDS:
- Smokeview:
- Python:
- Git:
- VS Code:

## Known Issues

- None recorded yet.
```

### Done Criteria

- Versions or install paths are recorded.
- Any installation problem is documented.
- You know how you will verify FDS and Smokeview later.

### Reflection Prompts

- Why should reports include software versions?
- What could go wrong if only screenshots are saved?
- Which parts of the workflow need to be reproducible?

### Optional Stretch Task

Write the commands or checks you expect to use:

```powershell
python --version
git --version
fds
smokeview
```

Adjust the FDS and Smokeview commands if your installation uses different executable names or paths.

---

## Day 5: Python Environment And Shared Scripts

### Learning Objectives

- Understand why post-processing matters.
- Define the first shared script: an FDS device CSV plotter.
- Prepare for repeatable figures instead of manual spreadsheet work.

### Key Concepts

Consultancy-style modelling needs traceable results, not only visual impressions. Device outputs can become time-history plots for temperature, visibility, velocity, or other measured quantities.

A script should not silently produce misleading plots. It should report unclear inputs, missing columns, duplicated names, or unexpected file structure.

### Practical Exercise

Create or plan this folder:

```text
04_shared_scripts/
  README.md
  requirements.txt
  fds_devc_plotter.py
```

Suggested `requirements.txt`:

```text
pandas
matplotlib
```

### Writing Task

Write this script brief in `04_shared_scripts/README.md`:

```markdown
# Shared Scripts

## FDS Device CSV Plotter

The FDS device CSV plotter reads an FDS device output CSV, handles a possible units row, identifies time and device columns, plots each device against time, and saves figures to an output folder.

The script should report missing, duplicated, or unclear columns instead of silently producing a misleading figure.
```

Draft the expected command-line interface:

```text
python fds_devc_plotter.py path/to/device_output.csv --out figures/device_plots
```

### Done Criteria

- Python environment plan exists.
- Script requirements are defined.
- Dummy CSV testing is planned.

### Reflection Prompts

- What makes a plot reproducible?
- What should the script do if it cannot find a time column?
- What information should be included in a figure caption?

### Optional Stretch Task

Draft a dummy CSV for later testing:

```csv
Time,Temperature_1,Temperature_2
s,C,C
0,20,20
10,32,28
20,45,37
30,58,49
```

---

## Day 6: Weekly Review And Portfolio QA

### Learning Objectives

- Build a QA habit before technical complexity starts.
- Record decisions and unresolved issues.
- Finish Week 1 with a usable foundation.

### Key Concepts

QA is not a final polish step. It is part of daily work. A portfolio should show judgement, not just output volume.

Decision logs make assumptions visible. QA checklists make repeated work more reliable. Learning logs turn tasks into evidence of development.

### Practical Exercise

Create or plan:

```text
00_project_management/portfolio_quality_checklist.md
00_project_management/decision_log.md
learning_log.md
```

Suggested QA checklist:

```markdown
# Portfolio Quality Checklist

- [ ] Disclaimer included where needed
- [ ] Standards labelled correctly
- [ ] Assumptions recorded
- [ ] Limitations stated
- [ ] References included
- [ ] Large raw outputs kept local
- [ ] File names are clear
- [ ] README explains current status
```

Suggested decision log:

```markdown
# Decision Log

| Date | Decision | Reason | Alternatives Considered | Follow-up |
|---|---|---|---|---|
|  | Use public GitHub repository for selected portfolio outputs | Supports transparent portfolio evidence | Private-only portfolio | Keep heavy raw outputs local |
```

### Writing Task

Add this Week 1 learning-log entry:

```markdown
## Week 1 Reflection

This week I built the professional framework for the portfolio before starting modelling. I set up the intended repository structure, clarified the disclaimer, separated UK and international references, planned reusable templates, recorded the software setup process, and defined the first Python post-processing script.

The main lesson is that credible modelling work depends on documentation, assumptions, version control, and limitations as much as on the simulation itself.
```

### Done Criteria

- Week 1 reflection is written.
- QA checklist exists.
- Decision log exists.
- Repository is ready for Week 2 fire dynamics and first FDS input work.

### Reflection Prompts

- What is the strongest part of my Week 1 setup?
- What still feels vague?
- What must be fixed before I start Case 00?

### Optional Stretch Task

Write three GitHub issue titles for Week 2:

```text
Create first FDS input skeleton
Write HRR learning note
Document Smokeview workflow
```

---

## Week 1 Completion Checklist

```markdown
- [ ] Repository skeleton defined
- [ ] Public disclaimer prepared
- [ ] README purpose paragraph drafted
- [ ] Standards map created
- [ ] Knowledge-base structure planned
- [ ] Case-study template planned
- [ ] Report template drafted
- [ ] Software setup notes created
- [ ] Python shared scripts folder planned
- [ ] FDS device CSV plotter brief written
- [ ] Portfolio QA checklist created
- [ ] Decision log started
- [ ] Week 1 reflection written
```

## Official Reference Links

- [Tool / model] NIST FDS-SMV homepage: https://pages.nist.gov/fds-smv/
- [Tool / model] NIST FDS-SMV manuals: https://pages.nist.gov/fds-smv/manuals.html
- [UK] GOV.UK Approved Document B: https://www.gov.uk/government/publications/fire-safety-approved-document-b
- [UK] GOV.UK workplace fire safety responsibilities: https://www.gov.uk/workplace-fire-safety-your-responsibilities

## Notes For Week 2

Week 2 should move from professional setup into fire dynamics foundations and the first FDS input. Before starting Week 2, confirm that Week 1 outputs are present, the disclaimer is visible, and the standards-labelling rule is understood.
