# 5.9 Mathematical Functions of NumPy

## Universal Functions (ufunc)
Operate Element-wise on array, producing a new array
* np.sqrt()
* np.floor() - Largest integer valie of every element in array
* cos - cosine
* exp -exponentiation


## Shape Manipulation
* Flatten
    * `arr.ravel()` -Doesn't affect original array
* Resize
    * `arr.resize(3,4)` - **Affects Original Array**
* Reshape
    * `arr.reshape(3,4)` - Doesn't affect original array
* Stack - Combines arrays
    * `np.hstack((new_cyclist_trials,new_cyclist_trials2))`
* Split
    * `np.hsplit(arr,2)`-splits into 2 arrays

## Broadcasting
* Can broadcast either a scalar with an array or two arrays of same dimensions

## Linear Algebra Functions
* `arr.transpose()` -interchanges rows and cols
* `arr.trace()` - sums diagonal
* `np.linalg.inv(arr)` - square array inverse