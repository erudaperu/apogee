# Avionics and bench hardware

I plan to build a sensor-logging assembly that gives the software real measurements to work with. I will begin with available development hardware and document what it can actually do before deciding whether a custom PCB is worthwhile.

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
