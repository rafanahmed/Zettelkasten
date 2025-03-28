

2025-03-18 
11:14 PM


Tags: [[Hypotheses Testing]], [[Statistics]], [[Z-Test]], [[Significance Level]]


## Reference: 
![[Lecture6.pdf]]



###### P Value:
Definition:
- The p-value is the probability (assuming H0 (the null hypothesis) is TRUE) that the test statistic would take a value as extreme or more extreme than the observed one. 
- The smaller the p-value, the stronger the evidence AGAINST H0 (the null hypothesis)
Interpretation:
- It measures whether the test statistic is likely or unlikely under H0.
- Small p-values suggest that the null hypothesis (H0) is unlikely
- The smaller the p-value, the stronger the case for rejecting the null hypothesis
Decision Rule:
- You are able to make a decision on whether or not H0 (null hypothesis) should be rejected by comparing the p-value to the chosen significance level (denoted as α) 
- Reject null hypothesis (H0) if p-value <= α (significance level).
- DO NOT Reject H0 if p-value > α



###### Large Sample Test for Population Mean:

For n>= 30, assuming normally:
- Two Tailed Test:![[IMG_7B096749E7BD-1.jpeg]]
	- Ha : μ =/= μ0,​ where
		- Ha = Alternative hypothesis, which is the statement that contradicts the null hypothesis (H0) and represents the claim we are trying to provide evidence for.
		- μ = population mean (true mean of the population)
		- μ0 = hypothesized population mean (value we test against H0)
	- P-value: 2 * P(Z > |Z∗|), where
		- Z* (Test Statistic): Standardized value of our sample mean (xˉ) compared to the null hypothesis mean (μ0) using this formula: Z* = (xˉ - μ0) / (s / √n)
	- Area in red = Reject H0
- Left-tailed Test: ![[IMG_205473F34BB8-1.jpeg]]
	- Ha : μ < μ0
	- P-value: P(Z < Z*)
	- Area in red = Reject H0
- Right-Tailed Test: ![[IMG_1BA0BCED69C5-1.jpeg]]
	- Ha : μ > μ0
	- P-value: P(Z > Z*)
	- Area in red = Reject H0

Example 1:
A homeowner wants to estimate the average house price in the neighborhood. She randomly samples 64 homes similar to hers and finds that the average selling price is $252,000 with a standard deviation of $15,000. Is this sufficient evidence to conclude that the average selling price exceeds $250,000? Use α = .01.
Solution:
 - ![[IMG_29C8ABF501DB-1.jpeg]]
 - Answer: There is not enough evidence to conclude that the average house price is greater than $250,000 at the 1% significance level

Example 2:
The daily yield for a chemical plant has averaged 880 tons for several years. The quality control manager wants to know if this average has changed. She randomly selects 50 days and records an average yield of 871 tons with a standard deviation of 21 tons. Conduct the test using α=.05.
Solution:
- ![[Example2Lecture6.pdf]]
- Answer: The data provide significant evidence at the 0.05 level that the average daily yield has changed from 880 tons, with the observed decrease being statistically significant.

Example 3:
A sprinkler system is designed so that the average time for the sprinklers to activate after being turned on is no more than 15 seconds. An agency claims that the system may not work as it proposes. A test of 6 systems gave the following times: 17, 31, 12, 17, 13, 25. Test agency’s claim using a = .05.
Solution:
- ![[IMG_9728EE733AAA-1.jpeg]]
- Answer: There is insufficient evidence at the 5% level to support the claim that the average activation time is greater than 15 seconds.


