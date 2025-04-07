

2025-04-07 
01:32 AM


Tags: [[Statistics]], [[Hypotheses Testing]], [[Chi-Square Test]]


## Reference:
![[Lecture8.pdf]]



## Chi-Square Goodness-of-Fit Test (One-Way Table)

#### Overview:
- **Purpose**:
	- To compare the observed frequency counts for a single categorical variable with the counts expected under a hypothesized distribution.

#### Example: M&M's Milk Chocolate Candies
- **Company Claim**:
	- Mars, Incorporated asserts that the new mix of M&M’s Milk Chocolate Candies has the following color proportions:
		- Brown: 13%
		- Red: 13%
		- Yellow: 14%
		- Green: 16%
		- Orange: 20%
		- Blue: 24%
- **Observed Data (Sample of 60 Candies)**:
	- ![[Screenshot 2025-04-07 at 1.48.57 AM.png]]
- **Expected Counts Calculation**:
	- The expected count for each color is calculated by multiplying the sample size (60) by the claimed proportion. For example, for blue:$$\text{Expected Blue }= 0.24 \times 60 = 14.4$$Similarly, the expected counts for the other colors are:
		- Orange: $$0.20 \times 60 = 12.0$$
		- Green: $$0.16 \times 60 = 9.6$$
		- Yellow: $$0.14 \times 60 = 8.4$$
		- Red: $$0.13 \times 60 = 7.8$$
		- Brown: $$0.13 \times 60 = 7.8$$
- **Chi-Square Statistic**: 
	- The test statistic is defined as: $$\chi^2 = \sum \frac{\text{(Observed - Expected)}^2}{\text{Expected}}$$In the example, the calculation is:$$\chi^2 = \frac{(9 - 14.4)^2}{14.4}
+ \frac{(8 - 12.0)^2}{12.0}
+ \frac{(12 - 9.6)^2}{9.6}
+ \frac{(15 - 8.4)^2}{8.4}
+ \frac{(10 - 7.8)^2}{7.8}
+ \frac{(6 - 7.8)^2}{7.8}
\approx 10.180$$
- **Degrees of Freedom**:
	- With 6 categories, the degrees of freedom are: $$\text{df }= k-1=6-1=5$$
- **Interpreting the p-Value**:
	- The p-value is determined by finding the tail area above the computed χ^2 value using the chi-square distribution with 5 degrees of freedom.
	- A large χ^2 statistic (with a small p-value) suggests that the observed counts differ significantly from the expected counts.

#### Additional Example: “When Were You Born?”
- **Context**:
  A sample of 140 births is collected to examine if births are evenly distributed across the days of the week.
- **Data**:
  The counts for Sunday through Saturday are provided. The test would check if these observed frequencies differ significantly from what would be expected if births were uniformly distributed.

------------------------------------------------------------------------

## Chi-Square Test for Independence (Two-Way Table)

#### Overview
- **Purpose**: 
	- To determine whether there is a significant association between two categorical variables.

#### Example: Student Survey on Goals
- **Scenario**:
	- Students in grades 4–6 are surveyed about what they consider most important: good grades, athletic ability, or popularity.
	- The responses are tabulated in a two-way table with the categories defined by grade and by goal.
- **Hypotheses**:
	- **Null Hypothesis (H_{0})**:
		- Grade and goals are independent (i.e., the distribution of goals is the same across different grades).
	- **Alternative Hypothesis (H_{a})**:
		- Grade and goals are dependent (i.e., the distribution of goals varies by grade).
- **Expected Counts in Two-Way Tables:**
	- The expected count for a cell in the table is calculated as: $$\text{Expected Count} = \frac{(\text{Row Total}) \times (\text{Column Total})}{\text{Grand Total}}$$
- **Test Statistic**:
	- The chi-square statistic is computed in the same way:$$\chi^2 = \sum \frac{\text{(Observed - Expected)}^2}{\text{Expected}}$$The degrees of freedom for the test are: $$\text{df }= (\text{number of rows } - 1) \times (\text{number of columns} - 1)$$
- **p-Value and Conclusion:**
	- The p-value is obtained from the chi-square distribution with the computed degrees of freedom.
	- A small p-value (typically < 0.05) leads to rejection of H_{0}, indicating that there is an association between the variables. 

------------------------------------------------------------------------

## Conditions for Using Chi-Square Tests
- **Adequate Expected Cell Counts**:
	- For a 2-by-2 table: all cells should have an expected count of 5 or more.
	- For larger tables: at least 80% of the cells should have an expected count of 5 or more, and no cell should have an expected count of zero.
- **Independence**:
	- The observations must be independent. Chi-square tests are not appropriate for correlated data (e.g., matched pairs or panel data).

------------------------------------------------------------------------

## Summary and Key Points
- **Chi-Square Goodness-of-Fit Test**:
	- Compares observed counts with expected counts to assess whether a categorical variable conforms to a specified distribution.
	- The M&M’s example illustrates how to calculate expected counts, compute the chi-square statistic, and interpret the test using degrees of freedom.
- **Chi-Square Test for Independence:**
	- Examines whether two categorical variables are related by comparing observed cell frequencies to those expected under the assumption of independence.
- **Practical Considerations:**
	- Ensure adequate cell counts and independence of observations to validate the use of these tests.



