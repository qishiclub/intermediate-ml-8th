![[Pasted image 20230105154825.png]]

## Cross-Validation Procedure
![[Pasted image 20221227174433.png]]
In general, we have $K$-fold cross-validation. As $K$ increases, the bias of the error estimation decreases while the variance of the error estimation increases.
* We only use $\frac{K-1}{K}$ of the data to fit the model each time, so the bias is large when $K$ is small. But this also depends on how much data we have. (See plot below. 5-fold cross validation, 50 observations vs 200 observations.)
![[Pasted image 20221227175025.png]]
* If $K$ is large (leave-one-out cross-validation in the extreme case), all experiments in cross-validation are pretty much the same (high overlap), so the variance is high.

Since we have $K$ experiments, can we estimate the standard error of the error estimation? Not really. It does not give good estimate of standard error if we do it naively due to the correlation in these experiments.

![[Pasted image 20221230181102.png]]


## Right vs Wrong
• Consider a simple classifier applied to some two-class data: 
1. Starting with 5000 predictors and 50 samples, find the 100 predictors having the largest correlation with the class labels. 
2. We then apply a classifier such as logistic regression, using only these 100 predictors.

* **Wrong**: Apply cross-validation in step 2. 
* **Right**: Apply cross-validation to steps 1 and 2.