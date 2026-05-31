# Codex Context File — Advanced Fire Engineering and Modelling Portfolio

**Document version:** 0.1  
**Prepared for:** Codex-assisted repository setup and long-term project planning  
**Project duration:** 6 months  
**Working pattern:** 2 hours/day, 6 days/week, normally after 17:00 UK time  
**Target career direction:** General fire engineering consultant with advanced modelling strength  
**Primary region:** UK first, with broad exposure to international and industrial practice  
**Portfolio type:** Public GitHub repository + final PDF portfolio + website  
**Important limitation:** This is a self-directed learning and portfolio project. It is not a certified fire engineering design.

---

## 1. Project Purpose

The purpose of this project is to build a public, structured, technically credible portfolio demonstrating capability in:

- Fire engineering fundamentals
- Fire CFD and smoke modelling
- Evacuation modelling
- ASET/RSET-style reasoning
- Smoke control sensitivity studies
- Battery/equipment fire risk studies
- Industrial liquid spill/pool fire consequence modelling
- Model validation, sensitivity, and uncertainty
- Consultancy-style technical reporting
- Python-based post-processing and automation
- GitHub-based software/research project organisation
- Website-based visual communication of engineering work

The intended career positioning is:

> General fire engineering consultant with advanced modelling strength.

The portfolio should show broad learning across building fire engineering, fire science, industrial fire risk, evacuation modelling, and modelling credibility.

The project should avoid presenting the author as a certified fire engineer. The goal is to demonstrate learning, judgement, reproducible workflows, and professional communication.

---

## 2. Public Disclaimer

This disclaimer must appear in:

- `disclaimer.md`
- repository `README.md`
- every case study report
- website footer
- final PDF portfolio

```text
This portfolio is a self-directed learning and professional development project in fire engineering and fire modelling. It is intended to demonstrate modelling workflow, technical reasoning, data processing, and consultancy-style reporting.

The case studies are simplified training exercises unless explicitly stated otherwise. They are not certified fire engineering designs, fire risk assessments, regulatory submissions, or safety approvals. The results must not be used for real-world design, compliance, emergency planning, or operational decisions.

All assumptions, scenarios, geometries, and design fires are simplified for educational purposes. Any real project would require competent professional review, project-specific data, applicable statutory guidance, stakeholder consultation, and formal quality assurance.
```

---

## 3. Important Planning Decisions Already Made

### 3.1 Career/portfolio direction

The selected portfolio direction is **hybrid**:

- UK building fire engineering awareness
- Advanced fire CFD and smoke modelling
- Evacuation and ASET/RSET modelling
- Industrial fire risk
- Battery/equipment fire risk
- Liquid spill/pool fire modelling
- Modelling validation and uncertainty

### 3.2 Target identity

The portfolio should position the author as:

> A general fire engineering consultant candidate with advanced modelling strength, strong thermal-fluid background, and practical engineering/reporting capability.

### 3.3 Tool stack

Use:

- FDS
- Smokeview
- Python
- Markdown
- GitHub
- ParaView
- PyroSim
- Pathfinder
- PDF outputs
- Website outputs

### 3.4 Repository policy

- Repository is public.
- Heavy simulation results stay local.
- Final selected figures, reports, scripts, input files, and documentation may be public.
- Raw outputs should not be committed unless small and intentionally selected.

### 3.5 Report policy

Every serious case study must have a final consultancy-style report.

### 3.6 PhD separation policy

The author’s PhD work should remain separate.

The portfolio may include a fictional industrial liquid spill/pool fire case, but it must not use unpublished PhD data, direct PhD experimental geometries, or confidential/sensitive research material.

### 3.7 Physical experiment policy

The portfolio is modelling/reporting only for now.

No physical fire experiments are included in this six-month portfolio plan.

---

## 4. UK vs International/Industrial Practice

The portfolio is UK-priority, but broad. For every case study, explicitly label whether a reference, standard, or guidance document is:

- `[UK]`
- `[International]`
- `[US/NFPA]`
- `[Industrial/Insurance]`
- `[Tool/Model]`
- `[General fire science]`

### 4.1 UK-specific context

UK building fire engineering often involves:

- Approved Document B
- Building Regulations
- BS 9999
- BS 7974
- BS 5839
- fire strategy reports
- means of escape
- smoke control
- performance-based fire engineering
- Building Control / regulatory review
- Building Safety Regulator context for relevant buildings
- Fire Safety Order and responsible person duties for non-domestic premises

### 4.2 International / industrial context

International and industrial fire consultancy may involve:

- NFPA standards
- FM Global Data Sheets
- API / IEC / ISO standards
- process safety concepts
- insurance risk engineering
- asset protection
- business interruption
- hazardous-area and industrial risk context
- AHJ-style approval routes
- multinational client standards

### 4.3 Practical difference

The physics is broadly the same:

- combustion
- heat release
- smoke transport
- radiation
- convection
- ventilation effects
- evacuation timing
- uncertainty

The differences are mainly:

