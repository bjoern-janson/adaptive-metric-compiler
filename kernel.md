# Unified Adaptive Metric Compiler (AMP)

## Causal Mass

$$
\Phi = D_{\text{KL}}\big(P(X|\text{agent}) \parallel P(X|\neg\text{agent})\big)
$$

$$
\mathcal{M}_C = \int_{\Omega} \left| \frac{\partial A}{\partial \Delta} \right| \cdot (-\log_2 p(\Delta)) \, d\Omega
$$

$$
\Delta(x_1,x_2) \neq 0
$$

---

## Salience & Gating

$$
\chi(\Delta) = \rho = \sigma(\mathcal{M}_C - \theta)
$$

$$
\mathcal{B}(\rho) =
\begin{cases}
1 & \rho \ge \rho_{\text{crit}} \\
0 & \rho < \rho_{\text{crit}}
\end{cases}
$$

---

## Mapping Quality

$$
M_Q: E \longrightarrow A
$$

$$
Q_M = \frac{C \times T \times G_L \times K \times R_a \times I_c}{D}
$$

$$
\begin{array}{rll}
C &= \frac{\Delta H(\text{Search})}{I_{\text{stored}}} &
K &= -\frac{d \, D_{\text{KL}}(P_{\text{true}} \| P_{\text{model}})}{dt} \\

G_L &= \frac{\partial \Omega_{\text{viable}}}{\partial I_{\text{stored}}} &
R_a &= \frac{\min(\text{Scale},\text{Horizon})}{\max(\text{Scale},\text{Horizon})} \cdot \log_2(1+\mathcal{L}) \\

I_c &= \frac{\text{Preserved Invariants}}{\text{Relevant Structure}} &
D &= K(M_Q)
\end{array}
$$

---

## Discovery Operator & Metric

$$
D_\Omega: M_Q \longrightarrow M_Q'
$$

$$
D_M = \frac{\Delta \Omega_{\text{viable}}(M_Q \to M_Q')}{C_{\text{search}}(M_Q \to M_Q')}
$$

---

## Leverage

$$
L_M = \frac{\Delta \Omega_{\text{viable}} \times \Delta Q}{\Delta C_M}
$$

---

## Phase Transition

$$
\frac{\partial^2 G_B}{\partial I_c^2} \bigg|_{I_c = I_{\text{crit}}} \to \infty
\implies
M_Q \xrightarrow{D_\Omega} M_Q'
$$

---

## Kernel Sequence

$$
\boxed{
\Delta \longrightarrow \chi \longrightarrow \mathcal{B} \longrightarrow F \longrightarrow M_Q \longrightarrow Q_M \longrightarrow D_\Omega \longrightarrow M_Q'
}
$$

---

## Terminal Limits

$$
\boxed{
\lim_{K(M_Q) \to K(I_{\text{true}})}
\frac{\partial \Omega_{\text{viable}}}{\partial K(M_Q)}
\longrightarrow
\infty
}
$$

$$
\boxed{
\text{Intelligence} = \text{recursive execution of } D_\Omega
}
$$

$$
\boxed{
\text{Optimization: } \nabla Q_M(M_Q)
\qquad
\text{Discovery: } D_\Omega(M_Q)=M_Q'
}
$$
