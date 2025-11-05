# TSP Genetic Algorithm Solver

This project implements a **Genetic Algorithm** to solve the **Traveling Salesman Problem (TSP)**.
The algorithm evolves a population of tour candidates through multiple generations, using crossover and mutation operations to find near-optimal solutions.

## Implementation Details

### Mutation Strategies
- **Inversion Mutation**: Reverses a random segment of the tour;
- **Swap Mutation**: Swaps two random cities in the tour.

### Crossover Strategies
- **Ordered Crossover (OX)**: Preserves a segment from one parent and fills remaining positions from the other parent;
- **Inver-Over Crossover**: Applies directed inversions based on city successors from both parents,

### Key Features
- **Tournament selection**: Selects parents through competitive sampling;
- **Elitism**: Preserves top 5% of individuals across generations;
- **Adaptive mutation rate**: Dynamically adjusts based on evolutionary progress.

## Testing

The notebook tests all 4 combinations (2 mutations × 2 crossovers) on multiple problem instances:
- **G problems**;
- **R1 problems**;
- **R2 problems**;

For each problem, the algorithm identifies the best strategy combination and visualizes the cost evolution across generations.

## Best Strategies by Problem Type

### G Problems (Geometric)
**Strategy**: `inver_over_crossover` + `inversion_mutation`  

### R1 Problems (Random Symmetric)
**Strategy**: `ox_crossover` + `swap_mutation`  

### R2 Problems (Random with Negative Values)
**Strategy**: `ox_crossover` + `inversion_mutation`  
