## Claim

Two sampling schemes are proposed to estimate the surrogate objective and KL constraint:

1. **Single Path**: Collect trajectories by sampling $s_0 \sim \rho_0$, then running the current policy $\pi_{\theta_{\mathrm{old}}}$. Estimate $Q_\pi(s,a)$ via discounted sums of rewards along each trajectory: $\hat{Q}(s_t, a_t) = \sum_{t'=t}^{\infty} \gamma^{t'-t} r(s_{t'})$.

2. **Vine**: Sample states $s_1, \ldots, s_N$ from trajectory rollouts, then for each state $s_n$ and a set of actions $a_k \sim q(\cdot | s_n)$, perform short rollouts with **common random numbers** (CRN) to estimate $\hat{Q}(s_n, a_k)$. CRN uses the same random seed for rollouts from the same state, dramatically reducing variance.

The importance-sampled surrogate objective is:

$$L_{\theta_{\mathrm{old}}}(\theta) = \frac{1}{|\mathcal{S}|} \sum_{s_n} \frac{1}{|\mathcal{A}_n|} \sum_{a \in \mathcal{A}_n} \frac{\pi_\theta(a|s_n)}{q(a|s_n)} \hat{Q}(s_n, a)$$