- regulation
- terminology
- acceptance criteria
- documentation style
- approval route
- stakeholder expectations
- risk ownership

### 4.4 Standards labelling rule

Whenever standards are mentioned, label them clearly:

```text
[UK] Approved Document B
[UK] BS 9999
[UK] BS 7974
[UK] BS 5839
[International / US] NFPA 101
[International / US] NFPA 92
[International / US] NFPA 921
[International / industrial] FM Global Data Sheets
[Tool / model] FDS User Guide
[Tool / model] FDS Validation Guide
[General engineering] Heat transfer, fluid mechanics, combustion, risk analysis
```

Do not imply that an international or US standard automatically applies to a UK project.

---

## 5. Source References for Planning

These are source links for the project context. Codex should preserve them in `references.md` but should not invent interpretations beyond the notes below.

### 5.1 FDS and Smokeview

- NIST FDS-SMV main page: https://pages.nist.gov/fds-smv/
- NIST FDS-SMV manuals page: https://pages.nist.gov/fds-smv/manuals.html

Planning notes:

- FDS is described by NIST as a large-eddy simulation code for low-speed flows with emphasis on smoke and heat transport from fires.
- Smokeview is the visualisation program used to display output from FDS and CFAST simulations.
- The NIST manuals page lists current release version: FDS 6.11.0, SMV 6.11.0.
- The manuals page provides the FDS User’s Guide, Technical Reference Guide, Verification Guide, Validation Guide, and Smokeview guides.

### 5.2 UK Approved Document B

- GOV.UK Approved Document B page: https://www.gov.uk/government/publications/fire-safety-approved-document-b

Planning notes:

- GOV.UK describes Approved Document B as building regulation guidance in England covering fire safety matters within and around buildings.
- The page applies to England.
- The page lists versions incorporating 2020, 2022, and 2025 amendments, collated with 2026 and 2029 amendments.
- Always check the current version before relying on it.

### 5.3 PyroSim

- PyroSim: https://www.thunderheadeng.com/pyrosim/

Planning notes:

- PyroSim is a graphical interface for FDS-based fire and smoke modelling.
- Use PyroSim to assist model creation, geometry handling, and case setup.
- Do not use PyroSim as a substitute for understanding FDS input files.

### 5.4 Pathfinder

- Pathfinder: https://www.thunderheadeng.com/pathfinder/

Planning notes:

- Pathfinder is evacuation and crowd movement simulation software.
- Use Pathfinder for evacuation/egress modelling demonstrations.
- Treat evacuation outputs as scenario-based estimates, not absolute truth.

---

## 6. Repository Structure

Create the repository with this structure:

