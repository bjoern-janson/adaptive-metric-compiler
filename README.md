# Adaptive Metric Compiler

> A theoretical framework for recursive metric discovery and intelligence as adaptive metric compilation.

---

## Overview

Adaptive Metric Compiler (AMP) is a theoretical framework that models intelligence as the recursive discovery, evaluation, and compilation of increasingly effective internal metrics.

Most optimization frameworks assume that an objective function, representation, or metric already exists. AMP instead focuses on the process by which better metrics are discovered.

The central hypothesis is that intelligence is fundamentally a process of **adaptive metric compilation**:

- detecting meaningful differences,
- allocating computational resources,
- constructing internal mappings,
- evaluating mapping quality,
- discovering improved mappings,
- recursively repeating the process.

Rather than viewing intelligence as optimization alone, AMP distinguishes **optimization within an existing metric** from **discovery of entirely new metrics**.

---

## Central Hypothesis

A bounded agent continuously transforms environmental differences into increasingly informative internal metrics.

As mapping quality improves, the space of computationally viable solutions expands, enabling further metric discovery in a recursive process.

---

## Kernel

```math
\Delta
\xrightarrow{\chi,\mathcal{B},F}
M_Q
\xrightarrow{Q_M,D_\Omega}
M_Q'
\implies
\lim_{K(M_Q)\rightarrow K(I_{\text{true}})}
\frac{\partial\Omega_{\text{viable}}}
{\partial K(M_Q)}
\rightarrow\infty
```

where

- **Δ** — meaningful environmental differences
- **χ** — salience computation
- **𝓑** — computational gating
- **F** — metric construction
- **M₍Q₎** — current internal metric
- **Q₍M₎** — mapping quality
- **DΩ** — metric discovery operator
- **M′₍Q₎** — compiled successor metric

This pipeline represents the complete computational cycle proposed by AMP, from perception to recursive representational improvement.

---

## Core Components

### 1. Causal Mass

AMP begins by identifying differences that possess genuine causal significance.

Rather than measuring information solely by probability, the framework weights differences according to both informational rarity and their influence on future action.

---

### 2. Salience

Not every detectable difference deserves computation.

Salience converts causal significance into computational priority, determining which information proceeds through the compilation pipeline.

---

### 3. Metric Construction

Selected information is transformed into an internal computational metric.

Instead of assuming a fixed representation, AMP treats representations as adaptive structures that determine which distinctions become computationally accessible.

---

### 4. Mapping Quality

Metrics are evaluated according to multiple structural criteria, including:

- information compression
- search efficiency
- invariant preservation
- predictive improvement
- scalability
- representational alignment
- computational complexity

Mapping quality therefore measures how effectively a metric supports future computation.

---

### 5. Metric Discovery

Optimization improves solutions inside an existing metric.

Discovery constructs entirely new metrics.

AMP formalizes this distinction through a discovery operator that searches over the space of possible mappings rather than merely optimizing within one.

---

### 6. Recursive Intelligence

Each newly discovered metric expands the viable computational space available to the agent.

This expanded space enables additional discoveries, producing an open-ended process of recursive metric compilation.

Within AMP,

> **Intelligence is the recursive execution of metric discovery.**

---

## Optimization vs Discovery

AMP distinguishes two fundamentally different computational processes.

Optimization searches within an existing metric.

```text
M_Q
   │
 optimize
   ▼
better solution
```

Discovery changes the metric itself.

```text
M_Q
   │
 DΩ
   ▼
M_Q'
```

This distinction allows the framework to model conceptual change, representation learning, and scientific discovery within a single formal system.

---

## Repository Structure

```text
adaptive-metric-compiler/

├── README.md
├── formalism.md
├── causal-mass.md
├── salience.md
├── mapping-quality.md
├── discovery-operator.md
├── phase-transitions.md
├── examples/
└── simulations/
```

---

## Status

Adaptive Metric Compiler is an early-stage theoretical framework.

The formal definitions presented here represent a foundation for future mathematical development, empirical validation, computational experiments, and comparisons with existing theories of intelligence, representation learning, optimization, and information processing.

The framework is intended as a research program rather than a completed theory.
