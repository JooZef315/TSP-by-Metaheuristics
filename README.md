# TSPbyMetaheuristics

## Traveling Salesman Problem Solver

## Description

This Python package provides implementations of three metaheuristic algorithms to solve the Traveling Salesman Problem (TSP): **Steepest Ascent Hill Climbing**, **Simulated Annealing**, and **Ant Colony Optimization**. The Traveling Salesman Problem is a classic problem in combinatorial optimization where the goal is to find the shortest possible route that visits each city exactly once and returns to the original city.

## Files

- `hillClimbing.py`: Implementation of the Steepest Ascent Hill Climbing algorithm for solving the TSP.
- `simulatedAnnealing.py`: Implementation of the Simulated Annealing algorithm for solving the TSP.
- `antColony.py`: Implementation of the Ant Colony Optimization algorithm for solving the TSP.
- `travelingSalesman.py`: Utility functions for reading TSP instances from files and other generic tasks.

## Features

- Solves the Traveling Salesman Problem using three different metaheuristic algorithms.
- Supports reading TSP instances from files in standard formats.
- Easy-to-use interface for running and comparing different algorithms.

## Installation

1. Clone the repository:
   ```bash
   pip install TSPbyMetaheuristics
   ```
2. You're ready to use the package!

## Usage

1. Import the desired algorithm(s) from the package:

   ```python
   from TSPbyMetaheuristics import hillClimbing, simulatedAnnealing, antColony

   tspHC = hillClimbing(simulations= 100)
   tspSA = simulatedAnnealing(T0= 100)
   tspAC = antColony(genrations_num= 20, Beta= 5)
   ```

2. Read a TSP instance from a file using the provided utility functions:
   ```python
    tspHC.read_routes_from_file('file.txt')
    tspSA.read_routes_from_file('file.txt')
    tspAC.read_routes_from_file('file.txt')
    #OR
    tspHC.read_routes_from_list([[x1, y1], [x2, y2]])
    tspSA.read_routes_from_list([[x1, y1], [x2, y2]])
    tspAC.read_routes_from_list([[x1, y1], [x2, y2]])
   ```
3. Apply the chosen algorithm(s) to solve the TSP:
   ```python
   solution_hc, shortest_path_hc = tspHC.steepest_ascent()
   solution_sa, shortest_path_sa = tspSA.simulated_annealing()
   solution_ac, shortest_path_ac = tspAC.run_monte_carlo( simulations = 20)
   ```
4. Compare the solutions obtained and choose the best one for your problem.

For more details on the usage of each algorithm, refer to the documentation in their respective files.

## Example Output

![Steepest Ascent Hill Climbing](/hc.png)
![Ant Colony Optimization](/as.png)

## License

This project is licensed under the [MIT License](License.txt).
