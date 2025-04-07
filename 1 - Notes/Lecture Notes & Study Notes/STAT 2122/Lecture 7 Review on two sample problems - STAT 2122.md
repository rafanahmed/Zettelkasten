

2025-04-06 
07:35 PM


Tags: [[Statistics]], [[Hypotheses Testing]], [[Z-Test]], [[Significance Level]], [[T-Test]]


## Reference:
![[Lecture7.pdf]]



## Types of Samples in Comparative Studies:

#### Two Large Independent Samples
- **Scenario**: Comparing groups where each sample is sufficiently large (typically *n* >= 30).
- **Example**: Determining if there is a difference in the average daily dairy product intake between men and women :
	- **Men**: Sample size  = 50, Sample mean = 736, Sample standard deviation = 35
	- **Women**: Sample size = 50, Sample mean = 762, Sample standard deviation = 30
This scenario assumes that the samples are randomly selected and independent.

#### Two Small Independent Samples
- **Scenario**: Comparison using small samples (where sample sizes are less than 30) under the assumption that both populations are normally distributed and have equal variances.
- **Example**: Investigating whether increasing calcium intake reduces blood pressure.
	- **Study Design:** A randomized comparative experiment with 21 healthy black men.
	- **Grouping:** 10 received a calcium supplement for 12 weeks, while 11 received a placebo.
	- **Response Variable:** Decrease in systolic blood pressure (measured in mm Hg), where a decrease is positive and an increase is recorded as a negative response.

#### Two Dependent Samples (Paired Data)
- **Scenario:** When the same subjects are measured twice (before and after an intervention) or when samples are naturally paired.
- **Example:** A pharmaceutical company claims that its medicine lowers blood pressure. Data for 5 patients are recorded before and after taking the medication.
	- **Data table**: ![[Screenshot 2025-04-06 at 8.33.56 PM.png]]
- **Objective**: At α=0.05, test if there is enough evidence to support the company’s claim.

------------------------------------------------------------------------

## Testing Differences Between Two Population Means

#### Large Sample Test for Difference Between Two Population Means
- **Hypotheses**:
	- **Two-Tailed**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} \neq D_{0} $$
	- **Right-Tail**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} > D_{0} $$
	- **Left-Tail**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} < D_{0} $$
- (Note: D_{0} is usually 0 when testing for no difference)

- **Test Statistic**:
	- For large samples$$n_{1}\geq 30 \text{ and } n_{2} \geq 30$$the test statistic is:$$z = \frac{(\bar{x}_{1}- \bar{x}_{2}) - D_{0}}{\sqrt{\frac{s_{1}^2}{n_{1}} + \frac{s_{2}^2}{n_{2}}}}$$Under H_{0}, *z* follows an approximately standard normal distribution. 

- **p-Value Computation**:
	- **Two-tailed:** Compare |z| against the critical value from the standard normal distribution.
	- **One-tailed**: Use the appropriate tail (right or left) of the standard normal distribution.

- **Example Revisited**:
	- Using the dairy products example, with α=0.05, the test would involve computing the *z*-statistic with the provided sample means, standard deviations, and sizes.

#### Small Sample Test for Difference Between Two Population Means
- **Assumptions**:
	- Both populations are normally distributed.
	- The populations have equal variances.

- **Hypotheses**:
	- Same as for the large sample test:
		-  **Two-Tailed**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} \neq D_{0} $$
		- **Right-Tail**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} > D_{0} $$
		- **Left-Tail**:$$H_{0} : \mu_{1} - \mu_{2} = D_{0} \quad \text{vs.} \quad H_{a} : \mu_{1} - \mu_{2} < D_{0} $$

- **Test Statistic**:
	- The test statistic is given by: $$t = \frac{(\bar{x}_{1} - \bar{x}_{2} - D_{0})}{s_{p}\sqrt{ \frac{1}{n_{1}}+\frac{1}{n_{2}} }}$$where the pooled standard deviation s_{p} is computed as: $$s^2_{p} = \frac{(n_{1} - 1)s^2_{1}+(n_{2} - 1)s^2_{2}}{n_{1}+n_{2}-2}$$Under H_{0}, *t* follows a Student's *t*-distribution with $$n_{1}+n_{2}-2$$degrees of freedom

- **p-Value Computation**:
	- **Two-tailed:** Calculate the probability that |t| exceeds the observed value.
	- **One-tailed:** Use the appropriate tail of the *t*-distribution.

