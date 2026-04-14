## Claim

**Algorithm 1** defines an iterative policy optimization procedure with guaranteed monotonic improvement. At each iteration $i$, the algorithm solves:

$$\pi_{i+1} = \arg\max_\pi \left[ L_{\pi_i}(\pi) - C \cdot D_{KL}^{\max}(\pi_i, \pi) \right]$$

where $C = \frac{4\epsilon\gamma}{(1-\gamma)^2}$. This is a minorization-maximization (MM) procedure: the penalized surrogate $M_i(\pi) = L_{\pi_i}(\pi) - C \cdot D_{KL}^{\max}(\pi_i, \pi)$ minorizes $\eta(\pi)$, and:

$$\eta(\pi_{i+1}) - \eta(\pi_i) \geq M_i(\pi_{i+1}) - M_i(\pi_i) \geq 0$$

Thus every iteration produces a policy at least as good as the previous one.