---

## 0x09. Island Perimeter

### Project Overview
This project involves writing a function that calculates the perimeter of an island in a grid. The grid is represented by a list of lists, where:
- `1` represents land.
- `0` represents water.

### Key Concepts
- **Perimeter Calculation**: The perimeter is calculated by counting the edges of each land cell that are either touching water or are at the grid's boundary.

### Requirements
- The grid is rectangular, with a width and height of at least 1.
- The grid is surrounded entirely by water.
- There is only one island (one or more connected land cells).
- The island does not contain any "lakes" (water cells within the island).

### Function Signature
```python
def island_perimeter(grid: List[List[int]]) -> int:
```

### Approach
1. Traverse each cell in the grid.
2. For every land cell (`1`), check its four neighbors (top, bottom, left, right).
3. Add to the perimeter for each side of the land cell that is either at the grid’s edge or adjacent to a water cell (`0`).

### Example
Given the following grid:
```
[
    [0, 1, 0, 0],
    [1, 1, 1, 0],
    [0, 1, 0, 0],
    [0, 1, 0, 0]
]
```
The perimeter of the island is `16`.

### Implementation
```python
def island_perimeter(grid):
    perimeter = 0
    for i in range(len(grid)):
        for j in range(len(grid[i])):
            if grid[i][j] == 1:
                # Check top
                if i == 0 or grid[i-1][j] == 0:
                    perimeter += 1
                # Check bottom
                if i == len(grid) - 1 or grid[i+1][j] == 0:
                    perimeter += 1
                # Check left
                if j == 0 or grid[i][j-1] == 0:
                    perimeter += 1
                # Check right
                if j == len(grid[i]) - 1 or grid[i][j+1] == 0:
                    perimeter += 1
    return perimeter
```

### Testing
Ensure to test the function with various grid configurations to handle different cases like single cells, rectangular islands, and complex shapes.

### Additional Notes
- The time complexity of the solution is `O(n * m)`, where `n` is the number of rows and `m` is the number of columns.
- The solution is simple yet effective for computing the island perimeter in any valid grid configuration.

---
