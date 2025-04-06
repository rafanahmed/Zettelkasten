

2025-04-06 
02:34 AM


Tags: [[Statistics]], [[Hypotheses Testing]], [[Z-Test]], [[Significance Level]]


## Reference:
![[Lecture5 2.pdf]]



## 1. Hypotheses: Definitions and Setup

**Definition:**  
A _hypothesis_ is a claim or statement about the unknown population parameter. In testing, we consider two complementary statements:

- **Null Hypothesis (H₀):**  
    The default assumption that the parameter equals a specified value.  
    **Format:**  
    𝐻₀: parameter = value
    
- **Alternative Hypothesis (Hₐ):**  
    The competing claim that the parameter is either less than, greater than, or simply not equal to the specified value.  
    **Formats:**
    
    - 𝐻ₐ: parameter < value
        
    - 𝐻ₐ: parameter > value
        
    - 𝐻ₐ: parameter ≠ value
        

_Examples from the lecture include:_

- **Business School Claim:**  
    A claim that MBA graduates earn more than $85,000 per year.
    
    - **Claim:** μ > 85000
        
    - **Hₐ:** μ > 85000
        
    - **H₀:** μ ≤ 85000
        
- **Automobile Battery Life:**  
    A report stating the battery life is 74 months.
    
    - **Claim:** μ = 74
        
    - **H₀:** μ = 74
        
    - **Hₐ:** μ ≠ 74
        
- **Radio Station Audience:**  
    A claim that the station captures more than 39% of the local audience.
    
    - **Claim:** p > 0.39
        
    - **H₀:** p ≤ 0.39
        
    - **Hₐ:** p > 0.39

------------------------------------------------------------------------
## 2. Common Mistakes in Setting Hypotheses

Two errors are highlighted as frequent pitfalls:

- **Mistake 1:**  
    Using a sample statistic instead of the population parameter (e.g., writing H₀: X = 10 rather than H₀: μ = 10).
    
- **Mistake 2:**  
    Mismatching the values in H₀ and Hₐ (e.g., H₀: μ = 10 vs. Hₐ: μ ≠ 20).  
    The hypotheses must be complementary, with both parts referring to the same parameter value.

------------------------------------------------------------------------
## 3. Determining the Tail of the Test

The direction (or tail) of a test is decided by the alternative hypothesis:

- **Left-Tailed Test:**  
    If Hₐ uses “<” (e.g., Hₐ: μ < value)
    
- **Right-Tailed Test:**  
    If Hₐ uses “>” (e.g., Hₐ: μ > value)
    
- **Two-Tailed Test:**  
    If Hₐ uses “≠” (e.g., Hₐ: μ ≠ value)
    

_Examples:_

- H₀: μ = 10 vs. Hₐ: μ < 10 (left-tailed)
    
- H₀: μ = 10 vs. Hₐ: μ > 10 (right-tailed)
    
- H₀: μ = 20 vs. Hₐ: μ ≠ 20 (two-tailed)

------------------------------------------------------------------------
## 4. Decision Making in Hypothesis Testing

After performing a test, there are two possible decisions:

- **Reject H₀:**  
    Conclude that there is sufficient evidence in favor of Hₐ.
    
- **Fail to Reject H₀:**  
    Conclude that there is not enough evidence to support Hₐ.

------------------------------------------------------------------------
## 5. Types of Errors

Using the courtroom analogy:

- **Type I Error:**  
    Rejecting H₀ when it is actually true (a false positive).
    
- **Type II Error:**  
    Failing to reject H₀ when it is false (a false negative).
    

In the analogy, consider:

- **H₀:** The person is not guilty
    
- **Hₐ:** The person is guilty  
    A Type I error occurs if an innocent person is found guilty, while a Type II error happens if a guilty person is acquitted.

![[Screenshot 2025-04-06 at 3.39.51 AM.png]]

------------------------------------------------------------------------
## 6. Significance Level, Test Statistic, and Rejection Region

### **Significance Level (α):**

- **Definition:**  
    The maximum allowable probability of committing a Type I error.
    
- **Common Values:**  
    0.10, 0.05, 0.01
    
- **Trade-Off:**  
    Lowering the probability of a Type I error typically increases the risk of a Type II error, so the level is chosen based on the severity of each error.
    

### **Test Statistic:**

- **Definition:**  
    A standardized value calculated from sample data that measures how far the sample statistic is from the null hypothesis value.
    
- **Purpose:**  
    To decide whether to reject H₀.
    

### **Rejection Region:**

