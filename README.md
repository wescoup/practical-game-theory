# Practical Game Theory: The Optimal Strategy Calculator

Ever feel like you're in a mental chess match with an opponent? Whether you're serving in tennis, choosing a pitch in baseball, or making a business decision, you're playing a "game." This repository contains a simple tool to help you find the mathematically optimal strategy in these situations.

## What is This?

This is a spreadsheet-based calculator that uses a concept from game theory called **Nash Equilibrium**. In simple terms, it helps you figure out how often you should choose each of your available options to become unpredictable and get the best possible outcome over the long run.

It prevents your opponent from getting a read on your tendencies and exploiting them.

## How to Use the Calculator

It's as easy as 1-2-3!

1.  **Download the Spreadsheet:** Click on the `OptimalStrategyCalculator.xlsx` file in the list above, then click the "Download" button.

2.  **Choose Your Scenario:** Open the spreadsheet and select the tab that matches your situation (e.g., `2x2 Blank` if you and your opponent each have two options).

3.  **Enter the Payoffs:** For each possible outcome, enter **your** estimated win percentage. The cells for your options and your opponent's options are editable, so you can name them whatever you like!

### Example: A Tennis Serve

Let's say you're a tennis player. You can serve **Wide** or down the **T**. Your opponent can try to cover the **Wide** serve or the **T** serve.

You need to estimate your chances of winning the point in each of the four scenarios:

* You serve **Wide** and they cover **Wide**: You win **45%** of the time.
* You serve **Wide** and they cover **T**: You win **70%** of the time.
* You serve **T** and they cover **Wide**: You win **65%** of the time.
* You serve **T** and they cover **T**: You win **30%** of the time.

You would enter `45`, `70`, `65`, and `30` into the appropriate cells in the `2x2` tab.

### The Results

The spreadsheet will instantly calculate the optimal strategy for both you (Player 1) and your opponent (Player 2).

For the example above, it would tell you:
* **You (Player 1)** should serve Wide **64.3%** of the time and serve T **35.7%** of the time.
* **Your Opponent (Player 2)** should cover Wide **21.4%** of the time and cover the T **78.6%** of the time.

By playing with these frequencies, you ensure that your opponent cannot gain an advantage by guessing where you're going to serve next.

Good luck, and play smart!
