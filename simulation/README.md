# Modelling and simulation

I want a model that helps me ask better design questions and compare expected behavior with observations. I have not created or validated a simulation yet.

## My starting approach

I will use [OpenRocket](https://openrocket.info/features.html) as an established model-rocketry design and simulation reference. Any small model I write myself will have a stated learning purpose and a comparison case; I will not present agreement with my own code as independent validation.

## Deliverables I plan to keep here

- A versioned model file and a readable summary of its assumptions.
- A parameter table with units, provenance and uncertainty.
- Exported reference scenarios with tool version and settings.
- A comparison notebook or script that reproduces figures from saved results.
- A discrepancy note explaining where predictions differ and what I do not know.

## Questions for the first model

1. Which geometry and mass properties are measured, estimated or still undecided?
2. Which effects does the selected model include, and which does it omit?
3. How sensitive are the outputs to uncertain inputs?
4. Which quantities will my planned sensors actually observe?
5. Which comparisons can I make on a bench before any flight phase?

## Acceptance evidence

I will call the first modelling milestone complete when another person can open the saved model, identify its assumptions, reproduce one exported scenario and see a sensitivity comparison. Synthetic results will be labeled as model outputs, not measurements.

**Current status:** planned. No geometry, motor selection, performance target or simulated result has been committed.
