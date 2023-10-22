# A-B-Testing

![image](https://github.com/oktaydoganyildiz/A-B-Testing/assets/70387935/e423d56b-edb6-48e2-9e34-722efe337af4)

This repository contains the code and documentation for an A/B testing project that compares different bidding methods.



# Business Problem 👩‍💻
Facebook recently introduced a new bidding type called "average bidding" as an alternative to the existing "maximum bidding." One of our clients,has decided to test this new feature and wants to conduct an A/B test to determine whether "average bidding" results in more conversions than "maximum bidding." The A/B test has been running for one month, and bombabomba.com is now expecting you to analyze the results of this A/B test. The ultimate success metric for bombabomba.com is "Purchase," so the focus for statistical tests should be on the "Purchase" metric.



# The Goal of the Project 🎯
As a company that will advertise on Facebook, we want to understand which option is more advantageous for us.
Which of these two options will increase our number of clicks and purchases?
Is there a significant difference between the two options?
To find the answer to these questions, we are applying the AB Test today.


# Procedure

![image](https://github.com/oktaydoganyildiz/A-B-Testing/assets/70387935/23d54cbb-e2f6-46dc-890e-651978888ebb)

1. **Formulate Hypotheses**:
   - **Null Hypothesis (H0)**: There is no statistically significant difference between the two groups.
   - **Alternative Hypothesis (H1)**: There is a statistically significant difference between the two groups.

2. **Assumption Checks**:

   a. **Normality Assumption (Shapiro-Wilk Test)**:
      - H0: Data follows a normal distribution.
      - H1: Data does not follow a normal distribution.

   b. **Homogeneity of Variance (Levene Test)**:
      - H0: The variances between the two groups are equal (homogeneous).
      - H1: The variances between the two groups are not equal (heterogeneous).

   - Both tests are used to check assumptions for independent samples.

3. **Hypothesis Testing**:
   - Depending on the status of the assumptions, two different tests are conducted:

   a. **If Assumptions Are Met - Independent Two-Sample t-Test**:
      - H0: There is no statistically significant difference between the two groups.
      - H1: There is a statistically significant difference between the two groups.

   b. **If Normality or Homogeneity of Variance Assumptions Are Not Met - Mann-Whitney U Test**:
      - The Mann-Whitney U test is used when these assumptions are violated, and it is used to determine differences in medians.

4. **Interpret Results Based on the p-value**:

   - In the case of the independent two-sample t-test:
      - If p-value < α (the chosen significance level), H0 is rejected, and it is concluded that there is a statistically significant difference between the two groups.
      - If p-value ≥ α, the null hypothesis is not rejected, indicating no statistically significant difference.



