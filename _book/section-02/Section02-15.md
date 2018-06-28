# 15. WARNING - Update

### Instructor Notes
Dear students,

in the following tutorial, the first line of code we will type will be:

```
	from sklearn.cross_validation import train_test_split 
```
However the "cross_validation" name is now deprecated and was replaced by "model_selection" inside the new anaconda versions.

Therefore you might get a warning or even an error if you run this line of code above.

To avoid this, you just need to replace:
```
	from sklearn.cross_validation import train_test_split 
```
by
```
	from sklearn.model_selection import train_test_split 
```
and you will get no warning ;)

Hope you are having a great ML journey so far, I'll see you in the next tutorial.

Hadelin