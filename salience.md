# Salience

Salience is the second stage of the Adaptive Metric Compiler (AMP).

Its purpose is to transform **causal significance into computational priority**.

While Causal Mass estimates the importance of an environmental difference, salience determines whether that difference receives computational resources.

In AMP, attention is not allocated according to information alone, but according to estimated future utility.

---

# Motivation

Every intelligent system operates under finite computational resources.

At any moment, the environment contains vastly more information than can be processed.

Consequently, computation must be selective.

The problem is therefore not:

> "What information exists?"

but:

> "Which information deserves computation?"

Salience provides this selection mechanism.

---

# From Causal Mass to Salience

Let

$$
\mathcal{M}_C
$$

denote the causal mass assigned to an environmental difference.

AMP transforms causal mass into salience using a sigmoid activation:

$$
\chi_{\Delta}
=
\rho
=
\sigma(M_C-\theta)
$$

where:

* (\sigma(\cdot)) is the logistic function,
* (\theta) is a computational threshold,
* (\rho) is the resulting salience score.

The sigmoid produces a continuous estimate between zero and one.

Small causal differences produce weak activation.

Large causal differences rapidly approach maximal salience.

---

# Computational Gating

Salience alone does not allocate computation.

Instead, it drives a computational gate:

$$
B_{\rho}
=
\begin{cases}
1 & \rho \geq \rho_{\mathrm{crit}} \\
0 & \rho < \rho_{\mathrm{crit}}
\end{cases}
$$

where:

* (\rho_{\mathrm{crit}}) is the activation threshold.

If the gate evaluates to:

$$
\mathcal{B}_{\rho}=1
$$

the observation proceeds through the compiler.

Otherwise it is discarded.

---

# Interpretation

The computational gate represents the finite processing capacity of bounded agents.

Only observations whose estimated importance exceeds available resources receive further computation.

This prevents computational effort from being wasted on differences that are unlikely to improve future performance.

---

# Why a Sigmoid?

AMP does not require a sigmoid specifically.

Any monotonic activation function capable of transforming causal significance into computational priority could be substituted.

The logistic function is adopted because it has several useful properties:

* continuous,
* differentiable,
* bounded,
* naturally interpretable as activation probability.

It also allows small differences near the threshold to produce large changes in computational allocation.

---

# Salience as Resource Allocation

Salience should not be interpreted as awareness.

Instead, it represents the allocation of limited computational resources.

The framework therefore treats salience as a computational scheduling mechanism rather than a psychological phenomenon.

In biological systems this allocation may correspond to attention.

In machine learning it may correspond to routing, activation, or selective computation.

In planning systems it may correspond to search prioritization.

---

# Context Dependence

Salience is inherently contextual.

The same observation may possess high salience under one objective and negligible salience under another.

For example:

* a medical image may be highly salient to a radiologist,
* nearly irrelevant to a financial trading system.

AMP therefore models salience as a property of the interaction between:

* the observation,
* the agent,
* the current task,
* the available computational resources.

---

# Relationship to Causal Mass

Causal Mass estimates intrinsic computational importance.

Salience estimates whether that importance justifies computation under current resource constraints.

Conceptually:

```text
Difference
     │
     ▼
Causal Mass
     │
     ▼
Salience
     │
     ▼
Resource Allocation
```

Causal Mass answers:

> "How important is this?"

Salience answers:

> "Is it important enough to process?"

---

# Relationship to Metric Construction

Only gated observations are used to construct internal metrics.

The pipeline therefore becomes:

```text
Environmental Difference
          │
          ▼
     Causal Mass
          │
          ▼
      Salience χ
          │
          ▼
 Computational Gate 𝓑
          │
          ▼
 Metric Construction
          │
          ▼
 Mapping Quality
```

This filtering dramatically reduces the computational burden of downstream metric construction.

---

# Properties

An effective salience mechanism should satisfy several desirable properties.

## Bounded

Salience should produce finite computational demand regardless of environmental complexity.

---

## Adaptive

Thresholds should shift as computational resources change.

Under resource scarcity, only the highest-value observations should be processed.

---

## Context Sensitive

Priority depends on current goals, environment, and existing knowledge.

---

## Computationally Efficient

The salience computation itself should consume substantially less computation than the downstream processing it enables.

Otherwise, the filtering stage becomes counterproductive.

---

# Role Within AMP

Salience is the bridge between perception and representation.

It transforms weighted environmental differences into computational decisions.

Only information that survives this stage contributes to metric construction, mapping quality, and recursive metric discovery.

Within AMP, intelligence is therefore selective before it is representational.

The compiler does not attempt to model everything.

It first decides **what is worth modeling**.
