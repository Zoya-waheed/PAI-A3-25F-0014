# Programming for AI – Assignment 3
## Overview
This repository contains my implementation of Assignment 3 for Programming for AI.
## Project Structure
* `Assignment3_Programming_for_AI.ipynb`: Completed assignment notebook.
* `data/`: Provided datasets.
* `outputs/`: Generated dashboard figures and wave animation.
## Requirements
* Python 3
* NumPy
* Pandas
* Matplotlib
## How to Run
1. Open the notebook in VS Code or Jupyter Notebook.
2. Select a Python kernel with the required libraries.
3. Run all cells from top to bottom.
## One Thing I Found Difficult
The hardest part for me was the date column in the weather data (Question 4). The file had two date formats mixed together, and when I let pandas guess them with `format='mixed'` it did not give any error, but it read dates like 10/04/2026 as 4 October instead of 10 April. I only noticed when I checked the date range, which came out as January to December instead of March to June, and 23 of the 60 DD/MM dates turned out to be wrong. I fixed it by parsing the two formats separately with `errors='coerce'` and joining them with `fillna`, and then I checked that no dates were missing. It taught me that code which runs without any error can still give wrong results, so now I check the output instead of just trusting it.