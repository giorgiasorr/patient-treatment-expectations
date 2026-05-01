# From Synthetic to Real-World Data: Detecting Patient Expectations of Treatment Outcomes

Detecting patient expectations of treatment outcomes in online health discussions using NLP and synthetic data.

---

## Overview

Online health platforms such as Reddit provide a space where patients share experiences, concerns, and expectations about treatments. These expectations—beliefs about what a treatment will or will not do—play an important role in treatment engagement and outcomes, but remain underexplored from an NLP perspective.

This project focuses on modelling and automatically detecting patient expectations of treatment outcomes from text, using a combination of synthetic and real-world data.

---
## Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

---
## Research Focus

The project investigates how synthetic data can be used to model and detect patient expectations in real-world health-related text.

Key directions include:

- Evaluating the **quality and diversity** of LLM-generated synthetic patient posts  
- Analyzing how different **prompting strategies** affect synthetic data generation  
- Assessing how well models trained on synthetic data **generalize to real-world Reddit data**  
- Identifying which types of expectations are **most difficult to detect**

The broader goal is to explore whether synthetic data can serve as a reliable alternative in settings where annotated medical data is scarce due to privacy and ethical constraints.

---

## Task

The task is formulated as a **multi-dimensional classification problem** over expectation statements.

Each expectation is labeled along the following dimensions:

- **Outcome type**: positive / negative / neutral  
- **Certainty**: low / medium / high  
- **Temporal orientation**: prospective / retrospective  
- **Source of belief**: personal / professional / social / media / not specified  

---

## Methodology

### Synthetic Data Generation
- Generate Reddit-style patient posts using a small language model (GPT-Neo 2.7B)
- Apply different prompting strategies:
  - zero-shot
  - few-shot
  - controlled prompting
- Automatically label data based on a structured expectation schema

### Data Analysis
- Evaluate **coverage** of expectation dimensions  
- Assess **linguistic diversity and realism**  
- Perform **human verification** of generated samples  

### Modeling
- Train classifiers on synthetic data:
  - Logistic Regression (TF-IDF baseline)
  - RoBERTa (transformer-based model)

### Evaluation
- Test on manually annotated real-world Reddit posts  
- Measure performance using:
  - Precision, Recall, Macro F1  
- Conduct **error analysis** to identify challenging expectation types  

---

## Data

- **Synthetic dataset**: generated and automatically labeled using LLMs  
- **Real-world dataset**: manually annotated Reddit posts  

> Note: Data may not be publicly released due to platform and privacy constraints.

---

## Project Status

Work in progress. Current focus:

- Finalizing annotation of the real-world Reddit dataset using a structured expectation schema  
- Generating synthetic data using different prompting strategies  

---

## Motivation

This project addresses key challenges in medical NLP:

- Lack of annotated datasets for expectation detection  
- Multidimensional nature of patient expectations  
- Privacy constraints limiting access to clinical data  

By combining structured annotation and synthetic data generation, the project explores a scalable approach to analyzing patient perspectives in online health discourse.

---

## Author

Giorgia Sorrentino  
MSc Computational Linguistics