# What I want to build

I want one substantial solo project where I can explain both the hardware and the software: the physical design, how I acquire measurements, how I preserve data and how I turn a recording into something I can inspect.

My starting scope is a **simulation and instrumentation platform**, with a later option to integrate it into a commercially powered model rocket. My own work will focus on design, electronics, firmware, tools and analysis. Motor construction and propulsion chemistry are outside this project.

## First-version requirements

All requirements below are **planned**. None is claimed as implemented or verified.

| ID | My requirement | Evidence I will produce |
| --- | --- | --- |
| SYS-01 | I can trace a record from its source to its displayed value. | A replay fixture, decoded output and display capture |
| SYS-02 | I can distinguish synthetic, bench and flight data. | Dataset metadata and visible source labels |
| HW-01 | I document the selected sensors, interfaces and power assumptions. | Block diagram, interface table and component decision |
| HW-02 | I can record sensor data on a stationary bench. | Timestamped recording with setup notes |
| MECH-01 | I can explain the packaging and service access of the avionics assembly. | Versioned CAD, drawings and a fit-check record |
| FW-01 | I report missing, invalid or stale samples explicitly. | Host tests and a bench fault-injection record |
| SW-01 | I can replay a recording without connected hardware. | Reproducible command and sample dataset |
| SW-02 | I reject unsupported schemas and malformed records clearly. | Parser tests with expected failures |
| ANA-01 | I compare any proposed AI method with a simple baseline. | Reproducible evaluation and failure examples |
| DOC-01 | I distinguish planned features from completed work. | Build journal and verification matrix |

## Decisions I have not made

- How much time and money I can commit to each milestone.
- Which tools, development boards, sensors and workshop access I already have.
- Which CAD tool I will use and how I will manufacture or source parts.
- Whether the first physical result is a bench assembly or a model-rocket integration.
- Which telemetry transport I need after wired replay works.
- The flight envelope, recovery approach and launch venue for any later flight phase.

I will not select numeric flight targets simply to make the project sound more ambitious. I will choose them after the model, hardware constraints and supervised launch route are understood.

## My definition of a useful first milestone

I can run a clearly labeled synthetic recording through a documented data contract, replay it in a small ground tool, and show how bad records are handled. In parallel, I have a justified avionics shortlist and a packaging concept. This gives me a real software result and a concrete hardware design to build next.
