# CS 3510 Minesweeper Project Starter Code

### By: Connor Cole, Valentina Grando, Allison Ronan

## Overview

This is our final project, built around the provided framework from project_files. We altered AI1 and AI2, and then created a python script to run all test files inside of varied_density_boards and varied_size_boards. The following commands can be used inside of the same directory as the rest of the project from the command line to test our code.

- #### Front end: 

  ```
  python -i minesweeperGameEngine.py -f deterministic_board.json
  ```

  This will run the boards provided in deterministic_board using the front end code.

- #### All test cases (first size, next density)

  ```
  python test1depth.py
  python test1density.py
  ```

  This will run the code for all test case files.

- ###### Single test case

  ```
  python minesweeperPerformanceTest.py -f ./varied_size_boards/25rows_40cols_10d_0.json 1 > results_test
  ```

  This will take case of singular test cases.

  

  ## Files

* `minesweeperAI1.py` - This is our first algorithm, which is a divide and conquer styled approach
* `minesweeperAI2.py` - This is our second algorithm, based on the Naive Single point algorithm

- Make sure python3 is installed before running