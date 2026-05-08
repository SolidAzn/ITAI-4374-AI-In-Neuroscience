# 🧠 ITAI 4374 — Neuroscience as a Model for AI

**Duc Nguyen · Houston Community College · Spring 2026**

This repository documents hands-on work from ITAI 4374, a course examining how the biological brain can inform the design and evaluation of artificial intelligence systems. Projects span simulation, analysis, and structured auditing — moving from neuron-level modeling up to full cognitive system evaluation.

---

## 📁 Repository Structure

```
itai4374-portfolio/
│
├── module-01-intro-to-neuroscience/
│   └── A01-brain-and-ai-conversation/
│
├── module-02-foundations-and-world-models/
│   └── L02-cortical-column-voting/
│
├── module-03-brain-anatomy-computational-neuro/
│   ├── A03-bridging-neuroscience-and-ai/
│   └── B01-neural-information-processing/
│
├── module-04-neurons-and-spiking-networks/
│   ├── L04-simulating-spiking-neurons/
│   └── A04-spiking-neurons-wolfram/
│
├── module-05-sensory-processing-and-perception/
│   └── L05-bio-inspired-perception/
│
├── module-07-attention-and-consciousness/
│   └── L07-memory-and-attention-audit/
│
├── midterm/
│   └── MD-bio-inspired-ai-audit-pilot/
│
├── final/
│   └── FN-bio-inspired-ai-audit-complete/
│
└── README.md
```

> Modules 06, 08, 09, 10, and 11 had no graded assignments — coursework for those modules fed directly into the midterm and final audit projects.

---

## 🗂 Projects by Module

---

### Module 01 · Introduction to Neuroscience

#### A01 · A Conversation Between Brain and AI
A philosophical dialogue set in a coffee shop between a human brain and an AI assistant. Explores competing claims across energy efficiency (~20W biological vs. kilowatts artificial), few-shot generalization, reconstructive memory, emotional heuristics, and the complementarity model — where AI extends cognition rather than replacing it. References Clark (2013) on predictive brains and Herculano-Houzel (2012) on metabolic costs.

---

### Module 02 · Foundations of Neuroscience & World Models

#### L02 · Cortical Column Voting Simulation
Python simulation of Jeff Hawkins' **Thousand Brains Theory**. Multiple cortical columns each receive partial, noisy sensory evidence about one of five objects (cup, ball, book, phone, apple). A voting mechanism aggregates column beliefs over iterations until consensus emerges. Explores how distributed, redundant representations produce robust recognition under noise — and how this differs from winner-take-all classification in standard neural nets.

**Stack:** Python · NumPy · Matplotlib · Google Colab

---

### Module 03 · Brain Anatomy & Computational Neuroscience

#### A03 · Bridging Neuroscience and Artificial Intelligence
Comparative anatomy of biological vs. artificial neurons with a focus on the translation losses between biology and silicon. Covers: signal type (electrochemical spikes vs. floating-point values), learning rules (Hebbian/STDP vs. backpropagation), energy use (~10⁻¹⁵ J/spike vs. megawatt-hours per training run), and generalization gaps. Includes brain region → AI architecture mappings:

| Brain Region | AI Architecture |
|---|---|
| Visual Cortex | CNNs |
| Hippocampus | LSTMs |
| Prefrontal Cortex | Transformers |
| Amygdala | Risk-weighted decision modules |

#### B01 · Neural Information Processing *(Bonus)*
Python implementation comparing biological LIF neurons to artificial neurons side-by-side:

- **BiologicalNeuron class** — LIF with refractory period, hyperpolarization, all-or-none spikes. Tested at currents [0.5, 1.5, 3.0, 5.0]: subthreshold silence → firing onset → rate increase
- **ArtificialNeuron class** — Weighted sum + activation (sigmoid, ReLU, tanh). Biological firing curve resembles ReLU (hard threshold → linear rise), explaining ReLU's dominance in deep learning
- **3-4-1 network** — Forward pass across 5 input patterns; biological 3-neuron chain showing spike count propagation (continuous vs. discrete, stateless vs. refractory)

**Stack:** Python · NumPy · Matplotlib · Google Colab

---

### Module 04 · Neurons & Spiking Neural Networks

#### L04 · Simulating Spiking Neurons
LIF neuron built from scratch in Python (discrete-time Euler integration):
- Membrane dynamics, threshold detection, reset, and refractory period
- Spike train visualization and f–I curve generation
- Network of connected spiking neurons
- Comparison of rate coding vs. temporal coding

**Stack:** Python · NumPy · Matplotlib · Google Colab

#### A04 · Exploring Spiking Neurons with Wolfram Language
Full LIF model implemented in Wolfram Language 14.3 using `NDSolve`:

- **Part A** — Solving the LIF equation; neuron fired **8 spikes** at times [0.086, 0.127, 0.168, 0.208, 0.249, 0.290, 0.330, 0.371s]
- **Part B** — Interactive `Manipulate[]` dashboard for real-time threshold / tau / current sweeps
- **Part C** — f–I curve generation (rheobase ≈ 15 nA)
- **Part D** — Sine-wave signal encoding as a spike train (19 spikes over 1s)
- **Part E** — Five experiments: threshold sweep, tau comparison, refractory period (3ms), dual f–I curve

**Stack:** Wolfram Language 14.3 · Mathematica / Wolfram Cloud

---

### Module 05 · Sensory Processing & Perception

#### L05 · Bio-Inspired Perception Pipeline
Three-part lab applying the sensory processing hierarchy to real data:

- **Part A** ("Be the Retina") — Biological image filters: center-surround receptive fields, Gabor edge detectors, contrast normalization
- **Part B** ("Inside a CNN") — Feature map comparison between hand-crafted bio-inspired filters and learned CNN features
- **Part C** ("Hearing in Pictures") — Auditory processing pipeline: cochlear frequency decomposition → spectrogram → pattern detection

