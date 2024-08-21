# 0x07. Rotate 2D Matrix

## Overview

This repository provides a solution to the problem of rotating a given 2D matrix (square) 90 degrees clockwise. The algorithm modifies the matrix in place, ensuring efficient space utilization.

## Problem Statement

Given an `n x n` 2D matrix, rotate it 90 degrees clockwise. For example:

**Input:**
```
[[1, 2, 3],
 [4, 5, 6],
 [7, 8, 9]]
```

**Output:**
```
[[7, 4, 1],
 [8, 5, 2],
 [9, 6, 3]]
```

## Installation

To run the example, clone the repository:

```bash
git clone <repository-url>
cd rotate-2d-matrix
```

## Usage

1. Call the function to rotate the matrix in place:
   ```python
   rotate(matrix)
   ```
2. The `matrix` variable will be modified directly.

## Conclusion

This method allows for an efficient rotation of a 2D matrix with a time complexity of O(n) and space complexity of O(1). For detailed implementation and examples, refer to the source code in the repository.
