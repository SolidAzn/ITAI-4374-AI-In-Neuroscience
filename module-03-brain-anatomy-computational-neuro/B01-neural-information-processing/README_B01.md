# B01 — Neural Information Processing (Bonus)

**Module 03 · Apr 10, 2026**

## Overview
Side-by-side Python implementation and comparison of a biological LIF neuron and an artificial neuron, culminating in a written analysis of what each reveals about the other.

## What Was Built

### BiologicalNeuron class
- Leaky integrate-and-fire with refractory period and hyperpolarization
- All-or-none spikes at threshold
- Tested at input currents [0.5, 1.5, 3.0, 5.0]
- Result: subthreshold silence → firing onset → increasing rate

### ArtificialNeuron class
- Weighted sum + configurable activation (sigmoid, ReLU, tanh)
- Compared sigmoid, ReLU, and tanh input-output curves
- Key insight: biological f–I curve resembles ReLU (hard threshold → linear rise) — one reason ReLU displaced sigmoid in modern deep learning

### 3-neuron biological chain
- Spike counts propagate: A (input) → B (hidden) → C (output)
- Demonstrates continuous vs. discrete, stateless vs. refractory differences

## Key Takeaway
The artificial neuron is an abstraction chosen for mathematical convenience, not biological fidelity — and the gap between them is a map of where AI might still borrow from neuroscience.

## Stack
Python · NumPy · Matplotlib · Google Colab

## Files
- `B01_Implementation_Duc_Nguyen_ITAI4374_ipynb_-_Colab.pdf`
