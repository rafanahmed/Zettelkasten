

2025-03-31 
10:50 PM


Tags: [[Discrete Math]], [[Function & Relations]], [[Number Theory]], [[Integer Properties]], [[Sequences]], [[Recursion]], [[Summation]]


## Reference:
![[Chapter 8 ITSC 2175.pdf]]



## 8.1 Sequences:

#### Key Definition:
- A **sequence** is a special type of function in which the domain is a set of consecutive integers.
	- Ex. A **sequence** can be defined to denote a student's GPA for each of the four years the student attended college. The domain of the function is $$ \{1, 2, 3, 4\} $$for each of the four years. The function *g* is specified by the numerical values for the GPA in each year:$$ g(1) = 3.67, \quad g(2) = 2.88, \quad g(3) = 3.25, \quad g(4) = 3.75 $$
	- When a function is specified as a sequence, using SUBSCRIPTS to denote the input TO the function is more common. 
	  So$$g_{k}$$is used INSTEAD OF$$g(k)$$A value *gk* is called a **term** of a sequence, and *k* is the ***index*** of *gk*. The sequence is written:$$g_{1} = 3.67, \quad g_{2} = 2.88, \quad g_{3} = 3.25, \quad g_{4} = 3.75 $$
- A sequence with a finite domain is called a **finite sequence**. 
	- A finite sequence has an initial index *m* and a final index *n*, where $$ n \geq m$$Then, $$a_{m}$$is the **initial term** and $$a_{n}$$is the **final term**$$a_{m}, \; a_{m+1}, \; \dots \;, a_{n}$$
- A sequence with an infinite domain is called an **infinite sequence**.
	- In an infinite sequence, the indices go to infinity in the positive direction.
	- There is an initial index *m*, and the sequence is defined for all indices *k* suck that k >= m:$$a_{m}, \; a_{m+1}, \; a_{m+2}, \; \dots$$
- A sequence can be specified by an **explicit formula** showing how the value of term *ak* depends on *k*.
	- For example,$$d_{k} = 2^k \text{ for } k\geq 1$$
	- The infinite sequence $$\{d_{k}\}$$starts with:$$2, 4, 8, 16, \dots$$
- ![[Screenshot 2025-03-31 at 11.48.58 PM.png]]
- ![[Screenshot 2025-03-31 at 11.49.19 PM.png]]
- ![[Screenshot 2025-03-31 at 11.49.35 PM.png]]
- ![[Screenshot 2025-03-31 at 11.50.21 PM.png]]
#### Increasing and Decreasing Sequences:
- A sequence is **increasing** if for every two consecutive indices, *k* and *k + 1*, in the domain,$$a_{k} < a_{k+1}$$
- A sequence is **nondecreasing** if for every two consecutive indices *k* and *k + 1*, in the domain, $$a_{k} \leq a_{k+1}$$
	- Increasing and nondecreasing sequences example:$$2, < 4, <5, <6 \quad \text{Increasing AND nondecreasing}$$$$2, \leq 4, \leq 4, \leq 6 \quad \text{Nondecreasing BUT NOT increasing}$$
- A sequence is **decreasing** if for every two consecutive indices, *k* and *k + 1*, in the domain, $$a_{k} > a_{k+1}$$
- A sequence is **non-increasing** if for every two consecutive indices, *k* and *k + 1*, in the domain, $$a_{k} \geq a_{k+1}$$
	- Increasing and nondecreasing sequences example:$$6, > 5, > 4, > 2 \quad \text{Decreasing AND nonincreasing}$$$$6, \geq 4, \geq 4, \geq 2 \quad \text{Nonincreasing BUT NOT decreasing}$$

#### Geometric Sequences: 
- A **geometric sequence** is a sequence of real numbers where each term after the initial term is found by taking the previous term and multiplying by a fixed number called the **common ratio**.
	- A geometric sequence can be **finite** or **infinite**.
		- ![[Screenshot 2025-04-01 at 12.13.15 AM.png]]
		- ![[Screenshot 2025-04-01 at 12.13.41 AM.png]]
	- The **infinite geometric sequence** with initial term $$a_{0} =1$$and common ratio $$r=\frac{1}{2}$$begins with:$$1,\; \frac{1}{2},\; \frac{1}{4}, \;\frac{1}{8}, \; \frac{1}{16}, \; \dots$$
	- The **finite geometric sequence** with initial term $$a_{0} =5$$final index *6*, and a common ratio $$r = -1$$is:$$5, \; -5,\; 5,\; -5,\; 5,\; -5,\; 5$$
