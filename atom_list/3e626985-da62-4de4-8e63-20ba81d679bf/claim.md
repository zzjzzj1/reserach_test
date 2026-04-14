## Claim

Kakade & Langford (2002) proved a performance lower bound for **mixture policies** of the form $\pi_{\mathrm{new}} = (1-\alpha)\pi_{\mathrm{old}} + \alpha \pi'$ (Equation 6):

$$\eta(\pi_{\mathrm{new}}) \geq L_{\pi_{\mathrm{old}}}(\pi_{\mathrm{new}}) - \frac{2\epsilon\gamma}{(1-\gamma)^2}\alpha^2$$

where $\epsilon = \max_s \left|\mathbb{E}_{a \sim \pi'(a|s)}\left[A_\pi(s,a)\right]\right|$. This bound applies only to mixture policies, not general stochastic policies.