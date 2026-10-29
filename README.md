# Sequence of Operation: Heating and Hot Water Plant (As-Is and To-Be)

**A formal, written sequence of operation for the house's heating and DHW plant, in the structured style used for commercial BMS specifications: system description, operating modes, setpoints, control logic, interlocks, alarms and fail-safes, for both the current (Evohome on/off) system and the target (supervisory optimum start/stop + OpenTherm) system. It's the document a controls engineer programmes from and a commissioning engineer tests against.**

[![YouTube](https://img.shields.io/badge/YouTube-The%20Control%20Cabinet-red?logo=youtube)](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)
[![Portfolio](https://img.shields.io/badge/Portfolio-the--control--cabinet-24292f?logo=github)](https://github.com/the-control-cabinet/the-control-cabinet)
![Domain](https://img.shields.io/badge/BMS-sequence%20of%20operation-blue)
![Status](https://img.shields.io/badge/Status-Design%20stage-yellow)

> **The short version:**
> - **As-is:** two Evohome controllers, four BDR91s switching the boiler's switched live, zone valves, two cylinders, UFH mixing.
> - **To-be:** supervisory optimum start/stop over RAMSES-II + an OpenTherm master with weather compensation, PID trim, DHW priority, anti-cycling and an interlocked changeover.
> - **Format:** numbered clauses per mode (occupied, unoccupied, preheat, DHW priority, frost, fault, manual override) with setpoint tables and a points-list reference.
> - **Traceability:** every clause maps to a test in the commissioning plans.

**Portfolio position:** Management level · specification. Specifies: [optimum start/stop](https://github.com/the-control-cabinet/optimum-start-stop-supervisory) · [OpenTherm control](https://github.com/the-control-cabinet/opentherm-boiler-control-esphome). Tested by: their commissioning plans

---

## Documents

| Doc | Contents |
|---|---|
| [01 System description](docs/01-system-description.md) | Plant, controls and points reference |
| [02 As-is sequence (Evohome on/off)](docs/02-as-is-sequence.md) | Current operation, clause by clause |
| [03 To-be sequence (supervisory + OpenTherm)](docs/03-to-be-sequence.md) | Target operation by mode |
| [04 Setpoints and alarms](docs/04-setpoints-and-alarms.md) | Tables referenced by the clauses |

## Roadmap
- [ ] Review the as-is clauses against the real system
- [ ] Finalise the to-be values after tuning
- [ ] Cross-reference every clause to a commissioning test

## Skills demonstrated (as built)
| Skill | Evidence |
|---|---|
| Specification writing | Structured sequence of operation by mode |
| Control philosophy | Modes, interlocks, fail-safes |
| Traceability | Clauses mapped to commissioning tests |

📺 [The Control Cabinet on YouTube](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)

*Built and documented by James · part of [The Control Cabinet BMS portfolio](https://github.com/the-control-cabinet/the-control-cabinet). MIT Licence.*