```text
advanced-fire-engineering-portfolio/
│
├── README.md
├── portfolio_plan.md
├── disclaimer.md
├── learning_log.md
├── skills_matrix.md
├── standards_map.md
├── references.md
├── .gitignore
│
├── 00_project_management/
│   ├── six_month_roadmap.md
│   ├── weekly_schedule.md
│   ├── decision_log.md
│   ├── issue_tracker_guidance.md
│   ├── codex_task_list.md
│   └── portfolio_quality_checklist.md
│
├── 01_knowledge_base/
│   ├── 01_fire_dynamics/
│   │   ├── heat_release_rate.md
│   │   ├── fire_growth_curves.md
│   │   ├── compartment_fire_basics.md
│   │   ├── plumes_ceiling_jets_smoke_layers.md
│   │   ├── radiation_convection_conduction.md
│   │   ├── pool_and_spill_fires.md
│   │   ├── ventilation_controlled_fires.md
│   │   └── smoke_visibility_toxicity.md
│   │
│   ├── 02_fire_engineering_practice/
│   │   ├── uk_regulatory_context.md
│   │   ├── approved_document_b_notes.md
│   │   ├── bs_9999_notes.md
│   │   ├── bs_7974_notes.md
│   │   ├── performance_based_design.md
│   │   ├── aset_rset_method.md
│   │   ├── fire_strategy_reports.md
│   │   └── fire_risk_assessment_practice.md
│   │
│   ├── 03_international_and_industrial_practice/
│   │   ├── nfpa_overview.md
│   │   ├── industrial_fire_risk.md
│   │   ├── property_protection_vs_life_safety.md
│   │   ├── battery_energy_storage_fire_risk.md
│   │   ├── insurance_risk_engineering.md
│   │   └── ahj_and_approval_routes.md
│   │
│   ├── 04_fds_modelling/
│   │   ├── fds_input_file_structure.md
│   │   ├── mesh_resolution.md
│   │   ├── boundary_conditions.md
│   │   ├── design_fire_selection.md
│   │   ├── devices_slices_boundaries.md
│   │   ├── smokeview_workflow.md
│   │   ├── paraview_workflow.md
│   │   └── verification_validation_uncertainty.md
│   │
│   ├── 05_evacuation_modelling/
│   │   ├── pathfinder_basics.md
│   │   ├── occupant_characteristics.md
│   │   ├── pre_movement_time.md
│   │   ├── route_choice.md
│   │   ├── congestion_and_bottlenecks.md
│   │   └── aset_rset_linking.md
│   │
│   └── 06_consultancy_skills/
│       ├── client_brief_interpretation.md
│       ├── assumptions_register.md
│       ├── design_fire_register.md
│       ├── risk_register.md
│       ├── technical_report_writing.md
│       ├── qa_review_process.md
│       ├── limitations_and_disclaimers.md
│       └── presenting_results_to_clients.md
│
├── 02_templates/
│   ├── case_study_template/
│   │   ├── README.md
│   │   ├── brief.md
│   │   ├── assumptions_register.md
│   │   ├── design_fire_register.md
│   │   ├── model_log.md
│   │   ├── qa_checklist.md
│   │   ├── report.md
│   │   ├── report_appendix.md
│   │   ├── figures/
│   │   ├── fds/
│   │   ├── pathfinder/
│   │   ├── pyrosim/
│   │   ├── scripts/
│   │   └── website_summary.md
│   │
│   ├── report_templates/
│   │   ├── full_consultancy_report_template.md
│   │   ├── short_case_study_template.md
│   │   ├── executive_summary_template.md
│   │   └── limitations_statement_template.md
│   │
│   ├── spreadsheet_templates/
│   │   ├── assumptions_register_template.csv
│   │   ├── risk_register_template.csv
│   │   ├── design_fire_register_template.csv
│   │   └── sensitivity_matrix_template.csv
│   │
│   └── codex_prompts/
│       ├── create_case_folder.md
│       ├── generate_fds_variants.md
│       ├── postprocess_fds_outputs.md
│       ├── create_report_figures.md
│       ├── check_report_completeness.md
│       └── build_website_project_page.md
│
├── 03_case_studies/
│   ├── case_00_first_fds_room_fire/
│   ├── case_01_makerspace_smoke_tenability/
│   ├── case_02_aset_rset_and_pathfinder/
│   ├── case_03_smoke_control_sensitivity/
│   ├── case_04_battery_charging_enclosure_fire_risk/
│   ├── case_05_industrial_liquid_spill_fire/
│   └── case_06_model_validation_uncertainty/
│
├── 04_shared_scripts/
│   ├── fds_devc_plotter.py
│   ├── compare_fds_cases.py
│   ├── sensitivity_summary.py
│   ├── generate_case_summary_table.py
│   ├── image_compressor.py
│   ├── report_figure_indexer.py
│   └── requirements.txt
│
├── 05_website/
│   ├── README.md
│   ├── src/
│   ├── public/
│   ├── case_study_data/
│   └── build_notes.md
│
├── 06_final_outputs/
│   ├── portfolio_summary.pdf
│   ├── cv_attachment_fire_engineering_portfolio.pdf
│   ├── case_study_one_pagers/
│   ├── interview_talking_points.md
│   └── skills_evidence_matrix.md
│
└── 99_local_results_placeholder/
    └── README.md
```

---

## 7. Git Ignore Policy

Use a `.gitignore` like this:

```gitignore
# Heavy FDS outputs
*.smv
*.sf
*.bf
*.s3d
*.prt5
*.q
*_devc.csv
*_hrr.csv
*_slcf.csv
*_bndf.csv
*_prof.csv
*_mass.csv
*_line.csv
*_cpu.csv
*.out
*.err

# Smokeview / visualisation large files
*.avi
*.mp4
*.mov
*.vtk
*.vtu
*.pvtu

# PyroSim / Pathfinder heavy or licence-sensitive files
*.psm.bak
*.pfr.bak

# Local-only result folders
local_results/
outputs_raw/
simulation_outputs/
smokeview_exports_full/
pathfinder_results_full/

# Python
__pycache__/
*.pyc
.venv/
venv/

# OS
.DS_Store
Thumbs.db
```

Note: If selected small CSV examples are needed for reproducible demo scripts, place them in a specific `sample_data/` folder and override the ignore rule explicitly.

---

## 8. Case Study Set

The portfolio contains seven case studies. Case 00 is a foundation case. Cases 01-06 are serious portfolio cases.

---

### Case 00 — First FDS Room Fire Workflow

**Folder:**

```text
03_case_studies/case_00_first_fds_room_fire/
```

**Purpose:**  
Foundation exercise.

**Type:**  
Modelling workflow demonstrator.

**Real-world basis:**  
Fictional simple room.

**Skills demonstrated:**

- FDS input file structure
- Smokeview
- basic devices and slices
- Python plotting
- simple assumptions log
- basic report writing

**Deliverables:**

- FDS input file
- Smokeview screenshots
- Python plots
- README
- short report
- model log

**Not intended as:**  
A major CV case study. It is evidence of progression and foundation workflow.

---

### Case 01 — Makerspace Smoke Tenability Study

**Folder:**

```text
03_case_studies/case_01_makerspace_smoke_tenability/
```

**Purpose:**  
First serious consultancy-style case.

**Type:**  
UK building fire engineering + fire CFD.

**Real-world basis:**  
Simplified and anonymised makerspace/workshop environment.

