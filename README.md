# Assignment 2 Support Code

This is the support code for COMP3702 2024 Assignment 2 (BeeBot).

The following files are provided:

**environment.py**

This file contains a class representing a game environment and supporting helper methods. You should make use of this 
class in your solver.

This file contains a number of functions which will be useful in developing your solver:

~~~~~
__init__(filename)
~~~~~
Constructs a new instance based on the given input filename.


~~~~~
get_init_state()
~~~~~
Returns a State object (see below) representing the initial state of the level.


~~~~~
perform_action(state, action)
~~~~~
Simulates the outcome of performing the given 'action' starting from the given 'state', where 'action' is an element of
GameEnv.ACTIONS and 'state' is a State object. Returns the reward (negative cost) of performing the action, and the
resulting new state.


~~~~~
is_solved(state)
~~~~~
Checks whether the given 'state' (a State object) is solved (i.e. all targets are covered by a widget). Returns
True (solved) or False (not solved).


~~~~~
render(state)
~~~~~
Prints a graphical representation of the given 'state' (a State object) to the terminal.


**state.py**

This file contains a class representing a BeeBot environment state. You should make use of this class and its functions
in your solver. You may add your own code to this class, but
should avoid removing or renaming existing variables and functions to ensure Tester functions correctly.

~~~~~
__init__(self, environment, BEE_posit, BEE_orient, widget_centres, widget_orients, force_valid=True)
~~~~~
Constructs a game environment state. Refer to the docstring for this method for information on the arguments taken
by this method.


**constants.py**

This file contains constants used by the Environment and State classes. It may be helpful to import this file into
your solver.


**play.py**

Running this file launches an interactive environment simulation. Becoming familiar with the environment mechanics may
be helpful in designing your solution.

The script takes 1 argument, input_filename, which must be a valid testcase file (e.g. one of the provided files in the
testcases directory). e.g.

**play_game.py**

Running this file launches an interactive environment simulation with a GUI. Player actions are bound to the game window.

The script takes 1 argument, input_filename, which must be a valid testcase file (e.g. one of the provided files in the
testcases directory). e.g.
`python3 play_game.py testcases/ex1.txt`

~~~~~
$ python play_game.py testcases/example.txt
~~~~~

When prompted for an action, press W to move the BEE forward, S to move the BEE in reverse, A to turn the BEE
left (counterclockwise) and D to turn the BEE right (clockwise). Use Q to exit the simulation, and R to reset the
environment to the initial configuration.


**solution.py**

This file is a template you should use to implement your solution.

You should implement the `vi_initialise()`, `vi_is_converged()`, `vi_iteration()`, `vi_get_state_value()`, `vi_select_action()`, `pi_initialise()`, `pi_is_converged()`, `pi_iteration()`, and `pi_select_action()` functions as well as any initialisation or helper functions you require.

**testcases**

A directory containing input files which can be used to evaluate your solution.

Testcase files can contain comments, starting with '#', which are ignored by the input file parser.

