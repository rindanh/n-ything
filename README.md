# N-y thing
A program to solve N-y thing problem using these algorithms:

- Hill Climbing Algorithm
- Simulated Annealing Algorithm
- Genetic Algorithm


## Model folder
We need these models: 

1. Bishop 
2. Queen
3. Knight
4. Rook

All these models will inherit the **ChessPiece** abstract base class, which has these attributes: 

- position

  save it as a pair of values (x,y)

- move possibilities (virtual function)

  a function that checks all the move possibilities of eating the other pieces. <br>
  example: Queen should check all horizontal, vertical, and diagonal pieces.   

- color

  **black** or **white**

## N-ything

#### solver.py
In the *solver.py* file, we need to implement these methods:

1. *generate_solution* : This function will receive the current state of the problem and make a solution based on the best cost.

2. *generate_random_solution* : This function  will receive the current state of the problem and will make a random solution out of it.

    I think we need to implement another function for the genetic algorithm, please let us know :D



#### cost.py
In the *cost.py* file, we need to implement this method:

1. *cost_function.py* : This function will receive the state of a solution and calculate the cost function.

Those function above will be used in the algorithms.


## Utillities

#### parser.py
This will parse the external file and returns the array of Pawns object 

#### printer.py
This will print the state of the chess board to the screen 

## Main Program 

The flow of the main program is as follows:

1. File *parser.py* contains the **parser function** that will parse the external file and returns an **array of Pawns** object that is going to be used as the parameter to the algorithm functions.

2. The user will have to choose one of the three algorithms.

3. The **array of Pawns** object will be thrown into the parameter of those three algorithms (meaning that those algorithms have the same parameters)

4. The algorithms will return an array that depicts the position of the chess pawns. 

5. The array then will be printed by the function in the *printer.py* file.