**Client/design question:**

> In a small workshop/makerspace fire scenario, how quickly do smoke and heat conditions become challenging at eye level, and what variables most affect tenability?

**Skills demonstrated:**

- room/corridor fire modelling
- smoke layer interpretation
- visibility analysis
- temperature analysis
- design fire assumptions
- tenability discussion
- UK fire engineering framing
- limitations writing

**UK-specific knowledge coverage:**

- Approved Document B context
- fire strategy thinking
- basic means of escape awareness
- limitations of simplified CFD

**Outputs:**

- FDS model
- Smokeview screenshots
- temperature plots
- visibility plots
- assumptions register
- design fire register
- final consultancy-style PDF report

---

### Case 02 — ASET/RSET and Pathfinder Evacuation Study

**Folder:**

```text
03_case_studies/case_02_aset_rset_and_pathfinder/
```

**Purpose:**  
Connect fire modelling output to evacuation modelling.

**Type:**  
Evacuation / life safety / performance-based design.

**Real-world basis:**  
Simplified teaching space, makerspace, or lab.

**Client/design question:**

> Does the available safe escape time exceed the required safe escape time for a simplified fire scenario?

**Skills demonstrated:**

- Pathfinder basics
- occupant loading
- pre-movement time assumptions
- route choice
- bottleneck identification
- ASET/RSET comparison
- uncertainty in human behaviour

**Important limitation:**  
Frame this as a method demonstration, not a real compliance assessment.

**Outputs:**

- Pathfinder model
- evacuation time outputs
- evacuation plots
- ASET/RSET table
- assumptions register
- final report

---

### Case 03 — Smoke Control Sensitivity Study

**Folder:**

```text
03_case_studies/case_03_smoke_control_sensitivity/
```

**Purpose:**  
Show practical design-option comparison.

**Type:**  
Building fire engineering + smoke control.

**Real-world basis:**  
Simplified corridor, atrium, workshop, or plant room.

**Client/design question:**

> How do different ventilation or smoke extraction assumptions affect visibility and temperature conditions?

**Skills demonstrated:**

- comparison of scenarios
- mechanical/natural ventilation assumptions
- smoke extraction sensitivity
- reporting design options
- communicating uncertainty
- practical recommendation writing

**Scenario variants:**

```text
A — door closed / limited leakage
B — door open
C — natural vent added
D — mechanical extract added
E — larger design fire
```

**Outputs:**

- multi-case FDS comparison
- sensitivity plots
- visual comparison figures
- engineering recommendation section
- final report

---

### Case 04 — Battery Charging Enclosure Fire Risk Study

**Folder:**

```text
03_case_studies/case_04_battery_charging_enclosure_fire_risk/
```

**Purpose:**  
Industrial/current-topic risk case.

**Type:**  
Battery/equipment fire risk + smoke consequence.

**Real-world basis:**  
3D printer farm, makerspace battery charging area, e-bike battery cabinet, or small equipment storage area.

**Client/design question:**

> What are the credible fire scenarios for a small battery charging/storage area, and what controls would reduce consequence?

**Skills demonstrated:**

- hazard identification
- scenario matrix
- risk register
- conservative modelling assumptions
- ventilation and smoke spread
- mitigation hierarchy
- risk-based communication

**Knowledge coverage:**

- battery fire risk basics
- detection
- separation
- ventilation
- emergency response
- uncertainty and limitations

**Outputs:**

- risk assessment-style report
- optional simplified FDS consequence model
- risk matrix
- recommended controls
- final report

---

### Case 05 — Industrial Liquid Spill Fire

**Folder:**

```text
03_case_studies/case_05_industrial_liquid_spill_fire/
```

**Purpose:**  
Link thermal-fluid strength to fire consulting without using PhD work.

**Type:**  
Industrial fire risk / pool fire / spill fire.

**Real-world basis:**  
Fictional plant room or fuel handling area.

**Client/design question:**

> What are the thermal and smoke consequences of a credible liquid fuel spill fire under different ventilation conditions?

**Skills demonstrated:**

- spill/pool fire physics
- heat release rate assumptions
- ventilation/crossflow effect
- flame/smoke movement interpretation
- industrial consequence analysis
- thermal radiation discussion

**PhD separation rule:**

- Use fictional geometry.
- Use public/literature-style assumptions only.
- Do not use unpublished PhD data.
- Do not reproduce the PhD experimental setup directly.
- Do not present the case as a PhD result.

**Outputs:**

- consequence modelling report
- design fire register
- sensitivity cases
- final report

---

### Case 06 — Model Validation, Sensitivity, and Credibility Study

**Folder:**

```text
03_case_studies/case_06_model_validation_uncertainty/
```

**Purpose:**  
Demonstrate professional modelling judgement.

**Type:**  
Modelling quality / verification / uncertainty.

**Client/design question:**

> How sensitive are the modelling conclusions to mesh size, HRR, ventilation, and output location?

**Skills demonstrated:**

