## Claim

**Theorem 1.** Let $\alpha = D_{TV}^{\max}(\pi_{\mathrm{old}}, \pi_{\mathrm{new}}) = \max_s D_{TV}(\pi_{\mathrm{old}}(\cdot|s) \| \pi_{\mathrm{new}}(\cdot|s))$. Then:

$$\eta(\pi_{\mathrm{new}}) \geq L_{\pi_{\mathrm{old}}}(\pi_{\mathrm{new}}) - \frac{4\epsilon\gamma}{(1-\gamma)^2}\alpha^2$$

where $\epsilon = \max_{s,a} |A_\pi(s,a)|$.

This generalizes the conservative policy iteration bound from mixture policies to **arbitrary stochastic policies**, with a constant factor of 4 instead of 2 (due to the more general setting).