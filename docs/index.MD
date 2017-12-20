Solve Sudoku using AI
===================


Week1
----------

What exactly is intelligence
-------------
Intelligence has been defined in many different ways including as one's capacity for logic, understanding, self-awareness, learning, emotional knowledge, planning, creativity, and problem solving. It can be more generally described as the ability or inclination to perceive or deduce information, and to retain it as knowledge to be applied towards adaptive behaviors within an environment or context. (From wiki)

What is Agent, Environment?
--------------
An agent is anything that can be viewed as perceiving its environment through sensors and acting upon that environment through actuators.

![env-agent](https://github.com/nik-hil/AIND-Sudoku/blob/master/docs/images/env.jpeg?raw=true)
An intelligent agent is one that takes actions to maximize its expected utility given a desired goal.


Strategies to solve Sudoku
---------

 1. **Eliminate** For each solved boxes, eliminate this value from the values of all its peers.
 1. **only_choice** Go through all the units, and whenever there is a unit with a value that only fits in one box, assign the value to this box.
 1. **reduce_puzzle** Iterate eliminate() and only_choice(). If at some point, there is a box with no available values, return False. If the sudoku is solved, return the sudoku. If after an iteration of both functions, the sudoku remains the same, return the sudoku.
 1. **search** Use depth search to call above fun to solve sudoku. Restrict the search for solution with boxes which have fewer possibilities.
 1. **naked_twin** If two possible number are peer. Remove these number from other boxes of peer.
    
 
