# My decision log

I use this log to preserve reasoning, especially when a choice affects both software and hardware. An entry is a decision only when I mark it accepted.

| ID | Question | Status | Current direction |
| --- | --- | --- | --- |
| D-001 | Where do I start? | Proposed | Simulation, replay and bench instrumentation |
| D-002 | What belongs in my own implementation? | Proposed | CAD/packaging, avionics integration, firmware, ground tools and analysis |
| D-003 | How will a later model rocket be powered? | Proposed | An appropriate certified commercial motor; no motor development |
| D-004 | Which controller and sensors fit the first requirements? | Open | Compare existing equipment before buying |
| D-005 | What is the first ground interface? | Proposed | Recorded files or a wired link before wireless |
| D-006 | Where does AI belong? | Proposed | Offline analysis, evaluated against a simple baseline |
| D-007 | What are my time and budget limits? | Open | Awaiting a personal inventory and allocation |

## Template for a new decision

```text
ID and title:
Date:
Status: proposed / accepted / superseded

Problem I need to solve:
Constraints and evidence:
Options I considered:
Choice and reason:
Tradeoffs I accept:
How I will verify the choice:
What would make me revisit it:
Links to supporting work:
```

I will keep superseded decisions with a link to the replacement. A changed design should leave an explanation, not just a changed file.
