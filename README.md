# CS 3510 Minesweeper Project Starter Code

### By: Connor Cole, Valentina Grando, Allison Ronan

## Overview

This is our final project, built around the provided framework from project_files. We altered AI1 and AI2, and then created a python script to run all test files inside of varied_density_boards and varied_size_boards. The following commands can be used inside of the same directory as the rest of the project from the command line to test our code.

- #### Front end: 

  ```
  "python -i minesweeperGameEngine.py -f deterministic_board.json"
  ```

  This will run the boards provided in deterministic_board using the front end code.

- #### All test cases (first size, next density)

  ```
  "python test1depth.py"
  "python test1density.py"
  ```

  This will run the code for all test case files.

- ###### Single test case

  ```
  "python minesweeperPerformanceTest.py -f ./varied_size_boards/25rows_40cols_10d_0.json 1 > results_test"
  ```

  This will take case of singular test cases.

  

  ## Files

* `minesweeperAI1.py` - This is our first algorithm, which is a divide and conquer styled approach
* `minesweeperAI2.py` - This is our second algorithm, based on the Naive Single point algorithm

- Make sure python3 is installed before running













## How to run

* Make sure all files are in the same directory
* Make sure you have `python3` installed (`python2` will most likely not work). Make sure you have common libraries installed, including `numpy` and `tk`. If you run the program and receive some import error, you are most likely missing a library, which can be downloaded fairly simply through a quick google search. Please let us know if you are unable to run the files on Piazza.
* On command prompt/anaconda/terminal, type and enter `python3 minesweeperGameEngine.py`. Depending on how you installed python, if that does not work, try `python minesweeperGameEngine.py`. A GUI should appear, and clicking either button will run through the algorithm. 
  *  You can also run, for example, `python3 minesweeperGameEngine.py -f deterministic_board.json`, which will use that json file. The default is `test_board.json`
* On command prompt/anaconda/terminal, type and enter `python3 minesweeperPerformanceTest.py`. Depending on how you installed python, if that does not work, try `python minesweeperPerformanceTest.py`. No GUI will appear, but some games will be automatically ran, and you will get a quick summary of how many were won and lost.
  * You can also run, for example, `python3 minesweeperPerformanceTest.py -g 15 16 17 0 3 1 10 `, which indicates 10 randomly generated gameboard of size $15 \times 16$ with 17 bombs and a safe square of (0, 3). Each gameboard will be solved independently using your first (1) algorithm.
  * You run also run, for example, `python3 minesweeperPerformanceTest.py -f deterministic_board.json 2`, which will use the given board json and your second (2) algorithm.  

## AI code specifications

* Please use the comments, the sample AI, and print statements to help understand the format, but briefly, you will be given the current state of the game board and must decide whether to:
  * 1) open up another square
  * 2) submit your answer (the locations of all bombs) 
* The game can end in 2 ways:
  * you returned a list of bomb locations, but the set of bombs did not match the real locations of the bombs (incorrect)
  * you returned a list of bomb locations, and the list matched the real locations of the bombs (correct)