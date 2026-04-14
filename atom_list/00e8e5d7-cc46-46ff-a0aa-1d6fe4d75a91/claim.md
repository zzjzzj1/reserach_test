## Claim

TRPO is evaluated on three continuous control locomotion tasks in MuJoCo:

- **Swimmer** (10D state, 2D action)
- **Hopper** (12D state, 3D action)
- **Walker** (18D state, 6D action)

Neural network policies with 2 hidden layers of 30–50 units are used. TRPO with $\delta = 0.01$ and $\gamma = 0.99$ (both single path and vine variants) solves all three tasks and significantly outperforms baselines including natural gradient, cross-entropy method (CEM), covariance matrix adaptation (CMA), and reward-weighted regression (RWR).
123321312fuckerlll