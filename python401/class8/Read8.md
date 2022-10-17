# Data Analysis with Pandas
  ### import Pandas 
  ```python
         import numpy as np
         import pandas as pd
  
  ```
  
  ### Object creation
   1. Creating a Series by passing a list of values, letting pandas create a default integer index
   2. Creating a DataFrame by passing a NumPy array, with a datetime index using date_range() and labeled columns
   3. Creating a DataFrame by passing a dictionary of objects that can be converted into a series-like structure
   
  ### Viewing data
   1. Use DataFrame.head() and DataFrame.tail() to view the top and bottom rows of the frame respectively
   2. describe() shows a quick statistic summary of your data:
   3. DataFrame.sort_values() sorts by values:

  ### Selection
  ##### getting 
   1. Selecting via [] (__getitem__), which slices the rows:
   2. Selection by label ```df.loc[dates[0]]```
      - howing label slicing, both endpoints are included```df.loc["20130102":"20130104", ["A", "B"]]```
   3. Selection by position ex  ```df.iloc[3]``` ```df.iloc[3:5, 0:2]``` ``` df.iloc[[1, 2, 4], [0, 2]]```
   4. Boolean indexing ex ``` df[df["A"] > 0]``` ```df[df > 0]```
   
  ##### Setting 
  1. Setting a new column automatically aligns the data by the indexes
   ```  s1 = pd.Series([1, 2, 3, 4, 5, 6], index=pd.date_range("20130102", periods=6))```
  2. Setting values by label ```df.at[dates[0], "A"] = 0```
  3. Setting values by position: ```In [49]: df.iat[0, 1] = 0```
  


         


