# Offline analysis and AI

I want to use analysis to explain recordings and find data-quality problems. AI is a possible extension, not a feature I will claim before I have a useful task and an evaluation.

## First question

Can I flag unusual or unreliable sensor segments more usefully than a simple set of transparent rules?

I will begin with deterministic checks for missing samples, stale values and implausible changes. Those checks give me a baseline and help me understand the data before considering a learned method.

## Evaluation I plan to build

| Part | My approach |
| --- | --- |
| Data | Clearly labeled synthetic scenarios, followed by separately labeled bench recordings |
| Baseline | Simple rules with saved parameters and known limitations |
| Candidate | A small offline method chosen only after the baseline exists |
| Split | Separate recordings or scenarios to reduce leakage between training and evaluation |
| Metrics | False positives, missed labeled events and detection delay where meaningful |
| Review | Example successes, failures and cases where the baseline wins |

I will not treat synthetic accuracy as evidence of flight performance. If I do not have trustworthy labels, I will describe the work as exploratory analysis rather than a validated detector.

## Planned outputs

- A reproducible analysis command or notebook.
- Dataset identifiers, preprocessing settings and method versions.
- A comparison table against the baseline.
- Plots that identify units, data source and uncertainty.
- A short explanation of whether the added complexity helped.

AI will remain offline and outside flight-critical control. The first useful outcome may be a well-tested baseline with no trained model at all.

**Current status:** planned. No dataset evaluation, trained model or performance result exists yet.
