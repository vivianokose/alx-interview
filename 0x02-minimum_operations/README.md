# 0x02. Minimum Operations

This directory contains tasks that help you understand the concept of minimum operations in algorithms.

## Tasks

### 0. Minimum Operations

Given an array of integers, find the minimum number of operations required to make all elements equal.

**Example:**

Input: `[3, 2, 1]`  
Output: `2`  
Explanation: We can make all elements equal to 1 by subtracting 2 from the first element and subtracting 1 from the second element.

### 1. Minimum Operations with Constraints

Given an array of integers and a set of constraints, find the minimum number of operations required to make all elements equal while satisfying the constraints.

**Example:**

Input: `[3, 2, 1]`, `[(0, 1), (1, 2)]`  
Output: `3`  
Explanation: We can make all elements equal to 1 by subtracting 2 from the first element, subtracting 1 from the second element, and adding 1 to the third element.

### 2. Minimum Operations with Costs

Given an array of integers and a cost function, find the minimum cost required to make all elements equal.

**Example:**

Input: `[3, 2, 1]`, `lambda x: x^2`  
Output: `14`  
Explanation: We can make all elements equal to 1 by subtracting 2 from the first element (cost = 4), subtracting 1 from the second element (cost = 1), and adding 1 to the third element (cost = 1).
