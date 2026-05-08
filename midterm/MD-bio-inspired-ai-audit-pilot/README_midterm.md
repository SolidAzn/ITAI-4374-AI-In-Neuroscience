# Midterm — Bio-Inspired AI Audit: Pilot

**ITAI 4374 · Spring 2026 · Duc Nguyen**

A structured pilot audit of Claude Sonnet (claude.ai) evaluated through three neuroscience lenses: brain architecture, perception, and memory. This pilot established the audit methodology later expanded in the final project.

## System Profiled
- **Model:** Claude Sonnet 4.6
- **Access:** claude.ai free tier, Microsoft Edge, Windows
- **Method:** Fresh sessions for each experiment, no API modifications

## Experiments

### Experiment 1 — Parallel vs. Sequential Processing (Module 02)
Four simultaneous tasks (haiku, compound interest, syllogism, translation) delivered in one prompt. Claude answered all four in a single pass — but this apparent parallelism is high-speed sequential token generation, not anatomical specialization like the brain's parallel cortical streams.

### Experiment 2 — Perceptual Ambiguity (Module 03)
Uploaded the duck-rabbit ambiguous figure. Claude identified both interpretations without prompting and self-reported perceiving the duck "first" — but acknowledged it processes the image all at once, with no true perceptual rivalry like the brain experiences.

### Experiment 3 — Memory Across Sessions (Module 04)
Shared a richly contextual story (Iceland trip, dog named Pixel, coding in Rust) with the memory feature enabled. Tested recall across three levels: direct facts (strong), associative binding (degraded), emotional/episodic context (lost). Claude's memory feature stores isolated semantic facts — not episodic memories.

## Key Finding
Claude's memory feature functions as a flat fact-extraction system, not hippocampal consolidation. It captures *that* something happened, not *how it felt* or *what surrounded it*.

## Files
- `MD_Duc_Nguyen_ITAI4374.docx` — full written report
