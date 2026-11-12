# My roadmap

I am building toward a physical model rocket with a certified commercial motor, my own design work and an inspectable instrumentation system. I can dedicate at least one hour a day, so I will plan around **seven hours a week minimum**. I have not assigned a launch date or a budget.

I know CAD, have basic electronics experience and am new to rocketry. I have access to 3D printers and a soldering iron. My first phase is therefore learning and scope definition, with hardware and software developed together from the start.

| Milestone | Hardware / physical work | Software work | Exit evidence |
| --- | --- | --- | --- |
| M0 — Learn and define | Learn model-rocketry fundamentals; identify a local club or experienced supervisor; inventory tools and budget | Define initial measurements, units and a replay use case | Learning notes, a review route, requirements and open decisions |
| M1 — Design the first version | Model the rocket concept; draft CAD and avionics packaging; compare suitable components | Define the record contract; build a synthetic fixture, parser and replay | Reviewed concept, CAD exports, hardware shortlist and reproducible replay |
| M2 — Build and measure | Build the physical assembly and a separate avionics bench setup; record fit and assembly checks | Implement acquisition, health flags and logging | Assembly record, bench data, host tests and observed fault behavior |
| M3 — Integrate | Fit the verified instrumentation into the model and document the actual configuration | Connect recordings to the ground display and offline analysis | Fit checks, configuration record, replay capture and integration report |
| M4 — Review readiness | Review the model, commercial motor choice, recovery approach and supervised launch arrangements | Freeze and document the logging configuration | Readiness review with resolved and unresolved items stated |
| M5 — Fly, record and compare | Conduct a model-rocket flight only after the readiness review and applicable requirements are met | Compare recorded observations with predictions and document discrepancies | Flight record, data provenance, analysis and a revision plan |

**Current milestone: M0 — planning.** These milestones describe my intended work. No hardware, software, tests or flight results have been completed yet.

## My first seven sessions

I will use these as roughly one-hour starting blocks and carry unfinished work into the next session. They are a work order, not a promise that the design will be finished in one week.

- [ ] **Session 1:** Read established model-rocketry fundamentals and record the terms and design questions I need to understand.
- [ ] **Session 2:** Find a suitable local club or experienced supervisor, and establish the requirements for the eventual launch location.
- [ ] **Session 3:** Document the 3D-printer and soldering-iron access, confirm exact board and measurement-tool availability, and set a budget ceiling before selecting parts.
- [ ] **Session 4:** Sketch the first rocket concept and identify what needs review before I commit to dimensions or components.
- [ ] **Session 5:** Define the initial measurements, units and quality flags; draft one example data record.
- [ ] **Session 6:** Outline the parser and replay behavior, including a missing-sample case.
- [ ] **Session 7:** Review the hardware and software choices together, update the decision log and choose the next smallest build task.

For the first phase, I will use the Canadian Association of Rocketry's [model-rocketry information](https://www.canadianrocketry.org/en/regulations/model-rocketry) and [affiliated-club directory](https://www.canadianrocketry.org/en/membership/affiliated-clubs) as starting references. I have not selected a club or launch location, and I still need to establish which requirements apply to the actual activity.

## My continuing cadence

I will reserve regular sessions for physical design and electronics, regular sessions for firmware and ground software, and one review session to connect the evidence and update the journal. I will adjust the split to the current milestone while keeping both sides moving.

Wireless telemetry, a custom PCB and AI are extensions I will add when they solve a documented problem. The core project remains my physical model rocket, its instrumentation and the software that lets me inspect what happened.
