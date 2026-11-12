# My reuse-first parts and budget plan

I will start with the equipment I can access and the resources that are free, then estimate a specific next purchase only when it removes a real blocker. **My planned new spending for the starting phase is C$0.** This is a development-phase budget, not a claim that a complete flying rocket will cost nothing.

## Resources I can start from

| Resource | Availability | My proposed use | New purchase planned |
| --- | --- | --- | --- |
| ESP8266 | Available; exact development-board variant to confirm | Bench firmware, generated records and then sensor acquisition | C$0 |
| Jetson | Available; exact variant and working setup to confirm | Ground-side replay or offline analysis when useful | C$0 |
| uOttawa 3D printers | Free access | Initial fit models, bench fixtures and packaging prototypes | C$0 within the access provided |
| Soldering iron | Access available | Electronics assembly after the design and components are checked | C$0 |
| CAD and simulation software | Use free tools or access I already have | Design work and documented reference scenarios | C$0 |
| Python and Git | Free tools | Record schema, parser, replay, tests and version control | C$0 |

Printing access does not establish that every material or part is available or suitable for flight. I will check the actual printer/material options and record what I use.

## What I need to inventory or borrow first

| Item | Why I need to check it | My next action |
| --- | --- | --- |
| Compatible board cables and power supplies | Board availability does not confirm a complete working setup | Inventory existing accessories and read the exact board documentation |
| Multimeter | Basic electrical checks and debugging | Confirm lab or borrowing access |
| Breadboard, jumpers and basic components | Non-flight sensor experiments | Check existing lab stock and borrowing options |
| Suitable sensor breakout | The first real measurement path | Define the measurement, then check available sensors |
| Logging/storage resources | Preserve recordings | Start with wired records saved on the ground computer; evaluate onboard storage later |
| Airframe and recovery materials | A complete physical model rocket | Build a reviewed parts list before estimating purchases |
| Commercial motor and launch access | Eventual flight phase | Resolve the configuration and supervised launch route before any purchase |

I have not priced the last three flight-related categories because the configuration is not selected. I will not hide those unknown costs inside a C$0 total.

## My first no-purchase deliverables

1. A model-rocket concept and list of assumptions to review.
2. A small synthetic dataset, record contract, parser and replay tool.
3. ESP8266-generated test records over a supported connection, once its variant and accessories are checked.
4. A packaging or fit prototype using the free printer access where appropriate.
5. An inventory showing what is available, what I can borrow and what is actually missing.

These are planned deliverables. I have not implemented or built them yet.

## My board allocation

I will begin with the **ESP8266 on the bench** and keep the **Jetson on the ground**. This is a project-planning choice: it lets me learn acquisition separately from analysis and reuse the equipment already available. It does not qualify either board for flight. I will measure timing, data integrity, power behavior and packaging constraints before deciding on flight instrumentation.

I do not plan to buy a Raspberry Pi or a newer board for the first phase. If the Jetson needs missing accessories, I can develop the file-based tools on the computer I already use.

I will start from the manufacturer references for [ESP8266 UART support](https://docs.espressif.com/projects/esp-faq/en/latest/software-framework/peripherals/uart.html), [ESP8266 I2C support](https://docs.espressif.com/projects/esp-faq/en/latest/software-framework/peripherals/i2c.html), and [Jetson Nano setup](https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit). I will match documentation to my exact board before using it.

## Before I spend anything

I will record the missing function, why borrowing or an existing part is insufficient, the compatible part, a current Canadian-dollar quote, shipping/tax and the milestone it unlocks. I will then set a spending ceiling. Until that comparison exists, an item is a candidate, not a purchase decision.
