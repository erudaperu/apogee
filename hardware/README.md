# Avionics and bench hardware

I plan to build the sensor-logging assembly for my model rocket and give the software real measurements to work with. My electronics experience is basic, so I will use bench work to improve it and verify each part before integration. I will begin by checking the development hardware I can access and document what it can do before deciding whether a custom PCB is worthwhile.

## My current equipment position

I have access to 3D printers and a soldering iron. I have not confirmed a multimeter, sensors or an exact development-board inventory. I will confirm exact controller candidates and compare them against the measurement requirements before buying. I have not selected or purchased a controller for this project, and the budget is still open.

I will choose hardware from the measurement, logging and power requirements rather than build the requirements around a board name.

## Candidate functions

- A microcontroller to acquire and timestamp measurements.
- Motion and/or environmental sensors selected from the first requirements.
- Local recording and a simple wired path for inspection.
- Power and health monitoring appropriate to the selected components.

These are proposed functions. I have not selected parts or built an electrical design.

## Selection table I will complete

| Item | Evidence I need before choosing |
| --- | --- |
| Controller | Available tools, interfaces, memory needs and debugging access |
| Sensors | Datasheet range, resolution, timing, calibration and interface |
| Storage | Required recording duration, error handling and power-loss behavior |
| Power | Component requirements, measured consumption and operating margin |
| Connectors | Mechanical fit, accessibility and repeatable assembly |

## My first bench sequence

1. Document the exact parts and their manufacturer references.
2. Bring up one sensor and record stationary observations.
3. Compare reported units and orientation with the documented setup.
4. Add timestamps and quality flags, then save an inspectable recording.
5. Exercise non-hazardous faults such as a disconnected sensor or interrupted recording.
6. Compare the saved data with what the ground tool displays.

## Evidence I will keep

I will include a setup photo, connection documentation, firmware version, input conditions, expected behavior, observed behavior and limitations for each bench result. Hardware photographs will show what I built; they will not stand in for measurement evidence.

**Current status:** planned. No board, sensor, PCB or wiring design has been selected or verified.
