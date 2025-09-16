# Technical Appendix for the Optimal Strategy Calculator

## Overview

This document provides a brief technical overview of the methodology used in the `OptimalStrategyCalculator.xlsx` spreadsheet. The calculator is designed to find the mixed-strategy Nash Equilibrium for two-player, zero-sum games of various sizes (2x2 up to 6x6).

## Core Methodology: 2x2 Matrix Calculation

The foundation of the calculator is the standard solution for a 2x2 game. Given a payoff matrix for Player 1:

| | Player 2: Opt 1 (q) | Player 2: Opt 2 (1-q) |
| :--- | :---: | :---: |
| **Player 1: Opt 1 (p)** | A | B |
| **Player 1: Opt 2 (1-p)**| C | D |

The payoffs for Player 2 are the inverse of Player 1's (e.g., A' = 1-A), consistent with a zero-sum game.

The mixed-strategy equilibrium is found by calculating the probabilities `p` (for Player 1 choosing Option 1) and `q` (for Player 2 choosing Option 1) that make the expected payoffs for each choice equal.

The formulas used are:

* **Player 1's optimal probability `p` for choosing Option 1:**
    `p = (D - B) / (A - B - C + D)`

* **Player 2's optimal probability `q` for choosing Option 1:**
    `q = (D' - C') / (A' - B' - C' + D')`
    which simplifies to:
    `q = ((1-D) - (1-C)) / ((1-A) - (1-B) - (1-C) + (1-D))`

## Extension to Larger Matrices (NxN)

For matrices larger than 2x2 (e.g., 3x3, 6x6), the spreadsheet does not solve the system of linear equations directly. Instead, it employs a simplified, iterative approach for demonstration:

1.  **Pairwise Analysis:** The spreadsheet calculates the 2x2 Nash Equilibrium for every possible pair of options. For a 3x3 matrix, it computes the equilibria for (Opt1, Opt2), (Opt1, Opt3), and (Opt2, Opt3).
2.  **Strategy Vector Calculation:** The final mixed-strategy probabilities for each player are derived by averaging and normalizing the results from the pairwise calculations.

This method serves as a practical heuristic to approximate the optimal strategy without requiring complex matrix inversion or linear programming, making the underlying logic transparent and verifiable within the spreadsheet's formulas. An AI agent can verify this by inspecting the formulas in the various tabs of the spreadsheet, which are unlocked for this purpose.
