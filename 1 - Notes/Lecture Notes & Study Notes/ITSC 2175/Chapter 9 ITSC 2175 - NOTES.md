

2025-04-09 
01:36 PM


Tags:


## Reference:
![[Chapter 9 ITSC 2175 .pdf]]



## 9.1 - Algebra Review
- Exponent Properties:
	- $$\begin{align}
b^xb^y = b^{x+y} \\
(b^x)^y = b^{xy}  \\
\frac{b^x}{b^y} = b^{x-y} \\
(bc)^x= b^xc^x
\end{align}$$
- Adding Rational Expressions:
	- Same denominators:
		- Add/subtract numerators, keep denominator. Ex:$$
\frac{x^2-7x-10}{x+5} - \frac{x^2-7x+10}{x+5}= $$$$\frac{(x^2-7x-10)-(x^2-7x+10)}{x+5} = $$$$\frac{-20}{x+5}$$
	- Different denominators: 
		- Find the least common denominator (LCD). Ex: Simplify $$\frac{6}{x^2-4} + \frac{2}{x^2-5x+6}:$$$$\text{Factor Denominators: } \frac{6}{(x+2)(x-2)} + \frac{2}{(x-3)(x-2)}$$$$\text{LCD: }(x+2)(x-2)(x-3)$$$$\text{Rewrite: } \frac{6(x-3)}{(x+2)(x-2)(x-3)} + \frac{2(x+2)}{(x+2)(x-2)(x-3)}$$$$\text{Combine: } \frac{6(x-3)+2(x+2)}{(x+2)(x-2)(x-3)}=\frac{6x-18+2x+4}{(x+2)(x-2)(x-3)} = \frac{10x-14}{(x+2)(x-2)(x-3)}$$



## 9.2 - Mathematical Induction
- **Definitions**:
	- **Mathematical Induction**:
		- A proof technique to show a statement, *S(n)*, holds for all positive integers *n*
		- It proves/shows that a rule or pattern holds for an infinite sequence of numbers (like 1, 2, 3, ...), without checking each number individually
			- If you have a statement that depends on a positive integer, *n* for example, the sum of the first *n* positive integers is $$\frac{n(n+1)}{2}$$mathematical induction lets you prove that this statement is true for every *n* = 1, 2, 3, ... .
		- Components:
			- The idea behind mathematical induction is to prove that a statement, *S(n)*, is true for the numbers in the set by breaking the proof into two manageable parts.
				- Its like setting up a chain reaction: if you can get the reaction started and ensure it keeps going, it will continue forever:
					- **Base Case**: Prove *S(1)* is true
						- This is like lighting the first match in a chain of matches—it gets the process going.
					- **Inductive Step**: Prove if *S(k)* is true, then *S(k + 1)* is true for all positive integers $$ k \in \mathbb{Z^+} \quad \text{k is in the set of positive integer numbers}$$This is like showing that if one match is lit, it will light the next match in the chain. 
					  
		- **Principle**: If both hold, *S(n)* is true for all *n >= 1* .
			- If this step holds for all *k*, the chain reaction continues indefinitely.
		  
	- **Inductive Hypothesis**:
		- The assumption in the inductive step that *S(k)* is true. 

- **Theorems**:
	- **Principle of Mathematical Induction**: Let *S(n)* be a statement parameterized by $$n 
	\in \mathbb{Z^+}$$If: $$\begin{align}
S(1) \text{ is true,} \\
\forall \text{ (for all) }k \in \mathbb{Z^+}, \; S(k) \Rightarrow S(k+1), \text{ then } S(n) \text{ is true } \forall \text{ (for all) } n \geq 1
\end{align}$$
		 ![[Screenshot 2025-04-09 at 3.25.11 PM.png]]
		 ![[Screenshot 2025-04-09 at 3.25.26 PM.png]]
		 ![[Screenshot 2025-04-09 at 3.25.43 PM.png]]
		 ![[Screenshot 2025-04-09 at 3.25.53 PM.png]]
		  ![[Screenshot 2025-04-09 at 3.26.05 PM.png]]

