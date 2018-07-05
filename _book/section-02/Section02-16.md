# 16. Splitting the Dataset into the Training set and Test set

## MAKING THE MACHINE LEARNING MODELS

### Activity
* We are going to split the two data sets into training and test set.
* Machine learning means the machine is going to learn to do something from a data set.
* We are going to build our machine learning models on a data set but then we have to test on a new set which is going to be slightly different from the data set on which we build th machine learning model
* Test the performance on the test set shouldnt be that different from the performance from the training set

### Splitting the Datasets on Python
```
	# Splitting the dataset into the Training set and Test set
	import sklearn.cross_validation import train_test_split
	X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, random_state = 0)
```
* The better we learn the correlationship, the better we are at predicting the test set learned correctly from the training set.

### Splitting the Datasets on R
```
	# Splitting the data set into the Training set and Test set
	# install.packages('caTools')
	set.seed(123)
	split = sample.split(datasets$Purchased, SplitRatio = 0.8)
	training_set = subset(dataset, split == TRUE)
	test_set = subset(dataset, split == FALSE)
```
* Once you installed the caTools packages once, you can comment it because you do need to install it again
* You can check if caTools library in the Packages on the right hand side
* Select caTools package before running the code
* Now, you can view the training_set and the test_set which should show the respective number of observations