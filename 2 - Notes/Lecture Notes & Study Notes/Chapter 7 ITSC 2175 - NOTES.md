

2025-03-28 
12:01 PM


Tags: [[Discrete Math]], [[Function & Relations]], [[Integer Properties]], [[Encryption]], [[Function Compositions]], 


## Reference:
![[Chapter 7 ITSC 2175.pdf]]



## 7.1 Definition of functions:

#### Key Concepts:
- **Function as a mapping**:
	- A function maps elements from one set X to elements of another set Y. 
	- Discrete mathematics is often concerned with functions that map between other kinds of sets, such as:
		- Binary strings 
		- A set of tasks
	- A function to X to Y can be viewed as a subset of $$ X \times Y : (x,y) ∈ f $$if f maps to x to y. 
	- A function is a relation that assigns every element a in a set A (the domain) exactly one element b in a set B (the target or codomain). This is often denoted as: $$ f : A \to B $$and formally defined as a subset of $$ A \times B $$This satisfies the following: For every a ∈ A, there exists exactly one $$ b \in B $$such that $$(a,b)\in f $$
- **Domain, Target and Range**:
	- **Domain:** All possible inputs from set A.
	- **Target (Codomain):** The set B into which all outputs fall.
		- The "target" (or "codomain") is the set that we decide the outputs could belong to when we write the function. It is the list of all values that we allow as possible answers.
	- **Range:** The subset of B consisting of those elements that are actually output by f.
		- The "range" is the actual set of values that come out when we apply the function to every input in its domain.
	- The **target** is what the function is set up to potentially produce, while the **range** is what it really produces.

- **Well-Defined Functions:**
	 - For a relation to be a function, every input must have one—and only one—output.
	 - Missing arrows (no output for an element) or multiple arrows (more than one output for a given input) invalidate the function.
	 - All functions are relations. However, not all relations are functions.    

#### Arrow Diagrams and Finite Functions:
- **Finite Functions:**
	- If f is a function mapping to X to Y and X is a **finite** set, 
		- then the function f can be specified by listing the pairs (x, y) in f.
	- When set A is finite, the function may be explicitly written as a list of ordered pairs, or depicted graphically via an arrow diagram.

- **Arrow Diagrams:**
	- In an arrow diagram for a function f, the elements of the domain X are listed on the left and the elements of the target Y are listed on the right.
	- There is an arrow from $$ x \in X $$to $$y \in Y$$if and only if$$ (x,y) \in f$$So all together:$$ x \in X \to y \in Y \iff (x,y) \in f $$x is in X TO y is in Y IF AND ONLY (x, y) is in f
	- These diagrams visually represent functions. Elements of the domain are listed on the left, and those of the target on the right. An arrow from a to b indicates f(a) = b. A valid function has exactly one arrow emerging from each element in the domain.
		- ![[Screenshot 2025-03-29 at 4.11.20 PM.png]]
		- ![[Screenshot 2025-03-29 at 4.11.50 PM.png]]
		- ![[Screenshot 2025-03-29 at 4.12.27 PM.png]]
			- In an arrow diagram, domain elements are on the left, target elements on the right. An arrow for each domain element points to a target element.
	- For the function:$$f : X \to Y$$an element **y** is in the **range** of **f** if and only if there is an **x in set X** such that **(x, y) is in f**:$$f = \{y : (x,y) \in f, \text{ for some } x \in X \}$$ 
	- The range of f is a subset of the target, but the range is not necessarily equal to the target. In an arrow diagram, the range is the set of elements in the target that have arrows coming into them.
		- ![[Screenshot 2025-03-29 at 4.21.58 PM.png]]
		  In an arrow diagram for f, each element in the domain has exactly one arrow leaving it.
		- ![[Screenshot 2025-03-29 at 4.23.13 PM.png]]
		  The range of f is the set {a, c, d} because a, c, and d are the target elements with at least one arrow coming in.
		- ![[Screenshot 2025-03-29 at 4.24.07 PM.png]]
		  If the arrow from x to a is removed, f is no longer a function because f is not defined on input x.
		- ![[Screenshot 2025-03-29 at 4.25.01 PM.png]]
		  If an arrow from y to b is added, f is no longer a function because f maps y to both d and b.

- **Well-Defined Algebraic Functions:**
	- A mathematical function **f** is often defined by describing how **f** acts on an input **x**, as in:$$ f(x) = x^2 - 2 $$However, the definition is not complete until the domain and target of f are specified. For example:$$ g: \mathbb{R} \to \mathbb{R} , \text{ where } g(x) = |x|$$**g** maps every real number to a real number. However, **g** does not map any number to a negative number.

