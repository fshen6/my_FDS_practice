# FDS Learning Week 1 Checklist

Source plan: `first_3_months_fire_portfolio_plan.md`

Week 1 focus: repository setup and professional framework before modelling.

How to update this checklist:

- Use `[ ]` for not started.
- Use `[x]` for complete.
- Add short notes under any item when something is unclear, blocked, or worth revisiting.

## Week 1 Learning Outcomes

- [x ] I can explain what this portfolio is meant to prove: modelling workflow, technical reasoning, data processing, QA discipline, and consultancy-style reporting.
- [x ] I can explain what this portfolio is not: a certified fire engineering design, compliance submission, safety approval, or real-world decision tool.
- [x ] I can distinguish the roles of GitHub repository, final PDF portfolio, and public website.
- [x ] I can write limitation and disclaimer wording without overclaiming professional authority.
- [x ] I can separate UK-specific guidance, international/US guidance, industrial/insurance practice, tool documentation, and general engineering references.
- [x ] I can explain why UK and international standards should not be mixed without clear labelling and context.
- [x ] I can describe the purpose of assumptions registers, design fire registers, risk registers, model logs, QA checklists, and report templates.
- [x ] I can record software versions and setup details so future reports are traceable.
- [x ] I can explain why numerical post-processing is needed in addition to Smokeview screenshots.
- [x ] I can run a basic weekly review: what was created, what changed, what is blocked, and what comes next.

## Day 1 - Project Brief and Repository Skeleton

Learning points:

- [x ] Understand what a professional public portfolio should demonstrate.
- [x ] Understand the difference between learning evidence and certified professional work.
- [x ] Understand how GitHub, PDF output, and website output support different audiences.
- [x ] Understand why public disclaimers and limitation statements are needed.

Practical tasks:

- [x ] Create or confirm the local repository workspace.
- [x ] Create or plan the top-level project files:
  - [x ] `README.md`
  - [x ] `portfolio_plan.md`
  - [x ] `disclaimer.md`
  - [x ] `learning_log.md`
  - [x ] `skills_matrix.md`
  - [x ] `standards_map.md`
  - [x ] `references.md`
  - [x ] `.gitignore`
- [x ] Write the first project-purpose paragraph for `README.md`.
- [x ] Confirm the repository opens locally.
- [x ] Confirm the public disclaimer file exists or is queued for creation.

Day 1 exit check:

- [x ] I can explain the project purpose in one short paragraph.
- [x ] I can state clearly that the work is educational and non-certified.

## Day 2 - Standards Map and Knowledge Base Structure

Learning points:

- [x ] Understand UK vs international standards separation.
- [x ] Understand Approved Document B as England-specific building fire safety guidance.
- [x ] Understand the difference between statutory guidance, British Standards, NFPA-style practice, industrial guidance, and modelling documentation.
- [x ] Understand why references should be labelled before being used in reports.

Practical tasks:

- [x] Create or update `standards_map.md`.
- [x] Create or plan the `01_knowledge_base/` structure.
- [x ] Add standards/reference labels:
  - [x ] `[UK]`
  - [x ] `[International / US]`
  - [x ] `[International / industrial]`
  - [x ] `[Tool / model]`
  - [x ] `[General engineering]`
- [x ] Add a written rule not to mix UK and international standards without explanation.

Day 2 exit check:

- [ ] I can label a source correctly before using it.
- [ ] I can explain why source jurisdiction matters in fire engineering writing.

## Day 3 - Case Study and Report Templates

Learning points:

- [ ] Understand the purpose of a consultancy-style report structure.
- [ ] Understand how a client/design question frames a case study.
- [ ] Understand scope, exclusions, assumptions, limitations, and QA as separate report elements.
- [ ] Understand why repeatable templates make future case studies easier and more consistent.

Practical tasks:

- [ ] Create or plan `02_templates/case_study_template/`.
- [ ] Create or plan reusable template files:
  - [ ] `brief.md`
  - [ ] `assumptions_register.md`
  - [ ] `design_fire_register.md`
  - [ ] `risk_register.md`
  - [ ] `model_log.md`
  - [ ] `qa_checklist.md`
  - [ ] `report.md`
  - [ ] `website_summary.md`
