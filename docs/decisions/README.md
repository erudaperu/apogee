# My decision log

I use this log to preserve reasoning, especially when a choice affects both software and hardware. An entry is a decision only when I mark it accepted.

| ID | Question | Status | Current direction |
| --- | --- | --- | --- |
| D-001 | What am I building? | Accepted | A physical model rocket from the start, with my own design and instrumentation; simulation and bench work support that goal |
| D-002 | What belongs in my own implementation? | Proposed | CAD/packaging, avionics integration, firmware, ground tools and analysis |
| D-003 | How will my model rocket be powered? | Accepted | An appropriate certified commercial motor; no motor development |
| D-004 | Which controller and sensors fit the first requirements? | Open | Confirm available equipment and compare candidates before buying |
| D-005 | What is the first ground interface? | Proposed | Recorded files or a wired link before wireless |
| D-006 | Where does AI belong? | Proposed | Offline analysis, evaluated against a simple baseline |
| D-007 | How much time can I dedicate? | Accepted | At least one hour a day; a minimum planned cadence of seven hours a week |
| D-008 | What are my budget and equipment limits? | Open | Start with available/free resources; set a spending ceiling before any purchases |
| D-009 | How do I account for my starting experience? | Accepted | Use my CAD familiarity, improve basic electronics skills, and learn rocketry fundamentals with established references and local guidance |
| D-011 | What should I spend now? | Accepted | Start with what I have and what is free; no new purchases in the starting phase |
| D-012 | How do I use the available boards? | Proposed | ESP8266 for bench acquisition; Jetson for ground-side replay/analysis; validate before flight selection |
| D-010 | What workshop access is confirmed? | Accepted | Free 3D-printer access at uOttawa and access to a soldering iron; ownership is not implied |

I have an **ESP8266 and a Jetson available**. I will confirm their exact board variants and existing accessories before connecting hardware. My starting allocation is ESP8266 bench acquisition and Jetson ground-side analysis; flight suitability remains unverified. I will use the computer already available for software work if the Jetson needs missing accessories. I have not selected a flight computer or authorized new purchases.

These accepted scope and time decisions reflect my starting direction as of **2026-11-12**. They do not imply that the design has been reviewed or that any hardware or software is complete.

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
