Exploratory Analysis of CDC BRFSS Health Data

Project Overview

This project explores a sample of 20,000 responses from the 2000 Behavioral Risk Factor Surveillance System (BRFSS), an annual public health survey conducted by the U.S. Centers for Disease Control and Prevention (CDC).

The analysis uses Python to summarize respondents' health characteristics, examine relationships among demographic and behavioral variables, and visualize patterns involving smoking, exercise, body mass index (BMI), and desired weight.

Objectives

Identify categorical and numerical variables in a public health dataset

Calculate descriptive statistics and relative frequency distributions

Filter observations using multiple conditions

Compare health and behavioral characteristics across groups

Create and interpret bar charts, mosaic plots, box plots, histograms, and scatterplots

Engineer new variables, including BMI and the difference between desired and current weight

Dataset

The dataset contains 20,000 observations and nine original variables:

Variable

Description

genhlth

Self-reported general health

exerany

Whether the respondent exercised in the past month

hlthplan

Whether the respondent had health coverage

smoke100

Whether the respondent had smoked at least 100 cigarettes

height

Height in inches

weight

Current weight in pounds

wtdesire

Desired weight in pounds

age

Age in years

gender

Respondent gender as recorded in the source data

Source: CDC Behavioral Risk Factor Surveillance System (BRFSS), 2000 sample distributed through OpenIntro.

Tools and Libraries

Python

Jupyter Notebook

pandas and NumPy

Matplotlib and Seaborn

statsmodels

Analysis Highlights

Descriptive statistics

The notebook calculates measures such as the mean, median, standard deviation, quartiles, and interquartile range. It also uses frequency and relative frequency tables to summarize categorical variables.

Smoking and gender

A grouped frequency table and mosaic plot are used to compare lifetime smoking history across the gender categories recorded in the dataset. In this sample, male respondents had a higher proportion of respondents who reported smoking at least 100 cigarettes.

BMI and health indicators

BMI is calculated from height and weight:

$$BMI = \frac{weight_{lb}}{height_{in}^2} \times 703$$

Box plots compare BMI across self-reported health categories and exercise status. Respondents who reported exercising in the previous month had a slightly lower median BMI than respondents who did not.

Current versus desired weight

A new variable, wdiff, is created as:

$$wdiff = desired\ weight - current\ weight$$

Negative values indicate a desire to lose weight, positive values indicate a desire to gain weight, and zero indicates that desired and current weight are equal. The analysis compares this measure across gender categories using numerical summaries and side-by-side box plots.

Key Findings

Current weight and desired weight have a strong positive relationship.

Many respondents reported a desired weight below their current weight.

Female respondents in this sample tended to report a more negative desired-weight difference than male respondents.

Approximately 70.76% of recorded weights fell within one standard deviation of the sample mean.

BMI distributions contained high-value outliers and differed modestly across exercise and self-reported health groups.

These findings describe associations in the sample and should not be interpreted as causal relationships.

Repository Structure

cdc-brfss-health-data-analysis/
├── README.md
└── cdc_brfss_health_data_analysis.ipynb

How to Run

Clone or download this repository.

Open cdc_brfss_health_data_analysis.ipynb in Jupyter Notebook, JupyterLab, or Google Colab.

Install the required libraries if necessary:

pip install numpy pandas matplotlib seaborn statsmodels requests

Run the notebook from top to bottom. The notebook retrieves the dataset from a public online source, so an internet connection is required for the initial data load.

Skills Demonstrated

Exploratory data analysis

Descriptive statistics

Data filtering and subsetting

Feature engineering

Categorical and numerical data visualization

Interpretation and communication of analytical findings

Acknowledgements

This project was completed as an educational data-analysis lab. The original lab was adapted by David Akman and Imran Ture from OpenIntro materials by Andrew Bray and Mine Çetinkaya-Rundel. The analysis responses, Python implementation, interpretations, and portfolio documentation are presented here for learning and professional-development purposes.