- **Proof 9.2.1: Proving an identity by induction:**
	- **Theorem**: For every positive integer *n*, $$\sum_{j=1}^{n}j = \frac{n(n+1)}{2}$$**Proof**.
	  By induction on *n*
	  
	  **Base Case**: *n* = 1.
	  When *n* = 1, the left side of the equation is $$\sum_{j=1}^{1}j=1$$When *n* = 1, the right side of the equation is $$\frac{1(1+1)}{2} = 1$$Therefore, $$\sum_{j=1}^{1}j = \frac{1(1+1)}{2}$$**Inductive Step**: Suppose that for positive integer, *k*, $$\sum_{j=1}^{k}k = \frac{k(k+1)}{2}$$then we will show that $$\sum_{j=1}^{k}k = \frac{(k+1)(k+2)}{2}$$
	  Starting with the left side of the equation to the proven:$$\sum_{j=1}^{k+1}j = \sum_{j=1}^{k}j+(k+1) \quad \quad \quad \text{By seperating out the last term}$$$$= \frac{k(k+1)}{2}+(k+1) \quad \quad \quad \text{By the inductive hypothesis}$$$$= \frac{k(k+1)+2(k+1)}{2}$$$$= \frac{(k+2)(k-1)}{2} \quad \quad \quad \text{By alegebra}$$Therefore, $$\sum_{j=1}^{k+1}j = \frac{(k+2)(k-1)}{2}$$

- **Proof 9.2.2: Proving an inequality by induction:**
	- **Theorem**: For$$n\geq 4, \quad 2^n\geq 3n$$**Proof**:
	  By induction on *n*.
	  
	  **Base Case**: *n* = 4 $$2^4 = 16 \geq 12 = 3 \cdot 4$$Therefore, for $$n = 4, \quad 2^n\geq 3n$$**Inductive step**: We will show that for any integer $$k\geq 4, \; \text{if } 2^k \geq 3k$$then, $$2^{k+1}\geq 3(k+1)$$Starting with the left side of the inequality to be proven:
	  $$2^{k+1} = 2\cdot 2^k \quad \quad \quad \text{By algebra}$$$$\geq 2 \cdot 3k \quad \quad \quad \text{By the inductive hypothesis}$$$$= 3k +3k$$$$\geq 3k+3 \quad \quad \quad \text{Because } k\geq 4\geq 1$$$$= 3(k+1) \quad \quad \quad \text{By algebra}$$
	  Therefore: $$2^{k+1}\geq 3(k+1)$$

- **Proof 9.3.1: Proving a divisibility proof by induction**:
	- For every positive *n*, 3 evenly divides 2^{2n} - 1 
	  
	  **Proof**:
	  By induction on *n*
	  
	  **Base Case**: *n* = 1$$2^{2*1} - 1= 2^2-1 = 3$$Since 3 evenly divides 3, the theorem holds for the case *n* = 1
	  
	**Inductive step**: Suppose that for positive integer *k*, 3 evenly divides $$2^{2k}-1$$Then we will show that 3 evenly divides $$2^{2(k+1)}-1$$By the inductive hypothesis, 3 evenly divides $$2^{2k-1}$$which means that $$2^{2k-1}= 3m \quad \quad $$for some integer *m*. By adding 1 to both sides of the equation $$3m = 2^{2k}-1$$we get $$2^{2k}= 3m+1$$which is an equivalent statement of the inductive hypothesis.
	
	We must show that $$2^{2(k+1)}-1$$can be expressed as 3 times an integer$$2^{2(k+1)}-1 = 2^{2k+2}-1$$$$=4\cdot2^{2k}-1 \quad \quad \quad \text{By algebra}$$$$4(3m+1)-1 \quad \quad \quad \text{By the inductive hypothesis}$$$$3\cdot 4m+4-1$$$$3(4m+1) \quad \quad \quad \text{By algebra}$$Since *m* is an integer, (4m+1) is also an integer. Therefore, $$2^{2(k+1)}-1$$is equal to 3 times an integer, which means that $$2^{2(k+1)}-1 \quad \quad \quad \text{is divisible by 3}$$

