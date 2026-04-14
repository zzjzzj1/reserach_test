## Claim

Using the relationship $D_{TV}(p \| q)^2 \leq D_{KL}(p \| q)$, Theorem 1 directly implies:

$$\eta(\tilde{\pi}) \geq L_\pi(\tilde{\pi}) - C \cdot D_{KL}^{\max}(\pi, \tilde{\pi})$$

where $C = \frac{4\epsilon\gamma}{(1-\gamma)^2}$ and $D_{KL}^{\max}(\pi, \tilde{\pi}) = \max_s D_{KL}(\pi(\cdot|s) \| \tilde{\pi}(\cdot|s))$.

This provides a lower bound on the true policy performance in terms of the surrogate objective and the maximum KL divergence between old and new policies.