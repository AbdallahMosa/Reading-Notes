# Linear Regressions
## what is Linear Regressions ?
  - Linear regression is a statistical method for modeling relationships between a dependent variable with a given set of independent variables.
## Python scikit-Learn 
  - The package scikit-learn is a widely used Python library for machine learning, built on top of NumPy and some other packages. It provides the means for preprocessing data, reducing dimensionality, implementing regression, classifying, clustering, and more. Like NumPy, scikit-learn is also open-source.
 
## 1-  Simple Linear Regression With scikit-learn
  - Step 1: Import packages and classes 
 
    ``` python 
         import numpy as np
         from sklearn.linear_model import LinearRegression 
  
  
 - Step 2: Provide data
      ``` python 
      >>> x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
      >>> y = np.array([5, 20, 14, 32, 22, 38])
    
 - Step 3: Create a model and fit it 
        ``` python 
             model = LinearRegression() 
     - This statement creates the variable model as an instance of LinearRegression. You can provide several optional parameters to LinearRegression:
     1. fit_intercept is a Boolean that, if True, decides to calculate the intercept 𝑏₀ or, if False, considers it equal to zero. It defaults to True.
     2. normalize is a Boolean that, if True, decides to normalize the input variables. It defaults to False, in which case it doesn’t normalize the input variables.
     3. copy_X is a Boolean that decides whether to copy (True) or overwrite the input variables (False). It’s True by default.
     4. n_jobs is either an integer or None. It represents the number of jobs used in parallel computation. It defaults to None, which usually means one job. -1 means to use all available processors.
     
          ``` python 
          >>> model = LinearRegression().fit(x, y)
 
 
 - Step 4: Get results 

        ```  
        r_sq = model.score(x, y)
         print(f"coefficient of determination: {r_sq}")
        # coefficient of determination: 0.7158756137479542
   
   
 - Step 5: Predict response
      
      
                  ```
                            >>> y_pred = model.intercept_ + model.coef_ * x
                            >>> print(f"predicted response:\n{y_pred}")
                            predicted response:
                            [[ 8.33333333]
                             [13.73333333]
                             [19.13333333]
                             [24.53333333]
                             [29.93333333]
                             [35.33333333]]



 ### 2- Multiple Linear Regression With scikit-learn
 ### 3-  Polynomial Regression With scikit-learn
 ### 4- Advanced Linear Regression With statsmodels

 ## Linear regression is implemented with the following:
 
  1. scikit-learn
  2. statsmodels

  