- mesh sensitivity
- HRR sensitivity
- ventilation sensitivity
- output-device sensitivity
- limitations writing
- modelling credibility
- defensible interpretation
- avoiding overclaiming

**Knowledge coverage:**

- FDS Verification Guide
- FDS Validation Guide
- model uncertainty
- QA process
- professional reporting

**Outputs:**

- modelling credibility report
- comparison plots
- QA checklist
- “what this model can and cannot support” section
- final report

---

## 9. Report Template for Every Serious Case Study

Every serious case study should include the following structure.

```text
Title page
- Project title
- Case study number
- Version
- Date
- Author
- Portfolio disclaimer

Document control
- Version
- Date
- Status
- Change summary
- Review status

Executive summary
- Objective
- Method
- Main findings
- Key limitations
- Recommendations

1. Introduction
- Background
- Purpose
- Scope
- Exclusions
- Portfolio status

2. Client / design question
- What decision is this study trying to support?
- What options are being compared?
- What information is missing?
- What assumptions are required?

3. Fire safety objectives
- Life safety
- Property protection
- Business continuity
- Environmental protection
- Firefighter access / operational safety

4. Regulatory / guidance context
- UK-specific guidance if applicable
- International guidance if applicable
- Tool/model references
- Explicit note: not a compliance design

5. Scenario definition
- Geometry
- Occupancy / use case
- Fire source
- Ventilation
- Detection/suppression assumptions
- Failure scenarios
- Exclusions

6. Design fire
- Fuel
- Ignition location
- HRR curve
- Growth rate
- Peak HRR
- Soot yield if used
- CO yield if used
- Radiative fraction
- Justification
- Sensitivity cases

7. Modelling method
- Software and version
- Geometry preparation
- Mesh
- Boundary conditions
- Material assumptions
- Devices and output quantities
- Simulation duration
- Visualisation workflow
- Post-processing workflow

8. Assessment criteria
- Temperature
- Visibility
- Smoke layer height
- Radiation
- CO/FED if included
- ASET/RSET if included
- Risk ranking criteria if applicable

9. Results
- Smoke movement
- Temperature development
- Visibility development
- Flow paths
- Evacuation outputs if applicable
- Key plots
- Key screenshots

10. Sensitivity and uncertainty
- Mesh sensitivity
- HRR sensitivity
- Ventilation sensitivity
- Occupant behaviour sensitivity
- Conservative assumptions
- Non-conservative assumptions

11. Engineering interpretation
- What the results mean
- What design decision they could support
- What should not be concluded
- Comparison between cases
- Practical implications

12. Recommendations
- Design improvements
- Operational controls
- Further modelling
- Further data required
- Priority actions

13. Limitations
- Simplified geometry
- Input uncertainty
- Model limitations
- Excluded physics
- Non-certified portfolio status

14. Conclusion
- Short answer to the client question
- Main technical lesson
- Professional development lesson

Appendices
- FDS input summary
- Pathfinder input summary if applicable
- Assumptions register
- Design fire register
- Risk register
- QA checklist
- Full plots
- References
```

---

## 10. Required Registers and Templates

### 10.1 Assumptions register

```markdown
| ID | Category | Assumption | Reason | Evidence/source | Effect if wrong | Conservative? | Status |
|---|---|---|---|---|---|---|---|
```

### 10.2 Design fire register

```markdown
| Scenario | Fuel/source | Growth rate | Peak HRR | Duration | Soot yield | CO yield | Justification | Sensitivity case |
|---|---|---:|---:|---:|---:|---:|---|---|
```

### 10.3 Risk register

```markdown
| Hazard | Cause | Consequence | Existing control | Likelihood | Severity | Risk rating | Recommended control |
|---|---|---|---|---:|---:|---:|---|
```

### 10.4 Model QA checklist

```markdown
[ ] Software version recorded
[ ] Units checked
[ ] Geometry checked
[ ] Mesh resolution recorded
[ ] HRR assumptions recorded
[ ] Ventilation assumptions recorded
[ ] Material assumptions recorded
[ ] Output devices named clearly
[ ] Simulation completed without fatal errors
[ ] Visual results reviewed
[ ] Numerical outputs plotted
[ ] Sensitivity cases completed
[ ] Limitations stated
[ ] Claims match evidence
[ ] Public disclaimer included
```

### 10.5 Document control table

```markdown
| Version | Date | Status | Change summary | Reviewer |
|---|---|---|---|---|
| 0.1 | YYYY-MM-DD | Draft | Initial draft | Self-review |
```

---

## 11. Knowledge Coverage Plan

### 11.1 Fire science

| Topic | Case where applied |
|---|---|
| Heat release rate | All FDS cases |
| Fire growth curves | Cases 01, 03, 04 |
| Compartment fire behaviour | Cases 01, 03 |
| Plumes, ceiling jets, smoke layers | Cases 00, 01, 03 |
| Visibility and smoke production | Cases 01, 03, 04 |
| Radiation and heat transfer | Cases 04, 05 |
| Pool/spill fires | Case 05 |
| Ventilation-controlled fires | Cases 03, 05 |
| Crossflow/wind effects | Case 05 |
| Toxicity/FED | Optional in later versions |

