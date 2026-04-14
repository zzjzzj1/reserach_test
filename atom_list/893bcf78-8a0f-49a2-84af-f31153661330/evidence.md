## Evidence

The derivation follows immediately from Theorem 1 by substituting the Pinsker-type inequality $D_{TV}(p \| q)^2 \leq D_{KL}(p \| q)$ into the TV-divergence bound. Since $\alpha^2 = (D_{TV}^{\max})^2 \leq D_{KL}^{\max}$, the penalty coefficient $C$ remains unchanged. This KL-based formulation is more amenable to optimization since KL divergence is smooth and differentiable.