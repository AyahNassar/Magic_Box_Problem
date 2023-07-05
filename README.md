# Magic Square Problem Solver 
The Magic Square problem is a puzzle that involves filling a square grid with distinct numbers so that the sums of the numbers in each row, each column, and both the main diagonals are the same. This common sum is often referred to as the "magic constant."

The 3x3 Magic Square problem specifically deals with a 3x3 grid, and it requires filling this grid with distinct numbers from 1 to 9. The magic constant for a 3x3 Magic Square is 15, meaning that every row, column, and diagonal should sum to 15.

Finding a solution to the Magic Square problem can be challenging as it's a combinatorial problem. There are 9! (362,880) ways to arrange the numbers 1 to 9 in a 3x3 grid, but only a few of these arrangements form a Magic Square. The challenge lies in efficiently exploring the solution space to find these magic squares without having to test all possible arrangements, which can be computationally expensive.


# This program uses three different solver methods to find solutions to the 3x3 Magic Square problem. The magic square is a grid filled with distinct numbers in a way that the sum of the numbers in each row, column, and diagonal is the same, called the "magic constant". In our case, the magic constant is 15.

## Solver Methods

1. **Solver1:** This is a simple hill-climbing algorithm. It starts from an initial random solution and iteratively swaps pairs of elements in an attempt to reduce the total deviation from the magic constant. It can get stuck in local optima.

2. **Solver2:** This method is an improved version of Solver1. It introduces a counter that tracks the number of iterations without improvement. If the algorithm gets stuck in a local optimum (no improvement for 1000 iterations), it restarts the search from a new random solution. This is called Random-Restart Hill Climbing.

3. **Solver3:** This is the most efficient method. It combines the strategies of Solver1 and Solver2. It performs hill-climbing with random restarts and also stochastically accepts some worse solutions. The introduction of randomness both in the acceptance of worse solutions and in the occasional restarts helps it escape local optima more efficiently, increasing the chances of finding the global optimum.

## Usage

Run the program and observe the outputs of the three solvers. The output is the number of iterations it took each solver to find a magic square (or reach the iteration limit).

You can also compare the performance of the solvers by running them multiple times and calculating the average number of iterations. The provided script runs each solver 31 times and prints out the average results.

## Future Improvements

The performance of these solvers could potentially be improved further by implementing more advanced search techniques, such as simulated annealing or genetic algorithms.

## Requirements

Python 3.6 or above.

