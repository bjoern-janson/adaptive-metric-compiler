# Causal Mass

Causal Mass is the first stage of the Adaptive Metric Compiler (AMP).

Its purpose is to determine **which environmental differences deserve computation**.

AMP argues that information alone is insufficient for intelligent behavior. An observation may be highly surprising while having no effect on future action, or it may be common yet critically important for successful decision-making.

Causal Mass therefore measures information according to both its informational content and its downstream causal influence.

---

# Motivation

Traditional information theory measures surprise.

For an observation \(x\),

\[
I(x)=-\log_2 P(x)
\]

Rare events contain more information than common ones.

However, intelligence is not driven by surprise alone.

An event that changes nothing is computationally irrelevant regardless of how unlikely it is.

Conversely, an event that dramatically alters future behavior should receive computational attention even if it occurs frequently.

AMP therefore introduces **Causal Mass**, which combines informational rarity with behavioral influence.

---

# Causal Influence

The causal influence of an agent is defined as

\[
\Phi
=
D_{\mathrm{KL}}
\left(
P(X|\mathrm{agent})
\parallel
P(X|\neg\mathrm{agent})
\right)
\]

where

- \(D_{\mathrm{KL}}\) is the Kullback–Leibler divergence,
- \(P(X|\mathrm{agent})\) is the probability distribution over outcomes with the agent,
- \(P(X|\neg\mathrm{agent})\) is the corresponding counterfactual distribution.

The quantity

\[
\Phi
\]

measures how much the existence of the agent changes the future distribution of states.

Large values correspond to agents that significantly alter future outcomes.

---

# Environmental Differences

Let

\[
\Delta(x_1,x_2)
\]

represent the difference between two environmental states.

A detectable distinction exists whenever

\[
\Delta(x_1,x_2)\neq0.
\]

These differences constitute the raw input to the Adaptive Metric Compiler.

Most differences are expected to possess negligible causal significance.

Only a small subset meaningfully changes future behavior.

---

# Definition of Causal Mass

AMP defines the causal mass of an environmental difference as

\[
\mathcal M_C
=
\int_{\Omega}
\left|
\frac{\partial A}{\partial\Delta}
\right|
\,
(-\log_2 p(\Delta))
\,d\Omega
\]

where

- \(A\) denotes future action,
- \(p(\Delta)\) is the probability of observing the difference,
- \(\Omega\) is the observation space.

This expression combines two independent quantities.

The first,

\[
\left|
\frac{\partial A}{\partial\Delta}
\right|,
\]

measures how strongly future action changes in response to the difference.

The second,

\[
-\log_2 p(\Delta),
\]

measures informational surprise.

Their product defines the total computational importance assigned to the observation.

---

# Interpretation

High causal mass occurs when a difference is

- behaviorally important,
- informative,
- predictive of future consequences.

Low causal mass occurs when a difference is

- redundant,
- irrelevant,
- unable to influence future computation.

The framework therefore distinguishes between **information** and **computational relevance**.

---

# Relationship to Information Theory

Shannon information measures uncertainty reduction.

\[
I(x)
=
-\log_2P(x)
\]

Causal Mass instead measures computational importance.

A highly informative observation is not necessarily behaviorally significant.

Likewise, a behaviorally significant observation may contain relatively little Shannon information.

AMP proposes that intelligent systems prioritize the latter.

---

# Relationship to Attention

Causal Mass is not itself attention.

Instead, it provides the input to the salience computation.

The computational pipeline is

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
```

Only differences with sufficient causal mass are propagated into later stages of the compiler.

---

# Properties

An effective causal-mass measure should satisfy several desirable properties.

## Behavioral Sensitivity

Differences that substantially alter future action should receive larger values.

---

## Information Weighting

Rare observations should contribute more than common observations, all else being equal.

---

## Context Dependence

The same observation may possess different causal mass for different agents, tasks, or environments.

Causal significance is therefore relational rather than absolute.

---

## Scale Independence

The framework is intended to apply across multiple scales, including

- sensory processing,
- concept formation,
- scientific discovery,
- machine learning,
- planning,
- adaptive control.

---

# Role Within AMP

Causal Mass is the first computational filter in the Adaptive Metric Compiler.

It determines which environmental differences are worth allocating computational resources toward.

Subsequent stages of the framework transform these weighted differences into

- salience,
- computational allocation,
- internal metrics,
- metric evaluation,
- recursive metric discovery.

Without Causal Mass, every observable difference would compete equally for computation.

The framework instead proposes that intelligence begins by estimating **which differences matter most**.
