# Research Goal

## Primary Objective

Develop and analyze a practical, scalable policy optimization algorithm — **Trust Region Policy Optimization (TRPO)** — that provides theoretical guarantees of monotonic improvement for general stochastic policies, while being effective for optimizing large nonlinear policies such as neural networks.

## Specific Goals

1. **Theoretical Foundation**: Prove that minimizing a surrogate objective function with a penalty (or constraint) on KL divergence guarantees monotonic policy improvement with non-trivial step sizes, extending the conservative policy iteration result of Kakade & Langford (2002) from mixture policies to general stochastic policies.

2. **Practical Algorithm Design**: Derive a practical algorithm (TRPO) from the theoretical foundations by:
   - Replacing the penalty on max KL divergence $D_{\mathrm{KL}}^{\max}(\pi, \tilde{\pi})$ with a constraint on average KL divergence
   - Using sample-based estimation of the surrogate objective and constraint via two schemes: *single path* and *vine*
   - Solving the constrained optimization approximately via conjugate gradient and line search

3. **Empirical Validation**: Demonstrate TRPO's effectiveness on:
   - Continuous control tasks: simulated robotic locomotion (swimming, hopping, walking) using neural network policies in MuJoCo
   - Discrete control tasks: Atari game playing from raw pixel images using convolutional neural networks

4. **Unifying Perspective**: Show that policy gradient methods and policy iteration methods are special limiting cases of the trust region optimization framework, providing a unifying theoretical perspective on policy update schemes.

## Key Claims to Verify

- The policy improvement bound $\eta(\tilde{\pi}) \geq L_\pi(\tilde{\pi}) - C \cdot D_{\mathrm{KL}}^{\max}(\pi, \tilde{\pi})$ holds for general stochastic policies (Theorem 1 and its KL divergence corollary).
- The MM (minorization-maximization) algorithm derived from this bound generates a monotonically improving sequence of policies.
- The practical TRPO algorithm (with average KL constraint) empirically preserves near-monotonic improvement.
- TRPO outperforms or matches natural policy gradient, CEM, CMA, and other baselines on locomotion and Atari benchmarks.
