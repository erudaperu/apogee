# Ground software and replay

I want a ground tool that makes recordings from my model rocket understandable without requiring the original hardware. Replay is my first software milestone because it gives the physical build, avionics and analysis work a stable interface. I will use the same tool for synthetic records, bench tests and the planned flight recordings.

## How I will learn through the ground tool

I will use Python for a small command-line tool that supports my main C/C++ firmware work. I want to improve in both languages while keeping embedded programming the priority. My [learning exercises](../learning/README.md#exercises-that-become-real-project-features) start with validating one record, detecting missing records and reading a file before I add a graphical interface. I will write these pieces myself and keep input handling, validation and presentation separate as the tool grows.

For each change, I will predict the output for a tiny fixture, test normal and invalid input, and explain one design choice. Once the behavior is stable, I will refactor it without changing the documented outputs. This is how I want the project to improve my coding rather than only accumulate features.

## My first user flow

1. I open a recording and see its source, schema version and units.
2. I replay, pause and inspect individual records.
3. I see missing or invalid samples without the display inventing values.
4. I export a selected interval while preserving the original data.
5. I can reproduce the same view from the same input and settings.

## Proposed components

| Component | What I want it to do |
| --- | --- |
| Parser | Validate structure and give useful error locations |
| Session model | Keep metadata, records and derived values separate |
| Replay clock | Support pause, seek and a documented playback speed |
| Display | Show measurements, units, source and quality flags |
| Export | Produce a documented format with dataset provenance |

I will choose the UI framework after the first parser and replay contract are clear. A command-line version is a reasonable first implementation; a richer display can follow.

## Acceptance evidence

I will publish a small synthetic fixture, a run command, a replay capture and parser tests. I will include malformed input and a missing-sample case. Live telemetry is a later option, not a prerequisite for completing the replay tool.

**Current status:** planned. No application, parser or replay demo is implemented yet.
