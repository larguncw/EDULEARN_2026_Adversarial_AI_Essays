# EDULEARN 2026 — Adversarial AI Essays

A public dataset of adversarially generated AI essays produced as part of our EDULEARN 2026 paper:

**"Evading AI Essay Detection Through Iterative Adversarial Refinement: A Study on TOEFL Writing and an Open Dataset"**

M. Scavone, K. Forynna, Y. Kong, Y. Song
UNC Wilmington & Georgia Institute of Technology

## Overview

This repository contains AI-generated essays that were produced using an iterative adversarial framework designed to evade commercial AI detection tools. Unlike prior work that generates AI essays in a single pass with fixed prompts, our approach uses a feedback-driven loop where an LLM progressively refines its writing style based on:

- Human-written essays from the TOEFL 11 corpus
- Detection reports returned by commercial AI detectors

Using this method, we reduced the detection success rate of commercial tools (GPTZero and Pangram) to near 0% within a small number of iterations.

## Repository Structure

```
├── Experiment 1 - Messy Data/
│   ├── 200 Pass Samples/            # 200 successful adversarial essays (mixed L1 backgrounds)
│   ├── Round 1/
│   ├── Round 2/
│   ├── Round 3/
│   └── Round 4/
│
├── Experiment 2 - Select Data/      # Experiment 2 essays (dedicated L1 backgrounds)
│   ├── Round 1/
│   ├── Round 2/
│   ├── ...
│   └── Round 11/
```

**Experiment 1** used mixed L1 backgrounds and proficiency levels from the TOEFL 11 corpus. Essays were generated across multiple rounds with human-written detection reports fed back into the model.

**Experiment 2** refined this approach by selecting human-written essays from a single L1 background at high proficiency, then building a dedicated writing profile for each language. This produced significantly better results across Arabic, German, Hindi, Italian, Japanese, Korean, Spanish, Telugu, Turkish, and Chinese L1 backgrounds.

## Key Findings

- Commercial AI detectors (GPTZero, Pangram) were reduced to near 0% detection through iterative adversarial generation
- LLMs perform better at human mimicry when given focused, single-L1 input rather than mixed backgrounds
- Experienced writing instructors (9–12 years experience, high AI literacy) achieved only 50–70% accuracy when evaluating the adversarial essays
- Educators identified four key diagnostic features: lexical inconsistency, structural incoherence, overrepresentation of LLM-preferred vocabulary, and systematic error patterns

## Usage

This dataset is intended for researchers working on AI-generated text detection. We welcome its use for training or evaluating detection models, provided appropriate citation is given.

## Citation

If you use this dataset, please cite our EDULEARN 2026 paper:

```
M. Scavone, K. Forynna, Y. Kong, and Y. Song, "Evading AI Essay Detection Through
Iterative Adversarial Refinement: A Study on TOEFL Writing and an Open Dataset,"
in Proc. EDULEARN26, 2026.
```

## Note on the TOEFL 11 Dataset

The human-written essays used in our experiments come from the TOEFL 11 corpus (Blanchard et al., 2014), which is available for research use through the [LDC Catalog](https://catalog.ldc.upenn.edu/). The authors of this paper cannot provide access to the TOEFL 11 dataset.
