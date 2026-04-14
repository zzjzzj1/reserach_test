## Evidence

Two independent proofs are provided in the appendix:

1. **Coupling argument** (Appendix A): Constructs an $\alpha$-coupled policy pair such that $P(a \neq \tilde{a} | s) \leq \alpha$. Using Lemma 2 ($|\bar{A}(s)| \leq 2\alpha \epsilon$) and Lemma 3 (per-timestep advantage bound), the proof sums over the time horizon to get $|\eta(\tilde{\pi}) - L_\pi(\tilde{\pi})| \leq \frac{4\alpha^2 \gamma \epsilon}{(1-\gamma)^2}$.

2. **Perturbation theory** (Appendix B): Uses resolvent operators $G = (1-\gamma P_\pi)^{-1}$ and $\tilde{G} = (1-\gamma P_{\tilde{\pi}})^{-1}$. Decomposes $\eta(\tilde{\pi}) - \eta(\pi)$ into a leading term equal to $L_\pi(\tilde{\pi}) - \eta(\pi)$ and an $O(\Delta^2)$ remainder bounded using $\ell_1$ operator norms.