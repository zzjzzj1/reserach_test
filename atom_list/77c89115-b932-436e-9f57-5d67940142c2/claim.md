## Claim

The expected return of a new policy $\tilde{\pi}$ can be expressed exactly in terms of the advantage function of the old policy $\pi$ (Equation 1):

$$\eta(\tilde{\pi}) = \eta(\pi) + \mathbb{E}_{s_0, a_0, \ldots \sim \tilde{\pi}}\left[\sum_{t=0}^{\infty} \gamma^t A_\pi(s_t, a_t)\right]$$

This can equivalently be written as a sum over states weighted by the discounted visitation frequency of $\tilde{\pi}$ (Equation 2):

$$\eta(\tilde{\pi}) = \eta(\pi) + \sum_s \rho_{\tilde{\pi}}(s) \sum_a \tilde{\pi}(a|s) A_\pi(s,a)$$