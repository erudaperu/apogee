# What I want to build

I want one substantial solo project where I can explain both the hardware and the software: the physical design, how I acquire measurements, how I preserve data and how I turn a recording into something I can inspect.

My scope is a **physical model rocket with my own design and instrumentation**, powered by a certified commercial motor. Modelling, bench testing and replay software support that end-to-end goal. My own work will focus on CAD, airframe and avionics packaging, electronics, firmware, ground tools and analysis. Motor construction and propulsion chemistry are outside this project.

I know CAD, have basic electronics experience and have no rocketry experience yet. I will start by learning established model-rocketry practice and finding a local club or experienced supervisor before finalizing the physical design. My planned cadence is at least one hour a day, or seven hours a week.

A second goal is to improve my programming through the build. I will prioritize C/C++ embedded-logic tasks and use Python alongside them for tests, ground tools and analysis. My [learning track](../../learning/README.md) keeps the work small enough to implement and understand myself.

## First-version requirements

All requirements below are **planned**. None is claimed as implemented or verified.

| ID | My requirement | Evidence I will produce |
| --- | --- | --- |
| SYS-01 | I can trace a record from its source to its displayed value. | A replay fixture, decoded output and display capture |
| SYS-02 | I can distinguish synthetic, bench and flight data. | Dataset metadata and visible source labels |
| HW-01 | I document the selected sensors, interfaces and power assumptions. | Block diagram, interface table and component decision |
| HW-02 | I can record sensor data on a stationary bench. | Timestamped recording with setup notes |
| MECH-01 | I can explain the packaging and service access of the avionics assembly. | Versioned CAD, drawings and a fit-check record |
| MECH-02 | I can trace my physical rocket design from a documented concept to an assembled model. | Design revisions, parts record, assembly photos and review notes |
| FW-01 | I report missing, invalid or stale samples explicitly. | Host tests and a bench fault-injection record |
| SW-01 | I can replay a recording without connected hardware. | Reproducible command and sample dataset |
| SW-02 | I reject unsupported schemas and malformed records clearly. | Parser tests with expected failures |
| ANA-01 | I compare any proposed AI method with a simple baseline. | Reproducible evaluation and failure examples |
| LEARN-01 | I can explain, debug and independently modify the core learning code. | My attempt, review notes, a reproduced failure and a focused follow-up change |
| DOC-01 | I distinguish planned features from completed work. | Build journal and verification matrix |

## Decisions I have not made

- A later spending ceiling, after the zero-purchase starting phase, and how I divide sessions between learning, hardware and software.
- Exact variants/accessories for the available ESP8266 and Jetson, plus sensors and measurement tools I can borrow. Free 3D printing at uOttawa and soldering-iron access are confirmed.
- Which CAD tool I will use and which parts are suitable for the 3D-printing access I have, versus sourcing them another way.
- A beginner-appropriate physical configuration and a supervised route to the first flight.
- Which telemetry transport I need after wired replay works.
- The flight envelope, recovery approach and launch venue for the planned flight phase.

I will not select numeric flight targets simply to make the project sound more ambitious. I will choose them after the model, hardware constraints and supervised launch route are understood.

## My definition of a useful first milestone

I can explain my first model-rocket concept, identify the learning and review steps it needs, and connect it to a justified avionics shortlist. In parallel, I can run a clearly labeled synthetic recording through a documented contract, replay it in a small ground tool, and show how bad records are handled. The exit evidence pairs a concrete physical design with working software.
