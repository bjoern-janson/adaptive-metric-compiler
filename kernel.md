# Kernel

The Kernel is the complete computational pipeline of the **Adaptive Metric Compiler (AMP)**.

It describes the transformation from raw environmental differences into recursively improved internal metrics.

The central hypothesis of AMP is:

$$
\Delta
\xrightarrow{\chi,\mathcal B,F}
M_Q
\xrightarrow{Q_M,D_\Omega}
M_Q'
$$

Environmental differences are transformed into computationally useful metrics, evaluated, and replaced by improved metrics.

---

# Overview

The Adaptive Metric Compiler consists of seven primary stages:

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
 Computational Gate
          │
          ▼
 Metric Construction
          │
          ▼
 Mapping Quality
          │
          ▼
 Discovery Operator
          │
          ▼
 Improved Metric
```

Each stage performs a distinct computational transformation.

---

# 1. Environmental Difference

The process begins with an observable difference:

$$
\Delta(x_1,x_2)\neq0
$$

A difference represents a distinction between environmental states.

However, not every distinction is computationally meaningful.

The first problem of intelligence is therefore:

> Which differences deserve computation?

AMP treats this as a selection problem.

---

# 2. Causal Mass

The first transformation assigns causal importance to differences.

$$
M_C=
\int_{\Omega}
\left|
\frac{\partial A}{\partial\Delta}
\right|
(-\log_2p(\Delta))
d\Omega
$$

Causal Mass combines:

- informational rarity,
- downstream behavioral influence.

A difference with high causal mass is both informative and capable of changing future action.

The output is a weighted representation of environmental significance.

---

# 3. Salience

Causal Mass is converted into computational priority:

$$
\chi(\Delta)=\rho=\sigma(M_C-\theta)
$$

where:

- $\theta$ is the computational threshold,
- $\rho$ is the salience value.

Salience determines whether an observation receives computational resources.

---

# 4. Computational Gate

The salience value controls access to later computation.

$$
\mathcal B(\rho)=
\begin{cases}
1 & \rho\geq\rho_{crit}\\
0 & \rho<\rho_{crit}
\end{cases}
$$

The gate implements computational scarcity.

Information below the threshold is discarded.

Information above the threshold proceeds into metric construction.

---

# 5. Metric Construction

Selected information is transformed into an internal metric:

$$
M_Q:E\rightarrow A
$$

where:

- $E$ is the environment,
- $A$ is the agent's internal computational space.

The mapping determines which environmental structures become computationally accessible.

Different metrics expose different solution spaces.

---

# 6. Mapping Quality

The constructed metric is evaluated using:

$$
Q_M=
\frac{
C\times T\times G_L\times K\times R_a\times I_c
}
{D}
$$

Mapping Quality measures whether a metric is computationally useful.

A high-quality metric should:

- compress search,
- improve prediction,
- preserve invariants,
- generalize across contexts,
- expand viable computation,
- minimize unnecessary complexity.

The purpose of evaluation is not to find a perfect representation immediately.

It is to identify metrics worth improving.

---

# 7. Discovery Operator

The Discovery Operator transforms one metric into another:

$$
D_\Omega:M_Q\rightarrow M_Q'
$$

Unlike optimization, which improves solutions inside a fixed representation, discovery changes the representation itself.

Optimization:

$$
\nabla Q_M(M_Q)
$$

Discovery:

$$
D_\Omega(M_Q)=M_Q'
$$

The output is not a better answer.

The output is a better computational space.

---

# Recursive Kernel

The complete recursive process:

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
Gate
    │
    ▼
Metric
    │
    ▼
Quality Evaluation
    │
    ▼
Discovery
    │
    ▼
New Metric
    │
    └───────────────┐
                    │
                    ▼
              New Differences
```

Each iteration operates on an improved computational landscape.

---

# Optimization and Discovery

AMP separates two fundamentally different processes.

## Optimization

Optimization searches within an existing metric.

Examples:

- parameter tuning,
- gradient descent,
- policy improvement,
- numerical search.

It follows:

$$
\nabla Q_M(M_Q)
$$

The representation remains fixed.

---

## Discovery

Discovery searches over possible metrics.

It follows:

$$
D_\Omega(M_Q)=M_Q'
$$

The representation changes.

This distinction explains why some advances produce incremental improvements while others create entirely new computational regimes.

---

# Kernel Sequence

The complete AMP kernel is:

$$
\boxed{
\Delta
\rightarrow
\chi
\rightarrow
\mathcal B
\rightarrow
F
\rightarrow
M_Q
\rightarrow
Q_M
\rightarrow
D_\Omega
\rightarrow
M_Q'
}
$$

where:

| Symbol | Meaning |
|---|---|
| $\Delta$ | Environmental difference |
| $\chi$ | Salience transformation |
| $\mathcal B$ | Computational gate |
| $F$ | Metric construction function |
| $M_Q$ | Internal metric |
| $Q_M$ | Mapping Quality |
| $D_\Omega$ | Discovery Operator |
| $M_Q'$ | Improved metric |

---

# Phase Transition

Repeated execution of the kernel may produce a computational phase transition.

A successful discovery can produce:

$$
\Delta\Omega_{viable}\gg\Delta C_M
$$

where the increase in viable computation greatly exceeds the cost of discovery.

At this point, the system has not merely optimized performance.

It has entered a new computational regime.

---

# Intelligence as Recursive Compilation

AMP defines intelligence as:

$$
\boxed{
\text{Intelligence}
=
\text{recursive execution of }D_\Omega
}
$$

The framework views intelligence as continual metric compilation.

A system becomes more capable not only by computing faster, but by discovering increasingly effective ways to organize computation itself.

---

# Summary

The AMP Kernel describes a recursive transformation:

1. Environmental differences are detected.
2. Causal significance is estimated.
3. Computational priority is assigned.
4. Internal metrics are constructed.
5. Metrics are evaluated.
6. New metrics are discovered.
7. The process repeats.

The central claim of AMP is:

> Intelligence is not only optimization within a representation. Intelligence is the recursive discovery of better representations.
