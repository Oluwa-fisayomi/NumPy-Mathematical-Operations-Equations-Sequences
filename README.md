# Industry-Based Hands-On Exercises — NumPy

## PSG: NumPy Mathematical Operations, Equations & Sequences

## Overview

This project contains my solutions to the Industry-Based Hands-On Exercises for the PSG NumPy lesson.

The exercises were designed to move beyond simply writing NumPy syntax and instead focus on applying NumPy to numerical problems in different real-world industries.

The main approach throughout the project was:

> Understand the problem → Represent the data → Perform the calculation → Inspect the result → Explain what the result means.

The project contains three industry-based exercises:

1. Business Analytics — Sales Performance Calculator
2. Education Analytics — Student Performance Analysis
3. Engineering & Scientific Computing — Trigonometric Series and Convergence

It also includes a Bonus Challenge involving a sports performance analysis.

---

## Objectives

The objectives of this project were to:

* Create and work with NumPy arrays.
* Inspect array types and shapes.
* Perform mathematical calculations using NumPy.
* Calculate totals and averages.
* Perform element-wise array operations.
* Calculate deviations from an average.
* Square numerical values.
* Use mathematical functions such as `np.sin()` and `np.radians()`.
* Create numerical sequences using `np.arange()`.
* Use `np.sum()` and `np.mean()`.
* Investigate how mathematical results change as the number of terms increases.
* Interpret numerical results in real-world contexts.
* Practice explaining what calculations mean rather than only displaying outputs.

---

# Exercise 1 — Business Analytics

## Sales Performance Calculator

### Scenario

A growing retail business recorded its daily sales for one week.

The objective was to use NumPy to analyze the business's weekly sales performance.

### Dataset

```python
daily_sales = np.array([125000, 150000, 175000, 140000, 190000, 210000, 160000])
```

### Tasks Completed

The exercise covered:

* Creating a NumPy array.
* Checking the array type.
* Checking the array shape.
* Calculating total weekly sales.
* Calculating average daily sales.
* Applying a hypothetical 10% sales increase.
* Comparing the original and adjusted sales.
* Interpreting the total and average sales figures.

### Key Results

Total weekly sales:

```text
₦1,150,000
```

Average daily sales:

```text
₦164,285.71
```

The 10% adjustment was performed using:

```python
adjusted_sales = daily_sales * 1.10
```

The `1.10` represents the original 100% plus a 10% increase.

### Business Interpretation

The business generated ₦1,150,000 in total sales during the week, with an average daily sales value of approximately ₦164,285.71.

The total sales figure provides an overview of the entire week's revenue, while the average daily sales figure provides an understanding of the typical daily performance.

---

# Exercise 2 — Education Analytics

## Student Performance Analysis

### Scenario

A training program recorded the scores of a group of students.

The objective was to understand the students' overall performance and determine how individual scores differed from the group average.

### Dataset

```python
scores = np.array([62, 75, 81, 69, 88, 94, 73, 85, 77, 91])
```

### Tasks Completed

The exercise covered:

* Creating and inspecting a NumPy array.
* Calculating the mean score.
* Calculating each student's deviation from the mean.
* Identifying positive and negative deviations.
* Squaring the deviations.
* Calculating the sum of squared deviations.
* Connecting these steps to the process of calculating standard deviation.
* Interpreting the results in an education context.

### Key Results

Mean score:

```text
79.5
```

Sum of squared deviations:

```text
932.5
```

### Understanding Deviations

A positive deviation means a student's score is above the group average.

A negative deviation means a student's score is below the group average.

A value close to zero means the student's score is close to the group average.

For example:

```text
Score: 94
Deviation: +14.5
```

This means the score of 94 is 14.5 points above the average.

### Why Square the Deviations?

The deviations were squared using:

```python
squared_deviations = deviations ** 2
```

Squaring changes negative values into positive values. This prevents positive and negative deviations from cancelling each other out when they are combined.

### Connection to Standard Deviation

The exercise demonstrated the following conceptual process:

1. Calculate the mean.
2. Calculate deviations.
3. Square the deviations.
4. Sum the squared deviations.
5. Continue with the appropriate division.
6. Take the square root.

Standard deviation provides additional information about how spread out the student scores are around the average.

---

# Exercise 3 — Engineering & Scientific Computing

## Trigonometric Series and Convergence

### Scenario

An engineering/scientific computing team wants to understand how an approximation changes as more terms are included in a calculation.

NumPy was used to create a sequence of values, work with a trigonometric function, and observe the idea of convergence.

### Angle

The angle used was:

```python
theta = 30
```

It was converted from degrees to radians using:

```python
theta_radians = np.radians(theta)
```

The resulting value was approximately:

```text
0.5235987756
```

### Sequence

The first sequence was created using:

```python
k = np.arange(1, 100, 1)
```

This generated:

* First value: `1`
* Last value: `99`
* Number of values: `99`

### Trigonometric Calculation

