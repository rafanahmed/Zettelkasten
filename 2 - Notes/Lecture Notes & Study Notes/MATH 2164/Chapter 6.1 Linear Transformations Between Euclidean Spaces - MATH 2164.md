

2025-04-01 
02:46 PM


Tags: [[Linear Algebra]], [[Vector Spaces]], [[Function & Relations]], [[Basis & Dimension]], [[Linear Transformations]], [[Matrix Representations]]


## Reference:
![[Chapter 6.1 Linear transformations Between Euclidean Spaces.pdf]]



## Section Summary:

- A function, in general, maps an element of one vector space to an element of another space
- A mapping of a function is also referred to as a **transformation** and can be used to manipulate an image. 
	- If an image needs to be enlarged or reduced, each vector in the original image can be **scaled**. An image can be rotated using a similar principle. 
	- These image **transformations** can be represented in terms of **matrix multiplication**. 
- Some linear transformations$$T(x)$$on vectors can be represented by matrix multiplication. 
- A transformation represented by matrix multiplication has BOTH properties of a **linear transformation**
- The *standard matrix* for a linear transformation can be FOUND USING the **standard basis** of the DOMAIN

- **Contents of Section:**
	- Identify terminology associated with transformations.
	- Determine if a transformation is linear.
	- Use matrices to express linear transformations.
	- Identify the standard matrix for a linear transformation.
	- Use properties of matrix transformations.
	- Use the standard basis to find a standard matrix.


## Transformations from  ℝⁿ → ℝᵐ:

- A **transformation** generalizes the concept of a function. A **transformation** T from $$\mathbb{R}^n$$to$$\mathbb{R}^m$$denoted by $$T: \mathbb{R}^n \to \mathbb{R}^m$$is a rule that assigns an element of a vector space (ℝⁿ) to an element of another vector space (ℝᵐ). 
- The **domain** of a transformation is the set of all inputs
- The **codomain** of a transformation is the **vector space** that contains the set of all outputs, in this case ℝᵐ. 
- In the case of this given transformation:$$T: \mathbb{R}^n \to \mathbb{R}^m$$
	- ℝⁿ is the **domain**
	- ℝᵐ is the **codomain**
- A transformation *T* is called an **operator** IF the domain AND the codomain are the SAME
- Transformations are defined by a **vector-valued** functions as shown:$$T(x_{1}, \; \dots, \; x_{n})= [f_{1}(x_{1}, \; \dots, \; x_{n}), \; \dots, \; f_{m}(x_{1}, \; \dots, \; x_{n})]$$OR
$$ 
T \begin{pmatrix}
x_{1} \\
\vdots \\
x_{n} \\
\end{pmatrix} = \begin{bmatrix}
f_1(x_1, \dots, x_n) \\
\vdots \\
f_m(x_1, \dots, x_n)
\end{bmatrix}
$$

- The vector $$T(x) \in \mathbb{R}^n$$in the transformation $$T: \mathbb{R}^n \to \mathbb{R}^m$$is the **image** of *x* under *T*. 
  
- The **pre-image** of $$v \in \mathbb{R}^m$$under the linear transformation$$T: \mathbb{R}^n \to \mathbb{R}^m$$is the set of all elements $$u \in \mathbb{R}^n$$such that $$T(u) = v$$
- The set of all elements of form *T(x)* where $$x \in \mathbb{R}^n$$ for a given transformation $$T: \mathbb{R}^n \to \mathbb{R}^m$$is the **range** of *T*. 
	- ![[Screenshot 2025-04-02 at 11.11.56 AM.png]]
	- ![[Screenshot 2025-04-02 at 11.18.04 AM.png]]
	- ![[Screenshot 2025-04-02 at 11.18.31 AM.png]]



## Linear Transformations:
- A **linear transformation** is a transformation that preserves the following properties for all vectors ***u*** and ***v*** in the domain of *T* and all scalars *r*. 
- Properties of linear transformations:
	- Additivity Property: $$T(u+v) = T(u)+T(v)$$
	- Homogeneity Property: $$T(rv) = rT(v)$$
	- These properties of vector algebra can be used to determine if a transformation is or is not a linear transformation.
- Determining whether a transformation is a linear transformation:
	- **EXAMPLE:** Use the properties of linear transformations to determine whether each of the following transformations is a linear transformation.
	  $$
	  a. \; T(\begin{bmatrix}
x_{1} \\
x_{2} \\
 \end{bmatrix}) = 
 \begin{bmatrix} 
x_{1} - x_{2} \\
x_{2} \\
\end{bmatrix}
	   $$$$
	  b. \; S(\begin{bmatrix}
x_{1} \\
x_{2} \\
 \end{bmatrix}) = 
 \begin{bmatrix} 
x_{1} \\
x_{1}x_{2} \\
\end{bmatrix}
	   $$
	   Solutions:
		- **a.** 
		  *T* satisfies the additivity property:$$
		  T(u+v) = T(\begin{bmatrix}
u_{1} + v_{1} \\
u_{2} + v_{2}
\end{bmatrix}
		  )
		  $$$$
		  = \begin{bmatrix}
u_{1} + v_{1} - (u_{2} + v_{2}) \\
u_{2}+v_{2} \\
\end{bmatrix}
		  $$$$
		  = \begin{bmatrix}
(u_{1}-u_{2}) +(v_{1}-v_{2}) \\
u_{2}+v_{2} \\
\end{bmatrix}
		  $$$$
		  = \begin{bmatrix}
u_{1}-u_{2} \\
u_{2} \\
\end{bmatrix} + \begin{bmatrix}
v_{1}-v_{2} \\
v_{2} \\
\end{bmatrix}
		  $$$$T(u) + T(v)$$
		  *T* also satisfies the homogeneity property:$$ T(rv) = T(r
		  \begin{bmatrix}
v_{1} \\
v_{2} \\
\end{bmatrix}
		  )
		  $$$$ = T(
		  \begin{bmatrix}
rv_{1} \\
rv_{2} \\
\end{bmatrix}
		  )
		  $$$$ = 
		  \begin{bmatrix}
rv_{1} - rv_{2} \\
rv_{2} \\
\end{bmatrix}
		  $$$$ =r 
		  \begin{bmatrix}
v_{1} - v_{2} \\
v_{2} \\
\end{bmatrix}
		  $$$$= rT(v)$$
		  Since BOTH the additivity and homogeneity properties are satisfied, *T* is a **linear transformation**.
		- **b.**
		  *S* does NOT satisfy the additivity property:$$
		  S(u+v) = S(\begin{bmatrix}
u_{1} + v_{1} \\
u_{2} + v_{2} \\
\end{bmatrix}
		  )
		  $$$$
		   = \begin{bmatrix}
u_{1} + v_{1} \\
(u_{1} + v_{1}) + (u_{2} + v_{2}) \\
\end{bmatrix}
		  $$$$
		   \neq \begin{bmatrix}
u_{1} + v_