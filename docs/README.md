# My project notebook

I am starting **APOGEE**, a solo project that connects physical design, embedded electronics and software around an instrumented model rocket. APOGEE is a working name. This repository currently contains my project plan; I have not yet built or flown the system.

My first useful result will be a small, inspectable path from synthetic sensor records to a replayable ground display. I will develop the physical design and avionics alongside that software, then connect them through the same documented interfaces.

## Read in this order

| Document | What I use it for |
| --- | --- |
| [Requirements](requirements/README.md) | Define the first version and its evidence |
| [Architecture](architecture/README.md) | Keep subsystem responsibilities and interfaces clear |
| [Roadmap](roadmap/README.md) | Choose the next milestone without promising a launch date |
| [Decisions](decisions/README.md) | Record why I choose components and tools |
| [Build journal](journal/README.md) | Separate completed work from next steps |
| [Verification](../verification/README.md) | Plan how I will check each claim |

## My documentation rules

- I label work **planned**, **in progress**, **implemented**, or **verified**, and attach evidence before calling it verified.
- I keep model predictions, synthetic records, bench measurements and flight observations separate.
- I record units, assumptions, versions and limitations beside results.
- I use first person for my own work and credit external designs, libraries and advice.

## References I will start from

- [OpenRocket features](https://openrocket.info/features.html): an existing model-rocketry design and simulation tool I can use as a reference rather than treating a new simulator as ground truth.
- [NAR Model Rocket Safety Code](https://www.nar.org/ModelRocketSafetyCode): a hobby-rocketry reference that calls for certified, commercially made motors. It is not a substitute for checking requirements in the eventual launch jurisdiction.

**Current status:** planning only. Budget, available tools, launch location and component choices are still open.
