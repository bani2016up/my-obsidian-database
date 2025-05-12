
## 1. Positive Definite Matrices

### Definition
A symmetric matrix $$ A \in \mathbb{R}^{n \times n} $$ is **positive definite** if for all non-zero vectors $$ \mathbf{x} \in \mathbb{R}^n $$:

$$
\mathbf{x}^T A \mathbf{x} > 0
$$

### Key Properties
1. All eigenvalues are **positive** ($$\lambda_i > 0$$)
2. The determinant is positive ($$\det(A) > 0$$)
3. All leading principal minors are positive

### Example
Consider the matrix:
$$
A = \begin{pmatrix} 2 & -1 \\ -1 & 2 \end{pmatrix}
$$

**Verification:**
1. Quadratic form:
   $$
   \mathbf{x}^T A \mathbf{x} = 2x_1^2 - 2x_1x_2 + 2x_2^2 = x_1^2 + x_2^2 + (x_1 - x_2)^2 > 0 \quad \forall \mathbf{x} \neq \mathbf{0}
   $$
2. Eigenvalues:
   $$
   \det(A - \lambda I) = \lambda^2 - 4\lambda + 3 = 0 \implies \lambda = 1, 3 \quad (\text{both positive})
   $$

---

## 2. Negative Definite Matrices

### Definition
A symmetric matrix $$ A $$ is **negative definite** if:
$$
\mathbf{x}^T A \mathbf{x} < 0 \quad \forall \mathbf{x} \neq \mathbf{0}
$$

### Key Properties
1. All eigenvalues are **negative** ($$\lambda_i < 0$$)
2. Leading principal minors alternate in sign:
   - Odd order: $$\det(A_k) < 0$$
   - Even order: $$\det(A_k) > 0$$

### Example
Matrix:
$$
B = \begin{pmatrix} -2 & 1 \\ 1 & -2 \end{pmatrix}
$$

**Verification:**
1. Quadratic form:
   $$
   \mathbf{x}^T B \mathbf{x} = -2x_1^2 + 2x_1x_2 - 2x_2^2 = -\left[x_1^2 + x_2^2 + (x_1 - x_2)^2\right] < 0
   $$
2. Eigenvalues:
   $$
   \det(B - \lambda I) = \lambda^2 + 4\lambda + 3 = 0 \implies \lambda = -1, -3 \quad (\text{both negative})
   $$

---

## 3. Tests for Definiteness

### Sylvester's Criterion
For a matrix $$ A $$:

| Definiteness       | Condition                          |
|--------------------|-----------------------------------|
| Positive definite  | $$\det(A_k) > 0 \quad \forall k$$ |
| Negative definite  | $$(-1)^k \det(A_k) > 0 \quad \forall k$$ |

### Example
For $$ A = \begin{pmatrix} 2 & -1 & 0 \\ -1 & 2 & -1 \\ 0 & -1 & 2 \end{pmatrix} $$:

$$
\begin{aligned}
\det(A_1) &= 2 > 0 \\
\det(A_2) &= \begin{vmatrix} 2 & -1 \\ -1 & 2 \end{vmatrix} = 3 > 0 \\
\det(A_3) &= 4 > 0
\end{aligned}
$$
⇒ Positive definite

---

## 4. Applications

### Optimization
- **Hessian matrix**:
  $$
  H(f) \text{ positive definite} \Rightarrow \text{Local minimum}
  $$
  $$
  H(f) \text{ negative definite} \Rightarrow \text{Local maximum}
  $$

### Statistics
- Covariance matrices are positive definite:
  $$
  \Sigma = \mathbb{E}[(\mathbf{X} - \mu)(\mathbf{X} - \mu)^T]
  $$