### 11.2 Fire engineering practice

| Topic | Case where applied |
|---|---|
| UK regulatory context | Cases 01, 02, 03 |
| Approved Document B awareness | Cases 01, 02, 03 |
| Performance-based design | Cases 01, 02, 03, 06 |
| ASET/RSET | Case 02 |
| Means of escape | Case 02 |
| Smoke control | Case 03 |
| Fire risk assessment | Case 04 |
| Industrial consequence analysis | Case 05 |
| Model credibility | Case 06 |

### 11.3 Modelling practice

| Topic | Case where applied |
|---|---|
| FDS input structure | Case 00 |
| Smokeview workflow | Cases 00, 01, 03, 05 |
| Python post-processing | All modelling cases |
| PyroSim workflow | Cases 03, 05 |
| Pathfinder workflow | Case 02 |
| ParaView workflow | Cases 03, 05, 06 |
| Mesh sensitivity | Case 06 |
| Design fire sensitivity | Cases 03, 05, 06 |
| QA and reporting | All serious cases |

---

## 12. Six-Month Roadmap

Assumed working pattern:

```text
2 hours/day
6 days/week
~12 hours/week
24 weeks
~288 total hours
```

### Weekly rhythm

| Day | Focus |
|---|---|
| Day 1 | Knowledge reading and notes |
| Day 2 | Model setup |
| Day 3 | Model development |
| Day 4 | Run / inspect / troubleshoot |
| Day 5 | Post-process / figures |
| Day 6 | Report writing / QA / reflection |

---

### Phase 1 — Setup and Foundations

**Weeks 1-2**

Goal:

- build the repository
- create templates
- create first basic FDS model
- create shared plotting scripts

Outputs:

```text
case_00_first_fds_room_fire/
portfolio_plan.md
standards_map.md
disclaimer.md
shared plotting script
```

Deliverables:

- repository skeleton
- `.gitignore`
- case template
- report template
- first FDS room fire model
- Python plotting script
- first short report

---

### Phase 2 — Building Fire Engineering and Smoke Tenability

**Weeks 3-6**

Main case:

```text
case_01_makerspace_smoke_tenability
```

Goal:

- build first serious consultancy-style study

Outputs:

- simplified makerspace geometry
- design fire assumptions
- FDS simulations
- Smokeview images
- temperature and visibility plots
- final report

Learning:

- Approved Document B context
- basic tenability thinking
- smoke layer movement
- design fire selection
- limitations

---

### Phase 3 — Evacuation and ASET/RSET

**Weeks 7-10**

Main case:

```text
case_02_aset_rset_and_pathfinder
```

Goal:

- use Pathfinder
- connect evacuation model to fire model outputs

Outputs:

- simplified evacuation model
- occupant assumptions
- pre-movement assumptions
- RSET results
- ASET/RSET comparison
- final report

Learning:

- evacuation model limitations
- occupant assumptions
- bottlenecks
- uncertainty in human behaviour

---

### Phase 4 — Smoke Control and Design Option Comparison

**Weeks 11-14**

Main case:

```text
case_03_smoke_control_sensitivity
```

Goal:

- produce professional design-option comparison

Outputs:

- baseline model
- open/closed ventilation cases
- natural ventilation case
- mechanical extract case
- comparison plots
- recommendation section

Learning:

- sensitivity study structure
- smoke control logic
- client-facing comparison
- practical design discussion

---

### Phase 5 — Battery and Equipment Fire Risk

**Weeks 15-18**

Main case:

```text
case_04_battery_charging_enclosure_fire_risk
```

Goal:

- create a risk-based fire study

Outputs:

- hazard register
- fire scenario matrix
- simplified consequence model
- mitigation options
- final risk-style report

Learning:

- risk matrix
- scenario selection
- practical controls
- uncertainty and conservative assumptions

---

### Phase 6 — Industrial Liquid Spill Fire

**Weeks 19-21**

Main case:

```text
case_05_industrial_liquid_spill_fire
```

Goal:

- create an industrial fire risk case without using PhD material

Outputs:

- fictional industrial setting
- liquid spill design fire
- ventilation/crossflow comparison
- thermal/smoke consequence discussion
- final report

Learning:

- industrial fire risk
- pool/spill fire modelling
- thermal radiation discussion
- separation from PhD work

---

### Phase 7 — Model Credibility, Validation, and Final Packaging

**Weeks 22-24**

Main case:

```text
case_06_model_validation_uncertainty
```

Goal:

- complete model credibility case
- prepare public portfolio

Final outputs:

- mesh sensitivity report
- model credibility report
- final portfolio PDF
- website
- GitHub repository cleanup
- CV attachment
- interview talking points

---

## 13. Website Structure

The website should be a visual front-end, not a full technical archive.

Suggested pages:

