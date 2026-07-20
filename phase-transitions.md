# Phase Transitions

Phase Transitions describe the conditions under which a small improvement in an internal metric produces a disproportionately large expansion in computational capability.

Within the Adaptive Metric Compiler (AMP), these transitions occur when metric discovery fundamentally restructures the computational landscape rather than merely improving performance within an existing representation.

---

# Motivation

Most computational improvements are incremental.

A better heuristic may reduce search time.

A more accurate model may improve prediction.

A larger dataset may increase performance.

These changes are continuous.

Occasionally, however, a new representation transforms the problem itself.

Examples include:

- positional notation,
- Cartesian coordinates,
- calculus,
- automatic differentiation,
- compilers,
- deep neural network architectures.

In these cases, a relatively small representational change enables a qualitatively different computational regime.

AMP models these events as **computational phase transitions**.

---

# Definition

Let

$$
M_Q
$$

denote the current internal metric.

Metric discovery produces

$$
M_Q
\xrightarrow{D_\Omega}
M_Q'
$$

Most discoveries produce gradual improvements.

A phase transition occurs when this transformation produces a discontinuous increase in viable computation.

---

# Formal Criterion

AMP proposes the transition criterion:

$$
\frac{\partial^2 G_B}
{\partial I_c^2}
\bigg|_{I_c=I_{crit}}
\rightarrow
\infty
\implies
M_Q
\xrightarrow{D_\Omega}
M_Q'
$$

where:

- $G_B$ denotes computational growth,
- $I_c$ measures invariant preservation,
- $I_{crit}$ is the critical level of structural information.

At the critical point, a small increase in preserved structure produces a disproportionately large increase in computational capability.

---

# Interpretation

The transition is not caused by additional computation alone.

Instead, it occurs because the internal metric captures a previously hidden regularity in the environment.

Once this regularity becomes explicit:

- search collapses,
- prediction improves,
- abstraction becomes possible,
- new discoveries become computationally feasible.

The representation itself has changed.

---

# Computational Phase Boundary

Before the transition:

```text
Small improvement
        │
        ▼
Small capability gain
```

After the transition:

```text
Small improvement
        │
        ▼
Large capability gain
```

The boundary separates two computational regimes.

The same optimization process now operates inside a fundamentally more expressive metric.

---

# Viable Computational Space

Throughout AMP,

$$
\Omega_{viable}
$$

denotes the set of computations that are feasible under an agent's resource constraints.

Metric discovery expands this space.

Most discoveries produce modest increases.

Phase transitions produce rapid expansion.

Conceptually:

```text
Before Discovery

████

↓

After Discovery

████████████████████
```

The increase reflects new classes of computationally accessible problems rather than merely faster solutions.

---

# Relationship to Mapping Quality

Mapping Quality measures the usefulness of the current metric.

Discovery generates a new metric.

Phase transitions occur when the new metric produces a nonlinear increase in computational usefulness.

The progression is therefore:

```text
Metric
   │
   ▼
Quality Evaluation
   │
   ▼
Discovery
   │
   ▼
Improved Metric
   │
   ▼
Phase Transition
```

Only some discoveries reach the critical threshold necessary for a structural transition.

---

# Computational Leverage

Phase transitions are characterized by unusually large computational leverage.

The leverage metric:

$$
L_M=\frac{\Delta\Omega_{viable}\Delta Q}{\Delta C_M}
$$

becomes exceptionally large because a relatively small discovery unlocks a vastly larger computational space.

This distinguishes transformational discoveries from ordinary optimization.

---

# Recursive Discovery

Phase transitions rarely occur in isolation.

Each transition increases the range of metrics that become discoverable in subsequent iterations.

The process therefore becomes self-reinforcing.

```text
Metric
   │
   ▼
Discovery
   │
   ▼
Improved Metric
   │
   ▼
Larger Search Space
   │
   ▼
More Discoveries
   │
   ▼
Next Transition
```

Successive transitions create increasingly expressive computational systems.

---

# Terminal Hypothesis

AMP proposes the asymptotic relationship:

$$
\boxed{
\lim_{K(M_Q)\rightarrow K(I_{true})}
\frac{
\partial\Omega_{viable}
}
{
\partial K(M_Q)
}
\rightarrow
\infty
}
$$

The hypothesis states that increasingly accurate internal metrics produce increasingly large expansions of viable computational space.

In this view, intelligence accelerates not because computation becomes arbitrarily faster, but because progressively better metrics reveal increasingly powerful computational structure.

---

# Examples

Potential examples of computational phase transitions include:

- positional number systems,
- symbolic algebra,
- Cartesian geometry,
- differential calculus,
- automatic differentiation,
- optimizing compilers,
- attention mechanisms,
- transformer architectures.

Each can be interpreted as replacing one computational metric with another that dramatically enlarges the space of tractable computation.

---

# Summary

Phase Transitions represent the highest level of the Adaptive Metric Compiler.

They occur when metric discovery produces a structural change rather than an incremental improvement.

Instead of merely solving problems more efficiently, the system acquires a new computational language in which previously intractable problems become tractable.

Within AMP, intelligence advances through recursive metric discovery, and the largest advances occur when those discoveries cross computational phase boundaries.
