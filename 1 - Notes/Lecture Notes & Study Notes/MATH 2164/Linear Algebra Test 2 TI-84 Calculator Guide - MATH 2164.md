

2025-03-27 
06:18 AM


Tags: [[Linear Algebra]], [[Matrix Determinants]], [[Matrix Invertibility]], [[Rank & Nullity Theorem]], [[Column & Row Space]], [[Fundamental Subspaces]], [[Function & Relations]], [[Basis & Dimension]], [[Vector Spaces]], [[Coordinate Systems]]


## Reference:
[[Linear Algebra Test 2 Guide - MATH 2164]], [[Linear Algebra Test 2 TI-84 Calculator Guide - MATH 2164.pdf]]


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
