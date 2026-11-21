# Homework 9: Decisions Under Uncertainty and Over Time

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is the repository for Homework 9 for [BEE 4750](https://envsys.viveks.me/), taught at [Cornell University](https://cornell.edu) in Fall 2026 by [Vivek Srikrishnan](https://viveks.me).

If enrolled in the class, a PDF of the completed notebook, **with all cells evaluated**, should be submitted to Gradescope *no later* than the due date, at 9:00pm. 50% will be deducted for late submissions, which can be accepted up to 24 hours from the original deadline.

## Learning Objectives

After completing this assignment, students will be able to:

* draw a scenario tree for a two-stage decision, and name its first-stage and recourse decisions;
* evaluate a plan's expected cost across scenarios, and find the best first-stage decision;
* compute and interpret the value of the stochastic solution (VSS) and the expected value of perfect information (EVPI);
* solve a short sequential decision by backward induction, by hand;
* explain how a system's dynamics change the timing of the best plan.

## Repository Overview

The repository consists of the following files:

- `hw09.ipynb`: Jupyter Notebook for the homework assignment. This is the only file you should need to edit.
- `hw09.pdf`: PDF version of the homework assignment, if you don't want to rely on the Jupyter Notebook.
- `Project.toml`, `Manifest.toml`: Julia environment files. These should just work, but feel free to add other packages as needed using the `Pkg` package manager. This is the only other file that you might end up making changes to, though you should do this using `Pkg`, not directly.
- `hw09.qmd`: Source file for Jupyter notebook generation. You shouldn't need to or want to touch this; everything is in the `.ipynb` file.
- `LICENSE`: This material is licensed using the MIT license. You can ignore this for working on the problem set.
- `README.md`: This file. You shouldn't need to touch this.
- `.gitignore`: This tells `git` what files to ignore. You shouldn't need to touch this.
- `.devcontainer/`: Settings for opening this repository in GitHub Codespaces (see the course website's assignment workflow page). You shouldn't need to touch this.

## Dependencies

This notebook was written using Julia 1.11.5. Most of each problem is by hand; Problem 1.4 uses `JuMP.jl` with the `HiGHS.jl` solver. `Plots.jl` is included in case you want to draw in code.

## Prerequisites

1. [Install Julia](https://julialang.org/downloads/) before beginning this assignment. This notebook was developed with version 1.11.5, but any 1.11.x should work (there could be some issues with other versions, depending on what's changed).
2. If necessary, [install git](https://happygitwithr.com/install-git.html) and [create a GitHub account](https://github.com).
3. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). I recommend doing this in a dedicated `BEE4750/` folder, which can also house homework assignment repositories and lecture notes. You can clone directly into the `BEE4750/` folder.   For Windows (or from another graphical interface), just create a `BEE4750` folder, then a `hw` folder inside of that, then clone into that folder. Or to clone into a `BEE4750/hw` folder, from a command prompt:
    ```bash
    cd BEE4750/
    mkdir hw
    cd hw/
    git clone https://github.com/bee-envsys-cornell/hw09.git
    ```