- **Functions on sets of strings:**
	- The domain and target set for a function can also be a set of strings.
	- For example, the function$$f : \{0,1\}^3 \to \{0,1\}^4 $$takes as input input a 3-bit string and outputs a 4-bit string. 
	- Suppose that **f** is defined so that for any $$ x \in \{0,1\}^3 , f(x) = \text{x0} $$
	- Then for any 3-bit string **x**, the output of **f** on input **x** is obtained by adding a 0 to the end of **x**. For example:$$ f(011) = 0110 $$

#### Function Equality:
- Two functions, **f** and **g**, are equal if **f** and **g** have the same domain and target, and **f⁡(x)=g⁡(x)** for every element **x** in the domain. The notation **f = g** denotes the fact that functions **f** and **g** are equal.



## 7.2 Floor and Ceiling Functions:

#### Definitions and Notation:
- The floor function and ceiling function map **real numbers** onto **integers**. The floor and ceiling functions **round real numbers** to a nearby **integer** in different ways. 
	- **Floor Function:** $$\text{floor}(x) = \lfloor x \rfloor$$$$\text{floor: } \mathbb{R} \to \mathbb{Z}, \text{where floor}(x) = \text{the largest intger } y \text{ such that } y \leq x $$Rounds a real number x **DOWN** to the NEAREST integer
		- Examples:$$\lfloor 3.7 \rfloor = 3 $$ $$\lfloor -1.2 \rfloor = -2$$
		- ![[Screenshot 2025-03-30 at 7.28.38 PM.png]]
	- **Ceiling Function:**$$\text{ceiling}(x) = \lceil x \rceil$$$$\text{ceiling: } \mathbb{R} \to \mathbb{Z}, \text{where ceiling}(x) = \text{the smallest intger } y \text{ such that } x \leq y$$Rounds a real number x **UP** to the NEAREST integer
		- Examples:$$\lfloor 3.7 \rfloor = 4 $$$$\lfloor -1.2 \rfloor = -1$$
		- ![[Screenshot 2025-03-30 at 7.29.38 PM.png]]
			- ![[Screenshot 2025-03-30 at 7.45.45 PM.png]]



## 7.3 Properties of Functions:
#### Fundamental Properties:
- **Injective (One-to-one) function:**
	- A function $$f:X \to Y $$is **one-to-one** or **injective** if $$x_{1} \neq x_{2}$$This implies that $$f(x_{1}) \neq f(x_{2})$$That is, **f** maps different elements in set X to different elements in set Y
	- A function **f** is one-to-one if$$f(a) = f(b) \Longrightarrow a = b$$This means no two distinct elements in the domain map to the same element in the target 
- **Surjective (Onto):**
	- A function$$f:X \to Y $$is **onto** or **surjective** if the range of **f** is EQUAL to the target of set **Y**. That is: 
	  For every $$y \in Y$$there is an $$x \in X$$such that $$f(x) = y$$
	- **f** is onto if every element in the target **Y** is the image of at least one element in the domain **X**. In other words, the range of **f** equals **Y**$$ \forall y \in Y, \; \exists x \in X \;\text{such that}\; f(x) = y $$
- **Bijective:**
	- A function is **bijective** if it is both **one-to-one** and **onto**. A bijective function is called a **bijection**. A bijection is also called a **one-to-one correspondence.**
- Analogy #1: Consider a function that maps employees (X) to offices (Y):
	- If the function is **one-to-one**:
		- Then no employee has to share an office.
	- If the function is **onto**:
		- Then not offices are empty, and the company's space is well utilized.
- Analogy #2: Consider a function used to define an assignment of processes (X) to computers in a distributed network (Y):
	- If the function is **one-to-one**:
		- Then no computer is time-sharing between different tasks.
	- If the function is **onto**:
		- Then all the resources of the network are being used.

- **One-to-one and Onto Functions**
	- ![[Screenshot 2025-03-30 at 11.32.16 PM.png]]
	- ![[Screenshot 2025-03-30 at 11.32.55 PM.png]]
	- ![[Screenshot 2025-03-30 at 11.33.24 PM.png]]
	- ![[Screenshot 2025-03-30 at 11.33.59 PM.png]]

	- When the domain and target are finite sets, information can be inferred about their relative sizes based on whether the function is one-to-one or onto.
		- If $$f : D \to T $$is **onto**, then for every element in the target, there is at least one element in the domain:$$|D| \geq |T| $$

		- If$$f : D \to T $$is **one-to-one**, then every element in the domain maps to a unique element in target: $$|D| \leq |T|$$

		- If $$ f: D \to T $$ is **bijection**, then **f** is one-to-one and onto: $$|D|\leq|T| \text{ and } |D|\geq|T|$$which implies that$$|D| = |T| $$
		- ![[Screenshot 2025-03-30 at 11.47.06 PM.png]]



