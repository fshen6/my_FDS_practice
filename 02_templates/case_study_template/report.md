# Case Study Report

## Executive Summary

Summarise the objective, method, main observations, and key limitations.

## 1. Introduction

Explain the purpose of the case and its portfolio context.

## 2. Design Question

State the question the model is trying to answer.

Example:

```text
For a simplified room fire, what smoke and temperature behaviour can be observed using a basic FDS + Smokeview + Python workflow?
```

## 3. Scenario Definition

Describe the modelled scenario.

- Geometry:
- Fire source:
- Ventilation:
- Simulation duration:
- Exclusions:

## 4. Assumptions

Summarise key assumptions and refer to `assumptions_register.md`.

## 5. Modelling Method

Describe how the model was created and analysed.

- FDS version:
- Mesh:
- Geometry approach:
- Fire definition:
- Output devices:
- Slice outputs:
- Smokeview workflow:
- Python post-processing workflow:

## 6. Results

Present the main outputs.

Suggested content:

- HRR check
- Smokeview observations
- Temperature plots
- Visibility plots, if used
- Device output plots
- Selected screenshots

## 7. Discussion

Explain what the results indicate.

Use cautious wording:

- The model indicates...
- Within the simplified assumptions...
- The result is sensitive to...
- This should not be interpreted as...

## 8. Limitations

State the key limitations.

- Simplified geometry
- Prescribed fire
- Mesh limitations
- Excluded physics
- Simplified materials
- No real-world compliance assessment

## 9. Conclusion

Summarise:

- main technical observation
- main workflow lesson
- what should be improved in the next case

## References

List sources and tool documentation.

- FDS User Guide
- Smokeview documentation
- Portfolio planning notes
- Other sources used

## Appendices

- FDS input summary
- Assumptions register
- Design fire register
- Risk register
- QA checklist
- Selected figures

