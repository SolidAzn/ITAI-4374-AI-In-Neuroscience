# L04 — Simulating Spiking Neurons

**Module 04 · Feb 20, 2026**

## Overview
LIF neuron built from scratch in Python using discrete-time Euler integration. Covers the full pipeline from single-neuron dynamics to small spiking networks.

## Parts Completed

### Part A — Single LIF Neuron
- Implemented membrane potential update equation
- Threshold detection, spike reset, refractory period
- Visualized membrane potential trace over time

### Part B — Spike Encoding
- Encoded input signals as spike trains
- Explored rate coding: firing frequency as a function of input strength

### Part C — f–I Curve
- Swept input current from 0 to max
- Plotted firing rate vs. input current
- Identified rheobase (minimum current to elicit spiking)

### Part D — Small Spiking Network
- Connected multiple LIF neurons
- Observed how spike counts propagate through layers

## Key Concepts Demonstrated
- All-or-none spiking
- Refractory period limiting maximum firing rate
- Rate coding as a neural information channel

## Stack
Python · NumPy · Matplotlib · Google Colab

## Files
- `L04_Duc_Nguyen_ITAI4374.ipynb`
