# 03 To-be sequence (supervisory + OpenTherm)

[← Back to README](../README.md)

| Mode | Clause |
|---|---|
| **3.1 Unoccupied** | Zones at the setback baseline (Evohome schedule). |
| **3.2 Preheat (optimum start)** | Supervisor raises each zone to comfort at its calculated start time; the OpenTherm node applies a preheat boost. |
| **3.3 Occupied** | Zones at comfort; the boiler flow setpoint = weather compensation + PID trim, clamped 30-70 °C. |
| **3.4 Optimum stop** | Supervisor sets each zone back at its calculated stop time. |
| **3.5 DHW priority** | Any cylinder call: flow setpoint to the DHW value until satisfied. |
| **3.6 Anti-cycling** | Minimum burn 10 min, minimum off 5 min (except DHW). |
| **3.7 Frost** | ⟨decide: boiler/Evohome frost features or a node rule⟩ |
| **3.8 Fault / fall-back** | Node or supervisor failure: interlocked changeover to Mode A (Evohome on/off); alarms raised. |
| **3.10 Heating/cooling interlock** | A room may heat **or** cool, never both: cooling is inhibited while that zone has heat demand, and heating is inhibited while cooling is active, with a dead band of at least 2 °C between the heating and cooling setpoints. Shading assists first ([lighting and shading](https://github.com/the-control-cabinet/lighting-and-shading-control)). |
| **3.11 Outdoor temperature source** | Weather compensation uses a validated outdoor temperature (local station cross-checked against online sources; fall back to the online value if they disagree). |
| **3.9 Manual override** | The changeover switch selects Mode A; the supervisor kill switch disables plant writes. |
