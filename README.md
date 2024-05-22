# Crossword Puzzle Solver

## Overview
This project is a crossword puzzle solver that uses constraint satisfaction techniques to fill in a crossword grid with words from a given list. The solver ensures that the words fit within the constraints of the crossword structure and overlap correctly.

## Features
- **Constraint Satisfaction Problem (CSP) Solver**: Utilizes CSP techniques such as node consistency, arc consistency (AC-3), and backtracking to find a solution.
- **Flexible Input**: Reads the crossword structure and word list from input files.
- **Efficient Heuristics**: Implements heuristics to improve the efficiency of the backtracking algorithm.

## Files
- `crossword.py`: Contains the `Variable` and `Crossword` classes, which define the crossword structure and variables.
- `crosswordcreator.py`: Contains the `CrosswordCreator` class, which handles the CSP solving process.
- `generate.py`: The main script to run the solver.
- `structure.txt`: An example structure file for the crossword grid.
- `words.txt`: An example word list file.

## Installation
1. **Clone the Repository**:
    ```sh
    git clone https://github.com/Owais-Faiz/crossword-solver.git
    cd crossword-solver
    ```

2. **Dependencies**:
    Ensure you have Python 3 installed on your system. No additional libraries are required.

## Usage
1. **Prepare Input Files**:
    - `structure.txt`: A text file representing the crossword structure where underscores (`_`) represent empty spaces and hashes (`#`) represent blocked cells.
    - `words.txt`: A text file containing a list of words to be used in the crossword, one word per line.

2. **Run the Solver**:
    ```sh
    python generate.py structure.txt words.txt
    ```

3. **Output**:
    - The solver will print the completed crossword to the terminal.
    - If no solution is found, it will print "No solution."

## Example
### Structure File (`structure.txt`)
```
____
##_#
____
```

### Words File (`words.txt`)
```
WORD
RED
RIDE
```

### Run the Solver
```sh
python generate.py structure.txt words.txt
```

### Expected Output
```
W O R D
█ █ E █
R I D E
```

## Methods
### `Variable` Class
Represents a single word in the crossword with its starting position, direction (across or down), and length.

### `Crossword` Class
Handles the initialization and management of the crossword grid, variables, and overlaps between words.

### `CrosswordCreator` Class
Implements the CSP solver with methods for enforcing node and arc consistency, ordering domain values, selecting unassigned variables, and backtracking to find a solution.

## Contribution
Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or bug fixes.

For details refer to the PDF "AI Project" file.

## Acknowledgments
This project is based on the CS50 AI course by Harvard, specifically the Crossword project. For more information, visit the [CS50 AI 2024 course page](https://cs50.harvard.edu/ai/2024/projects/3/crossword/).
