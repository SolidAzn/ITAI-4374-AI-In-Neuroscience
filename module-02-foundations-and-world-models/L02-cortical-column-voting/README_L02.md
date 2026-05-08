# L02 — Cortical Column Voting Simulation

**Module 02 · Jan 28, 2026**

## Overview
Python simulation of Jeff Hawkins' Thousand Brains Theory. Multiple cortical columns each receive partial, noisy sensory input about an object and vote to reach consensus — mirroring how the neocortex builds distributed, redundant object representations.

## What Was Built
- `create_sensory_input()` — generates noisy evidence matrices per column
- Voting mechanism that aggregates column beliefs across iterations
- Convergence visualization showing consensus emerging over time
- Experiments varying noise level and number of columns

## Objects Recognized
`cup · ball · book · phone · apple`

## Key Finding
Distributed voting is robust to noise in ways that winner-take-all classification is not — individual columns can be wrong, but the ensemble converges to the correct answer.

## Stack
Python · NumPy · Matplotlib · Google Colab

## Files
- `L02_Duc_Nguyen_ITAI4374.ipynb`
