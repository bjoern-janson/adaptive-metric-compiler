# Discovery Operator

The Discovery Operator is the central mechanism of the Adaptive Metric Compiler (AMP).

Its purpose is to generate **new internal metrics** rather than improve existing ones.

This distinction separates AMP from traditional optimization frameworks.

Most learning algorithms optimize parameters within a fixed representation.

AMP instead models intelligence as the continual discovery of better representations themselves.

---

# Motivation

Given an internal metric:

$$
M_Q
$$

an optimization algorithm searches for better solutions while remaining inside that metric.

For example:

- gradient descent adjusts parameters,
- A* searches a graph,
- dynamic programming improves policies,
- Bayesian inference updates beliefs.

In every case, the metric itself remains fixed.

The Discovery Operator instead searches over the space of possible metrics.

Its output is not a better solution.

Its output is a **better way of representing problems.**

---

# Definition

The Discovery Operator is defined as:

$$
D_{\Omega}:M_Q\longrightarrow M_Q'
$$

where:

- $M_Q$ is the current metric,
- $M_Q'$ is the discovered successor metric.

The operator transforms one computational representation into another.

---

# Interpretation

A discovery may:

- reveal hidden invariants,
- simplify search,
- expose new abstractions,
- reduce representational complexity,
- unify previously unrelated concepts,
- enlarge the computational search space.

The result is not merely improved performance.

The result is a different computational landscape.

---

# Optimization vs Discovery

Optimization follows the local structure of an existing metric:

$$
\nabla Q_M(M_Q)
$$

The representation remains unchanged.

Only the solution improves.

Discovery instead changes the metric itself:

$$
D_{\Omega}(M_Q)=M_Q'
$$

The optimization landscape is replaced by a new one.

This distinction forms one of the central claims of AMP.

---

# Discovery Efficiency

The effectiveness of metric discovery is measured by:

$$
D_M=
\frac{
\Delta\Omega_{viable}(M_Q\rightarrow M_Q')
}
{
C_{search}(M_Q\rightarrow M_Q')
}
$$

where:

- numerator: increase in viable computational space,
- denominator: computational cost of discovering the new metric.

Higher values indicate more computational leverage per unit search effort.

---

# Computational Leverage

The leverage created by discovery is:

$$
L_M=
\frac{
\Delta\Omega_{viable}\times\Delta Q
}
{
\Delta C_M
}
$$

where:

- $\Delta Q$ is the improvement in mapping quality,
- $\Delta C_M$ is the computational cost of discovery.

This quantity estimates how much computational capability is gained relative to the resources invested in discovering the new metric.

---

# Why Discovery Matters

Many of the largest advances in science and engineering arise not from solving problems faster, but from changing how problems are represented.

Examples include:

- positional number systems,
- Cartesian coordinates,
- calculus,
- automatic differentiation,
- compilers,
- attention mechanisms,
- transformer architectures.

Each introduced a new computational metric that dramatically simplified subsequent computation.

AMP models these events as applications of the Discovery Operator.

---

# Recursive Discovery

Discovery is not a single event.

Each newly discovered metric creates new opportunities for further discovery.

The process becomes:

```text
M₀
 │
 ▼
DΩ
 │
 ▼
M₁
 │
 ▼
DΩ
 │
 ▼
M₂
 │
 ▼
DΩ
 │
 ▼
M₃
```

Each iteration expands the computational possibilities available to the next.

---

# Relationship to Mapping Quality

Discovery depends on metric evaluation.

The pipeline is:

```text
Current Metric
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

Mapping Quality determines **how good** a metric is.

The Discovery Operator determines **how metrics evolve.**

---

# Search over Metrics

Traditional optimization searches:

```text
solution
```

inside:

```text
fixed representation
```

AMP instead searches:

```text
representation
```

itself.

This creates a hierarchy of search.

```text
Metric Space

M₁
│
├── solution
├── solution
└── solution

↓

DΩ

↓

M₂

├── solution
├── solution
├── solution
└── solution
```

Changing the representation changes every optimization problem that follows.

---

# Relationship to Intelligence

AMP defines intelligence as:

$$
\boxed{
\text{Intelligence}
=
\text{recursive execution of }D_{\Omega}
}
$$

Rather than equating intelligence with prediction or optimization, the framework proposes that intelligence is fundamentally the ability to construct increasingly effective internal metrics.

Optimization is one consequence of a good metric.

Discovery is the process that creates the metric.

---

# Relationship to Phase Transitions

Repeated applications of the Discovery Operator may eventually reach a critical point where a small representational improvement produces a disproportionately large increase in computational capability.

Formally:

$$
M_Q\xrightarrow{D_{\Omega}}M_Q'
$$

may produce:

$$
\Delta\Omega_{viable}\gg\Delta C_M
$$

creating a computational phase transition.

Such transitions correspond to moments where a new representation unlocks entire classes of previously inaccessible solutions.

---

# Summary

The Discovery Operator is the engine of the Adaptive Metric Compiler.

Unlike conventional optimization algorithms, it searches over representations rather than solutions.

By recursively constructing improved metrics, the Discovery Operator expands the viable computational space available to an agent, enabling increasingly powerful forms of reasoning, abstraction, and problem solving.

Within AMP, optimization improves solutions.

Discovery improves the space in which solutions exist.
