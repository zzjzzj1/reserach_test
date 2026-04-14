# Research Background

## Domain

This research project focuses on **policy optimization in reinforcement learning (RL)**, specifically on methods that provide theoretical guarantees of monotonic policy improvement while remaining practical for large-scale problems with high-dimensional policy parameterizations (e.g., neural networks).

## Context

Policy optimization in RL can be broadly categorized into three families:

1. **Policy iteration methods**: Alternate between estimating the value function under the current policy and improving the policy.
2. **Policy gradient methods**: Use estimators of the gradient of expected return obtained from sampled trajectories.
3. **Derivative-free optimization methods**: Treat the expected return as a black-box function (e.g., Cross-Entropy Method (CEM), Covariance Matrix Adaptation (CMA)).

Despite the better sample complexity guarantees of gradient-based methods, derivative-free methods have often been competitive or superior in practice on benchmarks such as Tetris and locomotion tasks with low-dimensional hand-engineered policies. Extending the success of gradient-based optimization (widely demonstrated in supervised learning) to RL with large, general-purpose policy representations (e.g., neural networks) is an important open challenge.

## Key Prior Work

- **Kakade & Langford (2002)**: Introduced *conservative policy iteration*, which provides explicit lower bounds on policy improvement for mixture policy updates. The improvement bound involves a surrogate objective $L_\pi(\tilde{\pi})$ penalized by a term proportional to $\alpha^2$, where $\alpha$ is the mixture weight.
- **Kakade (2002)**: Proposed the *natural policy gradient*, which uses the Fisher information matrix to precondition the gradient, yielding updates invariant to policy parameterization.
- **Peters & Schaal (2008)**: Developed natural actor-critic methods connecting policy gradient and natural gradient approaches.
- **Peters et al. (2010)**: Proposed Relative Entropy Policy Search (REPS), which constrains the state-action marginals $p(s,a)$ rather than conditionals $p(a|s)$.

## Mathematical Setting

The underlying framework is an infinite-horizon discounted Markov Decision Process (MDP) defined by the tuple $(S, A, P, r, \rho_0, \gamma)$, where:

- $S$: state space
- $A$: action space
- $P: S \times A \times S \to \mathbb{R}$: transition probability distribution
- $r: S \to \mathbb{R}$: reward function
- $\rho_0: S \to \mathbb{R}$: initial state distribution
- $\gamma \in (0,1)$: discount factor

Key quantities include:
- Expected discounted return: $\eta(\pi) = \mathbb{E}_{s_0, a_0, \ldots}\left[\sum_{t=0}^{\infty} \gamma^t r(s_t)\right]$
- State-action value function: $Q_\pi(s,a)$
- Value function: $V_\pi(s)$
- Advantage function: $A_\pi(s,a) = Q_\pi(s,a) - V_\pi(s)$
- Discounted visitation frequencies: $\rho_\pi(s) = \sum_{t=0}^{\infty} \gamma^t P(s_t = s | \pi)$
