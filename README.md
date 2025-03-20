# Spatio-Temporal-Predator-Prey-Simulation

## A python code to simulate predators and prey behaviour on a two dimensional plane of cells.
This is a spatio-temporal stochastic simualation of the interaction between two species - a predator and a prey
This simulation aims to capture the basic dynamics of predation in nature:

The space is divided into a 10 by 10 grid. A set number of predator and the prey population are initially randomly distributed across the 100 cells of the grid. The simulation then runs for a fixed number of steps, during each step every cell is updated according to the simulation rules.


### Simulation Rules:
The following actions occur in each time step for every cell in this order:

1. If at least one member of both predator and prey are present in a cell then predation occurs, each predator kills one member of the prey species if available in the cell. If there are more predators than prey in the cell, the prey population for the cell is set to zero for that cell.

2. Every surviving prey in the cell searches in its nearest neighbouring (top,right,bottom and left) cells, and if any one of them is empty then every prey have a chance (a) at reproducing one offspring each.

3. Each predator which has successfuly fed has a chance to reproduce (c) if it has a nearest neighbour cell which is devoid of other predators. For this purpose when predation occurs in a cell (as denoted in point 1), all predators of the cell is considered fed.

4. Each surviving prey in a cell has a chance to die naturally (b)

5. Each predator in a cell which has not fed has a chance to die of starvation (d) - $\textit{Natural death of Predators is not considered}$

6. At the end of each time step, all organisms has a chance to move to one of the neighbouring cell (or remain still)


### Simulation Parameters:

The following variables may be adjusted in this simulation

    Ini_N -> #Initial number of prey
    Ini_P -> #Initial number of predators

    a -> #Probability for a Prey to reproduce if survived
    b -> #Probability for a Prey to die naturally 
    c -> #Probability for a Predator to reproduce if fed
    d -> #Probability for a Predator to die of starvation

