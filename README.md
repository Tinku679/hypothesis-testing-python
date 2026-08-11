# Hypothesis Testing & Statistical Analysis Using Python

## 📌 Project Overview

This project contains practical **Hypothesis Testing** examples implemented using Python. It covers different statistical tests used in Data Analytics and Data Science to make data-driven business decisions.

The project includes:

* One-Sample Z-Test
* Two-Sample Z-Test
* One-Sample T-Test
* Two-Sample T-Test
* One-Way ANOVA
* Chi-Square Test of Independence
* Shapiro-Wilk Test for Normality
* Levene's Test for Equality of Variances
* p-value interpretation
* Null and Alternative Hypotheses
* Type I and Type II Errors
* Statistical significance

---

## 🛠️ Technologies & Libraries

* Python
* NumPy
* Pandas
* SciPy
* Statsmodels
* Matplotlib

---

# 📊 Hypothesis Testing Workflow

The general process followed in this project is:

```text
Define Business Problem
        ↓
Define H₀ and H₁
        ↓
Choose Significance Level (α)
        ↓
Select Statistical Test
        ↓
Calculate Test Statistic
        ↓
Calculate p-value
        ↓
Compare p-value with α
        ↓
Make Statistical Decision
        ↓
Business Conclusion
```

### Decision Rule

```text
If p-value ≤ 0.05
        ↓
Reject H₀
        ↓
Statistically Significant

If p-value > 0.05
        ↓
Fail to Reject H₀
        ↓
Not Statistically Significant
```

---

# 1️⃣ One-Sample Z-Test

A **One-Sample Z-Test** is used to determine whether the mean of a sample is significantly different from a known population mean.

### Example

A manufacturing company produces tablets with a target weight of **500 mg**.

* Population Mean = 500 mg
* Population Standard Deviation = 10 mg
* Sample Size = 50
* Sample Mean = 496 mg

### Hypotheses

```text
H₀: μ = 500

H₁: μ ≠ 500
```

A two-tailed Z-Test is performed to determine whether the machine has significantly deviated from the target.

---

# 2️⃣ Two-Sample Z-Test

A **Two-Sample Z-Test** compares the means of two independent samples.

## 🛒 E-Commerce A/B Testing — StyleHub

### Business Problem

StyleHub, a fictional online fashion retailer, wants to test whether a new checkout page can increase **Average Order Value (AOV)**.

Two checkout designs are tested:

* Design A → Existing checkout
* Design B → New checkout

Data is collected from **200 users for each design**.

### Hypotheses

```text
H₀: μA - μB = 0

There is no significant difference in AOV.

H₁: μA - μB ≠ 0

There is a significant difference in AOV.
```

### Test Configuration

```text
Test              : Two-Sample Z-Test
Sample Size       : 200 per group
Significance α    : 0.05
Test Type         : Two-Tailed
Metric            : Average Order Value
```

### Business Decision

The p-value is compared with α = 0.05.

```text
p-value < 0.05
→ Reject H₀
→ Significant difference in AOV

p-value ≥ 0.05
→ Fail to Reject H₀
→ No statistically significant difference
```

This example demonstrates how statistical testing can help an e-commerce company decide whether a new checkout design should be launched.

---

# 3️⃣ One-Sample T-Test

A **One-Sample T-Test** is used when comparing a sample mean against a known value when the population variance is unknown.

### Example: Delivery Time

An online food delivery company claims:

```text
Average Delivery Time = 30 minutes
```

A sample of delivery times is collected.

### Hypotheses

```text
H₀: μ = 30

H₁: μ > 30
```

This is a **Right-Tailed Test** because the business wants to know whether delivery time is greater than 30 minutes.

The project also demonstrates the **Shapiro-Wilk test** to check normality.

---

# 4️⃣ Two-Sample T-Test

A Two-Sample T-Test is used to compare the means of two independent groups when population variance is unknown.

### Example: Department Salaries

An HR department wants to determine whether employees in Department A and Department B have different average salaries.

### Hypotheses

```text
H₀: μA = μB

H₁: μA ≠ μB
```

### Assumption Checks

Before performing the test:

1. **Shapiro-Wilk Test**

   * Checks normality.

2. **Levene's Test**

   * Checks equality of variances.

3. **Independent Two-Sample T-Test**

   * Used to compare the group means.

---

# 5️⃣ One-Way ANOVA

**ANOVA (Analysis of Variance)** is used to compare the means of **three or more independent groups**.

### Example: Marketing Campaign

A marketing team wants to determine whether user engagement differs across:

* TikTok
* Instagram
* LinkedIn

### Hypotheses

```text
H₀: μTikTok = μInstagram = μLinkedIn

H₁: At least one group mean is different
```

### Assumptions

* Data should be approximately normally distributed.
* Groups should have similar variances.
* Observations should be independent.

