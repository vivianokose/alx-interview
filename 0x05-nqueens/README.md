# 0x05. N Queens

## Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Requirements](#requirements)
4. [Usage](#usage)
5. [Examples](#examples)
6. [Testing](#testing)
----
## Introduction
The **N Queens** problem is a classic computer science problem that involves placing `N` queens on an `N×N` chessboard so that no two queens threaten each other. This means that no two queens can share the same row, column, or diagonal.

## Problem Statement
Given an integer `N`, your task is to find all possible ways to place `N` queens on an `N×N` chessboard such that no two queens can attack each other.

### Constraints
- `1 ≤ N ≤ 10`

### Input
- A single integer `N`

### Output
- A list of solutions, where each solution is represented as a list of integers. Each integer represents the column position of the queen in the respective row.

## Requirements
- Python 3.x
- No additional libraries are required.

## Usage
1. Clone the repository:
    ```sh
    git clone https://github.com/vivianokose/0x05-n-queens.git
    cd 0x05-n-queens
    ```

2. Run the script with the desired value of `N`:
    ```sh
    python3 n_queens.py <N>
    ```

### Example
To find solutions for `N=4`:
```sh
python3 n_queens.py 4
```

## Examples
For `N=4`, the output will be:
```
[
    [1, 3, 0, 2],
    [2, 0, 3, 1]
]
```

This represents the following board configurations:

1. 
    ```
    . Q . .
    . . . Q
    Q . . .
    . . Q .
    ```

2. 
    ```
    . . Q .
    Q . . .
    . . . Q
    . Q . .
    ```

## Testing
You can run the provided tests to verify the implementation:
```sh
python3 -m unittest test_n_queens.py