## 7.4 The Inverse of a Function:

#### Inverse Function Definition:
- **Concept**:
	1. If a function $$f : X \to Y$$is a bijection, then the **inverse** of **f** is obtained by exchanging the first and second entries in each pair in **f**. The inverse of **f** is denoted by **f^-1**:$$f^{-1} = \{(y,x):(x,y) \in f\}$$
	2. If a function $$f : X \to Y$$is a bijection, its inverse$$f^{-1} : Y \to X $$is defined by reversing the ordered pairs of **f**. 
	   For every$$x \in X$$and$$y \in Y$$The following results:$$f(x) = y \iff f^{-1}(y) = x$$All together:$$\forall x \in X, \; \forall y \in Y, \quad f(x) = y \iff f^{-1}(y) = x $$
	- Arrow diagram for the inverse of a function:
		- ![[Screenshot 2025-03-31 at 12.12.46 AM.png]]
		- ![[Screenshot 2025-03-31 at 12.13.06 AM.png]]
		- ![[Screenshot 2025-03-31 at 12.13.39 AM.png]]
		- ![[Screenshot 2025-03-31 at 12.13.58 AM.png]]
 **Solving for the Inverse of a Function Analytically**:
	- $$f: R \to R \quad \quad \quad f(x)=3x-2$$$$\text{Check if }f \text{ is one-to-one: }x \neq x' \to 3x - 2 \neq 3x'-2 $$$$\text{Show the contrapositive: } 3x-2 = 3x'-2 \to x=x'$$$$ \text{ Add 2 on each side, canceling out the 2's: } \; (3x-2=3x'-2) \to 3x=3x'$$$$\text{Divide by 3 on each side to show its one-to-one: }\; (3x-3x') \to x=x'$$$$f\text{ is one-to one: }\; x = x'$$$$\text{Check that }f \text{ is onto: for every real number }y \text{, there is an  }x \text{ such that: }\; f(x) = 3x-2=y$$$$\text{Solve for }x \text{ in terms of }y\text{: }\; x = \frac{y+2}{3} \text{ <------ this function is }f^{-1} $$$$f^{-1}:R \to R \quad \quad \quad \quad f^{-1}(y) = \frac{y+2}{3}$$
	- The function $$f : \mathbb{R} \to \mathbb{R} $$defined by $$f(x) = x^2$$is not one-to-one because $$f(x) = f(-x)$$for any real number x.
	- However, if the domain is restricted to positive reals R^+, then$$f:\mathbb{R}^{+} \to \mathbb{R}^{+}, \; f(x) = x^2$$this is a bijection. To solve f^-1, express y=x^2 and solve for x in terms of y : x = sqrt(y). Therefore: f^-1(y) = sqrt(y)
	- The use of the variable y instead of x is not important. The important f^-1(sqrt(y)) is the same function as f^-1(y) = sqrt(y) is the same function as f^-1(x) = (sqrt(x)).
	  

- #### Encrypting Messages: 
	- The process of encrypting messages can be expressed through the mathematical language of functions.
	  
	- Consider encrypting 16-digit credit card numbers:
		- Let *N* be the set of all 16-digit numbers. 
		- An encryption scheme for *N* is a function *e*:$$N \to N $$To send a credit card number $$n \in N$$over an insecure communication channel, the sender encrypts *n* by computing $$e(n)$$
		- The encryption function *e* is chosen to be a bijection. 
		- The sender then sends *e(n)* over the channel. 
		- The receiver receives *e(n)* and wishes to decrypt the message to obtain the original number *n*. 
		- To accomplish this, the receiver applies the inverse function$$e^{-1}$$to$$e(n)$$in order to get the credit card number number$$n : e^{-1}(e(n)) = n$$
		- The sender and receiver must communicate ahead of time so that the receiver knows what function *e^-1* to apply to the number that is received. 
		- A secure encryption scheme must have the property that without foreknowledge of the function $$e^{-1}$$it would be difficult to determine *n* from *e(n)*. 
		  
	- Encrypting messages (such as credit card numbers) can be modeled by a bijective function$$f$$
	- The inverse inverse function $$f^{-1}$$is used for decryption



## 7.5 Composition of Functions:

