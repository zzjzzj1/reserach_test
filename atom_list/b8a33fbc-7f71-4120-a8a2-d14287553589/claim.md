## Claim

The perturbation-theory proof (Appendix B) provides an alternative derivation of Theorem 1 using operator methods. It defines the resolvent operators $G = (1 - \gamma P_\pi)^{-1}$ and $\tilde{G} = (1 - \gamma P_{\tilde{\pi}})^{-1}$, where $P_\pi$ is the state transition operator under policy $\pi$. Writing $\Delta = P_{\tilde{\pi}} - P_\pi$, the decomposition:

$$\eta(\tilde{\pi}) - \eta(\pi) = \underbrace{\gamma \rho_0^T G \Delta \tilde{G} r}_{= L_\pi(\tilde{\pi}) - \eta(\pi)} + O(\|\Delta\|^2)$$

The remainder is bounded using $\ell_1$ operator norms, yielding the same $\frac{4\epsilon\gamma}{(1-\gamma)^2}\alpha^2$ bound as the coupling proof.