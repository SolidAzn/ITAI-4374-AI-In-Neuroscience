# L05 — Bio-Inspired Perception Pipeline

**Module 05 · Feb 27, 2026**

## Overview
Three-part lab applying the brain's sensory processing hierarchy to real image and audio data. Each part pairs a biological mechanism with its computational analog.

## Parts Completed

### Part A — "Be the Retina" (All Students)
Implemented biological image filters from scratch:
- **Center-surround receptive fields** — on-center/off-surround mimicking retinal ganglion cells
- **Gabor filters** — oriented edge detectors modeling V1 simple cells
- **Contrast normalization** — divisive normalization as in visual cortex

### Part B — "Inside a CNN" (All Students + GPU Track)
Compared hand-crafted bio-inspired filters to learned CNN feature maps:
- Early CNN layers learn Gabor-like edge detectors spontaneously
- Deeper layers capture textures and object parts — mirroring V2→V4→IT hierarchy
- Visualized feature maps to see what each layer responds to

### Part C — "Hearing in Pictures" (All Students + GPU Track)
Auditory processing pipeline:
- Cochlear frequency decomposition modeled as a filterbank
- Spectrogram generation — frequency over time
- Pattern detection in the time-frequency domain

### Part D — Experiments
Varied filter parameters to observe effects on feature selectivity and noise robustness.

## Key Insight
The brain's perceptual hierarchy is not accidental — CNNs that learn from data independently converge on similar representations, suggesting these features are optimal for natural image statistics.

## Stack
Python · NumPy · Matplotlib · SciPy · Google Colab

## Files
- `L05_DucNguyen_ITAI4374.ipynb`