- **Example**:
	- Comparing two training procedures:
		- **Method 1:** $$n = 10, \bar{x} = 35, s=4.9$$
		- **Method 2:**$$n= 12, \bar{x} = 31, s= 4.5$$
	With α=0.01 the test statistic is computed using the above formula and compared against the critical value from the *t*-distribution with 10+12−2=20 degrees of freedom.

------------------------------------------------------------------------
## The Paired-Difference Test 

#### Context and Rationale:
- **When to Use**: Applied when the two samples are not independent but rather paired (e.g., measurements before and after treatment on the same subjects). This design helps eliminate variability due to individual differences.
- **Data Notation**: For *n* pairs, denote the measurements as:$$x_{1i} \quad \text{and} \quad x_{2i} \quad \text{for } i = 1, 2, \dots, n,$$with the difference $$d_{i} = x_{i} - x_{2}$$
#### Hypotheses:
- **Two-tailed**: $$H_{0}: \mu_{d} = D_{0} \quad \text{vs} \quad H_{a} : \mu_{d} \neq D_{0}$$
- **Right-Tail**:$$H_{0}: \mu_{d} = D_{0} \quad \text{vs} \quad H_{a} : \mu_{d} > D_{0}$$
- **Left-Tail**: $$H_{0}: \mu_{d} = D_{0} \quad \text{vs} \quad H_{a} : \mu_{d} < D_{0}$$
- Typically, D_{0} = 0 when testing for no difference

#### Test Statistic:
- For small samples, the test statistic is:$$t = \frac{\bar{d} - D_{0}}{s_{d} / \sqrt{ n }}$$where:
	- *d bar* is the sample mean of the differences
	- s_{d} is the sample standard deviation of the differences.
	- Under H_{0}, *t* follows a Student's *t*-distribution with *n* - 1 degrees of freedom

- **p-Value Computation**:
	- Compute the p-value corresponding to the observed *t* value using the *t*-distribution with n - 1 degrees of freedom. 

#### Example:
For the pharmaceutical company’s claim regarding blood pressure:
- **Data**:
  Before: 120, 150, 140, 135, 130
  After: 125, 130, 130, 140, 120
- The test would involve computing the differences for each patient, calculating *d bar* and s_{d}​, and then using the *t*-statistic to test the claim at α=0.05.

------------------------------------------------------------------------

## F-Distribution and Comparing Two Population Variances

#### F-Distribution Overview:
- **Definition**: If $$s^2_{1} \text{ and } s^2_{2}$$are the sample variances from the two independent, normally distributed populations (assuming equal variances), the ratio$$F = \frac{s^2_{1}}{s^2_{2}}$$follows an F-distribution,

- **Determining Factors**: The shape of the F-distribution is determined by two degrees of freedom:
	- $$\text{d.f. (numerator)} = n_{1}-1$$
	- $$\text{d.f. (denominator)} = n_{2}-1$$

#### Properties of the F-Distribution:
- **Degrees of Freedom:** Each F-curve is defined by its numerator (d.f.N) and denominator (d.f.D) degrees of freedom.
- **Skewness:** F-distributions are positively skewed.
- **Area:** The total area under the F-distribution curve equals 1.
- **Non-negativity:** F-values are always greater than or equal to 0.
- **Mean:** For all F-distributions, the mean is approximately equal to 1.

#### Comparing Two Population Variances:
- **Example (Context):** Often the same experimental data (e.g., training procedures comparing time to assemble a device) can be used to test whether the variances are equal by applying the F-test.
- **Interpretation:** The F-test helps determine if the assumption of equal variances is reasonable, which is a key assumption in the small sample tests for means.

------------------------------------------------------------------------

## Summary and Key Insights
- **Design Choices:**
	- **Independent samples** (large vs. small) require different test statistics (z-test vs. t-test) based on sample sizes and variance assumptions.
    - **Paired designs** are especially useful for controlling individual variability.
- **Hypothesis Testing Framework**:
	- For both large and small sample tests, clear specification of null (H_{0}​) and alternative (H_{a}​) hypotheses is critical.
	- The choice of test (z, t, or paired t) is dictated by the study design and sample size.
- **F-Distribution Application**:
	- Before applying a t-test for small samples, it is common to first assess the equality of variances using the F-test.
- **Mathematical Rigor**:
	- Each step—from hypothesis formulation to p-value computation—is essential for the integrity of the statistical test.




