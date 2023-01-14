![[Pasted image 20221228121554.png]]
![[Pasted image 20221228121656.png]]
$Pr\{\text{observation }i \in \text{bootstrap sample b}\} = 1- \left( 1- \frac{1}{N} \right)^{N} \approx 1-\frac{1}{e}=0.632$

How can we apply the bootstrap to estimate prediction error?
* One approach would be to fit the model in question on a set of bootstrap samples, and then keep track of how well it predicts the original training set. This however, **underestimates** the error due to overlapping.
* For each observation, we only keep track of predictions from bootstrap samples not containing that observation. The leave-one-out bootstrap estimate of prediction error is defined by
	$$ \widehat{Err}^{(1)} = \frac{1}{N} \sum^{N}_{i=1} \frac{1}{|C^{-i}|} \sum_{b\in C^{-i}} L(y_{i}, \hat{f}^{*b}(x_{i})).$$
The average number of distinct observations in each boot- strap sample is about 0.632 * N , so its bias will roughly behave like that of twofold cross-validation. Thus if the learning curve has considerable slope at sample size N/2, the leave-one out bootstrap will be biased upward as an estimate of the true error.

The “.632 estimator” is designed to alleviate this bias. It is defined by
$$ \widehat{Err}^{(.632)} =.368*\overline{err} + .632* \widehat{Err}^{(1)}.$$

It gets complicated... Keep it simple and use CV.