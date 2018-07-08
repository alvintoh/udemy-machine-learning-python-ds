# 17. Feature Scaling

## THE IMPORTANCE OF FEATURE SCALING

### Activity
* Looking at the Data.csv dataset, you will realise the variables are not on the same scale because the age are going from 27 to 50.
* And the salaries are going from 40k to like 90k
* The age and salaries variable do not have the same scales, so this will call some issues in your machine learning models
* This is because the a lot of the machine learning models are based on what is called the Euclidean Distance
* The Euclidean Distance will be dominated by the Salary values further expended by their square values because it is much larger than the Age values
* So we need to ensure the values are in the same range

### Feature Scaling
* There are several ways of scaling your data.
* One method is Standardisation which means that for each observaton and each feature, you withdraw the mean value of all the values of the feature and you divide it by the standard deviation
* Another method is Normalisation, which means you subtract your observation feature X by the minimum value of all the future values and you divide it by the difference between the maximum of your future values and the minimum of your future values.
* Normalisation is putting the values in the same range, so that no variable is dominated by the other.

### Feature Scaling in Python
```
	# Feature Scaling
	from sklearn.preprocessing import StandardScaler
	sc_X = StandardScaler()
	X_train = sc_X.fit_transform(X_train)
	X_test = sc_X.transform(X_test)
```
* So it really depends on the context, you need to scale the variables
* It depends on how much you want to keep interpretation in your models.
* If we scale the intepretation for Country, we will lose the interpretation to know which observations belongs to which country etc.
* Double click on X_train and X_test to view that dataset.
* We will also need to do Feature Scaling for some other cases like Decision Trees.
* We do not need to apply Feature Scaling to categorical variable for Y for this case.

### Feature Scaling in R
```
	# Feature Scaling
	training_set[, 2:3] = scale(training_se[, 2:3])
	test_set[, 2:3] = scale(test_set[, 2:3])
```
* A factor in R is not a numeric number
* You can view the scale variables in Data