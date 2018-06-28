# 13. Missing Data

## DEALING WITH THE PROBLEM OF MISSING DATA

### Activity
* As you can see in the Data.csv, there are two missing data.
* There is one missing data inside Age for Spain, and another missing data for Salary in Germany
* Well the first idea is to remove the lines of the observations where there is some missing data.
* But imagine if this dataset contains crucial information, it would be quite dangerous to remove an observation.
* Another idea is to take the mean of the columns, and replace the missing data with the mean

### Dealing with missing Data in Python
```
	# Taking care of missing Data
	from sklearn.preprocessing import Imputer
```
* From sklearn, it contains important libaries to preprocess any dataset
* Imputer will allow us to take care of any missing data

```
	imputer = Imputer.(missing_values = "NaN", strategy = "mean", axis = 0)
```
* Press Ctrl - i in Windows, and you can see the documentation associated with the function
* You can also go to help and just type in the object to get the documentation
* For the first value, we are going to input missing_values = "NaN"
* For the second value, the strategy would be to replace the missing value with the mean
* Axis will be equal to 0, as we want to take the mean of the column.

```
	imputer = imputer.fit(X[:, 1:3])
```
* To fit the imputer to X, we use the following method
* 1 represents the lowerbound column that is included and 3 represents the upperbound column that is excluded

```
	X[:, 1:3] = imputer.transform(X[:, 1:3])
```
* The method transform that is going to replace the missing data by the mean of the column
* Now select the block of code and Ctrl + i to run it, if there is output on the console, it means the code has run properly
* Input X on the console, and you should now see a complete data
* You can change the strategy of taking the mean to taking the median for some datasets to replace the missing values.

### Dealing with missing Data in R
```
	# Taking are of missing data
	dataset$Age = ifelse(is.na(dataset$Age), ave(dataset$Age, FUN = function(x) mean(x, na.rm = TRUE), dataset$Age)
```
* We check and replace missing data in dataset with the average of column age, if not we retain the value
* Ctrl enter and run it to see if all values in age are there now
* The dataset in Data tab, should now show the average age for the missing values in Age now

* Now lets do the same for salary
```
	dataset$Salary = ifelse(is.na(dataset$Salary), 
                     ave(dataset$Salary, FUN = function(x) mean(x, na.rm = TRUE)),
                     dataset$Salary)
```
* Run it and the dataset should have no missing values now