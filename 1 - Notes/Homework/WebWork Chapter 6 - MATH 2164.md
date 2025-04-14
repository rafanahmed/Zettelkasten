

2025-04-12 
02:42 PM


Tags:


## Reference:
![[Math2164DYs.rahmed6.Chapter_6.pdf]]


# Linear Transformations Cheat Sheet

---

## 1. Fundamentals of Linear Transformations

### Definition and Axioms

A function $$ T: V \to W $$is a linear transformation if, for all $$ \mathbf{u}, \mathbf{v} \in V $$and all scalars $$ c $$it satisfies:

- **Additivity:**
  $$
  T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
  $$

- **Homogeneity (Scalar Multiplication):**
  $$
  T(c\mathbf{u}) = c\,T(\mathbf{u})
  $$

- **Zero Preservation:**  
  A linear transformation must satisfy:
  $$
  T(\mathbf{0}) = \mathbf{0}
  $$

*Use these tests when analyzing functions defined on vectors, matrices, or polynomials (e.g., Problems 1, 3, and 4).*

### Recognizing Nonlinearity

Functions that include extra terms (constants, absolute values, etc.) or non-homogeneous operations typically are **not** linear. For example, functions with components like $$ x+4 $$ or $$ |x_2| $$ fail the linearity tests.

---

## 2. Matrix Representations of Linear Transformations

### Creating the Transformation Matrix

- **Standard Basis Method:**  
  For a linear transformation $$ T: \mathbb{R}^n \to \mathbb{R}^m $$, compute the images of the standard basis vectors $$ \mathbf{e}_1, \mathbf{e}_2, \dots, \mathbf{e}_n $$
  
  The image $$ T(\mathbf{e}_i) $$ becomes the $$ i^\text{th} $$ column of the matrix $$ A $$:
  $$
  T(\mathbf{x}) = A\mathbf{x}
  $$

- **Example:**  
  In problems such as Problems 14 and 16, calculate $$ T(\mathbf{e}_i) $$ and arrange them as columns of $$ A $$

### Special Cases: Conjugation and Transposition

- **Conjugation Transformation:**  
  A transformation of the form
  $$
  T(A) = S A S^{-1}
  $$
  is linear because it is built from matrix multiplications.

- **Transpose Map:**  
  The transformation defined by
  $$
  f(A) = A^T
  $$
  is linear since:
  $$
  (A+B)^T = A^T + B^T \quad \text{and} \quad (cA)^T = cA^T.
  $$

---

## 3. Kernel (Null Space) and Range (Image)

### Key Definitions

- **Kernel (Null Space):**
  $$
  \ker(T) = \{\, \mathbf{x} \in V : T(\mathbf{x}) = \mathbf{0} \,\}
  $$
  
- **Range (Image):**
  $$
  \operatorname{range}(T) = \{\, T(\mathbf{x}) : \mathbf{x} \in V \,\}
  $$

### Finding Bases and Dimensions

1. **Set up the equation:**
   $$
   T(\mathbf{x}) = \mathbf{0} \quad \text{or} \quad A\mathbf{x} = \mathbf{0}
   $$

2. **Solve the system via Gaussian elimination:**
   Identify free variables to determine the nullity (dimension of the kernel) and count pivot positions for the rank (dimension of the image).

3. **Rank-Nullity Theorem:**
   $$
   \dim(V) = \operatorname{rank}(T) + \operatorname{nullity}(T)
   $$

*This method is applicable to problems like Problems 12, 13, 23, and 24.*

---

## 4. One-to-One (Injectivity) and Onto (Surjectivity)

### Definitions and Tests

- **One-to-One (Injective):**  
  A transformation is one-to-one if each element of the codomain is the image of at most one element of the domain. Equivalently,  
  $$
  \ker(T) = \{\mathbf{0}\}.
  $$

- **Onto (Surjective):**  
  A transformation is onto if every element in the codomain has a preimage in the domain:
  $$
  \operatorname{range}(T) = W.
  $$

### How to Verify

- **Injectivity:**  
  Check if $$ \ker(T) $$ is trivial. If not, the transformation is not one-to-one.

- **Surjectivity:**  
  Use the transformation matrix $$ A $$ and check if its columns span the codomain.

