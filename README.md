Hypothesis Testing & Statistical Analysis with Python

A practical Python-based collection of Hypothesis Testing problems covering Z-Test, T-Test, ANOVA, and Chi-Squared Test with business-oriented examples.

This project contains practical statistical problem statements, hypotheses, Python implementations, assumption checks, p-value interpretation, and decision-making logic.

📌 Project Overview

The goal of this project is to understand how statistical hypothesis testing can be applied to real-world business and analytical problems.

Topics Covered

Null Hypothesis (H₀) and Alternative Hypothesis (H₁)

Significance Level (α)

p-value

Type I Error and Type II Error

Statistical Power

One-Sample Z-Test

Two-Sample Z-Test

One-Sample T-Test

Two-Sample T-Test

Shapiro-Wilk Normality Test

Levene's Test for Equality of Variances

One-Way ANOVA

Kruskal-Wallis Test

Chi-Squared Test of Independence

One-tailed and Two-tailed Tests

Business interpretation of statistical results

🧪 Statistical Testing Workflow

The project follows this general hypothesis-testing process:

State the Null and Alternative Hypotheses

Select the Significance Level (α)

Choose the Appropriate Statistical Test

Calculate the Test Statistic

Calculate the p-value

Compare p-value with α

Make a statistical decision

Interpret the result in a business context

Decision Rule

p-value ≤ 0.05 → Reject H₀

p-value > 0.05 → Fail to Reject H₀

📊 Projects & Business Problem Statements

1. E-Commerce A/B Testing — Average Order Value

Business Problem:StyleHub, an online fashion retailer, is testing a new checkout page design (Design B) against the existing Design A. The objective is to determine whether there is a statistically significant difference in Average Order Value (AOV).

Sample:

Design A: 200 users

Design B: 200 users

Hypotheses:

H₀: μA − μB = 0

H₁: μA − μB ≠ 0

Test Used: Two-Sample Z-TestSignificance Level: α = 0.05Test Type: Two-tailed

The Python implementation simulates AOV data for both designs and uses a two-sample Z-test to evaluate whether the observed difference is statistically significant.

2. Manufacturing Quality Control

Tests whether a pharmaceutical tablet's average active ingredient content differs from the target of 500 mg when the population standard deviation is known.

Test: One-Sample Z-Test

3. Food Manufacturing Quality Assurance

Tests whether the average weight of energy bars differs from the advertised target of 50 grams.

Test: One-Sample Z-Test

4. Resting Heart Rate Analysis

Tests whether the average resting heart rate of a sample is below a known population mean.

Test: Left-Tailed One-Sample Z-Test

5. Cloud Service SLA Analysis

Tests whether average monthly cloud-service uptime differs from a 99.9% SLA guarantee.

Test: Two-Tailed One-Sample Z-Test

6. Zomato Delivery Time Analysis

Tests whether the average delivery time is greater than the claimed 30 minutes.

Test: One-Sample T-TestAlternative: Right-tailed

The project also demonstrates the Shapiro-Wilk test for checking normality.

7. Beverage Quality Control

Tests whether the average soda-can content differs from the claimed 330 ml.

Test: One-Sample T-Test

8. Call Center Efficiency

Evaluates whether a new employee training program significantly changes Average Handle Time (AHT) from the 300-second KPI.

Test: One-Sample T-Test

9. Employee Salary Comparison

Compares average monthly salaries between two departments.

Test: Independent Two-Sample T-Test

Assumptions checked using:

Shapiro-Wilk Test

Levene's Test

Welch's t-test is used when equal variance cannot be assumed.

10. App Download Size Comparison

Compares average app download sizes between Apple's App Store and Google's Play Store using a sample of matched apps.

Test: Independent Two-Sample T-Test

11. Customer Spending Analysis

Tests whether average order value differs between male and female customers.

Test: Independent Two-Sample T-TestTest Type: Two-tailed

12. Battery Supplier Comparison

Compares battery life between two suppliers using small samples.

Test: Independent Two-Sample T-Test

Because the sample size is below 30, a t-test is used instead of a Z-test.

13. Marketing Campaign Effectiveness

Compares user engagement scores across TikTok, Instagram, and LinkedIn.

Test: One-Way ANOVA

Assumptions checked using:

Shapiro-Wilk Test

Levene's Test

If ANOVA assumptions are seriously violated, the project considers the Kruskal-Wallis test.

14. Employee Training Program Analysis

Compares performance scores across three training programs:

Online

In-Person

Blended

Test: One-Way ANOVA

15. Cloud Provider Upload Speed Analysis

Compares upload speeds across:

AWS

Azure

Google Cloud Platform

Test: One-Way ANOVA

The project also includes visualization of group distributions and mean upload speeds.

16. Store Customer Wait-Time Analysis

Tests whether average customer wait time differs across four store locations.

Test: One-Way ANOVA

17. Advertising Channel & Purchase Decision

Tests whether advertising channel is associated with purchase decision.

Categorical Variables:

Ad Channel

Purchase Decision

Test: Chi-Squared Test of Independence

18. Cuisine Type & Customer Satisfaction

Tests whether cuisine type is associated with customer satisfaction.

Test: Chi-Squared Test of Independence

19. Housing Status & Loan Default Risk

Tests whether housing status is associated with loan default status.

Test: Chi-Squared Test of Independence

🛠️ Technologies Used

Python

NumPy

Pandas

SciPy

Statsmodels

Matplotlib

📁 Project Structure

hypothesis-testing/
│
├── hypothesis_testing_problem_statements.py
├── README.md
└── anova_problem1.png

anova_problem1.png is generated by the ANOVA cloud-provider example when the Python code is executed.

▶️ How to Run

1. Clone the repository

git clone https://github.com/your-username/hypothesis-testing.git
cd hypothesis-testing

2. Install dependencies

pip install numpy pandas scipy statsmodels matplotlib

3. Run the Python file

python hypothesis_testing_problem_statements.py

You can also open the file in Jupyter Notebook or Google Colab and execute the examples step by step.

📈 Key Statistical Concepts

Z-Test

Used in this project for situations where the population standard deviation is known and the sample size is large.

T-Test

Used when the population standard deviation is unknown, especially for smaller samples.

ANOVA

Used to compare the means of three or more independent groups.

Chi-Squared Test

Used to determine whether two categorical variables are statistically associated.

💡 Key Learning

This project demonstrates how statistical testing can be used to move from sample data to evidence-based decisions.

The main learning points include:

Formulating business questions as statistical hypotheses

Selecting an appropriate statistical test

Checking assumptions before testing

Understanding p-values and significance levels

Interpreting one-tailed and two-tailed tests

Making decisions using statistical evidence

Translating statistical results into business conclusions

🎯 Business Decision-Making Example

In the StyleHub A/B testing example, Design B may show a higher AOV than Design A. However, a higher sample average alone does not prove that the new design performs better.

If the p-value is greater than 0.05, the difference is not statistically significant. In that situation, the correct statistical conclusion is to fail to reject H₀ rather than claim that Design B is better.

From a business perspective, the company could continue collecting data or run a longer experiment before making a final rollout decision.

👨‍💻 Author

Tinku Payal

Data Analytics | Python | SQL | Statistics | Power BI
