h Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A:Constant propagation is a process where better exploitation of constraints reduces the need to make decisions and the process where we determine how values of one variable impact values of another variable. In case of Naked Twins the presense of two boxes with the same two number and none other would eliminate these numbers from any other cell in the unit. 
Thus added a mechanism to identify twins in every unit and then within the unit remove the occurences of the twin values.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The way constraint propagation is achieved is to use the special methods to reduce the domain of variables on assigning a value.The methods used are
	1. Elimination - Eliminate the digit which in a box is single from all the peers.
        2. Only choice - If a digit is present in only one box of a unit then remove rest of the digits from the box.
        3. Naked Twins - The Naked twins is to if we have two boxes with the same two numbers then we can eliminate the digits from other boxes in the unit. 
   The key to algorithm is to create a project is creating the right list of units where boxes cannot have the digits repeat.

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