*These tests are essential for Problems 7, 8, 10, 11, and 20.*

---

## 5. Inverse Transformations

### When Inverses Exist

- **Invertibility:**  
  A linear transformation $$ T $$ is invertible if and only if it is both one-to-one and onto. For matrices, this means that the square matrix $$ A $$ must have a nonzero determinant.

- **2×2 Matrix Inverse Formula:**  
  For
  $$
  A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
  $$
  with determinant $$ ad - bc \neq 0 $$, the inverse is given by:
  $$
  A^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}.
  $$

### Application

In Problem 14, after obtaining $$ A $$, check invertibility and, if invertible, compute the inverse by the formula above.

---

## 6. Special Topics Involving Different Domains

### Linear Transformations on Matrix Spaces

- **Matrix Spaces $$ M_{n,n}(\mathbb{R}) $$:**  
  When working with transformations on matrices (e.g., transpose, conjugation), use standard matrix arithmetic.

### Linear Transformations on Polynomial Spaces

- **Polynomial Vector Spaces $$ P_k $$:**  
  Use the standard basis $$ \{1, t, t^2, \dots, t^k\} $$.  
  When given a transformation on $$ P_3 $$ or $$ P_2 $$ (like Problems 6 and 18), express the output polynomial in terms of the basis and construct the transformation matrix accordingly.

*Handling different vector spaces (matrices, polynomials, Euclidean spaces) requires flexibility in applying these concepts.*

---

## 7. Typical Problem Steps

When solving problems involving linear transformations, consider the following steps:

1. **Determine if the Transformation is Linear:**
   - Verify additivity and homogeneity.
   - Identify extra terms that would cause failure of linearity.

2. **Express the Transformation in Matrix Form:**
   - Identify the basis (often the standard basis).
   - Compute $$ T(\mathbf{e}_i) $$ for each basis vector and form the matrix from these images.

3. **Analyze the Kernel and Image:**
   - Set up the equation:
     $$
     A\mathbf{x} = \mathbf{0}.
     $$
   - Use Gaussian elimination to determine the kernel and count free variables for the dimension of the image.
   - Apply the Rank-Nullity Theorem.

4. **Test for Injectivity and Surjectivity:**
   - **Injectivity:** Verify that the kernel is trivial.
   - **Surjectivity:** Ensure the image spans the codomain.

5. **Inverse Computation (if Applicable):**
   - Confirm that the transformation’s matrix is square and non-singular.
   - Compute the inverse using standard methods (e.g., 2×2 inverse formula or Gaussian elimination).

6. **Specialized Operations:**
   - For transformations such as evaluation (e.g., $$ T(f(t)) = f(-6) $$), represent the map accordingly (often as mapping to constant functions).

---

## 8. Summary of Essential Formulas

- **Linearity Properties:**
  $$
  T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}) \quad \text{and} \quad T(c\mathbf{u}) = c\,T(\mathbf{u})
  $$

- **Matrix Representation:**
  $$
  T(\mathbf{x}) = A\mathbf{x} \quad \text{with} \quad A = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \cdots & T(\mathbf{e}_n) \end{bmatrix}
  $$

- **Kernel and Range:**
  $$
  \ker(T) = \{ \mathbf{x} \mid A\mathbf{x} = \mathbf{0} \}, \quad \operatorname{range}(T) = \{ A\mathbf{x} \mid \mathbf{x} \in V \}
  $$

- **Rank-Nullity Theorem:**
  $$
  \dim(V) = \operatorname{rank}(T) + \operatorname{nullity}(T)
  $$

- **2×2 Matrix Inverse:**
  $$
  \begin{bmatrix} a & b \\ c & d \end{bmatrix}^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}, \quad \text{if } ad-bc \neq 0.
  $$

- **Determinant of a 2×2 Matrix:**
  $$
  \det \begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc.
  $$

---

## Final Thoughts

Review these topics and formulas in depth to prepare for solving problems such as:
- Verifying the linearity of functions.
- Constructing the standard matrix for a transformation.
- Finding the kernel and image via Gaussian elimination.
- Determining one-to-one and onto properties using the Rank-Nullity Theorem.
- Computing inverses when the transformation is bijective.
- Handling special cases in matrix and polynomial vector spaces.





