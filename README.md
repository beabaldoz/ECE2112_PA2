# ECE2112_PA2
## Part A ##
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
numbers = np.arange(1,101)
C = (numbers**3).reshape(10,10)
print(C)
div_by_4 = C[C%4==0]
print("Shape of C:", C.shape)
print("Numbers divisible by 4:", div_by_4)
S = np.arange(1,37)**2
S = S.reshape(6,6)
Smean = S.mean()
above_mean = S[S>Smean]
print("S:",S)
print("Mean of S:",Smean)
print("Values above the mean:",above_mean)
