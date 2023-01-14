For a set of candidate models $\mathcal{M}_{m}$,
$$Pr(\mathcal{M}_{m}|Z) \propto Pr(\mathcal{M}_{m}) Pr(Z|\mathcal{M}_{m}).$$
Assuming the prior over all models are uniform, we only need to compare
$$Pr(Z|\mathcal{M}_{m}) \propto \int Pr(Z|\theta_{m}, \mathcal{M}_{m}) Pr(\theta_{m}|\mathcal{M}_{m})d\theta_{m}$$

Laplace approximation to the integral followed by some other simplifications (Ripley, 1996, page 64) to the above equation gives

$$\log Pr(Z|\mathcal{M}_{m}) = \log Pr(Z|\hat{\theta}_{m}, \mathcal{M}_{m}) - \frac{d_{m}}{2} \log N + O(1).$$

Bayesian information criterion (BIC):
$$BIC = -2 loglik + (\log N) d.$$