# ECE2112_PA2
## Part A - Normalization
#### This part shows how normalization works on a NumPy array. It is done by creating a random 5×5 array and standardizing it using the mean and standard deviation so that the new values have a mean of 0 and a standard deviation of 1.
import numpy as np
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
print("X: ", X)
X_mean = X.mean()
print("X mean: ", X_mean)
X_std = X.std()
print("X standard dev: ", X_std)
X_normalized = (X-X_mean)/X_std
print("X normalized: ", X_normalized)
## Part B - Cubes Divisible by 4
#### This part shows how to manipulate arrays and filter values using conditions. It is done by cubing the first 100 integers, reshaping them into a 10×10 array, and selecting only the values that are divisible by 4 using Boolean filtering.
numbers = np.arange(1,101)
C = (numbers**3).reshape(10,10)
print(C)
div_by_4 = C[C%4==0]
print("Shape of C:", C.shape)
print("Numbers divisible by 4:", div_by_4)
## Part C - Above-Mean Squares
#### This part shows how to compute array statistics and filter values based on the mean. It is done by creating a 6×6 array of squared numbers, finding the average, and selecting only the elements that are greater than the mean.
S = np.arange(1,37)**2
S = S.reshape(6,6)
Smean = S.mean()
above_mean = S[S>Smean]
print("S:",S)
print("Mean of S:",Smean)
print("Values above the mean:",above_mean)