```text
Home
- Who you are
- Portfolio purpose
- Skill areas
- Disclaimer

Projects
- Case 01: Makerspace smoke tenability
- Case 02: ASET/RSET and evacuation modelling
- Case 03: Smoke control sensitivity
- Case 04: Battery enclosure fire risk
- Case 05: Industrial spill fire
- Case 06: Model credibility and uncertainty

Skills
- FDS
- Smokeview
- Python
- PyroSim
- Pathfinder
- ParaView
- Technical reporting
- Fire engineering judgement

Knowledge map
- UK standards
- International/industrial standards
- Fire science
- Modelling and uncertainty

Downloads
- Portfolio PDF
- Case study one-pagers
- CV attachment
```

Each case page should show:

```text
Client question
Method
Key figures
Key result
What I learned
Tools used
Link to report PDF
Link to GitHub folder
```

---

## 14. How Codex Should Assist

Codex should act as:

- repository setup assistant
- file/template generator
- Python scripting assistant
- Markdown organiser
- website scaffold assistant
- report consistency checker
- data-processing helper

Codex should not act as:

- final fire engineering authority
- compliance judge
- safety certifier
- source of unsupported standards interpretation
- source of final HRR/design fire values without external checking

### Good Codex tasks

```text
Create the folder structure for this portfolio repository.
```

```text
Create a reusable Markdown report template for each fire engineering case study.
```

```text
Create a Python script that reads FDS device CSV output and plots each device against time.
```

```text
Create a script that compares multiple FDS case output files and produces summary plots.
```

```text
Create a GitHub Pages website skeleton with project cards for each case study.
```

```text
Create a checklist script that scans each case folder and reports missing required files.
```

```text
Create a README.md template for each case study folder.
```

```text
Generate CSV templates for assumptions register, design fire register, risk register, and sensitivity matrix.
```

### Avoid asking Codex to decide

```text
What HRR should I use?
What tenability criterion is correct?
Is this design safe?
Does this comply with UK regulations?
Which standard legally applies?
```

Those require source checking, professional judgement, and context-specific review.

---

## 15. Initial Codex Implementation Tasks

Codex should perform these in order.

### Task 1 — Create repository skeleton

Create all top-level folders and key Markdown files according to the structure above.

### Task 2 — Create global documentation files

Create:

```text
README.md
portfolio_plan.md
disclaimer.md
learning_log.md
skills_matrix.md
standards_map.md
references.md
```

### Task 3 — Create templates

Create:

```text
02_templates/case_study_template/
02_templates/report_templates/
02_templates/spreadsheet_templates/
02_templates/codex_prompts/
```

Populate them with placeholders, not final technical content.

### Task 4 — Create shared scripts folder

Create:

```text
04_shared_scripts/
```

Add placeholder Python files with docstrings for:

```text
fds_devc_plotter.py
compare_fds_cases.py
sensitivity_summary.py
generate_case_summary_table.py
image_compressor.py
report_figure_indexer.py
```

Add a basic `requirements.txt`.

Suggested Python dependencies:

```text
pandas
matplotlib
numpy
openpyxl
```

Optional later:

```text
plotly
markdown
jinja2
```

### Task 5 — Create case study folders

Create:

```text
03_case_studies/case_00_first_fds_room_fire/
03_case_studies/case_01_makerspace_smoke_tenability/
03_case_studies/case_02_aset_rset_and_pathfinder/
03_case_studies/case_03_smoke_control_sensitivity/
03_case_studies/case_04_battery_charging_enclosure_fire_risk/
03_case_studies/case_05_industrial_liquid_spill_fire/
03_case_studies/case_06_model_validation_uncertainty/
```

Each case folder should initially contain:

```text
README.md
brief.md
assumptions_register.md
design_fire_register.md
model_log.md
qa_checklist.md
report.md
report_appendix.md
figures/
fds/
pathfinder/
pyrosim/
scripts/
website_summary.md
```

### Task 6 — Create website skeleton

Create a simple website structure under:

```text
05_website/
```

Do not decide the framework unless the user specifies it.

For now, create:

```text
05_website/README.md
05_website/case_study_data/
05_website/public/
05_website/src/
05_website/build_notes.md
```

### Task 7 — Create project management files

Create:

```text
00_project_management/six_month_roadmap.md
00_project_management/weekly_schedule.md
00_project_management/decision_log.md
00_project_management/issue_tracker_guidance.md
00_project_management/codex_task_list.md
00_project_management/portfolio_quality_checklist.md
```

Populate with the six-month roadmap from this file.

---

## 16. Repository README Draft Outline

Create the root `README.md` using this outline:

