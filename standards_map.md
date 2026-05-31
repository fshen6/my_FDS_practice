# Standards And Guidance Map

This file defines how references should be labelled in this portfolio. The goal is to keep UK-specific guidance, international guidance, modelling documentation, and general engineering sources clearly separated.

## Reference Labels

| Label | Meaning | Example Uses |
|---|---|---|
| `[UK]` | UK-specific or England/Wales-specific context | Approved Document B, BS 9999, BS 9991, BS 7974, BS 5839 |
| `[International / US]` | US-origin or internationally referenced guidance | NFPA documents, US fire code context, international comparison notes |
| `[International / industrial]` | Industrial, insurance, multinational, or sector-specific practice | FM Global-style risk engineering, API/IEC/ISO industrial references |
| `[Tool / model]` | Software, modelling, validation, or tool documentation | FDS User Guide, FDS Validation Guide, Smokeview documentation, Pathfinder documentation |
| `[General engineering]` | Engineering science that is not jurisdiction-specific | heat transfer, combustion, fluid mechanics, uncertainty analysis |

## Rule For Mixing Standards

Do not mix UK and international standards without explicitly explaining:

1. which jurisdiction or practice context each reference belongs to;
2. why the non-UK reference is being mentioned;
3. whether it is being used for comparison, background learning, industrial context, or actual project guidance;
4. what the limitations are.

Never imply that an international, US, industrial, or tool-specific reference automatically applies to a UK building fire engineering project.

For UK building fire engineering context, start with the relevant UK guidance and standards unless the case is explicitly comparing frameworks or studying non-UK/industrial practice.

## Suggested Report Table

Use a table like this in case study reports.

| Reference | Label | Used For | How It Is Used | Limitation |
|---|---|---|---|---|
| BS 7974 | `[UK]` | Fire safety engineering framework | Scenario definition, assumptions, sensitivity, uncertainty, reporting | Portfolio learning only; not certified design |
| FDS User Guide | `[Tool / model]` | FDS modelling workflow | Input file setup, outputs, model interpretation | Tool guidance, not UK compliance guidance |
| Heat transfer textbook | `[General engineering]` | Fire science background | Radiation, convection, conduction concepts | General physics, not statutory guidance |

## Current Local UK Standards

The `Standards/` folder currently includes:

- `[UK]` BS 9999: fire safety in the design, management and use of buildings.
- `[UK]` BS 9991: fire safety in the design, management and use of residential buildings.
- `[UK]` BS 5839-1: fire detection and fire alarm systems in non-domestic premises.
- `[UK]` BS 7974: application of fire safety engineering principles to building design.

Check current official sources before relying on publication status, amendments, or detailed recommendations in a public report.

