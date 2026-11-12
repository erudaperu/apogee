# Getting better at coding through APOGEE

I want APOGEE to make me a better programmer as well as a better system builder. A working result matters, but I also want to understand the code well enough to change it, debug it and explain its tradeoffs without relying on a generated solution.

My priority is **getting stronger at C/C++ and embedded firmware**, with **Python alongside it for tests, replay and analysis**. I want both languages to grow through the same system, while giving the embedded side more of my coding practice. I will adjust the pace after small baseline exercises in both languages instead of assuming that I need to restart from the basics. The project is still at the planning stage; the exercises below are not completed features or test results.

**[Project roadmap](../docs/roadmap/README.md)** · **[Firmware](../firmware/README.md)** · **[Ground software](../ground-station/README.md)** · **[Build journal](../docs/journal/README.md)**

## How I want to learn

For each small feature, I will follow this loop:

1. **Attempt:** write the behavior in plain language, make a tiny example and try an implementation myself.
2. **Ask for a hint:** show the input, expected result, actual result and what I already tried. I will ask for the smallest useful nudge before a complete answer.
3. **Review:** compare the implementation with the requirements and look for one concrete issue at a time.
4. **Explain:** describe the data flow, important invariants and one edge case in my own words.
5. **Refactor:** improve naming, responsibilities or structure while keeping the behavior the same.
6. **Record:** commit the change with a short note about what I learned and what is still uncertain.

I can use documentation, libraries and coding assistance. For the core learning tasks, I will attempt the code before asking for a full implementation. If I study an example solution, I will close it, rebuild the important part independently and explain the differences. I will credit external code and keep original authorship clear.

## My one-hour session

| Time | What I will do |
| --- | --- |
| 5 minutes | Choose one observable behavior and write the expected result |
| 10 minutes | Read only the documentation needed for that behavior |
| 25 minutes | Implement a small change myself |
| 15 minutes | Test it, investigate one failure and improve the code |
| 5 minutes | Make a focused commit and write the next smallest task |

This is a guide, not a timer I have to obey. When debugging takes longer, I will keep the failing example and resume from it. I will give C/C++ embedded work the larger share of coding sessions and use Python to inspect and test what that code produces. Hardware, CAD and rocketry-learning sessions still belong in the project; I will not let an ambitious software plan crowd them out.

## Exercises that become real project features

These are specifications for me to implement, not solutions. I will start with tiny inputs that I can check by hand. The exercise numbers are references, not a required order: I can bring L4 forward after the baseline so I am practicing C/C++ from the beginning. The fixtures are synthetic and are not flight-performance predictions.

| Exercise | Skill I want to practice | Small input and expected behavior | Project use |
| --- | --- | --- | --- |
| **L1 — Validate one reading** | Functions, types, conditions and explicit errors in Python | A draft record with `sequence=0`, `timestamp_ms=0`, `value=12.5`, `unit="test-unit"`, `source_kind="synthetic"` is accepted. A missing unit, negative sequence or non-finite value produces a useful error. | Parser and data contract |
| **L2 — Find missing records** | Iteration, collections and boundary cases | Sequence numbers `[0, 1, 3]` identify missing record `2`; `[]` is valid empty input; `[0, 1, 1]` reports a duplicate rather than hiding it. | Recording quality checks |
| **L3 — Make a small CLI** | File I/O, module boundaries and error handling | A file containing three valid records produces a count of three. A malformed second record identifies its location. An empty file has a documented result. | Ground inspection tool |
| **L4 — Build a bounded buffer** | Arrays, state, ownership and invariants in C/C++ | A capacity-three buffer accepts `1, 2, 3`. Under my first explicit policy, pushing `4` is rejected and the stored values remain `1, 2, 3`. Removing then adding an item preserves FIFO order. | Firmware logging queue |
| **L5 — Share one fixture** | Interfaces, serialization and cross-language testing | A C/C++ encoder and Python decoder agree on the same tiny synthetic record. A changed version is rejected clearly. I will choose and document the format first. | Firmware-to-ground boundary |
| **L6 — Reproduce a bug** | Debugging, hypotheses and regression checks | I deliberately introduce a sequence-gap or buffer-boundary bug, reduce it to a failing case, fix it and explain why the check now passes. | Reliable development habits |
| **L7 — Refactor without changing behavior** | Cohesion, naming and test design | Parsing, validation and presentation become separate responsibilities; the documented examples still produce the same results. | Maintainable ground software |
| **L8 — Add measured input** | Driver boundaries and integration debugging | I replace the synthetic producer with a bench source while keeping the record contract. I document units, validity and limitations. | Avionics integration |

The sample field names in L1 are a learning fixture, not a frozen flight schema. I will reconcile them with the [data contract](../data/README.md) before integrating anything.

## My first two-week rotation

I will use these as a sequence of roughly one-hour sessions. I can repeat a session, carry unfinished work forward or swap a hardware session with a coding session. This is not a deadline for finishing a rocket or its software.

| Sessions | Coding focus | Physical/system focus |
| --- | --- | --- |
| 1–2 | Attempt a small Python L1 example and a host-side C/C++ buffer-state exercise; record where I need help in each language | Read model-rocketry fundamentals and capture design questions |
| 3–4 | Start L4 in C/C++; draw the state after each operation and use Python examples to check record ordering | Inventory the ESP8266, Jetson, accessories and borrowable measurement tools |
| 5–6 | Test L4 boundaries, then start L2/L3 as small Python inspection tools; make focused commits | Sketch the rocket and avionics packaging concept |
| 7 | Review the first code, explain it without prompts and choose one refactor | Update the model assumptions and open decisions |
| 8–9 | Extend the C/C++ record encoder and explicit error handling, keeping host tests separate from target code | Check toolchain and board documentation before target work |
| 10–11 | Start L5 with one shared fixture and a documented format | Connect the intended measurements to the proposed sensor interfaces |
| 12–13 | Work through L6 and L7; preserve the smallest failing example | Continue CAD and local club/review-route research |
| 14 | Demonstrate what actually works, note gaps and plan the next small feature | Review the hardware/software fit together |

I will advance when I understand the current exercise, not simply because a session number has passed. Real sensor acquisition comes after the necessary equipment and bench setup are available; I can make progress with synthetic records first.

## What will count as learning evidence

For a completed learning task, I want more than a green test result:

- A focused commit containing code I can explain.
- A small example with an expected result I established independently.
- An edge case or failure I investigated, including the cause.
- A short explanation of why I chose the interface or data structure.
- One change I can make without copying the original solution.

I will keep this in the [build journal](../docs/journal/README.md), alongside the engineering evidence. I will label an exercise **attempted**, **understood**, or **applied in the project**; those labels describe my progress, not a formal qualification.

## Before I add AI

I will build the parser, data-quality checks and a transparent analysis baseline first. Later, I can use the Jetson for offline experiments if it helps a defined task. I want to understand the inputs, evaluation and failure cases before making a model part of the project story.

**Current status:** learning plan written; exercises, code and assessments are not yet completed.