```markdown
# Advanced Fire Engineering and Modelling Portfolio

This repository documents a six-month self-directed portfolio project in fire engineering, fire CFD, evacuation modelling, industrial fire risk, and consultancy-style reporting.

## Purpose

The purpose is to demonstrate:
- fire engineering learning
- FDS and Smokeview workflow
- Python post-processing
- evacuation modelling with Pathfinder
- advanced visualisation with ParaView
- consultancy-style reporting
- assumptions, limitations, and QA discipline

## Disclaimer

This is not a certified fire engineering design or regulatory submission.

## Portfolio Structure

Briefly explain:
- knowledge base
- templates
- case studies
- shared scripts
- website
- final outputs

## Case Studies

List:
1. First FDS room fire workflow
2. Makerspace smoke tenability study
3. ASET/RSET and Pathfinder evacuation study
4. Smoke control sensitivity study
5. Battery charging enclosure fire risk study
6. Industrial liquid spill fire
7. Model validation and uncertainty study

## Tools

List:
- FDS
- Smokeview
- Python
- Markdown
- GitHub
- ParaView
- PyroSim
- Pathfinder

## Status

Mark as planning / early development.

## Author

Add author details later.
```

---

## 17. Skills Matrix

Create `skills_matrix.md` with this table:

```markdown
| Skill | Evidence | Case study | Status |
|---|---|---|---|
| FDS input file creation | FDS case files | Case 00, 01, 03, 05 | Planned |
| Smokeview visualisation | Screenshots and figures | Case 00, 01, 03, 05 | Planned |
| Python post-processing | Plotting scripts | All modelling cases | Planned |
| Fire dynamics | Technical reports | All cases | Planned |
| Smoke tenability | Visibility/temp analysis | Case 01 | Planned |
| Evacuation modelling | Pathfinder model | Case 02 | Planned |
| ASET/RSET reasoning | Comparison table | Case 02 | Planned |
| Smoke control sensitivity | Scenario comparison | Case 03 | Planned |
| Fire risk assessment | Risk register | Case 04 | Planned |
| Industrial fire consequence | Spill fire case | Case 05 | Planned |
| Model uncertainty | Sensitivity report | Case 06 | Planned |
| Consultancy reporting | Final PDF reports | Cases 01-06 | Planned |
```

---

## 18. Standards Map

Create `standards_map.md` with this principle:

```markdown
# Standards and Guidance Map

This portfolio separates UK-specific, international, industrial, tool-specific, and general fire science references.

## Labelling convention

- [UK]
- [International]
- [US/NFPA]
- [Industrial/Insurance]
- [Tool/Model]
- [General fire science]

## UK references

- [UK] Approved Document B
- [UK] BS 9999
- [UK] BS 7974
- [UK] BS 5839

## International / industrial references

- [US/NFPA] NFPA 101
- [US/NFPA] NFPA 92
- [US/NFPA] NFPA 921
- [Industrial/Insurance] FM Global Data Sheets
- [International] ISO / IEC / API references where applicable

## Tool/model references

- [Tool/Model] FDS User Guide
- [Tool/Model] FDS Technical Reference Guide
- [Tool/Model] FDS Verification Guide
- [Tool/Model] FDS Validation Guide
- [Tool/Model] Smokeview User Guide

## Rule

Do not imply that a reference applies legally to a project unless the jurisdiction and project context support it.
```

---

## 19. Quality Rules

Codex should preserve these quality rules throughout the project.

### 19.1 Evidence and limitation discipline

Every case study must include:

- assumptions
- limitations
- model scope
- exclusions
- uncertainty
- disclaimer
- source references

### 19.2 No overclaiming

Avoid statements like:

```text
This design is safe.
This complies with regulations.
The evacuation is acceptable.
This is a valid fire strategy.
```

Use statements like:

```text
Within the simplified assumptions used in this portfolio study...
The results suggest...
The model indicates...
This comparison demonstrates...
Further professional review would be required...
```

### 19.3 Public safety rule

Never present public portfolio results as real-world safety advice.

### 19.4 Separation from PhD

Do not include unpublished PhD results, data, or exact experimental setup.

### 19.5 Reproducibility rule

Each case should include enough public material to understand the workflow, while keeping heavy raw outputs local.

### 19.6 Local results rule

Use local-only folders for:

```text
local_results/
outputs_raw/
simulation_outputs/
smokeview_exports_full/
pathfinder_results_full/
```

Do not commit them.

---

## 20. Open Decisions

These are not yet decided and should not be assumed by Codex.

1. Website framework:
   - simple static HTML
   - React/Vite
   - Next.js
   - other

2. Final report generation workflow:
   - Markdown to PDF
   - LaTeX
   - Word/Google Docs style
   - other

3. First real-world environment:
   - iForge makerspace
   - 3D printer farm
   - battery charging/storage
   - generic lab/workshop

4. PyroSim and Pathfinder access:
   - full licence
   - trial/demo
   - not yet known

5. Public repository hosting:
   - GitHub only
   - GitHub Pages
   - separate portfolio website

Codex should ask before making these decisions.

---

## 21. Suggested Next Action

After reading this context file, Codex should ask for permission to:

1. Create the repository skeleton.
2. Create all placeholder Markdown files.
3. Create `.gitignore`.
4. Create templates.
5. Create shared Python script stubs.
6. Create the first version of `README.md`, `portfolio_plan.md`, `standards_map.md`, and `disclaimer.md`.

Codex should not yet generate technical FDS models until the project owner confirms the first case study scope.

