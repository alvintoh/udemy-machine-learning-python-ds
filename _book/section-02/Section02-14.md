# 14. Categorical Data

## HOW TO ENCODE CATEGORICAL DATA

### Activity
* Looking at the Data.csv, we see that we have two categorical variables which are Country and Purchased
* Their values contain categories
* So we need to encode the text we have over here into numbers

### Encoding categorical data in Python
```
	# Encoding categorical data
	from sklearn.preprocessing import LabelEncoder
	labelEncoder_X = LabelEncoder()
	X[:, 0] = labelEncoder_X.fit_transform(X[:, 0])
```
* We use the another library LabelEncoder from sklearn and create a class of it
* We then fit and transform the country column
* All of the countries are now encoded in numbers instead
* Now instead replace X[:, 0] country column with the labelEncoder_X.fit_transform(X[:, 0]) to show the countries in text instead
* If you print X on Ipython console, now X contains all number values
* The problem is that you need to somehow make the encoded values make sense
* So we have to prevent the machine learning equations from thinking that Germany is greater than France, and Spain is greater than Germany
* To prevent this we are going to the dummy variables

### Dummy Encoding in Python
* Instead of having one column for Country, we are going to have three columns equal to the number of categories countries
* So if the country is France, the France column is going to be one, else zero and likewise for the rest of the columns

```
	from sklearn.preprocessing import LabelEncoder, OneHotEncoder

	onehotencoder = OneHotEncoder(categorical_features = [0])
```
* We are going to use OneHotEncoder class to do this, so inspect this class documentation
* Look at the categorical features, and we need to specify the column of the categorical data which is 0

```
	X = onehotencoder.fit_transform(X).toarray()
```			
* The following method will encode the 0 column of X
* Ctrl Enter to see if the code can run, and print X in Ipython Console
* If you look at it in variable explorer, you can now see the values being encoded in 0s and 1s for Countries column
* Change the formatting of decimas to %.0f to no decimals if your data cannot be seen easily
* Now if you open the dataset, you can see the Countries column being replaced in X by 3 columns

```
	labelEncoder_Y = LabelEncoder()
	Y = labelEncoder_Y.fit_transform(Y)
```
* So now we are going to do the same thing for Y, for Purchased column
* Since there's only 2 categories we do not need to onehotencoder to encode more columns

### Encoding categorical data in R
```
	# Encoding categorical data
	dataset$Country = factor(dataset$Country, levels = c('France', 'Spain', 'Germany'), labels = c(1, 2, 3))
```
* We use a factor method to specify a vector, and c is a vector in R and we creating a vector of 3 elements of Countries
* Labels are used to represent the number associate with that country
* Execute the code and see the difference in output for Data
* Do the same for the Purchased column and you should see the Data being reflected differently for categorical columns of Country and Purchased.