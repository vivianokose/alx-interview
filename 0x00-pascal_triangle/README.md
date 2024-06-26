# 0x00-pascal_triangle

## Overview
This repository contains a Python module that defines a function to generate Pascal's Triangle. Pascal's Triangle is a triangular array of the binomial coefficients. This project is part of the ALX Software Engineering program.

## Contents
1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Examples](#examples)
5. [Testing](#testing)
6. [Contributing](#contributing)
7. [License](#license)

## Requirements
- Python 3.6 or higher

## Installation
Clone the repository to your local machine:
```bash
git clone https://github.com/yourusername/0x00-pascal_triangle.git
cd 0x00-pascal_triangle
```

## Usage
The module contains a function `pascal_triangle(n)` that returns a list of lists representing Pascal's Triangle up to the `n`th level.

### Function Definition
```python
def pascal_triangle(n):
    """
    Generate Pascal's Triangle up to the nth level.

    :param n: The number of levels of Pascal's Triangle to generate.
    :return: A list of lists representing Pascal's Triangle.
    """
```

### Example
```python
from pascal_triangle import pascal_triangle

# Generate Pascal's Triangle with 5 levels
triangle = pascal_triangle(5)
for row in triangle:
    print(row)
```

Output:
```
[1]
[1, 1]
[1, 2, 1]
[1, 3, 3, 1]
[1, 4, 6, 4, 1]
```

## Testing
To run the tests, use the `unittest` framework:
```bash
python -m unittest discover tests
```

## Contributing
We welcome contributions! If you have suggestions, improvements, or additional resources to add, please follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m 'Add some feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a pull request.

---

Happy coding!