- If the initial index of an infinite geometric sequence $$\{s_{k}\} \text{ is } 0$$then the explicit formula defining the sequence is: $$s_{k} = a  \cdot  r^k, \; \text{for } k\geq 0$$
	- Here, $$s_{0} = a  \cdot  r^0 = a$$is the initial term in the sequence

#### Interest Rates and Geometric Sequences: 
- Money in a bank account earning a fixed rate of interest can be expressed as a geometric sequence.
- Suppose **$1,000** is stored in a bank account that earns **6%** annual interest compounded monthly.
	- Since the interest rate is annual and compounded monthly, $$\frac{6}{12}\%$$of the current amount is added to the account each month.
	-                                       $$a_0 = 1,000$$is the initial balance in the account, and $$a_{n}$$is the balance in the account after *n* months of earning interest. 
	- Each month, the balance in the account increases by$$\frac{6}{12}\% = 0.005$$so the balance is *1.005* times the amount that was in the account in the previous month.
	- The sequence $$\{a_{n}\}$$is a geometric sequence with $$a_n = 1{,}000 \cdot (1.005)^n \quad \text{for } n \geq 0$$

#### Arithmetic Sequences: 
- An **arithmetic sequence** is a sequence of real numbers where each term after the initial term is found by taking the previous term and adding a fixed number called the **common difference**.
	- ![[Screenshot 2025-04-01 at 1.15.03 AM.png]]
	- ![[Screenshot 2025-04-01 at 1.16.11 AM.png]]
- An arithmetic sequence can be **finite** or **infinite**.
	- The **infinite arithmetic** sequence with initial term $$a_0 = 2$$and common difference $$d = 3$$begins with $$2, 5, 8, 11, \;\dots$$
	- The **finite arithmetic** sequence with initial term $$a_0 = 3$$final index *5*, and common difference $$d = -2$$is: $$3, \; 1, \; -1,\; -3,\; -5,\; -7$$
- If the initial index of an arithmetic sequence $$t_{n}$$ is *0*, then the explicit formula defining the sequence is: $$t_n = t_0 + dn,\ \text{for } n \geq 0$$where *d* is common difference 



## 8.2 Recurrence Relations:

#### Key Definition:
- Some sequences are most naturally defined by specifying one or more initial terms and then giving a rule for determining subsequent terms from earlier terms in the sequence.
- A rule that defines a term $$a_{n}$$as a function of previous terms in sequence is called a **recurrence relation**. 
- For example, in an arithmetic sequence, each number is obtained by adding a fixed value to the previous number.

-  **Recurrence relation defining an arithmetic sequence:** $$a_{0} = a \; \text { (initial value)}$$$$a_{n} = d + a_{n-1} \; \text{ for } \; n\geq 1 \; \text{(recurrence relation)}$$$$\text{Initial value = } a. \; \text{Common difference = d}$$
- **Recurrence relation defining an geometric sequence:** $$a_{0} = a \; \text { (initial value)}$$$$a_{n} = r \cdot a_{n-1} \; \text{ for } \; n\geq 1 \; \text{(recurrence relation)}$$$$\text{Initial value = } a. \; \text{Common ratio = r}$$

#### Fibonacci Sequence:
- A number sequence in which each term is the **sum of the two preceding terms**, starting from 0 and 1 (the initial value/condition)
- **Initial Conditions**:$$f_{0} = 0 \quad \quad \quad \quad f_{1} = 1 $$
- **Recursive Formula**:$$f_{n} = f_{n-1} + f_{n-2} \quad \quad \text{for } n\geq 2$$
- ![[Screenshot 2025-04-01 at 4.51.24 AM.png]]
- ![[Screenshot 2025-04-01 at 4.56.34 AM.png]]
- ![[Screenshot 2025-04-01 at 4.56.55 AM.png]]
- ![[Screenshot 2025-04-01 at 4.57.15 AM.png]]
- Both $$f_{0} \; \text { and } \; f_{1}$$are required to define $$f_{2}$$
	- However, if only $$f_{0}$$were given, the recurrence relationship could not be applied to $$f_{1} = f_{0} + f_{-1} $$because $$f_{-1}$$is not defined. 