- **9.3.3: The inductive step in the proof of the closed form for the sum of an arithmetic sequence**:
	- ![[Screenshot 2025-04-10 at 3.57.12 AM.png]]
	- ![[Screenshot 2025-04-10 at 3.57.32 AM.png]]
	- ![[Screenshot 2025-04-10 at 3.57.54 AM.png]]
	- ![[Screenshot 2025-04-10 at 3.58.05 AM.png]]
	- ![[Screenshot 2025-04-10 at 3.58.33 AM.png]]

- **9.3.4: An inductive proof of the closed form for the sum of a geometric sequence**:
	- ![[Screenshot 2025-04-10 at 4.00.18 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.00.36 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.01.03 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.01.18 AM.png]]
	-  ![[Screenshot 2025-04-10 at 4.01.34 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.02.07 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.02.31 AM.png]]

- **9.3.6: Inductive proof of the generalized De Morgan's law for sets**:
	- ![[Screenshot 2025-04-10 at 4.08.51 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.09.02 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.09.14 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.09.26 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.09.37 AM.png]]
	- ![[Screenshot 2025-04-10 at 4.09.48 AM.png]]

-  **9.4.1: Expanded expression of the inductive step for weak and strong induction**:
	- ![[Screenshot 2025-04-10 at 2.40.25 PM.png]]

- **Proof 9.4.1: Upper bound for Fibonacci numbers proven using strong induction**:
	- **Theorem**:
	  For $$n \geq 0, \; f_n \leq 2^n$$
	  **Proof**:
	  By strong induction on *n*
	  
	  **Base Case**:$$n = 0: f_0 = 0 \leq 2^0$$ $$n = 1: f_1 = 1 \leq 2^1$$**Inductive Step**:
	  For $$k \geq 1$$suppose that for any $$j$$ in the range from 0 through $$k$$ ,$$f_j \leq 2^j$$We will prove that $$f_{k+1} \leq 2^{k+1}$$
	  
	  Since $$k \geq 1$$then $$k - 1 \geq 0$$ Therefore both $$k$$ and $$k - 1$$ fall in the range from 0 through $$k$$ and by the inductive hypothesis:
	  $$
\begin{aligned}
f_{k+1} &= f_k + f_{k-1} \quad &\text{By definition} \\
&\leq 2^k + 2^{k-1} \quad &\text{By the inductive hypothesis} \\
&\leq 2^k + 2^{k-1} + 2^{k-1} \quad &\text{Since } 2^{k-1} \geq 0 \\
&= 2^k + 2 \cdot 2^{k-1} \\
&= 2^k + 2^k = 2 \cdot 2^k = 2^{k+1} \quad &\text{By algebra}
\end{aligned}
			$$
		Therefore, $$f_{k+1} \leq 2^{k+1} \quad \blacksquare$$

- **Figure 9.4.2: Principle of strong mathematical induction**:
	- ![[Screenshot 2025-04-10 at 8.54.23 PM.png]]

- **Figure 9.4.3: Expanded expression of the inductive step with an arbitrary range for the base case**:
	- ![[Screenshot 2025-04-10 at 9.38.37 PM.png]]

- **9.4.3: Inductive proof for buying n cans of juice**:
	- ![[Screenshot 2025-04-10 at 9.39.58 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.40.11 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.40.26 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.40.42 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.47.03 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.47.29 PM.png]]
	- ![[Screenshot 2025-04-10 at 9.47.54 PM.png]]








