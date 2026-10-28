# Electronics II — Amplifier Design and Simulation

**Sanaz Mazrae**  
Sharif University of Technology · Department of Electrical Engineering

Two transistor-level amplifier design projects developed and analyzed using LTspice. The work covers BJT biasing, differential amplification, active loads, frequency response, negative feedback, and large-signal performance. Each project includes its circuit schematics and a technical report with design calculations and simulation results.

## Project 1 — LM741-Type Operational Amplifier Input Stage

Design and analysis of a bipolar differential input stage with transistor current mirrors and active loads. The simulations examine DC operating points and small-signal parameters, open-loop frequency response, input/output impedance, the effect of output loading, transient distortion, slew rate, and DC offset adjustment.

**Design specifications:** ±15 V supplies, 50 dB voltage-gain target, maximum quiescent power of 12 mW, and input impedance above 2 MΩ. Frequency-response measurements consider 1 MΩ and 250 kΩ output loads.

**Files:** [Technical report](project-1-opamp-input-stage/Report.pdf) · [Main circuit](project-1-opamp-input-stage/ltspice/baseCircuit.asc) · [Offset-adjustment circuit](project-1-opamp-input-stage/ltspice/offsetImprovingCircuit.asc) · [Slew-rate simulation](project-1-opamp-input-stage/ltspice/slewRateCiruit.asc)

## Project 2 — Low-Distortion Power Amplifier

Design of a transistor-level amplifier for a 100 Ω load. The circuit combines a folded-cascode input stage, transistor-based bias networks, a complementary output stage, and negative feedback. The analysis addresses output-swing limitations, closed-loop gain, quiescent power, and total harmonic distortion (THD).

**Design specifications:** ±10 V supplies, 2 V/V closed-loop gain, output swing above 16.6 Vpp, THD below 0.05% at 16.4 Vpp, approximately 50 mW quiescent power, and fewer than 25 transistors.

The saved final-circuit simulation (`Q5.asc`, 1 kHz input) provides the following results:

| Parameter | Simulated result |
|---|---:|
| Closed-loop gain | ≈ 2.00 V/V |
| Output swing | ≈ 16.79 Vpp |
| Quiescent power | ≈ 46.48 mW |
| Total harmonic distortion | 0.047880% |
| Transistor count | 24 |

The reported THD corresponds to the saved approximately 16.79 Vpp simulation, rather than a separate measurement at exactly 16.4 Vpp.

**Files:** [Technical report](project-2-power-amplifier/Report.pdf) · [Design schematics](project-2-power-amplifier/ltspice/) · [Final circuit](project-2-power-amplifier/ltspice/Q5.asc) · [Fourier analysis log](project-2-power-amplifier/results/Q5.log)

## Simulation

Open the `.asc` files in **LTspice** and run the configured analyses. The PDF reports document the circuit configurations, calculation methods, simulation conditions, and interpretation of the results.
