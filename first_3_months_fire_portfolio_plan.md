# Advanced Fire Engineering Portfolio — First 3 Months Detailed Plan

**Document purpose:**  
This file is intended as a context and planning document for Codex and for project management. It defines the first 3 months of a 6-month public portfolio project in **UK-prioritised fire engineering consultancy with advanced modelling strength**.

**User profile and target direction:**  
- Self-funded PhD student in experimental thermal fluids.
- Does not plan to remain in academia.
- Interested in fire engineering consultancy and advanced fire science / specialist consulting.
- Long-term target role: **general fire engineering consultant with advanced modelling strength**.
- Priority market: **UK**, while learning broadly across UK and international/industrial practice.
- Portfolio type: public GitHub repository + final PDF attachment for CV + visual website.
- Heavy simulation results remain local; templates, inputs, scripts, final figures, reports, and website files go to GitHub.
- PhD work should remain separate from this portfolio.
- No physical experiments in this stage; modelling and reporting only.
- Working pattern: after 17:00, 6 days/week, normally 2 hours/day, with up to 3 hours available if needed.
- Portfolio disclaimer must be included in all public outputs.

---

## 0. Non-Certified Design Disclaimer

Use this disclaimer in the repository `README.md`, website footer, and every report.

> This portfolio is a self-directed learning and professional development project in fire engineering and fire modelling. It is intended to demonstrate modelling workflow, technical reasoning, data processing, and consultancy-style reporting.
>
> The case studies are simplified training exercises unless explicitly stated otherwise. They are not certified fire engineering designs, fire risk assessments, regulatory submissions, or safety approvals. The results must not be used for real-world design, compliance, emergency planning, or operational decisions.
>
> All assumptions, scenarios, geometries, and design fires are simplified for educational purposes. Any real project would require competent professional review, project-specific data, applicable statutory guidance, stakeholder consultation, and formal quality assurance.

---

## 1. First 3 Months: High-Level Objectives

The first 3 months should create a strong foundation rather than a polished final portfolio. The target outputs are:

1. A clean repository structure.
2. Reusable report, case study, and register templates.
3. Basic fire engineering knowledge notes.
4. A functioning FDS + Smokeview + Python workflow.
5. Case 00: first simple FDS room fire model.
6. Case 01: makerspace smoke tenability study.
7. Case 02: ASET/RSET and Pathfinder evacuation study.
8. Initial public website skeleton.
9. First draft of CV portfolio PDF structure.
10. A repeatable QA and reporting workflow.

---

## 2. Standards and Guidance Labelling Rule

Because the portfolio is UK-prioritised but broad, all standards/guidance references should be labelled:

| Label | Meaning | Examples |
|---|---|---|
| `[UK]` | UK-specific or England/Wales-specific context | Approved Document B, Fire Safety Order, BS 9999, BS 7974 |
| `[International / US]` | US-origin or internationally referenced | NFPA guidance |
| `[International / industrial]` | Industrial, insurance, or multinational practice | FM Global style risk engineering, API/IEC/ISO contexts |
| `[Tool / model]` | Modelling documentation | FDS User Guide, FDS Validation Guide, Pathfinder documentation |
| `[General engineering]` | Not jurisdiction-specific | heat transfer, combustion, fluid mechanics, uncertainty analysis |

**Rule:** Never imply that an international standard automatically applies to a UK project. Use UK guidance for UK building fire engineering context unless explicitly comparing frameworks.

---

## 3. External Reference Sources to Use

Use official and primary sources where possible.

### FDS and Smokeview

- NIST FDS-SMV homepage: https://pages.nist.gov/fds-smv/
- NIST FDS-SMV manuals: https://pages.nist.gov/fds-smv/manuals.html

Notes:
- FDS is described by NIST as a large-eddy simulation code for low-speed flows with emphasis on smoke and heat transport from fires.
- Smokeview is the companion visualisation program for FDS and CFAST outputs.
- The NIST manuals page lists the current release as FDS 6.11.0 / SMV 6.11.0 as of this planning document.

### UK fire safety context

- Approved Document B: https://www.gov.uk/government/publications/fire-safety-approved-document-b
- Workplace fire safety responsibilities: https://www.gov.uk/workplace-fire-safety-your-responsibilities
- Fire safety risk assessment checklist: https://www.gov.uk/government/publications/fire-safety-risk-assessment-5-step-checklist

Notes:
- Approved Document B applies to England and covers fire safety matters within and around buildings.
- GOV.UK lists current amended versions and updates. Always check the current page before citing details in a public report.
- Do not quote or reproduce large sections of standards or guidance.

### PyroSim and Pathfinder

- PyroSim: https://www.thunderheadeng.com/pyrosim/
- Pathfinder: https://www.thunderheadeng.com/pathfinder/

Notes:
- PyroSim is a graphical interface for creating FDS models.
- Pathfinder is an evacuation and crowd movement modelling tool.
- Confirm licence/access before relying on them for public outputs.

---

## 4. Repository Structure for First 3 Months

Codex should create or maintain this structure.

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
│   ├── first_3_months_plan.md
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
│   │   ├── risk_register.md
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
│   └── case_02_aset_rset_and_pathfinder/
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
│   ├── portfolio_summary_draft.md
│   ├── cv_attachment_fire_engineering_portfolio_draft.md
│   ├── case_study_one_pagers/
│   ├── interview_talking_points.md
│   └── skills_evidence_matrix.md
│
└── 99_local_results_placeholder/
    └── README.md
