## Claim

The surrogate (local approximation) objective $L_\pi$ is defined by replacing $\rho_{\tilde{\pi}}$ with $\rho_\pi$ in the performance identity (Equation 3):

$$L_\pi(\tilde{\pi}) = \eta(\pi) + \sum_s \rho_\pi(s) \sum_a \tilde{\pi}(a|s) A_\pi(s,a)$$

This surrogate matches the true objective $\eta$ to first order around the current policy parameters $\theta_0$ (Equation 4):

$$L_{\pi_{\theta_0}}(\pi_{\theta_0}) = \eta(\pi_{\theta_0}), \quad \nabla_\theta L_{\pi_{\theta_0}}(\pi_\theta)\Big|_{\theta=\theta_0} = \nabla_\theta \eta(\pi_\theta)\Big|_{\theta=\theta_0}$$