### Tests Used

```text
Shapiro-Wilk
      ↓
Normality

Levene's Test
      ↓
Equal Variances

One-Way ANOVA
      ↓
Compare Group Means
```

If ANOVA assumptions are violated, a **Kruskal-Wallis test** can be considered.

---

# 6️⃣ Chi-Square Test of Independence

The **Chi-Square Test of Independence** is used to determine whether two categorical variables are associated.

### Example: Advertisement Channel vs Purchase

A D2C company runs advertisements through:

* Instagram
* YouTube
* Google

The company wants to determine whether the advertisement channel is associated with the customer's purchase decision.

### Variables

```text
Ad Channel
→ Instagram
→ YouTube
→ Google

Purchase Decision
→ Purchased
→ Not Purchased
```

### Hypotheses

```text
H₀:
Ad Channel and Purchase Decision are independent.

H₁:
Ad Channel and Purchase Decision are not independent.
```

If the p-value is less than 0.05, there is evidence of a statistically significant association.

---

# 📚 Other Business Problems Covered

The project also contains practical statistical examples from different domains:

| Domain             | Business Problem               | Statistical Test  |
| ------------------ | ------------------------------ | ----------------- |
| Manufacturing      | Tablet weight calibration      | One-Sample Z-Test |
| Food Manufacturing | Energy bar weight              | One-Sample Z-Test |
| Healthcare         | Resting heart rate             | One-Sample Z-Test |
| Cloud Computing    | SLA uptime                     | One-Sample Z-Test |
| E-Commerce         | Checkout A/B Testing           | Two-Sample Z-Test |
| Food Delivery      | Delivery time                  | One-Sample T-Test |
| HR                 | Department salaries            | Two-Sample T-Test |
| Mobile Apps        | App download size              | Two-Sample T-Test |
| Manufacturing      | Battery supplier comparison    | Two-Sample T-Test |
| Marketing          | Social media engagement        | ANOVA             |
| HR                 | Training program effectiveness | ANOVA             |
| Cloud Computing    | Upload speed comparison        | ANOVA             |
| Retail             | Store waiting time             | ANOVA             |
| Marketing          | Ad channel vs purchase         | Chi-Square        |
| Banking            | Housing status vs loan default | Chi-Square        |

---

# 📈 Statistical Concepts Covered

## Null Hypothesis (H₀)

The default assumption that there is **no significant difference or relationship**.

## Alternative Hypothesis (H₁)

The claim that there **is a significant difference or relationship**.

## Significance Level (α)

The threshold used to determine statistical significance.

```text
α = 0.05
```

means we use a 5% significance level.

## p-value

The probability of observing a result as extreme as, or more extreme than, the observed result assuming H₀ is true.

---

# ⚠️ Type I and Type II Errors

### Type I Error

Rejecting H₀ when H₀ is actually true.

```text
False Positive
```

### Type II Error

Failing to reject H₀ when H₀ is actually false.

```text
False Negative
```

### Statistical Power

```text
Power = 1 - β
```

where β represents the probability of a Type II error.

---

# 💻 Example Python

```python
from statsmodels.stats.weightstats import ztest
import numpy as np

np.random.seed(42)

design_a_aov = np.random.normal(
    loc=120,
    scale=15,
    size=200
)

design_b_aov = np.random.normal(
    loc=125,
    scale=18,
    size=200
)

z_stat, p_value = ztest(
    design_a_aov,
    design_b_aov,
    value=0
)

alpha = 0.05

print(f"Z-Statistic: {z_stat:.4f}")
print(f"P-Value: {p_value:.4f}")

if p_value < alpha:
    print("Reject Null Hypothesis")
    print("There is a significant difference in AOV.")
else:
    print("Fail to Reject Null Hypothesis")
    print("No significant difference found.")
```

---

# 🎯 Key Learning

This project helped me understand how **statistical hypothesis testing** can be applied to real-world business problems.

Through these examples, I practiced:

* Translating business problems into statistical hypotheses
* Selecting the appropriate statistical test
* Understanding one-tailed and two-tailed tests
* Calculating test statistics
* Interpreting p-values
* Checking statistical assumptions
* Making data-driven conclusions
* Connecting statistical results with business decisions

---

# 🚀 Future Improvements

* Add confidence intervals
* Add effect size calculations
* Add power analysis
* Add post-hoc tests for ANOVA
* Add interactive visualizations
* Add more real-world datasets
* Build a Power BI dashboard for selected experiments

---

# 👨‍💻 Author

**Tinku Payal**

Aspiring Data Analyst | Python | SQL | Statistics | Power BI

Currently building practical skills in **Data Analytics, Python, SQL, Statistics, and Power BI**.

---

## ⭐ If you find this project useful

Feel free to ⭐ star the repository and explore the Python examples.

