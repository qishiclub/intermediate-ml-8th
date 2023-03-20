https://openai.com/blog/deep-double-descent/

![[Pasted image 20230118172632.png]]
When the models are large enough to fit the training set, continuing increasing the model complexity can lead to a second decline of the testing error. (e.g. Error peaks when number of parameters is about equal to the sample size for linear regression.) 

Some theoretical analysis on simple models (e.g. see Two Models of Double Descent for Weak Features)

![[Pasted image 20230118173057.png]]
![[Pasted image 20230118173824.png]]
Since early stopping has the effect of regularization (therefore has the effect of lowering the model complexity), the double descent also appears as training time increases for large model. Be aware if you use early stopping when training a DL model.

![[Pasted image 20230118174606.png]]
More data sometimes hurts if you model is not large enough.