## Claim

The coupling-based proof of Theorem 1 (Appendix A) constructs an $\alpha$-coupled policy pair $(\pi, \tilde{\pi})$ where at each state $s$, actions $(a, \tilde{a})$ are drawn jointly such that $P(a \neq \tilde{a} | s) = \alpha$. Two key lemmas are used:

- **Lemma 2**: For the expected advantage $\bar{A}(s) = \mathbb{E}_{\tilde{a} \sim \tilde{\pi}}[A_\pi(s, \tilde{a})]$, the bound $|\bar{A}(s)| \leq 2\alpha \max_{s,a} |A_\pi(s,a)| = 2\alpha\epsilon$ holds.
- **Lemma 3**: At each timestep, the expected advantage difference between coupled and uncoupled trajectories is bounded.

Summing over the infinite horizon yields:

$$\left|\eta(\tilde{\pi}) - L_\pi(\tilde{\pi})\right| \leq \frac{4\alpha^2 \gamma \epsilon}{(1-\gamma)^2}$$