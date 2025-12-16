# llm-nonlinear-dynamics
# Exploring Machine Learning and Nonlinear Dynamics in Large Language Models

This repository presents a research project examining large language model (LLM)
outputs through the combined frameworks of machine learning and nonlinear
dynamical systems. Generated text sequences are modeled as symbolic trajectories
evolving through a state space, enabling the study of stability, transitions, and
attractor-like behavior in language generation.

By integrating natural language processing, supervised learning, and
dynamics-based analysis, this work characterizes structured and emergent patterns
in LLM outputs that are not captured by conventional static evaluation metrics.

---

## Research Motivation

Large language models exhibit complex, nonlinear behavior arising from their
high-dimensional representations and probabilistic decoding mechanisms. Recent
work suggests that LLMs can display structured dynamical phenomena such as fixed
points, oscillations, multistability, and regime switching under controlled
generation conditions.

This project adopts a dynamical systems perspective by treating sequences of
generated text as evolving trajectories. Machine learning and natural language
processing are used to convert raw text into structured representations that
enable quantitative analysis. In particular, supervised learning provides a
principled way to relate observable text features to qualitative properties such
as desirability and stability within a dynamical systems framework. This use of
machine learning is impactful in that it enables qualitative dynamical
concepts—such as stability, regimes, and attractors—to be inferred directly from
high-dimensional language data, which is otherwise difficult using traditional
analytical methods alone.

---

## Research Questions

This project is guided by the following research questions:

- How does sampling temperature reshape the attractor landscape of GPT-2 outputs?
- How do random seeds behave as initial conditions in LLM generation?
- How does output desirability relate to attractor stability and mixing behavior?
- Do observed generation patterns align with predictions from nonlinear dynamical
  systems theory?

---

## Project Objectives

The objectives of this work are to:

- Represent LLM-generated text as time-ordered sequences in an embedded feature space
- Apply supervised machine learning to classify generated outputs
- Discretize classified outputs into symbolic states
- Construct state-transition representations of language generation dynamics
- Identify attractor-like structures and regime-dependent behavior across conditions

---

## Methodological Overview

The analysis pipeline follows a modular and sequential structure:

**Mini-Lab Code → NLP Processing → Machine Learning Classification → Symbolic Dynamics Analysis → Result Aggregation**

The pipeline begins with instructional mini-lab code used to generate LLM outputs
under varying prompts, temperatures, and random seeds. These outputs are then
processed using natural language processing techniques, classified via supervised
machine learning, mapped into symbolic state representations, and analyzed using
tools from nonlinear dynamical systems. Results are aggregated to enable
comparative analysis across experimental conditions.

Logistic regression was selected to provide a simple, interpretable baseline that
captures linear relationships between quantitative text features and output
desirability while avoiding overfitting on a limited dataset.

---

## Experimental Setup

LLM outputs were generated using GPT-2 via instructional mini-lab code under
controlled sampling conditions. The purpose of this setup was to create a
systematic dataset suitable for dynamical analysis.

**Generation parameters included:**
- **Prompts:** Jesus; Moon Landing (real, fake, and real-or-fake variants)
- **Temperatures:** 0.001, 0.300, 0.500, 0.700
- **Random seeds:** 1, 2, 3

This resulted in a total of 15 generated text files, which served as input to the
NLP, machine learning, and symbolic dynamics pipeline.

---


---

## Summary of Findings

Analysis of GPT-2 outputs revealed structured dynamical behavior across prompts,
temperatures, and random seeds.

Key observations include:
- Sampling temperature acts as a control parameter, reshaping attractor structure
  in a non-monotonic manner.
- Random seeds function as initial conditions, influencing convergence behavior
  and regime selection.
- The majority of runs converge to fixed-point attractors, with additional
  oscillatory and mixed regimes observed.
- Desirable outputs tend to reside in stable attractor regions characterized by
  slower mixing dynamics and smaller spectral gaps.
- Observed behaviors are consistent with established results in nonlinear
  dynamical systems literature.

Each primary analysis plot directly corresponds to one of the stated research
questions, linking temperature, seed sensitivity, attractor stability, and
theoretical predictions from nonlinear dynamical systems.

---

## Dynamical Interpretation

From a dynamical systems perspective, GPT-2 generation exhibits features
characteristic of nonlinear systems, including fixed points, oscillations,
multistability, and regime switching. Sampling temperature and random seed jointly
determine which attractor basin is entered, while output desirability correlates
with attractor stability.

These results support the use of symbolic dynamics and transition-based analysis
as effective tools for studying the behavior of large language models.

---

## Acknowledgments

Portions of the initial GPT-2 mini lab code used in this project were provided by
Prof. Neil Johnson as part of the course *Biophysics: Macroscopic Physics in the
Life Sciences (PHYS 3127)* at The George Washington University. The mini-lab code
was used to generate LLM outputs under varying prompts, temperatures, and random
seeds.

Prompt selection and sampling parameters were determined by other contributors
during the initial study design phase, after which all implementation, machine
learning analysis, and dynamical modeling were carried out independently.

---

## References

[1] S. Roy and D. Rana, “Machine learning in nonlinear dynamical systems,” *Resonance*,
vol. 26, pp. 707–726, 2021, doi: 10.1007/s12045-021-1194-0.

[2] A. Haluszczynski and C. Räth, “Controlling nonlinear dynamical systems into arbitrary
states using machine learning,” *Scientific Reports*, vol. 11, no. 12825, 2021,
doi: 10.1038/s41598-021-92244-6.

[3] T. J. B. Liu, N. Boullé, R. Sarfati, and C. J. Earls, “LLMs learn governing principles
of dynamical systems, revealing an in-context neural scaling law,” *arXiv preprint*
arXiv:2402.00795, 2024.

[4] Z. Wang *et al.*, “Unveiling attractor cycles in large language models: A dynamical
systems view of successive paraphrasing,” *arXiv preprint* arXiv:2502.15208, 2025.

[5] G. Haller, S. Jain, and M. Cenedese, “Dynamics-based machine learning for
nonlinearizable phenomena,” *SIAM News*, 2022. [Online]. Available:
https://sinews.siam.org

[6] X. Luo *et al.*, “How do large language models perform in dynamical systems?,” in
*Findings of the Association for Computational Linguistics: NAACL 2025*, 2025.
[Online]. Available: https://aclanthology.org/2025.findings-naacl.50

[7] M. Aminian, “Theory guides the frontiers of large generative models,” *SIAM News*,
vol. 58, no. 08, Oct. 2025. [Online]. Available:
https://www.siam.org/publications/siam-news/articles/theory-guides-the-frontiers-of-large-generative-models

[8] N. Johnson, “GPT-2 Mini Lab Code,” unpublished instructional material,
*Biophysics: Macroscopic Physics in the Life Sciences (PHYS 3127)*,
George Washington University, 2025.