The sine of the converted angle was calculated using:

```python
sin_theta = np.sin(theta_radians)
```

The result is approximately:

```text
0.5
```

### Series Terms

The individual terms were calculated using:

```python
series_terms = sin_theta / k
```

NumPy performed the division element by element across the array.

### Series Results

The experiment was repeated using progressively larger sequences.

| Number of Terms | Series Result |
| --------------: | ------------: |
|              99 |  2.5886887588 |
|             999 |  3.7422354303 |
|           9,999 |  4.8937530180 |

### Convergence Interpretation

When fewer terms were used, the calculated series result was smaller.

As more terms were added, the series result increased.

Increasing the number of terms changes the approximation because additional values are included in the calculation.

Convergence describes the behavior of a result as it gets closer to a limiting value when more terms are included.

---

# Bonus Challenge — Sports Performance Analysis

## Mini NumPy Numerical Experiment

### Scenario

A football player recorded the number of successful passes made in five matches.

The objective was to use NumPy to analyze the player's passing performance.

### Dataset

```python
matches = np.array([32, 38, 35, 42, 45])
```

### Calculations Performed

The experiment included several NumPy operations.

### 1. Total Successful Passes

```python
total_passes = np.sum(matches)
```

Result:

```text
192
```

### 2. Average Successful Passes

```python
average_passes = np.mean(matches)
```

Result:

```text
38.4
```

### 3. Deviations from the Average

```python
pass_deviations = matches - average_passes
```

Result:

```text
[-6.4, -0.4, -3.4, 3.6, 6.6]
```

### 4. Hypothetical 10% Increase

```python
projected_passes = matches * 1.10
```

Result:

```text
[35.2, 41.8, 38.5, 46.2, 49.5]
```

### 5. Additional Projected Passes

```python
additional_passes = projected_passes - matches
```

Result:

```text
[3.2, 3.8, 3.5, 4.2, 4.5]
```

### Interpretation

The player recorded a total of 192 successful passes across five matches, with an average of 38.4 successful passes per match.

The deviations show how each match compared with the average. The first match was below the average, while the fifth match was above the average.

The 10% projection demonstrated how NumPy can apply the same mathematical operation to every value in an array.

---

# NumPy Concepts Used

The project provided practical experience with the following NumPy concepts:

```python
np.array()
np.sum()
np.mean()
np.radians()
np.sin()
np.arange()
```

It also used:

```python
array * number
array - number
array ** 2
array / array
```

These operations demonstrate how NumPy can perform calculations across entire arrays without manually processing each value individually.

---

# What I Learned

Through these exercises, I practiced using NumPy for numerical analysis in different contexts.

I learned how to:

* Represent numerical data using arrays.
* Inspect NumPy arrays.
* Calculate totals and averages.
* Compare individual values with an average.
* Apply mathematical operations to entire arrays.
* Work with trigonometric functions.
* Generate numerical sequences.
* Build and analyze mathematical series.
* Observe how results change as more terms are included.
* Interpret numerical outputs in real-world scenarios.

Most importantly, the exercises helped me understand that numerical programming is not only about getting an output. It is also about understanding what the output means and how it can be useful.

---

# Project Structure

A possible GitHub repository structure is:

```text
Industry-Based-Hands-On-Exercises/
│
├── Industry-Based Hands-On Exercises.ipynb
│
└── README.md
```

The main notebook contains the Python/NumPy code, outputs, Markdown explanations, interpretations, and the Bonus Challenge.

---

# How to Run the Notebook

The exercise instructions allow the work to be completed using either Jupyter Notebook or Google Colab.

## Using Jupyter Notebook

1. Install or launch Jupyter Notebook.
2. Open the `.ipynb` file.
3. Run the cells from top to bottom.
4. Check that all outputs appear correctly.
5. Save the notebook.

## Using Google Colab

1. Open Google Colab.
2. Upload the `.ipynb` file.
3. Run the cells from top to bottom.
4. Check the outputs.
5. Save or download the completed notebook.

---

# Submission Checklist

Before submission, the notebook should:

* [x] Run without errors
* [x] Contain the required NumPy code
* [x] Contain Markdown explanations
* [x] Display the results
* [x] Include interpretation of the results
* [x] Include the three Hands-On Exercises
* [x] Include the Bonus Challenge
* [x] Have a clear notebook/repository name
* [ ] Be uploaded to GitHub
* [ ] Have the GitHub link shared according to the MLSG submission workflow

---

# Final Reflection

This project provided practical experience applying NumPy beyond basic syntax.

The exercises showed how the same numerical tools can be applied to business analytics, education analytics, engineering/scientific computing, and sports analysis.

The main takeaway from the project is:

> Don't just run the code. Understand the calculation. Don't just get the output. Interpret it.

This project strengthened my understanding of NumPy arrays, mathematical operations, sequences, and numerical analysis while also giving me practice connecting programming calculations to real-world problems.
