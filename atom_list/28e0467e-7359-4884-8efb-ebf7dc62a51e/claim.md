## Claim

TRPO is closely related to the **natural policy gradient** method (Kakade, 2002). The natural gradient update corresponds to using a linear approximation to $L_{\theta_{\mathrm{old}}}(\theta)$ and a quadratic (second-order Taylor) approximation to the KL divergence constraint. In contrast:

- **Standard policy gradient** uses $L_{\theta_{\mathrm{old}}}$ linearized with an $\ell_2$ constraint on $\theta - \theta_{\mathrm{old}}$.
- **Natural policy gradient** uses $L_{\theta_{\mathrm{old}}}$ linearized with a KL divergence constraint.
- **TRPO** uses the full nonlinear $L_{\theta_{\mathrm{old}}}$ with a KL divergence constraint, enforced via line search.

The natural gradient update direction is $F^{-1}g$ where $F$ is the Fisher information matrix, identical to the TRPO search direction before rescaling.