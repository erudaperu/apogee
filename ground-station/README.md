# Ground software and replay

I want a ground tool that makes recordings from my model rocket understandable without requiring the original hardware. Replay is my first software milestone because it gives the physical build, avionics and analysis work a stable interface. I will use the same tool for synthetic records, bench tests and the planned flight recordings.

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
