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
