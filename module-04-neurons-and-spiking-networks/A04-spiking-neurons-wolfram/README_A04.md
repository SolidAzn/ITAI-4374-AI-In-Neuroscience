# A04 — Exploring Spiking Neurons with Wolfram Language

**Module 04 · Mar 6, 2026**

## Overview
Full LIF neuron model implemented in Wolfram Language 14.3 using `NDSolve` for differential equation solving. Five parts covering analytical solution, interactive dashboard, f–I curve, signal encoding, and experiments.

## Results by Part

### Part A — NDSolve LIF Model
- Parameters: τ=20ms, V_rest=−70mV, V_thresh=−55mV, V_reset=−75mV, I=18nA
- **Neuron fired 8 spikes** at times: [0.086, 0.127, 0.167, 0.208, 0.249, 0.290, 0.330, 0.371s]

### Part B — Interactive Manipulate[] Dashboard
- Real-time sliders for threshold (−65 to −45mV), time constant (5–100ms), input current (0–40nA)
- **Rheobase ≈ 15 nA** — minimum current to elicit firing

### Part C — f–I Curve
- Swept I from 0 to 35 nA in steps of 1
- Non-linear rise: silence below rheobase, roughly linear above
- Real neurons show stronger saturation due to adaptation — not fully captured by LIF

### Part D — Sine-Wave Signal Encoding
- Input: 15 + 12·sin(2π·5·t) nA
- **19 spikes over 1 second** — spike density tracked sine wave peaks
- Information about amplitude preserved in firing rate; smooth shape lost in discretization

### Part E — Experiments
1. **Threshold sweep** (−65 to −45mV): spike count 31 → 0
2. **Tau comparison** (0.010, 0.020, 0.050s): smaller tau = faster, more spikes
3. **Refractory period** (3ms added): max firing rate decreased as expected
4. **Dual f–I curves** (tau=0.010 vs 0.040): faster tau rises earlier and more steeply

## Stack
Wolfram Language 14.3 · Mathematica / Wolfram Cloud

## Files
- `A04_Duc_Nguyen_ITAI4374.pdf`
