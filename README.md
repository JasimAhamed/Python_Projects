# Sudoku Solver

# Description

This project contains a Python implementation of a Sudoku solver using a backtracking algorithm. The solver fills in the empty cells of a partially completed Sudoku grid and ensures that the solution adheres to Sudoku rules: no repeated numbers in any row, column, or 3x3 sub-grid.

# How It Works

1. Grid Representation: The Sudoku grid is represented as a 2D list (matrix) where:
   - `0` denotes an unassigned cell.
   - Numbers from `1` to `9` denote assigned cells.

2. Backtracking Algorithm:
   - The `solveSudoku` function attempts to fill the grid by assigning numbers to unassigned cells.
   - The `isSafe` function checks if placing a number in a particular cell adheres to Sudoku rules.

3. Printing the Grid: Once solved, the grid is printed in a readable format.

# Code Overview

- **`printing(arr)`**: Utility function to print the Sudoku grid.
- **`isSafe(grid, row, col, num)`**: Checks whether placing `num` at position `(row, col)` is valid.
- **`solveSudoku(grid, row, col)`**: Recursively attempts to solve the Sudoku grid using backtracking.

## Usage

1. Define the Grid: Initialize the `grid` variable with your Sudoku puzzle. Use `0` for empty cells.

2. Run the Solver: Call `solveSudoku(grid, 0, 0)` to solve the puzzle.

3. Print the Solution: If the Sudoku is solvable, the grid will be printed with the solution.

# Example

```python
# Initial Sudoku grid (0 denotes empty cells)
grid = [
    [3, 0, 6, 5, 0, 8, 4, 0, 0],
    [5, 2, 0, 0, 0, 0, 0, 0, 0],
    [0, 8, 7, 0, 0, 0, 0, 3, 1],
    [0, 0, 3, 0, 1, 0, 0, 8, 0],
    [9, 0, 0, 8, 6, 3, 0, 0, 5],
    [0, 5, 0, 0, 9, 0, 6, 0, 0],
    [1, 3, 0, 0, 0, 0, 2, 5, 0],
    [0, 0, 0, 0, 0, 0, 0, 7, 4],
    [0, 0, 5, 2, 0, 6, 3, 0, 0]
]

if solveSudoku(grid, 0, 0):
    printing(grid)
else:
    print("No solution exists.")
# Output
[ 3 1 6 5 7 8 4 9 2
  5 2 9 1 3 4 7 6 8
  4 8 7 6 2 9 5 3 1
  6 4 3 7 1 2 9 8 0
  9 7 8 8 6 3 1 2 5
  2 5 1 4 9 0 6 0 7
  1 3 4 9 8 7 2 5 6
  8 6 2 3 5 1 9 7 4
  7 9 5 2 4 6 3 1 9 ]

  