- [ ] Insert the full report structure into `report.md`.
- [ ] Create or request a reusable case study folder generator script/checklist.

Day 3 exit check:

- [ ] I can create a new case study by copying the template.
- [ ] I can explain what each template file is for.

## Day 4 - Tool Installation and Version Recording

Learning points:

- [ ] Understand the basic workflow relationship between FDS, Smokeview, Python, Git, and VS Code.
- [ ] Understand the difference between solver, visualisation tool, and post-processing tool.
- [ ] Understand why software version control matters in professional reporting.
- [ ] Understand how installation issues should be recorded rather than hidden.

Practical tasks:

- [ ] Install or confirm installation of FDS.
- [ ] Install or confirm installation of Smokeview.
- [ ] Install or confirm the Python environment.
- [ ] Install or confirm Git.
- [ ] Install or confirm VS Code.
- [ ] Create or plan `00_project_management/software_setup.md`.
- [ ] Record:
  - [ ] operating system
  - [ ] FDS version
  - [ ] Smokeview version
  - [ ] Python version
  - [ ] package management method
  - [ ] known installation issues

Day 4 exit check:

- [ ] `fds` and `smokeview` can be called, or their install paths are documented.
- [ ] Version information is recorded in a reusable place.

## Day 5 - Python Environment and Shared Scripts

Learning points:

- [ ] Understand why post-processing matters in consultancy-style modelling.
- [ ] Understand why visual CFD screenshots alone are not enough evidence.
- [ ] Understand what FDS device CSV outputs are used for.
- [ ] Understand the basic expected behaviour of an FDS device CSV plotter.

Practical tasks:

- [ ] Create a Python virtual environment.
- [ ] Create or plan `04_shared_scripts/requirements.txt`.
- [ ] Create or plan `04_shared_scripts/fds_devc_plotter.py`.
- [ ] Add script usage instructions to `04_shared_scripts/README.md`.
- [ ] Ensure the plotter requirement is clear:
  - [ ] read a CSV path
  - [ ] detect or handle a units row
  - [ ] plot each device against time
  - [ ] save figures to an output folder
  - [ ] report missing or unclear columns
- [ ] Test the script on dummy CSV or sample data.

Day 5 exit check:

- [ ] I can explain what quantitative output adds beyond a Smokeview screenshot.
- [ ] The first plotting workflow either runs or has clear remaining blockers.

## Day 6 - Weekly Review and Portfolio QA

Learning points:

- [ ] Understand QA as a weekly habit, not a final clean-up step.
- [ ] Understand document control and version control as evidence of professional working practice.
- [ ] Understand what makes early-stage portfolio work look structured and credible.
- [ ] Understand how to capture decisions and issues before they are forgotten.

Practical tasks:

- [ ] Create or plan `portfolio_quality_checklist.md`.
- [ ] Create or plan `decision_log.md`.
- [ ] Create the first Git commit if the folder has been initialised as a Git repository.
- [ ] Write a Week 1 reflection in `learning_log.md`.
- [ ] Review whether each Day 1-5 exit check has been met.

Day 6 exit check:

- [ ] Repository is in a usable state.
- [ ] First Git commit is complete, or Git initialisation is explicitly listed as a blocker.
- [ ] Week 1 review is written.

## Week 1 Final QA

- [ ] Repository/project structure is usable enough to begin Week 2.
- [ ] Public disclaimer exists and is easy to find.
- [ ] Standards map has clear source labels.
- [ ] Knowledge base structure exists or has a documented creation plan.
- [ ] Case study template exists or has a documented creation plan.
- [ ] Software setup details are recorded.
- [ ] Python post-processing setup has started.
- [ ] Weekly reflection is written.
- [ ] Any blockers are listed with a next action.

## Notes And Blockers

- [ ] Note any unclear learning points here.
- [ ] Note any installation blockers here.
- [ ] Note any files/folders that still need to be created here.
- [ ] Note questions to ask Codex in the next session here.