- **Definition:**  
    The range of values for the test statistic that leads to the rejection of H₀.
    
- **Determination:**  
    Based on the tail of the test and the significance level (α).
    

_For example, in a one-sample z test for the population mean:_

- **When to Use:**
    
    - Large sample sizes (n ≥ 30)
        
    - The parameter of interest is the population mean (μ)
        
- **Determination of Rejection Region:**  
    Depends on whether the test is left-tailed, right-tailed, or two-tailed and the chosen α level (e.g., for a left-tailed test at α = 0.05, the critical z-value is approximately -1.645).

------------------------------------------------------------------------
## 7. Standardized Test Statistic and μ₀

- **Standardized Test Statistic:**  
    It measures how far the sample mean (or proportion) deviates from the hypothesized population parameter (μ₀) in units of standard error.  
    The typical formula for a z test is:$$z = \frac{\bar{x} - \mu_{o}}{\sigma / \sqrt{n }}$$Where:
    - **x bar (Sample Mean)**:
	    - This is the average of the observations in your sample.
	    - It is calculated as:$$\bar{x} = \frac{x_{1}+x_{2}+\dots+x_{n}}{n}$$where $$x_{1}+x_{2}+\dots+x_{n}$$are the individual sample data points and n is the number of observations (number of data points itself)
	    
	- **μ₀ (Hypothesized Mean)**:
		- This is the value of the population mean assumed under the null hypothesis H₀
		- In other words, H₀ often states that the true mean μ is equal to μ₀.
		
	- **σ (Population Standard Deviation)**:
		- This represents the standard deviation of the population.
		- In a true *z* test scenario, σ is assumed to be known. If σ is unknown and the sample size is not large, one typically uses a *t*-test with the sample standard deviation *s*.
		
	- ***n* (Sample Size)**:
		- The number of observations in the sample.
		
	- **σ / n (Standard Error of the Mean)**:
		- This quantity tells us how much variability to expect in the sample mean x bar if we repeatedly sampled from the population.
		- By dividing σ by √*n*, we account for the fact that averaging *n* data points reduces variability compared to single observations.


- If |*z*| exceeds the critical value (from *z*-tables) at your chosen significance level α, you reject H₀
- If |*z*| does not exceed that threshold, you fail to reject H₀

------------------------------------------------------------------------
## 8. Detailed Examples

### **Example: Testing a Claim on Work Hours**

- **Scenario:**  
    A CEO claims that the mean workday for the firm’s accountants is less than 8.5 hours.
    
- **Sample Data:**  
    n = 36, sample mean (x̄) = 8.2 hours, sample standard deviation (s) = 0.5 hours.
    
- **Steps:**
    
    1. **Hypotheses Setup:**
        
        - H₀: μ ≥ 8.5
            
        - Hₐ: μ < 8.5
            
    2. **Calculate Test Statistic:**  
        Use the formula for the z test.
        
    3. **Determine Rejection Region:**  
        For a left-tailed test at α = 0.05, identify the critical z-value (approximately -1.645).
        
    4. **Conclusion:**  
        Compare the computed z value with the critical value to decide whether to reject H₀.
        

### **Example: Testing Pulse Rates**

- **Scenario:**  
    A study of 64 college men reports a mean pulse rate of 70 bpm with a standard deviation of 10 bpm. The goal is to test if this mean is different from the standard 72 bpm.
    
- **Steps:**
    
    1. **Hypotheses Setup:**
        
        - H₀: μ = 72
            
        - Hₐ: μ ≠ 72 (two-tailed test)
            
    2. **Calculate Test Statistic:**  
        Use the z test formula.
        
    3. **Determine Rejection Region:**  
        For a two-tailed test at α = 0.05, split α into 0.025 in each tail and find the corresponding critical z-values.
        
    4. **Conclusion:**  
        Decide based on whether the test statistic falls in the rejection region.

------------------------------------------------------------------------
## Final Notes

- **Rigor and Precision:**  
    Every step in hypothesis testing—from setting up complementary hypotheses to calculating and interpreting the test statistic—is fundamental to drawing valid conclusions about the population.
    
- **Interdependence of Components:**  
    The choice of significance level, the determination of the tail of the test, and the calculation of the test statistic all interplay to affect both Type I and Type II error probabilities.
    
- **Practical Implications:**  
    Whether testing claims about salaries, product lifetimes, or physiological measures, the systematic approach outlined ensures that conclusions are backed by standardized statistical reasoning.
    

This consolidated summary integrates all key aspects and examples from the lecture notes, maintaining mathematical precision and logical clarity throughout.

