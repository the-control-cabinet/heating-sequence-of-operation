# 02 As-is sequence (Evohome on/off)

[← Back to README](../README.md)

**2.1 Heating demand.** When any Evohome zone requires heat, its controller closes the associated BDR91; the commoned switched live energises the boiler, which fires to its own dial setpoint.
**2.2 Zone valves.** The two radiator-circuit zone valves have their actuator heads **electrically disconnected and latched in manual override**. In manual override a valve is held partly open, **not necessarily fully open** ⟨verify for this valve model; assess the effect on flow⟩. Room temperature is controlled by the HR92 heads. The UFH circuit is controlled by the HCC80R and its BDR91.
**2.3 DHW.** Each cylinder's BDR91 calls when its CS92 sensor is below setpoint; the cylinder valve opens and the boiler fires.
**2.4 Boiler cycling.** TPI cycling by Evohome (rate per controller settings).
**2.4a Pump overrun and minimum flow.** The boiler has an integral pump with overrun. With HR92s on every radiator and the other zone valves closed, a minimum-flow path at the end of a call depends on an automatic bypass (internal to the boiler, or in the pipework) or an always-open radiator ⟨verify which exists⟩.
**2.5 Safety.** Boiler internal limits; cylinder high-limit thermostats ⟨verify in series with valves⟩; system pressure monitored.
