# Definitions

This document defines the primary mathematical objects and symbols used throughout the **Adaptive Metric Compiler (AMP)** framework.

AMP describes intelligence as the recursive construction, evaluation, and discovery of increasingly effective internal metrics.

---

# Core Objects

## Environment

$$
E
$$

The external environment from which observations and differences are generated.

The environment contains the underlying structure that an agent attempts to model.

---

## Environmental Difference

$$
\Delta
$$

An observable distinction between two environmental states.

A difference exists when:

$$
\Delta(x_1,x_2)\neq0
$$

Not all differences are computationally meaningful.

AMP begins by determining which differences deserve processing.

---

## Agent

$$
A
$$

The computational system interacting with the environment.

The agent transforms environmental information into internal representations and future actions.

---

# Causal Layer

## Causal Influence

$$
\Phi
$$

A measure of how much an agent changes the probability distribution of future states.

Defined as:

$$
\Phi=
D_{KL}
\left(
P(X|\text{agent})
\parallel
P(X|\neg\text{agent})
\right)
$$

Higher values indicate stronger causal influence.

---

## Causal Mass

$$
M_C
$$

A measure of the computational importance of an environmental difference.

Defined as:

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
- behavioral influence.

It determines which differences are worth computational attention.

---

# Selection Layer

## Salience

$$
\chi(\Delta)
$$

The transformation from causal significance into computational priority.

Defined as:

$$
\chi(\Delta)=\rho=\sigma(M_C-\theta)
$$

where:

- $\rho$ is the salience value,
- $\theta$ is the computational threshold,
- $\sigma$ is the activation function.

---

## Computational Gate

$$
\mathcal B(\rho)
$$

The mechanism that determines whether information proceeds through the compiler.

Defined as:

$$
\mathcal B(\rho)=
\begin{cases}
1 & \rho\geq\rho_{crit}\\
0 & \rho<\rho_{crit}
\end{cases}
$$

The gate represents limited computational resources.

---

# Representation Layer

## Internal Metric

$$
M_Q
$$

The internal mapping used by an agent to represent the environment.

Defined as:

$$
M_Q:E\rightarrow A
$$

A metric determines which environmental structures become computationally accessible.

---

## Metric Construction

$$
F
$$

The transformation that constructs an internal metric from selected information.

It represents the compilation step between environmental information and internal computational structure.

---

# Evaluation Layer

## Mapping Quality

$$
Q_M
$$

A measure of how effectively an internal metric supports future computation.

Mapping Quality evaluates whether a metric:

- compresses search,
- improves prediction,
- preserves invariants,
- generalizes,
- expands viable computation.

---

## Search Compression

$$
C
$$

Measures how much a metric reduces future search requirements.

Defined as:

$$
C=
\frac{\Delta H(\text{Search})}
{I_{stored}}
$$

---

## Task Performance

$$
T
$$

Measures how effectively a metric supports successful execution in a target domain.

Examples:

- prediction,
- planning,
- control,
- explanation.

---

## Predictive Improvement

$$
K
$$

Measures the rate at which the internal model approaches observed reality.

Defined as:

$$
K=
-\frac{dD_{KL}(P_{true}\parallel P_{model})}{dt}
$$

---

## Growth of Viable Computation

$$
G_L
$$

Measures the expansion of computational possibility produced by additional stored information.

Defined as:

$$
G_L=
\frac{\partial\Omega_{viable}}
{\partial I_{stored}}
$$

---

## Representational Adaptability

$$
R_a
$$

Measures how effectively a metric transfers across scales and planning horizons.

Defined as:

$$
R_a=
\frac{
\min(\text{Scale},\text{Horizon})
}
{
\max(\text{Scale},\text{Horizon})
}
\log_2(1+\mathcal L)
$$

---

## Invariant Preservation

$$
I_c
$$

Measures how well a metric preserves important structural relationships.

Defined as:

$$
I_c=
\frac{
\text{Preserved Invariants}
}
{
\text{Relevant Structure}
}
$$

---

## Complexity Penalty

$$
D
$$

The computational cost associated with maintaining a metric.

Defined as:

$$
D=K(M_Q)
$$

Higher complexity reduces overall mapping quality.

---

# Discovery Layer

## Discovery Operator

$$
D_\Omega
$$

The operator that transforms one metric into a new metric.

Defined as:

$$
D_\Omega:M_Q\rightarrow M_Q'
$$

Unlike optimization, discovery changes the representation itself.

---

## Discovered Metric

$$
M_Q'
$$

The successor metric produced by the Discovery Operator.

It represents an improved computational organization.

---

## Discovery Efficiency

$$
D_M
$$

Measures the computational gain obtained from metric discovery.

Defined as:

$$
D_M=
\frac{
\Delta\Omega_{viable}(M_Q\rightarrow M_Q')
}
{
C_{search}(M_Q\rightarrow M_Q')
}
$$

---

## Computational Leverage

$$
L_M
$$

Measures the increase in computational capability relative to discovery cost.

Defined as:

$$
L_M=
\frac{
\Delta\Omega_{viable}\times\Delta Q
}
{
\Delta C_M
}
$$

---

# State Space

## Viable Computational Space

$$
\Omega_{viable}
$$

The set of computations that are feasible under an agent's resource constraints.

Metric discovery expands this space.

---

## Information Storage

$$
I_{stored}
$$

The amount of information encoded within an internal metric.

The value is not raw information quantity, but information that contributes to computational structure.

---

# Phase Transition Layer

## Critical Information Level

$$
I_{crit}
$$

The point at which additional preserved structure produces disproportionate computational gains.

---

## Computational Growth

$$
G_B
$$

The growth of computational capability as a function of internal structure.

A phase transition occurs when:

$$
\frac{\partial^2G_B}{\partial I_c^2}
\bigg|_{I_c=I_{crit}}
\rightarrow
\infty
$$

---

# Kernel Sequence

The complete AMP transformation is:

$$
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
$$

The sequence represents:

1. detecting differences,
2. estimating causal importance,
3. selecting computationally valuable information,
4. constructing metrics,
5. evaluating metrics,
6. discovering improved metrics.

---

# Intelligence

AMP defines intelligence as recursive metric discovery:

$$
\text{Intelligence}=
\text{recursive execution of }D_\Omega
$$

The framework therefore treats intelligence as the ability to repeatedly construct better computational representations.
