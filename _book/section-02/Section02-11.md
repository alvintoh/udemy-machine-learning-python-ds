# 11. Importing the Dataset

## IMPORTING THE DATASET

### Spyder IDE Activity in Python
* Ensure that your dataset resides where your python file is.
* So inside Spyder IDE, press on file explorer on the right side
* Navigate to the folder that contains Data.csv
* For Mac users, after navigating to the correct directory, you have an option on the right hand side to set that as working directory.
* For Windows users, just ensure that you import the correct data set from your woking Python file location.
* If you press F5, you will set your working directory while running the Python file at the same time.

```
	#Importing the Dataset
	dataset = pd.read_csv("Data.csv")
```
* If you press Ctrl and Enter, on that specific line, if there is an output of dataset = pd.read_csv("Data.csv") on IPython console, it means the Dataset is successfully imported.
* Press on variable explorer and double click on the Dataset to view the full set of data
* On Dataset, the index starts from 0.

### Changing the format of the Salary Column
* To change the decimal place of values of salary to display no decimal place after the 0, and the value to a Float.
* Press on format inside the view Dataset. and input this,
```
	%.of
```
* In Machine Learning, in a Dataset we need to distinguish the matrix of features and the independent variable vector.

### Creating a matrix of 3 Independent Variables
* So right now, we are going to create a matrix of the three independent variables.
```
	X = dataset.iloc[:, :-1].values
```
* : means that we take all the lines, because whats on the left means the lines which is the rows of the Dataset
* Whats on the right of the comma, means the other columns
* :-1 means we take all of the columns except the last one
* .values means that we want to take all the values and that just the Python syntax and how it works
* Select the line and execute
* If you type X in the IPython console, you should see that we have our data from the first three columns

### Creating the Dependent Variable Vector
```
	Y = dataset.iloc[:, 3].values
```
* The index 3 represents the last column of Purchased for Dependent Variable

### Importing the Dataset in Rs
* To set the working directory in RStudio, click on Browse on Files, and click on ... to go to your working directory
* Click on More, and select Set As Working Directory
```
	# Data Preprocessing

	# Importing the dataset
	dataset = read.csv("Data.csv")
```
* Press Ctrl enter to execute and double click on the Data, and you should display the dataset.
* For R, the first observations start at 1 here and end at 10.