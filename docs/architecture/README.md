# System architecture

I am defining a measurement system with two development paths that meet at a shared data contract. This is a proposed architecture, not a diagram of working hardware.

## Responsibilities

| Part | What I want it to own | What I keep outside it |
| --- | --- | --- |
| Physical assembly | Packaging, access, mounting and documented mass properties | Data interpretation |
| Avionics | Sensors, power distribution and electrical interfaces | Ground visualization |
| Firmware | Acquisition, timestamps, health flags and recording | AI decisions |
| Ground software | Decode, inspect, replay and export records | Changing the original data |
| Simulation | Generate labeled scenarios and expose assumptions | Certifying real-world performance |
| Offline analysis | Compare recordings, estimates and anomaly methods | Flight-critical control |

My initial flight instrumentation is observational. I am not planning autonomous guidance or AI in the flight-control path.

## Proposed interfaces

| Interface | Producer → consumer | Contract I need to decide |
| --- | --- | --- |
| Sensor reading | Sensor driver → acquisition task | Unit, validity, timestamp convention and calibration version |
| Measurement record | Acquisition task → recorder/transport | Schema version, sequence number, source and sample time |
| Recording | Recorder → ground tool | File format, session metadata and interruption handling |
| Replay stream | File reader → display | Original timing, speed control and end-of-file behavior |
| Analysis result | Offline tool → report | Dataset identity, method version, parameters and limitations |

The first transport can be a file. I will settle and test the record contract before choosing wireless hardware.

## Boundaries I will test

- A corrupt record must not silently become a plausible measurement.
- A missing sample must stay distinguishable from a zero measurement.
- A display restart must not alter the source recording.
- A sensor fault must be visible in the record and in the ground display.
- An analysis result must point to the exact dataset and settings used.

## Open design questions

I still need to choose the controller, sensor set, clock strategy, storage method and first ground interface. I will record these choices in [the decision log](../decisions/README.md), along with the alternatives I considered.
