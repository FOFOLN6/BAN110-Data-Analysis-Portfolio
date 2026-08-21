Testing the Hot Hand: A Probability Simulation of Kobe Bryant's Shooting Streaks

Project Overview

This project investigates the basketball "hot hand" phenomenon using Kobe Bryant's shot-by-shot results from the 2009 NBA Finals. Python is used to calculate shooting streaks and compare Kobe's observed streak distribution with the results of a simulated independent shooter who has the same approximate shooting percentage.

The analysis introduces probability concepts through a practical sports example and demonstrates how simulation can provide a reference model for interpreting observed data.

Research Question

Do Kobe Bryant's shooting streaks in the 2009 NBA Finals appear longer or more frequent than the streaks expected from an independent shooter with a 45% probability of making each shot?

Objectives

Distinguish between independent and dependent events

Explore fair and weighted random processes through coin-flip simulations

Create a reusable Python function to calculate shooting streak lengths

Describe the distribution of observed shooting streaks

Simulate an independent shooter with a 45% hit probability

Compare simulated results with Kobe Bryant's observed results

Interpret probabilistic evidence without implying causation

Dataset

Each row represents one of Kobe Bryant's 133 field-goal attempts across five games in the 2009 NBA Finals.

Important fields include:

Variable

Description

game

Finals game number

quarter

Quarter or overtime period

time

Time remaining when the shot was attempted

description

Description of the shot attempt

basket

Shot result: hit (H) or miss (M)

The dataset is distributed through an OpenIntro educational dataset repository.

Tools and Libraries

Python

Jupyter Notebook

pandas and NumPy

Matplotlib

requests

Methodology

1. Data preparation

The notebook inspects the five Finals games, converts the overtime label into a sortable value, and orders the observations by game and period so the shot sequence can be analyzed correctly.

2. Streak calculation

A custom calc_streak() function counts consecutive made baskets until a miss occurs. Under this definition:

A streak of 0 means an immediate miss.

A streak of 1 means one made basket followed by a miss.

Longer values represent consecutive makes before the next miss.

3. Probability simulations

The notebook first demonstrates random sampling with fair and unfair coin simulations. It then simulates 133 independent basketball shots using:

$$
P(\text{hit}) = 0.45, \qquad P(\text{miss}) = 0.55
$$

4. Comparison

Bar charts and descriptive statistics are used to compare Kobe's observed streak lengths with those produced by the simulated independent shooter.

Key Findings

Kobe's observed streak-length distribution is right-skewed, with short streaks occurring most frequently.

His longest observed streak in this dataset was four consecutive made baskets.

A single simulated independent shooter commonly produces a similarly right-skewed distribution dominated by streaks of zero and one.

In this exploratory comparison, Kobe's streak pattern does not appear clearly different from a sequence of independent shots with the same approximate shooting percentage.

Because an individual simulation changes each time it is run, this comparison is illustrative rather than a formal hypothesis test. Repeating the simulation many times would provide stronger evidence about how unusual Kobe's observed streaks were under the independence model.

Repository Structure

02-kobe-bryant-hot-hand-simulation/
├── README.md
└── kobe_hot_hand_probability_simulation.ipynb

How to Run

Clone or download the repository.

Open kobe_hot_hand_probability_simulation.ipynb in Jupyter Notebook, JupyterLab, or Google Colab.

Install the required libraries if necessary:

pip install numpy pandas matplotlib requests

Run the notebook from top to bottom. An internet connection is required when the notebook initially retrieves the dataset.

Skills Demonstrated

Probability and independence

Random simulation with NumPy

Data preparation and sorting

Custom Python functions

Discrete distribution analysis

Comparative data visualization

Evidence-based interpretation

Possible Extension

Run the independent-shooter simulation thousands of times, record a statistic such as the maximum streak or the number of long streaks in each run, and calculate how often the simulated statistic is at least as extreme as Kobe's observed result.

Acknowledgements

This project was completed as an educational probability lab. The original lab was adapted by David Akman and Imran Ture from OpenIntro materials by Andrew Bray and Mine Çetinkaya-Rundel. The completed Python analysis, responses, interpretations, and portfolio documentation are presented for learning and professional-development purposes.