- Fibonacci's Sequence is an example of a **dynamical system**
	- A **dynamical system** is a system that changes over time. Moreover, the state of the system at any point in time is determined by a set of well-defined rules that depend on the past states of the system.
		- In a **discrete time dynamical system**, time is divided into discrete time intervals, and the state of the system stays fixed within each time interval.
		- The state during one time interval is a function of the state in previous time intervals.
		- Thus, the history of the system is defined by a sequence of states, indexed by the nonnegative integers.



## 8.3 Summations: 
- **Summation notation** is used to express the _sum_ of terms in a numerical sequence. Consider a sequence: $$a_{s}, \; a_{s+1}, \; \dots \; , \; a_{t}$$The notation to express the sum of the terms in that sequence is:$$\sum_{i=s}^{t} a_{i} = a_{s}, \; a_{s+1}, \; \dots \; , \; a_{t}$$
- In the summation $$\sum_{i=s}^{t} a_{i} $$the variable *i* is the **index** of the summation
  the variable *s* is the **lower limit**
  the variable *t* is the **upper limit**
- Summation notation can be used to sum up the terms in a sequence defined by an explicit formula:$$a_{n} = n^3, \quad \text{for } n=1, 2, 3, 4$$Then:$$\sum_{j=1}^4 j^3 = 1^3+2^3+3^3+4^3 = 1+8+27+64=100$$
- The expression$$\sum_{j=1}^4 j^3$$is called the **summation form** of the sum and the expression$$1^3+2^3+3^3+4^3$$is called the **expanded form** of the sum
- When the expression to be summed has more than one term, parentheses are used to indicate that all the terms are included in the summation as in $$\sum_{j=1}^n (j+1)$$because the expression $$\sum_{j=1}^n j+1$$is interpreted as $$(\sum_{j=1}^n j)+1$$
- **Computing Summations:**
	- ![[Screenshot 2025-04-03 at 5.54.33 PM.png]]
	- ![[Screenshot 2025-04-03 at 5.55.03 PM.png]]

- **Pulling out a final term from a summation:**
	- In working with summations, pulling out or adding in a final term to a summation is often useful:$$\sum_{k=m}^n a_{k}= \sum_{k=m}^{n-1} a_{k} + a_{n}, \quad \text{for } n>m$$
	- The drawing below illustrates the idea with an example. The expanded form of the sum is given to show why the two expressions are equal:
		- ![[Pasted image 20250403180115.png]]

- **Change of variables in summations**
	- When a variable is used to denote the lower or upper limit of a sum, the value of the variable must be provided to evaluate the sum.
		- In the summation below, the value of the sum depends on the variable *n*:$$\sum_{j=1}^n (j+2)^3$$By contrast, the variable *j* used for the index is internal to the sum and can be replaced with any other variable name:$$\sum_{j=1}^n (j+2)^3 = \sum_{k=1}^n (k+2)^3$$
	- More complex substitutions can be done for the index variable, which require that the upper and lower limit be adjusted.
		- Consider the substitution: $$i = k+2$$The steps are:
			1. Determine the new lower limit: when $$k= 1, \; i = k+2=1+2=3$$
			2. Determine the new upper limit: when$$k = n, \; i = k+2 = n+2$$
			3. Replace the variable in the terms: If$$i=k+2$$then$$k=i-2$$Replace *k* in the expression inside the sum with *i - 2*:$$(k+2)^3= ((i-2)+2)^3= i^3$$
		- Putting it all together, the result is:$$\sum_{k=1}^n (k+2)^3 = \sum_{i=3}^{n+2} i^3$$
		- To verify that the two sums are the same, verify that the expanded form for both sums is:$$3^3+4^3+\dots+(n+1)^3+(n+2)^2$$
	- The animation below illustrates with another example:
		- ![[Screenshot 2025-04-03 at 6.20.13 PM.png]]
		- ![[Screenshot 2025-04-03 at 6.20.38 PM.png]]![[Screenshot 2025-04-03 at 6.20.52 PM.png]]
		- ![[Screenshot 2025-04-03 at 6.21.11 PM.png]]
		- ![[Screenshot 2025-04-03 at 6.23.36 PM.png]]

