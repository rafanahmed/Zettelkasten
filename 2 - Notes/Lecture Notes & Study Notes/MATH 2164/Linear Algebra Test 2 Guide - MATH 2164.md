

2025-03-27 
03:25 AM


Tags: [[Linear Algebra]], [[Matrix Determinants]], [[Matrix Invertibility]], [[Rank & Nullity Theorem]], [[Column & Row Space]], [[Fundamental Subspaces]], [[Function & Relations]], [[Basis & Dimension]], [[Vector Spaces]], [[Coordinate Systems]]


## Reference:
[[2_18.pdf]], [[2_20.pdf]], [[2_25.pdf]], [[2_27.pdf]], [[3_11.pdf]], [[3_13.pdf]], [[3_18.pdf]], [[3_20.pdf]], [[3_25.pdf]]



##### Subject/Concept 1: Properties of Determinants

Theory and Explanation:
- Elementary Row Operations:
	- Determinants respond predictably to basic row operations:
		- **Row Interchange:** Swapping two rows (or columns) reverses the sign of the determinant:                                                                                                                                                                   det(B) = -det(A)
		- **Row Scaling:** Multiplying a single row by a scalar k scales the determinant by k:                                                det(B) = k det(A)                                                  
			- For an n × n matrix scaled entirely by k:                                                                                                   det(kA) = k^n det(A)
		- **Row Addition:** Replacing one row with the sum of itself and a multiple of another row leaves the determinant unchanged:                                                                                                                    det(B) = det(A)

- Consequences:
	- A matrix with a zero row or two proportional (or identical) rows has det⁡ = 0.
	- For triangular matrices, the determinant is the product of the diagonal entries.
	- The multiplicative property holds: det(AB) = det(A) * det(B).

	![[Screenshot 2025-03-27 at 3.58.38 AM.png]]

- **What to know**: It's a number you can calculate from a square matrix.
- **When is it useful**: To check if a matrix is invertible. If `det(A) ≠ 0`, the matrix is invertible.
- **Properties to memorize**:
  - Swapping rows → changes sign of det.
  - Scaling a row by k → det gets multiplied by k.
  - Add a multiple of one row to another → det doesn't change.
  - `det(AB) = det(A) * det(B)`
  - `det(kA) = k^n * det(A)` for n x n matrix.

------------------------------------------------------------------------

##### Subject/Concept 2: Invertibility, Cofactor/Adjoint Matrices, and Cramer’s Rule

Theory and Explanation:
- Invertibility:
	- A square matrix *A* is invertible if and only if `det(A) ≠ 0`.
	- Moreover, if *A* is invertible, then:  
	    - `det(A⁻¹) = 1 / det(A)`
	- Several equivalent conditions exist (e.g., *A* has full pivot positions, the homogeneous system `Ax = 0` has only the trivial solution).

- Cofactor and Adjoint Matrices:
	- Cofactor Matrix: Each entry *aᵢⱼ* has a cofactor *Cᵢⱼ* defined using minors and a sign `(-1)^(i+j)`.
	  - Adjugate (Adjoint) Matrix: The transpose of the cofactor matrix, denoted `adj(A)`, satisfies  
		  - `A · adj(A) = adj(A) · A = det(A)I`.
	  - This relation yields the formula for the inverse:  
		  - `A⁻¹ = (1 / det(A)) · adj(A)`.

- Cramer's Rule:
	- For a system `Ax = b` (with *A* being *n × n* and `det(A) ≠ 0`), the unique solution is given by  
		- `xⱼ = det(Aⱼ) / det(A)`,  where *Aⱼ* is the matrix *A* with its *j*th column replaced by *b*.

- ![[Screenshot 2025-03-27 at 4.18.36 AM.png]]

- A matrix is invertible if:
  - `det(A) ≠ 0`
  - Its reduced row echelon form is the identity matrix
  - It has a pivot in every row and column
- If invertible: `A⁻¹ = (1/det(A)) * adj(A)`
- **Adjoint**: Transpose of the cofactor matrix.

- Cramer's Rule:
	- Used to solve `Ax = b` for square systems.
	- Formula: `x_j = det(A_j) / det(A)`, where `A_j` is `A` with its j-th column replaced by `b`.
	- Only works if `det(A) ≠ 0`.

------------------------------------------------------------------------

##### Subject/Concept 3: Vector Spaces, Subspaces, Spanning Sets, and Linear Independence/Dependence

