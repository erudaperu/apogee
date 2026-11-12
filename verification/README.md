# Verification and evidence

I want every visible project claim to have a matching artifact. This matrix starts empty on purpose: I have planned the work, not performed the tests.

| ID | Check I plan to perform | Evidence I will save | Status |
| --- | --- | --- | --- |
| V-01 | Valid records survive encoding and decoding | Input fixture, expected output and test result | Planned |
| V-02 | Invalid schemas and malformed values are rejected | Negative fixtures and error output | Planned |
| V-03 | Missing samples remain visible through replay | Gapped fixture and display capture | Planned |
| V-04 | A stationary sensor recording has documented units and orientation | Setup notes, raw data and comparison | Planned |
| V-05 | A disconnected sensor produces a visible fault | Bench record and ground display | Planned |
| V-06 | Recording interruption leaves recoverable data or an explicit failure | Interruption procedure and observed result | Planned |
| V-07 | CAD matches the assembled packaging | Drawing revision, measured fit and photos | Planned |
| V-08 | A model scenario is reproducible | Model file, tool version and exported result | Planned |
| V-09 | Analysis can be repeated on the same dataset | Dataset identifier, settings and report | Planned |
| V-10 | Any AI candidate is compared with a simple baseline | Held-out evaluation and failure examples | Planned |
| V-11 | The physical model matches its documented configuration | Design revisions, assembly record and review notes | Planned |
| V-12 | I can explain and independently change a completed learning module | Learning journal entry, focused commit and a small change with checked behavior | Planned |

## My result template

```text
Check ID and date:
Requirement:
Versions and setup:
Input and conditions:
Expected behavior:
Observed behavior:
Result: pass / fail / inconclusive
Evidence links:
Limitations and follow-up:
```

## Learning evidence

A passing check shows behavior for the cases tested. To show my own understanding, I will also explain the relevant data flow, preserve a failure I investigated and make a small independent change. I will record that alongside the [coding learning track](../learning/README.md), without presenting an exercise as completed hardware or a flight result.

## Before any field phase

My objective includes a physical model-rocket flight. I will make a readiness review for the actual configuration, launch location, supervision and applicable requirements before that phase. I will use an appropriate certified commercial motor. The [NAR Model Rocket Safety Code](https://www.nar.org/ModelRocketSafetyCode) is a useful reference; I will establish which local rules and launch organization apply as part of my first learning phase.

Bench success will not be described as flight qualification. A simulation will not be described as a test flight.