- **Closed forms for sums**
	- A **closed form** for a sum is a mathematical expression that expresses the value of the sum without summation notation.
	- There are closed form expressions for some, although not all, of the summations that arise naturally in scientific applications.
	- For example, there is a closed form expression for the sum of terms in an 
	  **Arithmetic sequence**:
		- Closed form for the sum of terms in an arithmetic sequence:$$\text{For any integer } n\geq 1 \text{ :}$$$$\sum_{k=0}^{n-1} (a+kd) = an+\frac{d(n-1)n}{2}$$For Example:
			- In the sum $$5+8+11+14+17+20+23$$the initial term is $$a=5$$the common difference is $$d= 3$$and the number of terms in the sum $$n=7$$The theorem says that:$$5+8+11+14+17+20+23 = \sum_{j=0}^6 (5+3j) = 5\cdot7 + \frac{3\cdot 6 \cdot 7}{2} = 98$$
	- In another example, there is a closed form expression for the sum of terms in an
	  **Geometric sequence:**
		- Closed form for the sum of terms in a geometric sequence:$$\text{For any real number } r \neq 1 \text{ and any integer } n\geq 1 \text{ :} $$![[Screenshot 2025-04-03 at 8.18.41 PM.png]]![[Screenshot 2025-04-03 at 8.18.55 PM.png]]



## Summary:


**8.1 Sequences**

- **Definition**: A sequence is a function whose domain is a set of consecutive integers.
    - Notation: Use subscripts (e.g., aₖ instead of a(k)); aₖ is the _term_, and k is the _index_.
    - Finite: Has a start and end index (e.g., aₘ to aₙ).
    - Infinite: Starts at m and continues indefinitely.

- **Explicit Formula**: Expresses aₖ in terms of k directly (e.g., dₖ = 2ᵏ for k ≥ 1).

- **Monotonicity**:
    - _Increasing_: aₖ < aₖ₊₁
    - _Nondecreasing_: aₖ ≤ aₖ₊₁
    - _Decreasing_: aₖ > aₖ₊₁
    - _Nonincreasing_: aₖ ≥ aₖ₊₁

- **Geometric Sequences**:
    - Each term = previous term × constant ratio (r).
    - Formula: aₖ = a × rᵏ
    - Example: If a₀ = 1 and r = ½ → sequence: 1, ½, ¼, ⅛, ...

- **Arithmetic Sequences**:
    - Each term = previous term + constant difference (d).
    - Formula: tₙ = t₀ + d × n
    - Example: If a₀ = 3, d = –2 → sequence: 3, 1, –1, –3, ...

- **Bank Interest Example**:
    - $1,000 with 6% annual interest compounded monthly.
    - Monthly growth factor = 1.005.
    - Formula: aₙ = 1000 × (1.005)ⁿ


**8.2 Recurrence Relations**

- **Definition**: Defines each term based on one or more previous terms.
  
- **Arithmetic Sequence** (Recursive Form):
    - a₀ = a (initial value)
    - aₙ = d + aₙ₋₁ for n ≥ 1

- **Geometric Sequence** (Recursive Form):
    - a₀ = a
    - aₙ = r × aₙ₋₁ for n ≥ 1

- **Fibonacci Sequence**:
    - f₀ = 0, f₁ = 1
    - fₙ = fₙ₋₁ + fₙ₋₂ for n ≥ 2
    - Each term is the sum of the two before it.
    - Example of a **dynamical system** (state depends on past states).


**8.3 Summations**

- **Notation**: ∑ from i = s to t of aᵢ means summing values aₛ + aₛ₊₁ + ... + aₜ.
    - _i_ is the index.
    - _s_ is the lower limit.
    - _t_ is the upper limit.
    - E.g., ∑ (j = 1 to 4) of j³ = 1³ + 2³ + 3³ + 4³ = 100

- **Parentheses Use**: ∑ (j=1 to n)(j+1) ≠ ∑ (j=1 to n) j + 1

- **Breaking a Sum**:
    - ∑ (k=m to n) aₖ = ∑ (k=m to n–1) aₖ + aₙ

- **Change of Variables**:
    - E.g., if i = k+2, then ∑ (k=1 to n) (k+2)³ becomes ∑ (i=3 to n+2) i³

- **Closed Forms**:
    - Avoids ∑ by giving a formula for the total sum.
    - **Arithmetic Sequence**:
        - ∑ (k=0 to n–1) (a + k×d) = a×n + d×(n–1)×n / 2
        - Example: ∑ (j=0 to 6)(5 + 3j) = 98
    - **Geometric Sequence** (r ≠ 1):
        - ∑ (k=0 to n–1) a × rᵏ = a × (rⁿ – 1) / (r – 1)
        - Example: 3 + 6 + 12 + 24 + 48 + 96 = ∑ (j=0 to 5) 3 × 2ʲ = 189