#### Intro:
- Let *f* be a function that assigned employees to offices in a company
- Let *g* be the function that maps each office to the telephone number for the phone in that office. 
	- An employee, Rajiv, is assigned to the office$$f(\text{Rajiv})$$Rajiv's work phone number is $$g(f(\text{Rajiv}))$$
	- The process of applying a function to the result of another function is called a **composition**. 

#### Definition and Notation:
- **Function Composition**: 
	- Given two functions$$f:A \to B$$and $$g: B \to C$$their composition is defined as:$$(g \circ f)(x) = g(f(x))$$for every $$x \in A$$
		- ![[Screenshot 2025-03-31 at 2.35.15 AM.png]]
		- ![[Screenshot 2025-03-31 at 2.35.39 AM.png]]
		- ![[Screenshot 2025-03-31 at 2.36.14 AM.png]]
- **Associativity**:
	- Generally, the order in which the functions are applied is important, so$$f \circ g$$is not the same as $$g \circ f$$Define:$$f: \mathbb{R}^{+} \to \mathbb{R}^{+}, \; f(x) = x^3$$$$g: \mathbb{R}^{+} \to \mathbb{R}^{+}, \; g(x) = x+2$$Then:$$(f \circ g)(x)=f(g(x))=(x+2)^3$$$$(g \circ f)(x)=g(f(x))=x^3+2$$
	- More than two functions can be composed. Composition is associative, so the order in which one composes the functions does not matter: $$f \circ g \circ h = (f \circ g) \circ h = f \circ (g \circ h) = f(g(h(x)))$$
- **Identity Function**:
	- The identity function always maps a set onto itself and maps every element onto itself.
		- The identity function on A, denoted $$I_{A} = A \to A$$is defined as $$I_{A}(x) = x$$for all $$x \in A$$
	- If a function *f* from A to B has an inverse, then *f* composed with its inverse is the identity function. 
	  If $$f(a)=b$$then $$f^{-1}(b) = a$$and$$(f^{-1} \circ f)(a) = f^{-1}(f(a)) = f^{-1}(b) = a$$
		- Let$$f:A \to B \text{ be a bijection. Then } f^{-1}\circ f = I_{A} \text{ and } f \circ f^{-1} = I_{B}$$
- **Composition of a Function and Its Inverse**:
	- ![[Screenshot 2025-03-31 at 3.15.42 AM.png]]
	- ![[Screenshot 2025-03-31 at 3.15.59 AM.png]]
	- ![[Screenshot 2025-03-31 at 3.16.11 AM.png]]
	- ![[Screenshot 2025-03-31 at 3.16.57 AM.png]]
	- ![[Screenshot 2025-03-31 at 3.17.33 AM.png]]



## Summary:
**7.1 Definition of Functions**

- Function as Mapping:
    - Defines functions as mappings between sets (domain → target/codomain), highlighting discrete math examples like binary strings.
- Domain, Target, Range:
    - Domain: Set of inputs.
    - Target/Codomain: Set where outputs potentially lie.
    - Range: Actual outputs from domain inputs.
- Well-defined Functions:
    - Each input must have exactly one output.
- Arrow Diagrams & Finite Functions:
    - Visual representation where domain and target elements are connected by arrows representing mappings.
- Function Equality:
    - Functions equal if they share domains, targets, and mappings for every input.


**7.2 Floor and Ceiling Functions**
- Floor Function (⌊x⌋):
    - Rounds real numbers down to nearest integer (e.g., ⌊3.7⌋ = 3).
- Ceiling Function (⌈x⌉):
    - Rounds real numbers up to nearest integer (e.g., ⌈3.7⌉ = 4).


**7.3 Properties of Functions**
- Injective (One-to-One):
    - Each domain element maps uniquely to distinct target elements.
- Surjective (Onto):
    - Every target element has at least one corresponding domain element.
- Bijective:
    - Functions that are both injective and surjective (one-to-one correspondence).
    - Illustrated through analogies (employees/offices, processes/computers).


**7.4 Inverse of a Functions**
- Inverse Function:
    - Defined by reversing pairs from bijections.
    - Inverse exists only for bijective functions.
- Analytically Solving Inverses:
    - Algebraic examples provided.
- Application Example:
    - Encrypting messages (e.g., credit card numbers) using bijections and their inverses.


**7.5 Composition of Functions**
- Composition:
    - Applying one function to the result of another: (g∘f)(x) = g(f(x)).
- Associativity:
    - Compositions are associative (f∘g∘h), but not necessarily commutative (f∘g ≠ g∘f).
- Identity Function:
    - Maps elements to themselves, illustrating inverse functions (f⁻¹∘f = Identity).