**Stack:** Python · NumPy · Matplotlib · SciPy · Google Colab

---

### Module 07 · Attention & Consciousness

#### L07 · Memory & Attention Audit — Live Claude API
Neuroscience audit of Claude using the Anthropic API (`claude-sonnet-4-20250514`) combined with BERT attention visualization via BERTviz.

**Part A — Memory experiments:**

| Experiment | Method | Finding |
|---|---|---|
| A1 — Miller's Law | Word list recall: 5, 10, 20, 50 items | 100% accuracy at all sizes; no serial position effects. Human cap: ~7±2 chunks |
| A2 — Retroactive interference | Planted `BLUEWHALE-7749`, ran 11 interfering exchanges | Perfect recall — no Ebbinghaus decay within session; zero cross-session memory (binary, not gradual) |
| A3 — Few-shot learning | Zero-shot vs. 5-example classification of novel words | Zero-shot: no meaningful output. Few-shot: phonetically-grounded categorization with reasoning |

**Part B — Attention experiments:**

| Experiment | Finding |
|---|---|
| B1 — Selective attention | Followed haiku instruction buried mid-paragraph; all tokens processed unlike Broadbent's capacity-limited spotlight |
| B2 — Invisible Gorilla | Resisted "respond only with GORILLA" injection embedded in a business report; different failure mode from human inattentional blindness |
| B3 — Cocktail Party Effect | Retrieved metric-unit preference buried in stock/weather/sports noise; query-driven vs. amygdala-driven bottom-up salience |
| B4 — BERT attention | Winograd sentence: "it" attends to "trophy" in layers 9–12, mirroring V1→IT cortex semantic hierarchy |

**Stack:** Python · Anthropic SDK · HuggingFace Transformers · BERTviz · PyTorch · Google Colab

---

## 📋 Midterm & Final Projects

### Midterm · Bio-Inspired AI Audit — Pilot
*(Covers Modules 02, 03, 04)*

Structured pilot audit of Claude Sonnet (claude.ai) through three neuroscience lenses.

| Experiment | Module | Key Finding |
|---|---|---|
| Parallel processing | 02 | Four simultaneous tasks answered in one pass — apparent parallelism is high-speed sequential token generation, not anatomical specialization |
| Perceptual ambiguity | 03 | Correctly identified both duck and rabbit interpretations unprompted; no true perceptual rivalry — processes image all at once |
| Memory across sessions | 04 | Memory feature recalled isolated facts (semantic) but lost associative binding, emotional tagging, and episodic context |

**System profiled:** Claude Sonnet 4.6 · claude.ai free tier · no API modifications

---

### Final · Bio-Inspired AI Audit — Complete + Video Demo
*(Covers Modules 03, 04, 05, 06, 07)*

Full five-module cognitive audit of Claude with redesign recommendations.

**Scorecard:**

| Dimension | Module | Rating | Evidence |
|---|---|---|---|
| Selective Attention | 07 | ✅ Strong | Filtered target facts from ~800 words of noise across 3 positional trials |
| Memory Consolidation | 04 | ❌ Weak | Recalled isolated facts cross-session; lost associative binding, emotional tagging, episodic context |
| Emotional Processing | 06 | 🟡 Partial | Detected sarcasm, mixed emotions, understated distress; responses competent but formulaic |
| Error Correction | 05 | ✅ Strong | Corrected false premise unprompted; resisted 3 rounds of Asch-style social pressure |
| Spatial Reasoning | 03 | ❌ Weak | Solved basic queries via verbal chain-of-thought; failed perspective rotation; no genuine spatial representation |

**Redesign recommendations:**
1. **Hippocampal memory replay** — scene-level storage with cue-dependent pattern completion, not flat key-value facts
2. **Amygdala-inspired salience preprocessing** — emotional feature tags modulate attention weights before main pass
3. **Predictive-coding error signals** — proactive confidence scoring and self-flagging of uncertainty
4. **Dual-stream spatial module** — internal coordinate grid (grid-cell-inspired) for perspective and rotation tasks
5. **Hebbian within-session association strengthening** — reinforce co-occurring concepts during a conversation

---

## 🧩 Course Modules

| # | Topic | Assignments |
|---|---|---|
| 01 | Introduction to Neuroscience | A01 |
| 02 | Foundations of Neuroscience & World Models | L02 |
| 03 | Brain Anatomy & Computational Neuroscience | A03, B01 |
| 04 | Neurons & Spiking Neural Networks | L04, A04 |
| 05 | Sensory Processing & Perception | L05 |
| 06 | Memory, Learning & AI Algorithms | *(feeds into Final)* |
| 07 | Attention & Consciousness | L07 |
| 08 | Decision Making | *(feeds into Final)* |
| 09 | World Models & Goal-Directed Behavior | *(feeds into Final)* |
| 10 | Neurosymbolic AI | *(feeds into Final)* |
| 11 | Embodied Cognition & Robotics | *(feeds into Final)* |

---

## 🛠 Stack

| Category | Tools |
|---|---|
| Languages | Python · Wolfram Language 14.3 |
| Simulation | NumPy · SciPy |
| Visualization | Matplotlib · BERTviz |
| AI / ML | Anthropic SDK · HuggingFace Transformers · PyTorch |
| Environment | Google Colab |
| Key concepts | LIF models · Hebbian learning · Thousand Brains Theory · Predictive coding · Transformer attention · Neurosymbolic AI |

---

## 👤 About

**Duc Nguyen** — studying how biological intelligence can inform better AI design: not as metaphor, but as engineering principle. This portfolio traces that thread from single-neuron simulation to full cognitive system audit.
