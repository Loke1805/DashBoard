import numpy as np

# 1. Generate Matrix: Create a 5x5 matrix with random numbers (0-1) using a fixed seed
seed_value = 42
np.random.seed(seed_value)
matrix = np.random.rand(5, 5)

print("Original Matrix:")
print(matrix)

# 2. Invert Matrix: Compute and handle potential errors for non-invertible matrices
try:
    inverse_matrix = np.linalg.inv(matrix)
    print("\nInverse Matrix:")
    print(np.round(inverse_matrix, 2))  # Round to 2 decimal places for display
except np.linalg.LinAlgError:
    print("\nError: The matrix is singular (non-invertible).")
    inverse_matrix = None

# 3. Verify Identity Matrix: Multiply the matrix by its inverse to check closeness to the identity matrix
if inverse_matrix is not None:
    identity_check = np.dot(matrix, inverse_matrix)
    print("\nMatrix multiplied by its inverse (should be close to identity):")
    print(np.round(identity_check, 2))  # Round to 2 decimal places for display

# 4. Statistical Analysis: Calculate and display the mean, median, and variance of the matrix elements
mean_value = np.mean(matrix)
median_value = np.median(matrix)
variance_value = np.var(matrix)

print("\nStatistical Analysis of the Original Matrix:")
print(f"Mean: {mean_value:.2f}")
print(f"Median: {median_value:.2f}")
print(f"Variance: {variance_value:.2f}")
