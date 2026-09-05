# maximielfrancisco-pixel_Francisco-Maximiel-Anton-V.--PA-2-
------

### 1) Reproducible Normalization Problem - Creates a reproducible random 5x5 array and normalizes its values.
```python

import numpy as np

# It will generate a reproducible random 5x5 array
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
X

# Get the mean of X
xbar = np.mean(X)
xbar

# Get the standard deviation of X
stndrdev = np.std(X)
stndrdev

# Normalize the array
X_normalized = (X - xbar)/stndrdev
X_normalized

# Check the mean of the normalized array
np.mean(X_normalized)

# Check the standard deviation of the normalized array
np.std(X_normalized)

# Save the normalized array
np.save("X_normalized",X_normalized)
```

##### Step-by-Step Procedure of Functions:
- `import numpy as np` → imports the NumPy library and gives it the shorter name `np`.
- `np.random.seed(2112)` → sets the seed so that the same random numbers are generated every time.
- `np.random.randint(10, 101, size=(5, 5))` → generates random integers from 10 to 100 and creates a 5x5 array.
- `xbar = np.mean(X)` → calculates the mean of all the values in array `X`.
- `stndrdev = np.std(X)` → calculates the standard deviation of array `X`.
- `X_normalized = (X - xbar)/stndrdev` → normalizes every value by subtracting the mean and dividing by the standard deviation.
- `np.mean(X_normalized)` → checks the mean of the normalized array.
- `np.std(X_normalized)` → checks the standard deviation of the normalized array.
- `np.save("X_normalized",X_normalized)` → saves the normalized array as a NumPy `.npy` file.

  Outcome:

- The generated 5x5 array has a mean of `46.36`.
- The standard deviation is approximately `25.8641`.
- The mean of the normalized array is `0.0`.
- The standard deviation of the normalized array is approximately `1.0`.

##### The normalization was successful because the resulting array has a mean of 0 and a standard deviation of 1.
------

### 2) Cubes Divisible by 4 Problem - Creates the first 100 positive integers, cubes them, and selects the values divisible by 4.
```python

# Create and cube the first 100 positive integers
C = (np.arange(1,101) ** 3).reshape(10,10)
C

# Select values divisible by 4
div_by_4 = C[C % 4 == 0]
div_by_4

# Check the shape of C
C.shape

# Check the number of selected values
div_by_4.size

# Save the selected values
np.save("div_by_4.npy", div_by_4)
```

##### Step-by-Step Procedure of Functions:
- `np.arange(1,101)` → imports the NumPy library and gives it the shorter name `np`.
- `** 3` → sets the seed so that the same random numbers are generated every time.
- `.reshape(10,10)` → generates random integers from 10 to 100 and creates a 5x5 array.
- `C[C % 4 == 0]` → calculates the mean of all the values in array `X`.
- `C.shape` → calculates the standard deviation of array `X`.
- `div_by_4.size` → normalizes every value by subtracting the mean and dividing by the standard deviation.
- `np.save("div_by_4.npy", div_by_4)` → checks the mean of the normalized array.

  Outcome:

- The shape of array `C` is `(10, 10)`.
- There are `50` values that are divisible by 4.
- The selected values are stored in `div_by_4`.
- The selected values are also saved as `div_by_4.npy`.

------

### 3) Above-Mean Squares Problem - Creates the squares of the first 36 positive integers and selects the values above the mean.
```python

# Create the squares of the first 36 positive integers
S = (np.arange(1,37) ** 2).reshape(6,6)
S

# Get the mean of S
S_mean = np.mean(S)
S_mean

# Select values above the mean
above_mean = S[S > S_mean]
above_mean

# Count the values above the mean
above_mean.size

# Save the values above the mean
np.save("above_mean", above_mean)
```
##### Step-by-Step Procedure of Functions:
- `np.arange(1,37)` → creates an array containing the integers from 1 to 36.
- `** 2` → raises every integer in the array to the second power, which squares each number.
- `.reshape(6,6)` → changes the array into a 6x6 matrix.
- `S_mean = np.mean(S)` → calculates the mean of all the values in array 'S'.
- `S[S > S_mean]` → uses Boolean indexing to select only the values greater than the mean.
- `above_mean.size` → counts how many values are above the mean.
- `np.save("above_mean", above_mean)` → saves the selected values as a NumPy `.npy` file.
 
  Outcome:

- The mean of array `S` is approximately `450.1667`.
- The values above the mean are:
`484, 529, 576, 625, 676, 729, 784, 841, 900, 961, 1024, 1089, 1156, 1225, 1296`
- There are `15` values above the mean.
- The selected values are saved as `above_mean.npy`.
------