```

---

## 5. `.gitignore` for Public Repository

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

# Visualisation and video outputs
*.avi
*.mp4
*.mov
*.vtk
*.vtu
*.pvtu

# Large or local results
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

---

## 6. Report Template for Every Case Study

Every serious case study should use this structure.

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

## 7. First 3 Months Overview

| Month | Main Focus | Main Case Study | Main Output |
|---|---|---|---|
| Month 1 | Setup, knowledge foundation, first FDS workflow | Case 00 | Repository, templates, first FDS room fire report |
| Month 2 | Building fire engineering + smoke tenability | Case 01 | Makerspace smoke tenability consultancy-style report |
| Month 3 | Evacuation modelling + ASET/RSET | Case 02 | Pathfinder evacuation model and ASET/RSET report |

---

# Month 1 — Setup, Knowledge Base, and First FDS Workflow

## Month 1 Objectives

By the end of Month 1:

- Repository is created and structured.
- Templates are created.
- FDS and Smokeview are installed and tested.
- Python plotting workflow is working.
- Case 00 is complete.
- Knowledge base has initial notes.
- First short consultancy-style report is drafted.

## Month 1 Main Deliverables

```text
README.md
disclaimer.md
standards_map.md
skills_matrix.md
learning_log.md
02_templates/case_study_template/
02_templates/report_templates/
04_shared_scripts/fds_devc_plotter.py
03_case_studies/case_00_first_fds_room_fire/report.md
03_case_studies/case_00_first_fds_room_fire/website_summary.md
```

---

## Week 1 — Repository Setup and Professional Framework

### Week 1 Goal

Create the project structure and professional working framework before doing modelling.

### Day 1 — Project Brief and Repository Skeleton

**Syllabus covered:**
- What a portfolio is meant to prove.
- Difference between GitHub, PDF portfolio, and website.
- Public disclaimer and limitation statements.

**Exercise:**
- Create the repository locally.
- Create top-level files:
  - `README.md`
  - `portfolio_plan.md`
  - `disclaimer.md`
  - `learning_log.md`
  - `skills_matrix.md`
  - `standards_map.md`
  - `references.md`
  - `.gitignore`

**Report / writing task:**
- Write the first paragraph of the project purpose in `README.md`.

**Codex task:**
- Generate the repository skeleton using the structure in this document.

**Done criteria:**
- Repository opens locally.
- All top-level folders exist.
- Disclaimer file exists.

---

### Day 2 — Standards Map and Knowledge Base Structure

**Syllabus covered:**
- UK vs international standards separation.
- Approved Document B as England-specific building fire safety guidance.
- Difference between statutory guidance, British Standards, NFPA-style practice, and modelling documentation.

**Exercise:**
- Create `standards_map.md`.
- Create the `01_knowledge_base/` folder structure.

**Report / writing task:**
- Add a table to `standards_map.md` with labels:
  - `[UK]`
  - `[International / US]`
  - `[International / industrial]`
  - `[Tool / model]`
  - `[General engineering]`

**Done criteria:**
- Standards are clearly labelled.
- There is a written rule not to mix UK and international standards without explanation.

---

### Day 3 — Case Study and Report Templates

**Syllabus covered:**
- Consultancy report structure.
- Client question.
- Scope and exclusions.
- Assumptions registers.
- QA checklists.

**Exercise:**
- Create `02_templates/case_study_template/`.
- Create:
  - `brief.md`
  - `assumptions_register.md`
  - `design_fire_register.md`
  - `risk_register.md`
  - `model_log.md`
  - `qa_checklist.md`
  - `report.md`
  - `website_summary.md`

**Report / writing task:**
- Insert the full report structure into `report.md`.

**Codex task:**
- Ask Codex to create a reusable case study folder generator script or checklist.

**Done criteria:**
- Future case studies can be created by copying the template.

---

### Day 4 — Tool Installation and Version Recording

**Syllabus covered:**
- FDS and Smokeview workflow.
- Difference between solver, visualisation, and post-processing.
- Software version control for professional reporting.

**Exercise:**
- Install or confirm installation of:
  - FDS
  - Smokeview
  - Python environment
  - Git
  - VS Code
- Create `00_project_management/software_setup.md`.

**Report / writing task:**
- Record:
  - operating system,
  - FDS version,
  - Smokeview version,
  - Python version,
  - package management method,
  - known installation issues.

**Done criteria:**
- `fds` and `smokeview` can be called or their install paths are documented.
- Version information is recorded.

---

### Day 5 — Python Environment and Shared Scripts

**Syllabus covered:**
- Why post-processing matters in consultancy.
- Why visual CFD screenshots are not enough.
- Device output plotting.

**Exercise:**
- Create Python virtual environment.
- Create `04_shared_scripts/requirements.txt`.
- Create first version of `fds_devc_plotter.py`.

**Report / writing task:**
- Add script usage instructions to `04_shared_scripts/README.md`.

**Codex task:**
- Ask Codex to create a robust FDS device CSV plotter that:
  - reads a CSV path,
  - detects/handles a units row,
  - plots each device against time,
  - saves figures to a specified output folder,
  - reports missing or unclear columns.

**Done criteria:**
- Script runs on a dummy CSV or sample data.

---

### Day 6 — Weekly Review and Portfolio QA

**Syllabus covered:**
- QA mindset.
- Document control.
- Version control.
- What makes work look professional.

**Exercise:**
- Create `portfolio_quality_checklist.md`.
- Create first `decision_log.md`.
- Create first Git commit.

**Report / writing task:**
- Write a Week 1 reflection in `learning_log.md`.

**Done criteria:**
- Repository is in a usable state.
- First Git commit completed.
- Week 1 review written.

---

## Week 2 — Fire Dynamics Foundation and First FDS Input

### Week 2 Goal

Understand basic fire dynamics and create a first FDS room fire case.

### Day 1 — Fire Dynamics: HRR and Fire Growth

**Syllabus covered:**
- Heat release rate.
- Fire growth curves.
- Peak HRR.
- Difference between prescribed fire and material pyrolysis.
- Why design fire choice dominates results.

**Exercise:**
- Create `heat_release_rate.md`.
- Create `fire_growth_curves.md`.
- Write simple notes with equations and plain-English explanations.

**Report / writing task:**
- Add a "Design fire uncertainty" paragraph to the report template.

**Done criteria:**
- Notes explain why HRR is a major modelling assumption.

---

### Day 2 — FDS Input File Structure

**Syllabus covered:**
- `HEAD`
- `TIME`
- `MESH`
- `REAC`
- `SURF`
- `VENT`
- `OBST`
- `DEVC`
- `SLCF`
- `TAIL`

**Exercise:**
- Create `fds_input_file_structure.md`.
- Create Case 00 folder from template.
- Create `case_00_first_fds_room_fire/fds/week2_room_fire.fds`.

**Report / writing task:**
- Start Case 00 `brief.md`.

**Done criteria:**
- FDS input file exists and has a clear structure.

---

### Day 3 — Simple Room Geometry

**Syllabus covered:**
- Cartesian geometry.
- Room dimensions.
- Mesh domain.
- Boundary representation.
- Simplified geometry limitations.

**Exercise:**
- Build a simple 4 m × 3 m × 2.4 m room model.
- Add one door opening.
- Add one burner.

**Report / writing task:**
- Add geometry assumptions to Case 00 assumptions register.

**Done criteria:**
- Geometry is documented and input file is syntactically organised.

---

### Day 4 — Devices and Slices

**Syllabus covered:**
- Quantitative vs visual outputs.
- Temperature devices.
- Visibility devices.
- Slices and vector fields.
- Why output location matters.

**Exercise:**
- Add:
  - ceiling temperature device,
  - eye-level temperature device,
  - eye-level visibility device,
  - temperature slice,
  - visibility slice,
  - velocity vector slice.

**Report / writing task:**
- Add an output quantity table to `model_log.md`.

**Done criteria:**
- FDS file contains devices and slices with meaningful names.

---

### Day 5 — Run FDS and Open Smokeview

**Syllabus covered:**
- Simulation execution.
- Reading `.out` files.
- Smokeview basics.
- Common beginner errors.

**Exercise:**
- Run the FDS model.
- Open results in Smokeview.
- Save selected screenshots only.
- Keep raw full outputs local.

**Report / writing task:**
- Write first result observations in `model_log.md`.

**Done criteria:**
- FDS model runs.
- Smokeview opens.
- At least three screenshots are saved to the case folder.

---

### Day 6 — Week 2 Review

**Syllabus covered:**
- Simulation documentation.
- Error logging.
- Reporting uncertainty.

**Exercise:**
- Clean Case 00 folder.
- Update assumptions register.
- Update QA checklist.

**Report / writing task:**
- Add Week 2 reflection to `learning_log.md`.

**Done criteria:**
- Case 00 has working model files, screenshots, and logs.

---

## Week 3 — Case 00 Post-Processing and First Short Report

### Week 3 Goal

Turn the first FDS model into a short, professional case study.

### Day 1 — Device CSV Post-Processing

**Syllabus covered:**
- FDS device CSV output.
- Units row handling.
- Time-series plotting.
- Reproducible figures.

**Exercise:**
- Use `fds_devc_plotter.py` on Case 00 output.
- Plot:
  - ceiling temperature vs time,
  - eye-level temperature vs time,
  - visibility vs time.

**Report / writing task:**
- Add figure captions.

**Done criteria:**
- At least three clean plots exist.

---

### Day 2 — Smokeview Figure Selection

**Syllabus covered:**
- What makes a useful engineering figure.
- Avoiding decorative CFD screenshots.
- Captions and figure numbering.

**Exercise:**
- Select 3–5 Smokeview images.
- Compress and name them clearly.
- Add figure index.

**Report / writing task:**
- Add "Visual results" section to Case 00 report.

**Done criteria:**
- Figures support specific claims.

---

### Day 3 — First Short Report Draft

**Syllabus covered:**
- Consultancy-style short report.
- Executive summary.
- Objective, method, findings, limitations.

**Exercise:**
- Draft Case 00 report.

**Report / writing task:**
- Write:
  - Executive summary,
  - Introduction,
  - Method,
  - Results,
  - Limitations,
  - Conclusion.

**Done criteria:**
- Case 00 report draft is complete.

---

### Day 4 — QA Review of Case 00

**Syllabus covered:**
- Internal checking.
- Claims vs evidence.
- Model limitations.

**Exercise:**
- Complete QA checklist.
- Check every result claim against a plot or screenshot.
- Mark overclaims and rewrite them.

**Report / writing task:**
- Add "What this model cannot support" section.

**Done criteria:**
- No result claim exists without supporting evidence.

---

### Day 5 — Website Summary Draft

**Syllabus covered:**
- Public communication.
- Translating technical work into employer-facing summaries.

**Exercise:**
- Create Case 00 `website_summary.md`.

**Report / writing task:**
- Write:
  - client-style question,
  - method,
  - key outputs,
  - skills demonstrated,
  - limitations.

**Done criteria:**
- Case 00 is ready to become a website project card.

---

### Day 6 — Month 1 Midpoint Review

**Syllabus covered:**
- Portfolio evidence mapping.
- Skills matrix.

**Exercise:**
- Update `skills_matrix.md`.
- Add evidence links to Case 00.

**Report / writing task:**
- Write Week 3 reflection.

**Done criteria:**
- Case 00 is effectively complete as a foundation case.

---

## Week 4 — Preparation for Case 01: Makerspace Smoke Tenability

### Week 4 Goal

Prepare the first serious building fire engineering case study.

### Day 1 — UK Building Fire Context

**Syllabus covered:**
- Approved Document B high-level context.
- Difference between guidance awareness and compliance design.
- Fire safety objectives:
  - life safety,
  - property protection,
  - firefighter access,
  - business continuity.

**Exercise:**
- Create `approved_document_b_notes.md`.
- Identify which parts are relevant at a high level only.

**Report / writing task:**
- Add "UK guidance context" paragraph template.

**Done criteria:**
- Notes clearly state this is awareness, not compliance expertise.

---

### Day 2 — Tenability Concepts

**Syllabus covered:**
- Temperature tenability.
- Visibility.
- Smoke layer height.
- Radiant heat exposure.
- FED/toxicity as future extension.
- Why tenability criteria need citation and caution.

**Exercise:**
- Create `tenability_criteria.md` under fire engineering practice or fire dynamics.
- Build a table of tenability quantities to track.

**Report / writing task:**
- Draft "Assessment criteria" section for Case 01.

**Done criteria:**
- Assessment quantities are defined before modelling.

---

### Day 3 — Client Brief for Case 01

**Syllabus covered:**
- Client question definition.
- Scope and exclusions.
- Fictionalising a real-world environment safely.

**Exercise:**
- Create Case 01 folder from template.
- Draft `brief.md`.

**Proposed client question:**
> In a simplified makerspace/workshop fire scenario, how quickly do smoke and heat conditions become challenging at eye level, and which assumptions most affect the result?

**Report / writing task:**
- Draft sections:
  - Introduction,
  - Client/design question,
  - Scope,
  - Exclusions.

**Done criteria:**
- Case 01 has a clear design question.

---

### Day 4 — Assumptions Register for Case 01

**Syllabus covered:**
- Geometry assumptions.
- Occupancy assumptions.
- Fire source assumptions.
- Ventilation assumptions.
- Detection/suppression assumptions.
- Conservative vs non-conservative assumptions.

**Exercise:**
- Fill initial `assumptions_register.md`.

**Report / writing task:**
- Write the "Scenario definition" first draft.

**Done criteria:**
- All major unknowns are listed before modelling.

---

### Day 5 — Design Fire Register for Case 01

**Syllabus covered:**
- Fire source selection.
- HRR curve.
- Growth rate.
- Peak HRR.
- Soot and visibility implications.
- Sensitivity cases.

**Exercise:**
- Fill `design_fire_register.md`.
- Define baseline and sensitivity cases.

**Example case structure:**
- Baseline design fire.
- Lower HRR sensitivity.
- Higher HRR sensitivity.
- Door open vs door restricted.

**Report / writing task:**
- Draft "Design fire" section.

**Done criteria:**
- Case 01 modelling scenarios are defined.

---

### Day 6 — Month 1 Review and Case 01 Readiness Check

**Syllabus covered:**
- Readiness review.
- Avoiding premature modelling.
- Pre-modelling QA.

**Exercise:**
- Complete Case 01 pre-modelling checklist.
- Update Month 1 progress review.

**Report / writing task:**
- Write Month 1 review in `learning_log.md`.

**Done criteria:**
- Case 00 complete.
- Case 01 ready for modelling.
- Month 2 can begin without reworking repository basics.

---

# Month 2 — Case 01: Makerspace Smoke Tenability Study

## Month 2 Objectives

By the end of Month 2:

- Case 01 has a complete FDS model.
- Baseline and sensitivity cases are run.
- Smokeview figures and quantitative plots are produced.
- A full consultancy-style report is drafted and reviewed.
- A website case summary is created.

## Month 2 Main Deliverables

```text
03_case_studies/case_01_makerspace_smoke_tenability/brief.md
03_case_studies/case_01_makerspace_smoke_tenability/assumptions_register.md
03_case_studies/case_01_makerspace_smoke_tenability/design_fire_register.md
03_case_studies/case_01_makerspace_smoke_tenability/fds/
03_case_studies/case_01_makerspace_smoke_tenability/report.md
03_case_studies/case_01_makerspace_smoke_tenability/website_summary.md
```

---

## Week 5 — Case 01 Geometry and Baseline Model

### Week 5 Goal

Build and run the first baseline makerspace smoke model.

### Day 1 — Geometry Simplification

**Syllabus covered:**
- Simplifying real environments.
- What to include and exclude.
- How simplification affects conclusions.

**Exercise:**
- Sketch simplified makerspace geometry.
- Decide dimensions.
- Define openings and internal obstructions.

**Report / writing task:**
- Add geometry explanation and limitation statement.

**Done criteria:**
- Geometry is defined in plan view and text.

---

### Day 2 — FDS Geometry Implementation

**Syllabus covered:**
- `MESH`
- `OBST`
- `VENT`
- openings
- simplified furniture/equipment representation.

**Exercise:**
- Create baseline FDS geometry.
- Include room, doorway/openings, major obstructions.

**Report / writing task:**
- Update model log with geometry implementation notes.

**Done criteria:**
- Geometry compiles or is ready for syntax testing.

---

### Day 3 — Fire Source and Output Devices

**Syllabus covered:**
- Prescribed fire.
- Burner placement.
- Output device selection.
- Eye-level criteria.

**Exercise:**
- Add design fire source.
- Add devices:
  - temperature at eye level,
  - ceiling temperature,
  - visibility near exit,
  - visibility at room centre,
  - gas temperature near exit.

**Report / writing task:**
- Add output device table.

**Done criteria:**
- Model has outputs linked to the client question.

---

### Day 4 — Baseline Simulation Run

**Syllabus covered:**
- Running FDS.
- Checking fatal errors.
- Interpreting `.out` files.
- Local result storage.

**Exercise:**
- Run baseline case.
- Store heavy outputs locally.
- Keep selected figures only in repository.

**Report / writing task:**
- Add modelling log entry.

**Done criteria:**
- Baseline case runs or errors are clearly logged.

---

### Day 5 — Smokeview Baseline Review

**Syllabus covered:**
- Smoke movement interpretation.
- Smoke layer formation.
- Visibility visualisation.
- Flow paths.

**Exercise:**
- Open baseline in Smokeview.
- Export selected figures:
  - smoke development,
  - visibility slice,
  - temperature slice,
  - velocity vector field.

**Report / writing task:**
- Draft visual results observations.

**Done criteria:**
- Baseline visual outputs are selected and captioned.

---

### Day 6 — Week 5 Review

**Syllabus covered:**
- Baseline model QA.
- Geometry limitations.
- Whether results answer the brief.

**Exercise:**
- Complete baseline QA checklist.
- Update assumptions register.

**Report / writing task:**
- Write Week 5 reflection.

**Done criteria:**
- Baseline model is stable enough to build sensitivity cases.

---

## Week 6 — Case 01 Sensitivity Cases

### Week 6 Goal

Create meaningful sensitivity cases and compare them.

### Day 1 — Sensitivity Plan

**Syllabus covered:**
- Why sensitivity analysis is needed.
- HRR sensitivity.
- Ventilation sensitivity.
- Output location sensitivity.

**Exercise:**
- Create `sensitivity_matrix.md`.
- Define 3–4 cases.

**Possible cases:**
- Baseline.
- Higher HRR.
- Lower HRR.
- Door/opening variation.
- Alternative fire location.

**Report / writing task:**
- Draft "Sensitivity and uncertainty" plan.

**Done criteria:**
- Sensitivity cases are justified before running.

---

### Day 2 — Generate FDS Variants

**Syllabus covered:**
- Case management.
- Naming conventions.
- Avoiding uncontrolled file edits.

**Exercise:**
- Create:
  - `case01_baseline.fds`
  - `case01_high_hrr.fds`
  - `case01_low_hrr.fds`
  - `case01_door_open.fds`

**Codex task:**
- Ask Codex to generate case variants from a baseline file by changing parameters and preserving comments.

**Report / writing task:**
- Update model log with case names and differences.

**Done criteria:**
- Sensitivity input files are clearly named and documented.

---

### Day 3 — Run Sensitivity Cases

**Syllabus covered:**
- Batch case running.
- Runtime management.
- Error tracking.

**Exercise:**
- Run all sensitivity cases.
- Log completion/errors.

**Report / writing task:**
- Update `model_log.md`.

**Done criteria:**
- At least two sensitivity cases complete successfully.

---

### Day 4 — Comparative Post-Processing

**Syllabus covered:**
- Comparing time series.
- Avoiding misleading plots.
- Summary metrics.

**Exercise:**
- Use or create `compare_fds_cases.py`.
- Compare:
  - visibility at eye level,
  - temperature at eye level,
  - ceiling temperature,
  - time to threshold if defined.

**Report / writing task:**
- Create first comparison figures.

**Done criteria:**
- Comparative plots exist and are clearly labelled.

---

### Day 5 — Engineering Interpretation of Sensitivity

**Syllabus covered:**
- Engineering judgement.
- Conservative vs non-conservative assumptions.
- How to write useful recommendations.

**Exercise:**
- Identify which assumption most affects results.

**Report / writing task:**
- Draft "Engineering interpretation" section.

**Done criteria:**
- Report begins to answer: what matters most and why?

---

### Day 6 — Week 6 Review

**Syllabus covered:**
- Mid-case QA.
- Sensitivity completeness.
- Result quality check.

**Exercise:**
- Update QA checklist.
- Identify missing plots or reruns needed.

**Report / writing task:**
- Write Week 6 reflection.

**Done criteria:**
- Case 01 has baseline and sensitivity evidence.

---

## Week 7 — Case 01 Consultancy Report Draft

### Week 7 Goal

Turn Case 01 results into a full consultancy-style report.

### Day 1 — Executive Summary and Client Question

**Syllabus covered:**
- Executive summary writing.
- Decision-oriented findings.
- Avoiding academic phrasing.

**Exercise:**
- Draft executive summary.

**Report / writing task:**
- Write:
  - objective,
  - method,
  - main findings,
  - limitations,
  - recommendations.

**Done criteria:**
- Executive summary can be understood without reading the full report.

---

### Day 2 — Method and Scenario Sections

**Syllabus covered:**
- Method clarity.
- Traceability.
- Software and version reporting.

**Exercise:**
- Write:
  - scenario definition,
  - design fire,
  - modelling method,
  - assessment criteria.

**Report / writing task:**
- Insert tables from assumptions and design fire register.

**Done criteria:**
- A reader can reproduce the model conceptually.

---

### Day 3 — Results Section

**Syllabus covered:**
- Results vs interpretation.
- Figure selection.
- Captions.

**Exercise:**
- Insert:
  - smoke images,
  - temperature plots,
  - visibility plots,
  - comparison plots.

**Report / writing task:**
- Write factual result descriptions.

**Done criteria:**
- Result section does not overinterpret.

---

### Day 4 — Interpretation and Recommendations

**Syllabus covered:**
- Translating results into design advice.
- Conditional recommendations.
- Further work.

**Exercise:**
- Write:
  - engineering interpretation,
  - recommendations,
  - further work.

**Report / writing task:**
- Use wording such as:
  - "The model indicates..."
  - "The result is sensitive to..."
  - "This should not be interpreted as..."

**Done criteria:**
- Recommendations are clearly linked to evidence.

---

### Day 5 — Limitations and QA

**Syllabus covered:**
- Limitations.
- Model credibility.
- Public portfolio safety.

**Exercise:**
- Complete QA checklist.
- Add limitation section.

**Report / writing task:**
- Add non-certified design disclaimer.

**Done criteria:**
- Case 01 draft is complete.

---

### Day 6 — Review and Edit

**Syllabus covered:**
- Professional editing.
- Document control.
- Concision.

**Exercise:**
- Review report for clarity.
- Update document control.
- Write website summary draft.

**Done criteria:**
- Case 01 is ready for final polish.

---

## Week 8 — Case 01 Finalisation and Website Summary

### Week 8 Goal

Finish Case 01 and prepare it for public presentation.

### Day 1 — Figure Polish

**Syllabus covered:**
- Graph formatting.
- Figure consistency.
- Units and labels.

**Exercise:**
- Clean all figures.
- Ensure every figure has:
  - number,
  - title,
  - units,
  - caption,
  - source/model case.

**Done criteria:**
- Figures are presentation-ready.

---

### Day 2 — Report Final Edit

**Syllabus covered:**
- Report quality assurance.
- Avoiding unsupported claims.
- Public readability.

**Exercise:**
- Final edit of Case 01 report.

**Report / writing task:**
- Update executive summary and conclusion last.

**Done criteria:**
- Report is internally consistent.

---

### Day 3 — Website Project Page Draft

**Syllabus covered:**
- Portfolio presentation.
- Employer-facing summaries.

**Exercise:**
- Create project card content:
  - client question,
  - method,
  - tools,
  - key figure,
  - skills demonstrated,
  - link to report.

**Report / writing task:**
- Complete `website_summary.md`.

**Done criteria:**
- Case 01 can be shown on the website.

---

### Day 4 — Skills Matrix Update

**Syllabus covered:**
- Evidence-based CV claims.
- Skills mapping.

**Exercise:**
- Update `skills_matrix.md` with evidence from Case 01.

**Examples:**
- FDS modelling: Case 01 baseline and sensitivity models.
- Technical reporting: Case 01 final report.
- Fire engineering judgement: design fire and limitation discussion.

**Done criteria:**
- Skills claims point to specific outputs.

---

### Day 5 — Case 01 Retrospective

**Syllabus covered:**
- Project reflection.
- Lessons learned.
- What to improve before Case 02.

**Exercise:**
- Write retrospective:
  - what worked,
  - what was difficult,
  - what needs improvement,
  - what can be reused.

**Done criteria:**
- Lessons are documented for future case studies.

---

### Day 6 — Month 2 Review

**Syllabus covered:**
- Portfolio milestone review.
- Readiness for evacuation modelling.

**Exercise:**
- Create Month 2 review.
- List remaining issues.

**Done criteria:**
- Case 01 complete enough to serve as first serious portfolio case.

---

# Month 3 — Case 02: ASET/RSET and Pathfinder Evacuation Study

## Month 3 Objectives

By the end of Month 3:

- Basic evacuation modelling workflow is understood.
- Pathfinder is installed/available or alternative method is documented.
- Case 02 is built around a simplified evacuation scenario.
- ASET is estimated from fire/smoke outputs or defined from Case 01.
- RSET is estimated using Pathfinder and assumptions.
- A consultancy-style ASET/RSET report is produced.

## Month 3 Main Deliverables

```text
03_case_studies/case_02_aset_rset_and_pathfinder/brief.md
03_case_studies/case_02_aset_rset_and_pathfinder/assumptions_register.md
03_case_studies/case_02_aset_rset_and_pathfinder/pathfinder/
03_case_studies/case_02_aset_rset_and_pathfinder/report.md
03_case_studies/case_02_aset_rset_and_pathfinder/website_summary.md
01_knowledge_base/05_evacuation_modelling/
```

---

## Week 9 — Evacuation Modelling Foundation

### Week 9 Goal

Understand evacuation modelling concepts before using Pathfinder.

### Day 1 — ASET/RSET Method

**Syllabus covered:**
- Available Safe Egress Time.
- Required Safe Egress Time.
- Detection time.
- Alarm time.
- Pre-movement time.
- Travel time.
- Safety margin.
- Why this is a simplified method in this portfolio.

**Exercise:**
- Create `aset_rset_method.md`.

**Report / writing task:**
- Draft ASET/RSET definitions for Case 02.

**Done criteria:**
- You can explain ASET and RSET in plain language.

---

### Day 2 — Occupant Characteristics

**Syllabus covered:**
- Occupant load assumptions.
- Walking speed.
- Familiarity.
- Mobility variation.
- Behavioural uncertainty.

**Exercise:**
- Create `occupant_characteristics.md`.
- Define hypothetical occupant groups.

**Report / writing task:**
- Start Case 02 assumptions register.

**Done criteria:**
- Occupant assumptions are explicit.

---

### Day 3 — Pre-Movement and Behaviour

**Syllabus covered:**
- Pre-movement time.
- Alarm response.
- Staff/student behaviour.
- Uncertainty in human evacuation.

**Exercise:**
- Create `pre_movement_time.md`.
- Define baseline and sensitivity pre-movement assumptions.

**Report / writing task:**
- Add pre-movement section to Case 02.

**Done criteria:**
- RSET is not treated as only walking time.

---

### Day 4 — Pathfinder Setup

**Syllabus covered:**
- Pathfinder interface.
- Geometry import/manual setup.
- Occupants.
- Doors.
- Exits.
- Output review.

**Exercise:**
- Install/open Pathfinder.
- Create basic test model:
  - one room,
  - one exit,
  - small occupant group.

**Report / writing task:**
- Create `pathfinder_basics.md`.

**Done criteria:**
- Simple evacuation model runs.

---

### Day 5 — Simple Pathfinder Output Interpretation

**Syllabus covered:**
- Evacuation time.
- Bottlenecks.
- Density.
- Queueing.
- Output limitations.

**Exercise:**
- Run the simple Pathfinder model.
- Export results or screenshots.
- Write notes on outputs.

**Report / writing task:**
- Add output interpretation notes.

**Done criteria:**
- You can interpret basic Pathfinder outputs.

---

### Day 6 — Week 9 Review

**Syllabus covered:**
- Evacuation modelling limitations.
- Avoiding false precision.

**Exercise:**
- Complete Week 9 learning review.
- Confirm Case 02 scenario.

**Done criteria:**
- Case 02 is ready for structured setup.

---

## Week 10 — Case 02 Scenario and Pathfinder Model

### Week 10 Goal

Build the actual evacuation case linked to Case 01 or a similar simplified building scenario.

### Day 1 — Case 02 Client Brief

**Syllabus covered:**
- Life safety design question.
- Linking smoke modelling and evacuation modelling.

**Exercise:**
- Create Case 02 folder from template.
- Draft `brief.md`.

**Proposed client question:**
> For a simplified makerspace fire scenario, does the estimated available safe egress time exceed the required safe egress time under defined assumptions?

**Report / writing task:**
- Draft:
  - introduction,
  - client question,
  - scope,
  - exclusions.

**Done criteria:**
- Case 02 has a clear ASET/RSET question.

---

### Day 2 — Geometry and Occupant Setup

**Syllabus covered:**
- Evacuation geometry.
- Exit widths.
- Occupant placement.
- Simplification and limitations.

**Exercise:**
- Build geometry in Pathfinder.
- Add occupants.
- Add exits.

**Report / writing task:**
- Update assumptions register.

**Done criteria:**
- Evacuation geometry is defined.

---

### Day 3 — Baseline Evacuation Run

**Syllabus covered:**
- Pathfinder baseline run.
- Evacuation time output.
- Bottleneck identification.

**Exercise:**
- Run baseline evacuation simulation.
- Record total evacuation time.

**Report / writing task:**
- Add baseline RSET result table.

**Done criteria:**
- Baseline evacuation result is available.

---

### Day 4 — Pre-Movement Sensitivity

**Syllabus covered:**
- Pre-movement uncertainty.
- Conservative assumptions.
- Scenario comparison.

**Exercise:**
- Run sensitivity cases:
  - short pre-movement,
  - medium pre-movement,
  - long pre-movement.

**Report / writing task:**
- Create RSET sensitivity table.

**Done criteria:**
- RSET sensitivity to pre-movement is visible.

---

### Day 5 — Exit/Bottleneck Sensitivity

**Syllabus covered:**
- Exit restriction.
- Door width.
- Blocked route scenario.
- Bottlenecks.

**Exercise:**
- Run one or two geometry/route sensitivity cases.

**Report / writing task:**
- Draft bottleneck interpretation.

**Done criteria:**
- Model shows how route assumptions affect evacuation time.

---

### Day 6 — Week 10 Review

**Syllabus covered:**
- Evacuation case QA.
- Scenario completeness.

**Exercise:**
- Update model log.
- Complete partial QA checklist.

**Done criteria:**
- Case 02 has baseline and sensitivity evacuation outputs.

---

## Week 11 — Linking ASET and RSET

### Week 11 Goal

Connect fire modelling outputs with evacuation assumptions in a cautious, consultancy-style way.

### Day 1 — Define ASET from Smoke/Tenability

**Syllabus covered:**
- ASET extraction.
- Threshold logic.
- Use of Case 01 results.
- Limitations of linking separate models.

**Exercise:**
- Identify approximate ASET from Case 01 or define a simplified ASET scenario.
- Record criteria used.

**Report / writing task:**
- Draft "ASET derivation" section.

**Done criteria:**
- ASET estimate is transparent and cautious.

---

### Day 2 — Define RSET Components

**Syllabus covered:**
- Detection time.
- Alarm time.
- Pre-movement time.
- Travel time.
- Total RSET.

**Exercise:**
- Create RSET calculation table.

**Formula:**
```text
RSET = detection time + alarm/notification time + pre-movement time + travel time
```

**Report / writing task:**
- Add RSET table to report.

**Done criteria:**
- RSET is decomposed, not treated as one black-box number.

---

### Day 3 — ASET/RSET Safety Margin

**Syllabus covered:**
- Safety margin.
- Interpretation under uncertainty.
- Conservative/non-conservative assumptions.

**Exercise:**
- Calculate ASET - RSET for each scenario.

**Report / writing task:**
- Draft ASET/RSET comparison section.

**Done criteria:**
- Comparison table exists with interpretation.

---

### Day 4 — Uncertainty and Behavioural Limitations

**Syllabus covered:**
- Occupant behaviour uncertainty.
- Model simplification.
- False precision.
- Scenario dependency.

**Exercise:**
- Create uncertainty table:
  - input,
  - uncertainty,
  - impact,
  - sensitivity.

**Report / writing task:**
- Draft limitations section.

**Done criteria:**
- Case 02 does not overclaim evacuation safety.

---

### Day 5 — Recommendations

**Syllabus covered:**
- Life safety recommendations.
- Operational controls.
- Detection/alarm.
- Wayfinding.
- Exit management.
- Further work.

**Exercise:**
- Draft practical recommendations.

**Report / writing task:**
- Link every recommendation to evidence.

**Done criteria:**
- Recommendations are practical and conditional.

---

### Day 6 — Week 11 Review

**Syllabus covered:**
- ASET/RSET QA.
- Consistency checking.

**Exercise:**
- Complete intermediate QA review.
- Identify missing figures/tables.

**Done criteria:**
- Case 02 report has all core technical content.

---

## Week 12 — Case 02 Report and First 3-Month Portfolio Review

### Week 12 Goal

Finish Case 02 and review the first three months as a coherent portfolio phase.

### Day 1 — Case 02 Report Draft

**Syllabus covered:**
- Full report assembly.
- Evacuation model reporting.
- ASET/RSET communication.

**Exercise:**
- Assemble Case 02 report.

**Report / writing task:**
- Complete:
  - executive summary,
  - method,
  - results,
  - interpretation,
  - limitations,
  - recommendations.

**Done criteria:**
- Case 02 draft is complete.

---

### Day 2 — Report QA and Editing

**Syllabus covered:**
- Claims vs evidence.
- Data traceability.
- Professional wording.

**Exercise:**
- Complete QA checklist.
- Review all figures and tables.

**Report / writing task:**
- Edit for clarity and caution.

**Done criteria:**
- Report is ready for portfolio use.

---

### Day 3 — Website Summary for Case 02

**Syllabus covered:**
- Public-facing technical communication.
- Visual explanation of ASET/RSET.

**Exercise:**
- Create `website_summary.md`.
- Draft one visual diagram of ASET/RSET logic.

**Report / writing task:**
- Write employer-facing summary.

**Done criteria:**
- Case 02 can be shown on the website.

---

### Day 4 — First 3-Month Skills Matrix Review

**Syllabus covered:**
- Evidence-based portfolio mapping.
- Skill claims for CV.

**Exercise:**
- Update `skills_matrix.md`.

**Skills to map:**
- FDS modelling.
- Smokeview visualisation.
- Python post-processing.
- Fire dynamics.
- UK fire engineering awareness.
- Tenability analysis.
- Pathfinder evacuation modelling.
- ASET/RSET.
- Consultancy report writing.
- QA and assumptions management.

**Done criteria:**
- Each skill has evidence from a file/report/case.

---

### Day 5 — First CV Attachment Draft

**Syllabus covered:**
- Translating portfolio into job application language.
- Concise project summaries.

**Exercise:**
- Create `cv_attachment_fire_engineering_portfolio_draft.md`.

**Report / writing task:**
- Draft one-page portfolio attachment with:
  - profile statement,
  - tools,
  - case studies,
  - skills demonstrated,
  - GitHub/website placeholder links.

**Done criteria:**
- First CV attachment draft exists.

---

### Day 6 — First 3-Month Retrospective and Next Phase Plan

**Syllabus covered:**
- Project review.
- Gap analysis.
- Preparing for smoke control and specialist fire risk cases.

**Exercise:**
- Write `first_3_months_review.md`.

**Report / writing task:**
- Include:
  - completed outputs,
  - incomplete outputs,
  - strongest evidence,
  - weakest area,
  - tool issues,
  - next 3-month priorities.

**Done criteria:**
- First 3 months are reviewed as a coherent phase.
- Month 4 can begin with smoke control sensitivity study.

---

# 8. Summary of Reports Produced in First 3 Months

| Report | Month | Purpose | Expected status |
|---|---:|---|---|
| Case 00: First FDS Room Fire Workflow | Month 1 | Foundation workflow report | Complete short report |
| Case 01: Makerspace Smoke Tenability Study | Month 2 | First serious building fire CFD case | Complete full report |
| Case 02: ASET/RSET and Pathfinder Evacuation Study | Month 3 | Life safety / evacuation case | Complete full report |
| First CV Portfolio Attachment Draft | Month 3 | Job application support | Draft |
| Website project summaries | Months 1–3 | Public portfolio content | Draft for 3 cases |
| Skills matrix | Months 1–3 | Evidence mapping | Updated continuously |

---

# 9. Codex Role During First 3 Months

Codex should assist with:

## Repository and templates

```text
Create the repository folder structure described in first_3_months_plan.md.
Create empty placeholder README.md files in every major folder.
Create the case study template folder and populate it with Markdown templates.
```

## Python scripts

```text
Create a Python script that reads FDS device CSV output, handles a units row, plots each device against time, and saves figures into a specified folder.
```

```text
Create a Python script that compares selected device outputs across multiple FDS case folders and generates combined comparison plots.
```

## Report support

```text
Check report.md for missing required sections based on the consultancy report template.
Generate a Markdown table of figures from files in the figures folder.
Check that every figure referenced in report.md exists.
```

## Website support

```text
Create a simple static website or React/Vite project with case study cards.
Each case study card should read from a Markdown or JSON summary file.
```

## Do not ask Codex to decide

Codex should not decide:

- whether a model is safe,
- whether a design complies with UK fire regulations,
- what HRR is correct without human review,
- what tenability threshold is legally acceptable,
- what recommendation is professionally valid,
- whether a case study can be used for real-world safety decisions.

Those require human engineering judgement and source checking.

---

# 10. Open Decisions to Confirm Later

These are intentionally not assumed.

1. Website technology:
   - static HTML,
   - React/Vite,
   - Next.js,
   - or another option.

2. Final PDF workflow:
   - Markdown to PDF,
   - LaTeX,
   - Word/Google Docs export,
   - or website-to-PDF.

3. PyroSim and Pathfinder access:
   - full licence,
   - trial/demo,
   - university licence,
   - or alternative workflow.

4. Public GitHub release strategy:
   - publish from start,
   - publish after Month 1,
   - publish after first complete case,
   - keep private until mature.

5. Case 01 geometry source:
   - fully fictional makerspace,
   - iForge-inspired but anonymised,
   - generic workshop/lab.

6. Report visual identity:
   - simple academic style,
   - consultancy style,
   - website-matched design system.

---

# 11. Daily Work Block Template

Use this after 17:00.

```text
17:00–17:10  Review today’s task and previous notes
17:10–18:00  Main technical work or reading
18:00–18:10  Short break
18:10–18:50  Exercise / model / writing output
18:50–19:00  Commit notes, update task log, define next step
```

If 3 hours are available:

```text
17:00–17:10  Review
17:10–18:10  Main technical work
18:10–18:20  Break
18:20–19:10  Exercise / modelling
19:10–19:20  Break
19:20–19:50  Report writing
19:50–20:00  QA, Git commit, next step
```

---

# 12. First 3 Months Completion Criteria

At the end of Month 3, the portfolio should contain:

```text
[ ] Clean public-ready repository structure
[ ] Public disclaimer
[ ] Standards map with UK/international/tool labels
[ ] Knowledge base notes started
[ ] Case study template
[ ] Report template
[ ] Assumptions register template
[ ] Design fire register template
[ ] Risk register template
[ ] Model QA checklist
[ ] FDS device output plotting script
[ ] Case 00 complete
[ ] Case 01 complete
[ ] Case 02 complete
[ ] Website summaries for 3 cases
[ ] Skills evidence matrix
[ ] First draft CV portfolio attachment
[ ] First 3-month review
```

---

# 13. Next Phase After Month 3

Month 4 should begin with:

```text
case_03_smoke_control_sensitivity
```

Main focus:
- smoke control,
- design option comparison,
- ventilation sensitivity,
- practical recommendations,
- PyroSim/ParaView workflow if available.

Month 5:
- battery/equipment fire risk,
- industrial liquid spill fire.

Month 6:
- model credibility,
- uncertainty,
- website,
- final PDF portfolio.
