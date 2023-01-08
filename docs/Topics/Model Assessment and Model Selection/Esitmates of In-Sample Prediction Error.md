Instead of extra-sample error like $Err_{\mathcal{T}}$, we consider in-sample error
$$Err_{in} = \frac{1}{N} \sum_{i=1}^{N}E_{Y^0}[L(Y^{0}_{i} , \hat{f}(x_{i}))|\mathcal{T}]$$
where $Y^{0}_{i}$ is new response value at $x_{i}$.

Intuitively, we can see that $\overline{err}$ underestimates $Err_{in}$. Homework (Ex 7.4) will ask you to show that
$$E_{y}(Err_{in}) = E_{y}(\overline{err})+\frac{2}{N}\sum_{i=1}^{N}Cov(\hat{y_{i}}, y_{i})$$
in some special case.

$\sum_{i=1}^{N}Cov(\hat{y_{i}}, y_{i})=d \sigma_{\epsilon}^2$ if $\hat{y}_{i}$ is obtained by a linear fit with $d$ inputs.

We can use $C_{p}$ statistic to approximate the in-sample error for model selection:
$$C_{p} = \overline{err} + 2 \frac{d}{N} \hat{\sigma}_{\epsilon}^2.$$

From information theory perspective (minimize the KL divergence between the model distribution and the true distribution), we can get similar but more general formula:
$$-2E[\log Pr_{\hat{\theta}}(Y)] \approx -\frac{2}{N}E[log lik]+2 \frac{d}{N},$$
where $loglik = \sum_{i=1}^{N}\log Pr_{\hat{\theta}}(y_{i})$.

Akaike information criterion (AIC):
$$AIC = -\frac{2}{N} loglik + 2 \frac{d}{N}.$$
