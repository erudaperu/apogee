<img src="assets/project-wordmark.svg" alt="APOGEE — my model rocket and coding lab. Planning and requirements." width="100%">

**My solo hardware + software project · in progress, starting with planning and requirements.**

I want to build my own instrumented model rocket and understand the whole system: how I model it, design the physical assembly, collect measurements, write the firmware and make the data useful. A commercially powered model rocket is the goal from the start. I will use simulation and a sensor test bench to make design decisions and check the system before flight.

**APOGEE is my working title.** My scope is a model rocket using a certified commercial motor, with my own work focused on modelling, airframe design, packaging, electronics and software. I will start with available equipment and free resources; sensors, a later spending ceiling and the flight configuration still need decisions.

**[My coding track](learning/README.md)** · **[My roadmap](docs/roadmap/README.md)** · **[System architecture](docs/architecture/README.md)** · **[Open decisions](docs/decisions/README.md)** · **[Build journal](docs/journal/README.md)**

## What I'm working toward

| Hardware and physical design | Software and data |
| :--- | :--- |
| Model-rocket geometry, CAD and mass properties | Reproducible modelling and simulation comparisons |
| Avionics packaging, sensor selection and bench assembly | C/C++ acquisition firmware, timestamps and health reporting |
| Documented electrical interfaces and power assumptions | Ground software for inspection, replay and export |
| Fit checks, assembly records and measured bench behaviour | Offline analysis, with any AI evaluated against a baseline |

I want the result to be more than a launch video. I want someone to be able to follow a measurement from the sensor through my firmware and into the ground tool, then understand where it agrees with the model and where it does not.

<img src="assets/system-map.svg" alt="Proposed APOGEE architecture: model and CAD, rocket and sensors, firmware and logger, ground software and offline analysis" width="100%">

## Where I am now

| Work | Status |
| :--- | :--- |
| Project brief, subsystem plans and milestone structure | Written — initial planning draft |
| Model rocket with a certified commercial motor | Scope selected |
| Daily work cadence | At least one hour a day |
| Starting resources | ESP8266, Jetson, soldering access and free uOttawa 3D printing |
| Starting budget | No new purchases; later flight-build costs still open |
| Simulation, CAD, electronics and firmware | Planned |
| Ground station and analysis tools | Planned |
| Bench measurements and flight results | Not performed |

This repository currently contains my engineering and learning plan. I have not built the vehicle or implemented the flight system yet.

## How I will get better at coding

I want this project to make me a stronger programmer, especially in **C/C++ and embedded firmware**. I will use **Python for tests, replay and analysis**, working across both languages through the same data contract. My [coding track](learning/README.md) gives me small exercises, expected behaviours and a one-hour practice format.

I will attempt the core features myself, use hints and code review when I get stuck, and keep evidence that I can explain, debug and change my implementation. The exercises are specifications for me to work through, not completed solutions.

## My starting point

I know CAD and basic electronics, and I'm new to rocketry. I have an ESP8266 and a Jetson available, soldering-iron access and free 3D printing at uOttawa. I can commit at least an hour a day—about seven hours a week. I will use that time for a mix of learning, designing, building and recording what I find. My first phase includes model-rocketry fundamentals and identifying an appropriate local club or supervised launch route.

## My first milestone

I will define a beginner-appropriate model-rocket concept and its constraints, then create a small synthetic sensor recording, define its units and quality flags, and build a replay tool that handles both valid and broken records. Alongside that, I will compare feasible controller/sensor combinations and sketch the avionics packaging.

I will call that milestone complete when I can publish a reproducible demo, parser tests, a justified hardware shortlist, a model-rocket concept and a packaging concept. The next milestone will connect the same data contract to real bench measurements.

## My project map

| Area | What I am defining here |
| :--- | :--- |
| [Coding track](learning/README.md) | C/C++ and Python exercises, practice sessions and learning evidence |
| [Project notebook](docs/README.md) | How I organize the work and record evidence |
| [Requirements](docs/requirements/README.md) | What the first version must do and how I will check it |
| [Architecture](docs/architecture/README.md) | Subsystems, responsibilities and interfaces |
| [Roadmap](docs/roadmap/README.md) | Milestones, exit evidence and my first work session |
| [Modelling](simulation/README.md) | Reference scenarios, assumptions and sensitivity comparisons |
| [Mechanical design](mechanical/README.md) | CAD, packaging, drawings, mass properties and fit checks |
| [Parts and budget](procurement/README.md) | Available resources, borrow-first gaps and spending decisions |
| [Avionics](hardware/README.md) | Sensors, controller, power and bench measurements |
| [Firmware](firmware/README.md) | Acquisition, recording, health flags and host tests |
| [Ground software](ground-station/README.md) | Parsing, replay, inspection and export |
| [Data contracts](data/README.md) | Units, timestamps, provenance and recording formats |
| [Analysis and AI](analysis/README.md) | Offline methods, baseline comparisons and failure examples |
| [Verification](verification/README.md) | Planned checks and the evidence I need before making a claim |
| [Decisions](docs/decisions/README.md) | Alternatives, tradeoffs and choices still open |
| [Build journal](docs/journal/README.md) | What I attempted, learned and completed |

## How I will build it

I will start with a narrow, testable path and expand it as the results justify it. Wireless telemetry, a custom PCB and AI are possible extensions. I will keep them tied to a clear need and a way to measure whether they help.

I'm using [OpenRocket](https://openrocket.info/features.html) as a starting reference for model-rocketry design and simulation. I'll document the assumptions and differences in any models I write myself. My initial avionics will collect observations; offline analysis will stay separate from flight-critical control.

**Eren Arikan · [My GitHub](https://github.com/erudaperu)**