- Theory and Explanation
	- **Vector Spaces (Euclidean):**
		- ℝⁿ is the set of all *n*-tuples (or *n × 1* column vectors) with operations of vector addition and scalar multiplication defined in the usual way.
	- **Subspaces:**
		- A subset *W* ⊆ ℝⁿ is a subspace if it is nonempty (contains the zero vector) and is closed under vector addition and scalar multiplication.
	- **Spanning Sets and Linear Combinations:**
		- A vector *v* is a linear combination of vectors *v₁, ..., vₖ* if there exist scalars *a₁, ..., aₖ* such that                                                                                                                                                                         `v = a₁v₁ + ⋯ + aₖvₖ`.
		  - The span of a set *S* is the collection of all linear combinations of its vectors.
	- **Linear Independence and Dependence:**
		- Vectors *v₁, ..., vₖ* are linearly independent if the equation                                                                                  `a₁v₁ + ⋯ + aₖvₖ = 0`  
	     has only the trivial solution (*a₁ = ⋯ = aₖ = 0*); otherwise, they are dependent.

- ![[Screenshot 2025-03-27 at 4.23.04 AM.png]]

A vector space is a set where you can do vector addition and scalar multiplication.
- A **subspace** is a smaller vector space inside a bigger one (like a plane through the origin in 3D).
- To be a subspace:
  - Contains the zero vector
  - Closed under addition
  - Closed under scalar multiplication

**Linear combination**: Any expression like `a₁v₁ + a₂v₂ + ... + aₙvₙ`
- **Span**: The set of ALL linear combinations of some vectors.
- If a vector is in the span of others, you can write it as a combination of them.

A set of vectors is **linearly independent** if NO vector can be written as a combination of the others.
- Otherwise, they’re **dependent**.
- Shortcut: Put them in a matrix → row reduce → if any row of all zeros appears, they’re dependent.

------------------------------------------------------------------------

##### Subject/Concept 4: Basis, Dimension, and General Vector Spaces

- Theory and Explanation:
	- **Basis:**  
		- A basis of a vector space *V* is a set of vectors that is both a spanning set for *V* and linearly independent.
	- **Dimension:**  
		- The dimension of *V* is the number of vectors in any basis for *V*.
	- **General (Abstract) Vector Spaces:**  
		- Beyond ℝⁿ, vector spaces can include, for example, the set of all *2 × 2* matrices or polynomial spaces *Pₙ* (polynomials of degree ≤ *n*). The same axioms apply.

- ![[Screenshot 2025-03-27 at 4.31.34 AM.png]]

A **basis** is a minimal set of vectors that span a space AND are linearly independent.
- The **dimension** is how many vectors are in the basis.
- To find it: Row reduce → count pivot columns = dimension.

Changing coordinates from basis `B` to `C`:
  - Multiply: `[v]_C = M_C⁻¹ * M_B * [v]_B`
- `P_(B→C) = M_C⁻¹ * M_B`


------------------------------------------------------------------------

##### Subject/Concept 5: Coordinatization and Change of Coordinates

Theory and Explanation:
- Coordinatization:
	-  Given a basis *B = {u₁, u₂, ..., uₙ}* for a vector space *V*, every vector *v* can be written uniquely as  
		- `v = c₁u₁ + c₂u₂ + ⋯ + cₙuₙ`.  
	-  The coordinate vector of *v* relative to *B* is:
		- {v]_B = { c₁ ] { c₂ ] { ... ] { cₙ ]
		- This is computed by forming the matrix *M_B* with columns *u₁, u₂, ..., uₙ* and then
			- `[v]_B = M_B⁻¹ v`.
	- **Change of Coordinates:**  
		- To change from basis *B* to another basis *C*, if *M_B* and *M_C* are the matrices formed by the bases, then the transition (or change-of-coordinates) matrix is  
			- `P_{B→C} = M_C⁻¹ M_B`,  
			and for any vector *u*,  
			- `[u]_C = M_C⁻¹ u = P_{B→C}[u]_B`.

	![[Screenshot 2025-03-27 at 5.01.03 AM.png]]

When using a **non-standard basis**, you express vectors as combinations of new basis vectors.
- To find `[v]_B`: Solve `M_B * x = v` or just compute `M_B⁻¹ * v`.

Changing coordinates from basis `B` to `C`:
  - Multiply: `[v]_C = M_C⁻¹ * M_B * [v]_B`
- `P_(B→C) = M_C⁻¹ * M_B`

------------------------------------------------------------------------

##### Subject/Concept 6: Four Fundamental Subspaces

