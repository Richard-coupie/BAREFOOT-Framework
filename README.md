# BAREFOOT (Batch Reification/Fusion Optimization) Framework
## Batch Bayesian Optimization Implemented within a Model Reification and Fusion Framework

The code in this repository can be used to run a batch bayesian optimization routine. Two test cases are included in this repository.

To run the code, the following python packages will need to be installed:
- pandas
- numpy
- scipy
- pyDOE
- scikit-learn
- george
- matplotlib

Both versions of the code take command line inputs to specify the different limits that will be used in the code, these are input as an ordered list:
1. GP Kernel to be used ('M52', 'M32', 'SE')
2. The total number of iterations to completed
3. The number of test samples to use (these are found using a latin-hypercube sampling of the design space
4. The number of hyperparameter sets to use in the batch optimization procedure
5. The number of clusters (medoids) to partition the data into
6. The number of iterations to run before calling the truth model
7. The total budget that can be expended before stopping the code
8. The budget that must be expended before calling the truth model

The code is set up to run an example problem if no additional inputs are entered. This example code will run for two iterations. The example code is equivalent to entering the following run command:

```
python CC_CC_optimization.py M52 2 10 50 2 1 14000 1000
```



### Test Case 1 (Mechanical Models):
This test case uses three reduced order micromechanical models for predicting the normalized strain hardening rate of a dual-phase steel. The Truth Model in this case is a Representative Volume Element (RVE) model for the mechanical response of a dual-phase steel.



### Test Case 2 (Three Hump Camel):
This test case uses the Three Hump Camel Test Function as the Truth Model. Several (up to 5) approximations of this function have been used as the reduced-order models. 


