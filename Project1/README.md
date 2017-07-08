# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked twins strategy looks for boxes with same pairs inside the same unit. For example, if in a unit, there are two boxes where all possible digits are 1 and 2. Then we know digits 1 and 2 can only happen in those two boxes, therefore we remove 1 and 2 from all the other boxes in that unit.
Constrain propagation help us to reduce search space. When solving naked twins, we actually introduce new constraint in the units. So it helps to further reduce the number of possibilities when searching.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Actually we just add a new constraint for diagonal sudoku problem. It makes two more units, and some boxes have more peers, while we still apply constrains on each unit.

We add two diagonals as the two new units and add them to the existing units list. We then apply all the same constraints based on the new units list.
Just as rows, columns and 3*3 boxes, those two diagonals must have each digit used once. Since the rules are the same across units, the way of constraint propagation (elimination, only choice or naked twins) is same as the original sudoku.


### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.