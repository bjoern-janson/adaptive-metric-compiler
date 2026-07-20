# Formalism

This document presents the mathematical formalism of the **Adaptive Metric Compiler (AMP)** framework.

The objective of AMP is to formalize intelligence as the recursive discovery and compilation of increasingly effective internal metrics.

---

# 1. Environment

Let

$$
E
$$

denote the external environment.

The environment generates observable differences:

$$
\Delta \in E
$$

where:

$$
\Delta(x_1,x_2)\neq0
$$

indicates that two environmental states are distinguishable.

---

# 2. Causal Mass

Not every observable difference is equally important.

AMP assigns each difference a **causal mass**, measuring both its informational rarity and its influence on future behavior.

The causal influence of an agent is defined as:

$$
\Phi =
D_{KL}
\left(
P(X|\text{agent})
\parallel
P(X|\neg\text{agent})
\right)
$$

where $D_{KL}$ denotes the Kullback–Leibler divergence.

The causal mass of an environmental difference is:

$$
M_C=
\int_{\Omega}
\left|
\frac{\partial A}{\partial\Delta}
\right|
(-\log_2 p(\Delta))
d\Omega
$$

where:

- $A$ denotes downstream action,
- $p(\Delta)$ is the probability of observing the difference,
- $\Omega$ is the relevant observation space.

Large causal mass corresponds to rare differences that strongly influence future behavior.

---

# 3. Salience

Causal mass is transformed into computational salience through a sigmoid response:

$$
\chi(\Delta)=\rho=\sigma(M_C-\theta)
$$

where:

- $\theta$ is a salience threshold,
- $\sigma(\cdot)$ is the logistic function.

The resulting activation is converted into a binary computational gate:

$$
B(\rho)=
\begin{cases}
1 & \rho \geq \rho_{crit}\\
0 & \rho < \rho_{crit}
\end{cases}
$$

Only gated information proceeds through the remaining stages of the compiler.

---

# 4. Metric Construction

Selected information is transformed into an internal metric.

Define the mapping:

$$
M_Q:E\rightarrow A
$$

where:

- $E$ is the environment,
- $A$ is the agent's internal computational space.

The mapping determines which environmental distinctions become computationally accessible.

---

# 5. Mapping Quality

The quality of a metric is modeled as:

$$
Q_M=
\frac{
C\times T\times G_L\times K\times R_a\times I_c
}
{D}
$$

with:

$$
C=
\frac{\Delta H(\text{Search})}
{I_{stored}}
$$

$$
K=
-\frac{
dD_{KL}(P_{true}\parallel P_{model})
}
{dt}
$$

$$
G_L=
\frac{
\partial\Omega_{viable}
}
{
\partial I_{stored}
}
$$

$$
R_a=
\frac{
\min(\text{Scale},\text{Horizon})
}
{
\max(\text{Scale},\text{Horizon})
}
\log_2(1+\mathcal{L})
$$

$$
I_c=
\frac{
\text{Preserved Invariants}
}
{
\text{Relevant Structure}
}
$$

$$
D=K(M_Q)
$$

These quantities represent:

| Symbol | Interpretation |
|---|---|
| $C$ | Search compression |
| $T$ | Task performance |
| $G_L$ | Growth of viable computation |
| $K$ | Predictive improvement |
| $R_a$ | Representational adaptability |
| $I_c$ | Invariant preservation |
| $D$ | Metric complexity penalty |

Higher values of $Q_M$ correspond to metrics that better support computation.

---

# 6. Metric Discovery

Optimization operates inside a metric.

AMP instead introduces an operator that searches over metrics themselves.

Define:

$$
D_{\Omega}:M_Q\longrightarrow M_Q'
$$

where:

- $M_Q$ is the current metric,
- $M_Q'$ is the discovered successor metric.

The efficiency of discovery is:

$$
D_M=
\frac{
\Delta\Omega_{viable}(M_Q\rightarrow M_Q')
}
{
C_{search}(M_Q\rightarrow M_Q')
}
$$

This quantity measures the increase in viable computational space obtained per unit search cost.

---

# 7. Computational Leverage

The leverage produced by metric discovery is:

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

---

# 8. Phase Transition

AMP proposes that sufficiently accurate metrics produce structural phase transitions.

Formally:

$$
\frac{\partial^2G_B}{\partial I_c^2}
\bigg|_{I_c=I_{crit}}
\rightarrow
\infty
\implies
M_Q
\xrightarrow{D_{\Omega}}
M_Q'
$$

At this point, small representational improvements produce disproportionately large expansions in computational capability.

---

# 9. Kernel

The complete computational pipeline is:

$$
\Delta
\xrightarrow{\chi,B,F}
M_Q
\xrightarrow{Q_M,D_{\Omega}}
M_Q'
$$

This kernel summarizes the recursive compilation process proposed by AMP.

---

# 10. Recursive Intelligence

AMP distinguishes optimization from discovery.

Optimization follows the local gradient of mapping quality:

$$
\nabla Q_M(M_Q)
$$

Discovery constructs an entirely new metric:

$$
D_{\Omega}(M_Q)=M_Q'
$$

Recursive application of the discovery operator defines intelligence:

$$
\boxed{
\text{Intelligence}
=
\text{recursive execution of }D_{\Omega}
}
$$

---

# 11. Terminal Limit

The framework hypothesizes that increasingly accurate metrics generate accelerating expansions of viable computation.

Formally:

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

This expression represents the asymptotic hypothesis of AMP: as an internal metric approaches the informational structure of reality, each additional improvement enables disproportionately larger regions of computational possibility.

---

# Summary

The Adaptive Metric Compiler formalism models intelligence as a recursive cycle consisting of:

1. detecting meaningful environmental differences,
2. computing causal significance,
3. allocating computational resources,
4. constructing internal metrics,
5. evaluating metric quality,
6. discovering improved metrics,
7. recursively repeating the process.

Rather than viewing intelligence as optimization within a fixed representation, AMP models intelligence as the continual compilation of increasingly expressive computational metrics.
