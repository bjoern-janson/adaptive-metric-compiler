# Examples

This document presents examples of computational transitions that can be interpreted through the **Adaptive Metric Compiler (AMP)** framework.

The central idea is that major advances often occur not because a system receives more computational resources, but because it discovers a better internal metric.

A new metric changes which problems are computationally accessible.

---

# 1. Positional Number Systems

## Previous Metric

Early numerical systems represented quantities through additive structures.

For example:

$$
IIIIIIII
$$

represented eight.

Large calculations required explicit manipulation of many symbols.

The computational cost increased rapidly with magnitude.

---

## Metric Discovery

Positional notation introduced a new computational metric:

$$
M_Q:
\text{symbols}
\rightarrow
\text{place-value structure}
$$

The position of a symbol became meaningful.

A small set of symbols could represent arbitrarily large quantities.

---

## AMP Interpretation

The discovery operator:

$$
D_\Omega(M_Q)=M_Q'
$$

created a metric that compressed numerical structure.

The result was:

- reduced search complexity,
- easier arithmetic,
- scalable computation.

The improvement was not merely faster calculation.

The representation itself changed.

---

# 2. Cartesian Coordinates

## Previous Metric

Geometric reasoning was traditionally expressed through direct relationships between objects.

Distances, angles, and transformations required specialized reasoning.

---

## Metric Discovery

Cartesian coordinates introduced a mapping:

$$
\text{space}
\rightarrow
(x,y,z)
$$

Geometric structure became algebraically accessible.

---

## AMP Interpretation

The new metric preserved important invariants while enabling new operations.

Consequences included:

- analytical geometry,
- mathematical physics,
- numerical simulation.

The discovery expanded:

$$
\Omega_{viable}
$$

by transforming geometric problems into computational ones.

---

# 3. Calculus

## Previous Metric

Natural phenomena were described primarily through static relationships.

Continuous change was difficult to formalize.

---

## Metric Discovery

Calculus introduced a metric for change:

$$
\frac{dx}{dt}
$$

and accumulation:

$$
\int f(x)dx
$$

Dynamic systems became computational objects.

---

## AMP Interpretation

Calculus created a new computational language for describing evolving systems.

The metric transformation enabled:

- physics,
- engineering,
- optimization,
- differential equations.

A previously inaccessible class of problems became tractable.

---

# 4. Automatic Differentiation

## Previous Metric

Before automatic differentiation, obtaining gradients required manual derivation.

The computational bottleneck was human symbolic manipulation.

---

## Metric Discovery

Automatic differentiation transformed computation into:

$$
\text{program}
\rightarrow
\text{derivative computation}
$$

The system compiled derivatives automatically.

---

## AMP Interpretation

The discovery reduced the cost of metric construction.

Effects included:

- faster optimization,
- larger models,
- rapid experimentation.

The important transition was not simply better algorithms.

It was a new computational interface.

---

# 5. Compilers

## Previous Metric

Programs were written directly in machine instructions.

Human reasoning had to operate close to hardware.

---

## Metric Discovery

Compilers introduced:

$$
\text{high-level language}
\rightarrow
\text{machine execution}
$$

The programmer interacted with abstractions rather than hardware details.

---

## AMP Interpretation

The compiler created a new metric that separated:

- problem specification,
- execution mechanism.

This expanded viable computation by allowing humans to reason at higher levels of abstraction.

---

# 6. Alpha-Beta Pruning

## Previous Metric

Minimax search explored game trees directly.

The search space grew exponentially.

---

## Metric Discovery

Alpha-beta pruning introduced a metric where irrelevant branches could be eliminated.

The algorithm transformed the effective search space.

---

## AMP Interpretation

The discovery did not increase raw computation.

It reduced the computational geometry of the problem.

The same hardware could solve larger problems.

---

# 7. Deep Learning

## Previous Metric

Traditional machine learning relied heavily on engineered representations.

Feature construction was a major bottleneck.

---

## Metric Discovery

Deep neural networks introduced hierarchical learned representations.

The system could construct internal features automatically.

---

## AMP Interpretation

The metric itself became adaptive.

The model learned representations that exposed useful structure.

This shifted computation from:

```text
Human-designed features
