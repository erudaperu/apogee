# My roadmap

I am building toward a physical model rocket with a certified commercial motor, my own design work and an inspectable instrumentation system. I can dedicate at least one hour a day, so I will plan around **seven hours a week minimum**. I have not assigned a launch date. I will begin with a zero-purchase phase using available and free resources.

I know CAD, have basic electronics experience and am new to rocketry. I have an ESP8266 and a Jetson available, access to a soldering iron, and free 3D-printer access at uOttawa. My first phase is therefore learning and scope definition, with hardware and software developed together from the start.

| Milestone | Hardware / physical work | Software work | Exit evidence |
| --- | --- | --- | --- |
| M0 — Learn and define | Learn model-rocketry fundamentals; identify a local club or experienced supervisor; inventory tools and budget | Define initial measurements, units and a replay use case | Learning notes, a review route, requirements and open decisions |
| M1 — Design the first version | Model the rocket concept; draft CAD and avionics packaging; compare suitable components | Define the record contract; build a synthetic fixture, parser and replay | Reviewed concept, CAD exports, hardware shortlist and reproducible replay |
| M2 — Build and measure | Build the physical assembly and a separate avionics bench setup; record fit and assembly checks | Implement acquisition, health flags and logging | Assembly record, bench data, host tests and observed fault behavior |
| M3 — Integrate | Fit the verified instrumentation into the model and document the actual configuration | Connect recordings to the ground display and offline analysis | Fit checks, configuration record, replay capture and integration report |
| M4 — Review readiness | Review the model, commercial motor choice, recovery approach and supervised launch arrangements | Freeze and document the logging configuration | Readiness review with resolved and unresolved items stated |
| M5 — Fly, record and compare | Conduct a model-rocket flight only after the readiness review and applicable requirements are met | Compare recorded observations with predictions and document discrepancies | Flight record, data provenance, analysis and a revision plan |

**Current milestone: M0 — planning.** These milestones describe my intended work. No hardware, software, tests or flight results have been completed yet.

## Coding is part of every milestone

I will use the [coding learning track](../../learning/README.md) alongside this roadmap. My main coding priority is C/C++ embedded firmware, with Python supporting tests, replay and analysis. I will work on both from the beginning and give the embedded side the larger share of coding practice. A software milestone is not complete for me until I can explain the implementation, reproduce a useful failure and make a small change independently.

| Project stage | Coding work I will practice |
| --- | --- |
| M0–M1 | C/C++ state and bounded-buffer basics alongside Python validation, collections, file I/O and a clear command-line interface |
| M1–M2 | C/C++ data structures, bounded state, explicit errors and host tests before target integration |
| M2–M3 | Shared fixtures, interface debugging, replay and refactoring without changing behavior |
| M3 onward | Reproducible analysis, baseline comparisons and careful evaluation before AI |

## My first seven sessions

I will use these as roughly one-hour starting blocks and carry unfinished work into the next session. They are a work order, not a promise that the design will be finished in one week.

- [ ] **Session 1:** Read a small section of model-rocketry fundamentals, then attempt tiny Python validation and C/C++ state exercises to identify where I need help.
- [ ] **Session 2:** Find a suitable local club or experienced supervisor, and establish the requirements for the eventual launch location.
- [ ] **Session 3:** Check the ESP8266 and Jetson variants and accessories, confirm borrowable sensors and a multimeter, and follow my reuse-first parts plan before considering purchases.
- [ ] **Session 4:** Sketch the first rocket concept and identify what needs review before I commit to dimensions or components.
- [ ] **Session 5:** Define the initial measurements, units and quality flags; start a small C/C++ record or bounded-buffer function and check its state by hand.
- [ ] **Session 6:** Check the C/C++ boundary cases and write a small Python validation or missing-record helper for the ground tool.
- [ ] **Session 7:** Explain the code and hardware choices in my own words, make one small refactor, update the decision log and choose the next task.

For the first phase, I will use the Canadian Association of Rocketry's [model-rocketry information](https://www.canadianrocketry.org/en/regulations/model-rocketry) and [affiliated-club directory](https://www.canadianrocketry.org/en/membership/affiliated-clubs) as starting references. I have not selected a club or launch location, and I still need to establish which requirements apply to the actual activity.

## My continuing cadence

I will reserve regular sessions for physical design and electronics, hands-on coding sessions for firmware and ground software, and one review session to connect the evidence and update the journal. I will adjust the split to the current milestone while keeping both sides moving.

Wireless telemetry, a custom PCB and AI are extensions I will add when they solve a documented problem. The core project remains my physical model rocket, its instrumentation and the software that lets me inspect what happened.
