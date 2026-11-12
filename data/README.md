# Data and recording contracts

I want every recording to explain where it came from and how to interpret it. I have not collected data for this project yet.

## Proposed record fields

This is a discussion draft, not a frozen schema.

| Field | Meaning I want to preserve |
| --- | --- |
| `schema_version` | Which record contract the reader must understand |
| `session_id` | Which acquisition or generated scenario produced the record |
| `source_kind` | `synthetic`, `bench` or `flight` |
| `sequence` | Position in the source stream, including detectable gaps |
| `timestamp` | Sample time using a documented clock and unit |
| `measurements` | Named values with explicit units and sensor identity |
| `quality` | Validity, missing-data and device-health information |

## Session metadata

I plan to record firmware/software versions, configuration, calibration references, sensor orientation, tool versions and relevant test conditions. I will distinguish measured values from derived values and keep the original recording unchanged.

## Dataset organization

I will keep synthetic fixtures, bench recordings and any later field observations in separate folders, each with a README. Each dataset will include:

- Its purpose, source and collection or generation method.
- A small readable example and the exact schema version.
- Units, timestamp conventions and known gaps.
- A checksum or other stable identifier for reproducibility.
- Any exclusions or transformations used for analysis.

I will avoid publishing unnecessary personal location details in field records. The public data should support the engineering result without exposing unrelated information.

**First task:** agree on a minimal record, then create one valid fixture and several intentionally invalid examples before implementing the parser.
