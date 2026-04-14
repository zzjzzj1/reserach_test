## Claim

Instead of using the KL penalty with a large coefficient $C$, the paper proposes a **trust region** constrained optimization:

$$\max_\theta \; L_{\theta_{\mathrm{old}}}(\theta) \quad \text{subject to} \quad D_{KL}^{\max}(\theta_{\mathrm{old}}, \theta) \leq \delta$$

A practical relaxation replaces the worst-case (max) KL constraint with an **average KL** constraint:

$$\max_\theta \; L_{\theta_{\mathrm{old}}}(\theta) \quad \text{subject to} \quad \bar{D}_{KL}^{\rho_{\theta_{\mathrm{old}}}}(\theta_{\mathrm{old}}, \theta) \leq \delta$$

where $\bar{D}_{KL}^{\rho}(\theta_1, \theta_2) = \mathbb{E}_{s \sim \rho}[D_{KL}(\pi_{\theta_1}(\cdot|s) \| \pi_{\theta_2}(\cdot|s))]$. This heuristic uses a fixed $\delta$ (e.g., $\delta = 0.01$) chosen by the user.