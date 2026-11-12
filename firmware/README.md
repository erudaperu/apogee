# Firmware

I want small, testable firmware modules for my model rocket's instrumentation, with an observable path from sensor input to recorded output. I will verify them on the host and bench before integrating them into the physical model. I have not implemented this firmware yet.

## Proposed modules

| Module | Responsibility | First verification method |
| --- | --- | --- |
| Drivers | Read selected devices and report interface errors | Bench checks against documented conditions |
| Acquisition | Schedule samples and preserve their timestamps | Timing logs and missed-sample cases |
| Record encoder | Convert readings into the agreed data contract | Host tests and golden fixtures |
| Recorder | Save records and surface storage failures | Interrupted-recording tests |
| Health monitor | Expose stale, missing and invalid data | Injected fault cases |
| Transport adapter | Deliver records to the ground tool | Replay/bench comparison |

## Design choices I will make deliberately

- C or C++, based on the selected controller and toolchain.
- Bare-metal scheduling or an RTOS, based on measured needs.
- Timestamp source and rollover behavior.
- Buffer ownership and what happens when a consumer falls behind.
- How configuration and calibration versions appear in a recording.

I will document these choices rather than adding complexity for its own sake.

## What I want to test on the host

- Encoding and decoding compatibility.
- Boundary values, missing samples and invalid fields.
- Sequence gaps, timestamp rollover and out-of-order input.
- Bounded buffering behavior and explicit overflow reporting.

Host tests will establish logic behavior. Bench tests will establish how the actual controller and sensors behave. I will keep those claims separate.

**Current status:** planned. There is no firmware build, target configuration or timing result yet.
