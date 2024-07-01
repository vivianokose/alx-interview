# 0x01. Lockboxes

## Table of Contents

1. [Introduction](#introduction)
2. [Project Requirements](#project-requirements)
3. [Setup and Installation](#setup-and-installation)
4. [Usage](#usage)
5. [Algorithm Explanation](#algorithm-explanation)
6. [Examples](#examples)
7. [Testing](#testing)
8. [Conclusion](#conclusion)

## Introduction

The **Lockboxes** project is designed to help understand and solve problems related to unlocking a series of boxes using a set of keys. Each box may contain keys that open other boxes, and the objective is to determine if all boxes can be unlocked starting from the first box.

This README provides a comprehensive guide to the project, including requirements, setup instructions, usage examples, and an explanation of the underlying algorithm.

## Project Requirements

To successfully complete the Lockboxes project, the following requirements must be met:

- **Python Version:** The project should be implemented using Python 3.x.
- **Algorithm:** Implement an algorithm that determines if all boxes can be unlocked.
- **Complexity:** The algorithm should be optimized for efficiency.

## Setup and Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/lockboxes.git
   cd lockboxes
   ```

2. **Environment Setup:**
   Ensure you have Python 3 installed. You can create a virtual environment for the project:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Dependencies:**
   If there are any dependencies, install them using `pip`:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

The main function of the project is `canUnlockAll(boxes)`. Here is how you can use it:

```python
from lockboxes import canUnlockAll

boxes = [[1], [2], [3], [4], []]
print(canUnlockAll(boxes))  # Output: True
```

## Algorithm Explanation

The goal of the `canUnlockAll` function is to determine if all boxes can be unlocked. Here's a step-by-step explanation of the algorithm:

1. **Initialization:**
   - Start with the first box (index 0) as unlocked.
   - Use a set to keep track of unlocked boxes.

2. **Unlocking Process:**
   - Iterate through the boxes.
   - For each box, if it is unlocked, use its keys to unlock other boxes.
   - Continue this process until no more boxes can be unlocked.

3. **Termination:**
   - The algorithm terminates when all boxes are either unlocked or no more boxes can be unlocked with the available keys.
   - If all boxes are unlocked, return `True`; otherwise, return `False`.

## Examples

### Example 1

```python
boxes = [[1], [2], [3], [4], []]
print(canUnlockAll(boxes))  # Output: True
```
In this example, each box contains a key to the next box, so all boxes can be unlocked.

### Example 2

```python
boxes = [[1, 3], [3, 0, 1], [2], [0]]
print(canUnlockAll(boxes))  # Output: True
```
Here, the keys provided can unlock all the boxes.

### Example 3

```python
boxes = [[1, 4], [2], [3], [], [5]]
print(canUnlockAll(boxes))  # Output: False
```
In this case, the last box (index 4) contains a key to a non-existent box (index 5), so not all boxes can be unlocked.

## Testing

To ensure the correctness of the implementation, you can run tests using the `unittest` framework. Create a test file, e.g., `test_lockboxes.py`, and write your test cases:

```python
import unittest
from lockboxes import canUnlockAll

class TestLockboxes(unittest.TestCase):
    def test_all_boxes_unlocked(self):
        self.assertTrue(canUnlockAll([[1], [2], [3], [4], []]))

    def test_not_all_boxes_unlocked(self):
        self.assertFalse(canUnlockAll([[1, 4], [2], [3], [], [5]]))

    def test_complex_case(self):
        self.assertTrue(canUnlockAll([[1, 3], [3, 0, 1], [2], [0]]))

if __name__ == '__main__':
    unittest.main()
```

Run the tests using the following command:

```bash
python test_lockboxes.py
```

## Conclusion

The Lockboxes project provides a practical implementation of an algorithm to determine if all boxes can be unlocked given a set of keys. By following this README, you should be able to understand the project requirements, set up the environment, use the function, and test its correctness.

Happy coding!