- Theory and Explanation
	- For any *m × n* matrix *A*:
		- **Column Space (`col(A)`):**  
		  The span of the columns of *A*; a subspace of ℝᵐ. Its dimension is called the rank of *A*.
		- **Null Space (`null(A)`):**  
		  The set of all solutions to *Ax = 0*; a subspace of ℝⁿ. Its dimension (nullity) is the number of free variables.
		- **Row Space (`row(A)`):**  
		  The span of the rows of *A*; it has the same dimension as the column space.
		- **Left Null Space (`null(Aᵀ)`):**  
		  The set of all solutions to *Aᵀy = 0*; a subspace of ℝᵐ.

- The **Rank-Nullity Theorem** states:  
	- rank(A) + dim(null(A)) = n
		- Similarly, for *Aᵀ*:
			- rank(Aᵀ) + dim(null(Aᵀ)) = m

	 ![[Screenshot 2025-03-27 at 5.38.38 AM.png]]

Given a matrix `A`, you care about:
- **Column Space (Col A)**: All outputs `Ax`
- **Row Space**: Span of row vectors of `A`
- **Null Space (Nul A)**: All `x` such that `Ax = 0`
- **Left Null Space**: All `x` such that `Aᵗx = 0`

rank(A) + nullity(A) = number of columns in A
  

------------------------------------------------------------------------

## TI-84 Calculator Guide

### 1. Compute the Determinant of a Matrix

**Use for**:
- Checking invertibility
- Applying Cramer’s Rule
- Verifying properties like `det(AB) = det(A) * det(B)`
- Validating row operation effects

**TI-84 Steps**:
1. `2nd` → `MATRIX` → `EDIT` → Choose `[A]`, enter matrix.
2. `2nd` → `QUIT` → Return to home screen.
3. `2nd` → `MATH` → Choose `det(`.
4. `2nd` → `MATRIX` → Select `[A]` → Close `)`, then `ENTER`.

---

### 2. Perform Elementary Row Operations (via RREF)

**Use for**:
- Solving systems
- Finding pivot positions
- Determining linear independence
- Constructing basis from spanning sets

**TI-84 Steps**:
1. `2nd` → `MATRIX` → `EDIT` → Input matrix `[A]`.
2. On home: `2nd` → `MATRIX` → `MATH` → Select `rref(`.
3. Then `2nd` → `MATRIX` → Choose `[A]`, close `)`, then `ENTER`.

---

### 3. Compute Inverse of a Matrix

**Use for**:
- Coordinate vector transformations: `[v]_B = M_B⁻¹ * v`
- Change of basis
- Solving systems `x = A⁻¹b`

**TI-84 Steps**:
1. Store `[A]` via `2nd` → `MATRIX` → `EDIT`.
2. On home screen: `[A]` → `x⁻¹` (via `x⁻¹` button) → `ENTER`.

---

### 4. Multiply Matrices

**Use for**:
- Matrix equations like `M_B⁻¹ * v` or `M_C⁻¹ * M_B`
- Changing coordinates
- Linear combinations

**TI-84 Steps**:
1. Input `[A]` and `[B]` into matrices.
2. On home: `[A]` `*` `[B]` → `ENTER`.

---

### 5. Multiply Matrix by Scalar

**Use for**:
- Verifying determinant rules like `det(kA) = kⁿ * det(A)`
- Row/column scaling

**TI-84 Steps**:
1. Enter scalar → `*` → `2nd` → `MATRIX` → select matrix.
2. `ENTER`.

---

### 6. Use Cramer’s Rule

**Use for**:
- Solving `Ax = b` using `xⱼ = det(Aⱼ) / det(A)`

**TI-84 Steps**:
1. Compute `det(A)` and `det(Aⱼ)` where you replace j-th column with b.
2. Use steps from #1 to compute each determinant.
3. Divide: `det(Aⱼ)/det(A)` manually.

---

### 7. Solve System via Inverse Matrix

**Use for**:
- Shortcut solution to `Ax = b`

**TI-84 Steps**:
1. Enter matrix `[A]` and vector `[B]` (as a column matrix).
2. On home: `[A]⁻¹ * [B]` → `ENTER`.

---

### 8. Find a Basis (from Spanning Set)

**Use for**:
- Determining independence and dimension
- Finding basis from spanning set using Gaussian elimination

**TI-84 Steps**:
1. Store vectors as rows in a matrix `[A]`.
2. Perform `rref([A])`.
3. Look at pivot rows/columns to find basis vectors.

---

### 9. Construct Coordinate Vector `[v]_B`

