## Claim

The practical TRPO algorithm repeats three steps:

1. **Collect data**: Use single path or vine to gather state-action pairs with estimated Q-values.
2. **Construct objective**: Build the estimated surrogate objective $L_{\theta_{\mathrm{old}}}(\theta)$ and KL constraint $\bar{D}_{KL}(\theta_{\mathrm{old}}, \theta) \leq \delta$.
3. **Approximately solve**: Use conjugate gradient (CG) to compute the search direction $s \approx A^{-1}g$ where $A$ is the Fisher information matrix and $g$ is the policy gradient, then take a step of size $\beta = \sqrt{2\delta / (s^T A s)}$ with backtracking line search.

The Fisher information matrix is computed analytically as the Hessian of the KL divergence (rather than estimated empirically), and Fisher-vector products $Av$ are computed efficiently without forming the full matrix, enabling scalability to large parameter spaces.