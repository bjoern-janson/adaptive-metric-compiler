# Mapping Quality

Mapping Quality is the evaluation stage of the Adaptive Metric Compiler (AMP).

Its purpose is to measure how effectively an internal metric supports future computation.

Rather than evaluating a representation solely by prediction accuracy or compression, AMP models mapping quality as a multidimensional property that captures how useful a metric is for solving future problems.

---

# Motivation

Once an internal metric has been constructed, the system must determine whether it is a *good* metric.

A useful metric should not merely describe the environment accurately.

It should also make future computation easier.

Examples include metrics that:

- reduce search,
- preserve important structure,
- generalize beyond observed data,
- simplify reasoning,
- support efficient planning,
- enable future discoveries.

AMP therefore evaluates metrics according to their computational utility rather than their descriptive accuracy alone.

---

# Metric Mapping

AMP defines an internal metric as:

$$
M_Q:E\longrightarrow A
$$

where:

- $E$ denotes the environment,
- $A$ denotes the agent's internal computational space.

The mapping determines how environmental structure is represented internally.

Different mappings expose different computational possibilities.

---

# Mapping Quality

The overall quality of a metric is defined as:

$$
Q_M=
\frac{
C \times T \times G_L \times K \times R_a \times I_c
}
{D}
$$

where:

$$
C=\frac{\Delta H(\text{Search})}{I_{\text{stored}}}
$$

$$
K=-\frac{dD_{KL}(P_{\text{true}}\parallel P_{\text{model}})}{dt}
$$

$$
G_L=
\frac{\partial\Omega_{\text{viable}}}
{\partial I_{\text{stored}}}
$$

$$
R_a=
\frac{\min(\text{Scale},\text{Horizon})}
{\max(\text{Scale},\text{Horizon})}
\log_2(1+\mathcal{L})
$$

$$
I_c=
\frac{\text{Preserved Invariants}}
{\text{Relevant Structure}}
$$

$$
D=K(M_Q)
$$

Higher values correspond to metrics that better support future computation.

---

# Components

## Search Compression

$$
C=
\frac{\Delta H(\text{Search})}
{I_{\text{stored}}}
$$

A useful metric reduces the entropy of future search.

Representations that dramatically narrow the search space receive higher values.

---

## Task Performance

$$
T
$$

Task performance measures how effectively the metric supports successful execution on the target domain.

The precise definition depends on the application.

Examples include:

- prediction accuracy,
- planning success,
- control performance,
- scientific explanatory power.

---

## Predictive Improvement

$$
K=
-\frac{dD_{KL}(P_{\text{true}}\parallel P_{\text{model}})}{dt}
$$

A useful metric should continuously reduce divergence between the model and reality.

Higher values indicate faster convergence toward accurate internal models.

---

## Growth of Viable Computation

$$
G_L=
\frac{\partial\Omega_{\text{viable}}}
{\partial I_{\text{stored}}}
$$

This measures how much additional computational capability is created by storing new information.

Metrics that unlock disproportionately larger computational spaces receive larger values.

---

## Representational Adaptability

$$
R_a=
\frac{\min(\text{Scale},\text{Horizon})}
{\max(\text{Scale},\text{Horizon})}
\log_2(1+\mathcal{L})
$$

Adaptability measures how effectively the metric generalizes across scales and planning horizons.

Highly specialized metrics perform well only locally.

Adaptive metrics remain useful across multiple contexts.

---

## Invariant Preservation

$$
I_c=
\frac{\text{Preserved Invariants}}
{\text{Relevant Structure}}
$$

A high-quality metric preserves important structural relationships while discarding irrelevant variation.

This encourages abstraction without destroying useful information.

---

## Complexity Penalty

$$
D=K(M_Q)
$$

More expressive metrics generally require greater computational complexity.

The denominator penalizes unnecessarily complex mappings.

The objective is therefore not maximal complexity but maximal computational efficiency.

---

# Interpretation

A useful metric is one that simultaneously:

- compresses search,
- improves prediction,
- preserves invariants,
- generalizes across domains,
- expands viable computation,
- minimizes unnecessary complexity.

No single criterion is sufficient.

Mapping Quality therefore evaluates the overall computational usefulness of a representation.

---

# Relationship to Discovery

Mapping Quality evaluates existing metrics.

It does **not** create new ones.

The discovery operator acts on the evaluated metric:

$$
M_Q\xrightarrow{D_\Omega}M_Q'
$$

producing an improved mapping.

Quality determines *how good* a metric is.

Discovery determines *how metrics change*.

---

# Relationship to Optimization

Traditional optimization searches for better parameters within a fixed metric.

AMP separates this process from metric discovery.

Optimization follows:

$$
\nabla Q_M(M_Q)
$$

improving performance while remaining inside the same representational space.

Discovery instead transforms the representational space itself.

This distinction allows AMP to model conceptual innovation rather than parameter refinement alone.

---

# Computational Role

Within the Adaptive Metric Compiler, Mapping Quality acts as the evaluation function for recursive metric evolution.

The computational pipeline becomes:

```text
Environmental Difference
          │
          ▼
     Causal Mass
          │
          ▼
      Salience
          │
          ▼
 Metric Construction
          │
          ▼
 Mapping Quality
          │
          ▼
 Metric Discovery
          │
          ▼
 Improved Metric
```

Each cycle produces an increasingly expressive internal metric capable of supporting more powerful future computation.

---

# Summary

Mapping Quality measures how effectively an internal metric supports intelligent computation.

Rather than rewarding descriptive accuracy alone, AMP evaluates representations according to their ability to compress search, preserve structure, improve prediction, generalize across domains, and expand the space of viable computation.

It provides the objective function that guides recursive metric discovery throughout the Adaptive Metric Compiler.