**Use for**:
- Coordinatization in a non-standard basis

**TI-84 Steps**:
1. Form matrix `[M_B]` with basis vectors as columns.
2. Compute inverse: `M_B⁻¹`.
3. Multiply: `M_B⁻¹ * v`.

---

### 10. Change of Basis (from B to C)

**Use for**:
- Computing `[v]_C = M_C⁻¹ * M_B * [v]_B`

**TI-84 Steps**:
1. Input `M_B` and `M_C` into `[A]`, `[B]`.
2. Compute inverse: `M_C⁻¹ = [B]⁻¹`.
3. Multiply: `M_C⁻¹ * M_B`.

---

### 11. Compute Adjoint (Transpose of Cofactor Matrix)

**Use for**:
- Inverse via `A⁻¹ = 1/det(A) * adj(A)`

**TI-84 Steps**:
WARNING: TI-84 **cannot compute cofactors or adjoints directly**, but you can:
- Manually input the cofactor matrix as `[C]`.
- Use `2nd` → `MATRIX` → `MATH` → `Transpose(` to get `adj(A)`.

---

### 12. Compute Rank (Number of Pivots)

**Use for**:
- Applying Rank-Nullity Theorem
- Finding dimension of Column Space or Row Space

**TI-84 Steps**:
1. Perform `rref([A])`.
2. Count non-zero rows to get rank.

---

### 13. Test Linear Independence

**Use for**:
- Determining if vectors form a basis

**TI-84 Steps**:
1. Store vectors as rows of `[A]`.
2. Perform `rref([A])` and see if there are any free variables (non-pivot columns).






## Linear Algebra Formula Sheet (LaTeX Ready)

---

## Determinants

- Row swap: $\det(B) = -\det(A)$
- Row scaling: $\det(B) = k \cdot \det(A)$
- Row replacement: $\det(B) = \det(A)$
- Triangular matrix: $\det(A)$ = product of diagonal entries
- Multiplicative property: $\det(AB) = \det(A) \cdot \det(B)$
- Scalar multiplication: $\det(kA) = k^n \cdot \det(A)$

---

## Invertibility

A square matrix $A$ is invertible **iff**:
- $\det(A) \ne 0$
- $rref(A) = I_n$
- $Ax = 0$ has only the trivial solution
- $A$ has $n$ pivot positions
- $A^{-1} = \frac{1}{\det(A)} \cdot \text{adj}(A)$

---

## Cramer’s Rule

For $Ax = b$:
- $x_j = \frac{\det(A_j)}{\det(A)}$
- $A_j$ = matrix $A$ with the $j^{th}$ column replaced by $b$

---

## Vector Spaces & Subspaces

- Subset $W \subseteq \mathbb{R}^n$ is a subspace if:
  1. $0 \in W$
  2. Closed under addition
  3. Closed under scalar multiplication

---

## Linear Combinations & Span

- $\text{Span}(v_1, v_2, \dots, v_k) = \{a_1v_1 + a_2v_2 + \dots + a_kv_k\}$
- Set of all linear combinations of vectors

---

## Linear Independence

- Vectors $\{v_1, \dots, v_k\}$ are linearly independent if:
  - $a_1v_1 + \dots + a_kv_k = 0$ has only the trivial solution

---

## Basis & Dimension

- Basis = Linearly independent spanning set
- Dimension = Number of vectors in any basis
- Every vector $v$ in a space $V$ has a unique representation:
  $v = c_1v_1 + \dots + c_nv_n$

---

## Coordinate Vector

- For basis $B = \{b_1, \dots, b_n\}$:
  - $[v]_B = M_B^{-1}v$
  - $M_B$ = matrix with $b_i$ as columns

---

## Change of Basis

- From basis $B$ to $C$:
  - $[v]_C = M_C^{-1}M_B[v]_B$
  - $P_{B \to C} = M_C^{-1}M_B$

---

## Four Fundamental Subspaces

For matrix $A$:
- **Column Space**: span of columns of $A$
- **Row Space**: span of rows of $A$
- **Null Space**: solutions to $Ax = 0$
- **Left Null Space**: solutions to $A^Tx = 0$

**Rank-Nullity Theorem**:
$$
\text{rank}(A) + \text{nullity}(A) = n
$$

---

## Adjoint and Cofactor

- Adjoint: $\text{adj}(A) = (\text{cofactor matrix})^T$
- Inverse: $A^{-1} = \frac{1}{\det(A)} \cdot \text{adj}(A)$ (if $\det(A) \ne 0$)







