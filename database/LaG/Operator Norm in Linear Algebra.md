## Definition
Given a linear operator \( A: V \to W \) between normed vector spaces, the **operator norm** (or induced norm) is defined as:
$$
\|A\|_{op} := \sup_{\substack{x \in V \\ x \neq 0}} \frac{\|Ax\|_W}{\|x\|_V} = \sup_{\|x\|_V = 1} \|Ax\|_W
$$
where \(\|\cdot\|_V\) and \(\|\cdot\|_W\) are the norms on \(V\) and \(W\) respectively.

### Key Properties
1. **Submultiplicativity**: \(\|AB\| \leq \|A\|\|B\|\)
2. **Equivalent Definition**: Smallest constant \(C\) such that \(\|Ax\| \leq C\|x\|\) for all \(x\)
3. **Finite-Dimensional Case**: Always finite for linear maps between finite-dimensional spaces

## Examples

### 1. Matrix Norms (Euclidean Space)
For \( A \in \mathbb{R}^{m \times n} \):
$$
\|A\|_{op} = \sup_{\|x\|_2 = 1} \|Ax\|_2
$$
- **Special Case**: For symmetric matrices, equals spectral radius \(\rho(A)\)
- **Example**: \( A = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \) has \(\|A\|_{op} = 2\)

### 2. Integral Operators
For \( K: L^2([0,1]) \to L^2([0,1]) \) defined by:
$$
(Kf)(x) = \int_0^1 k(x,y)f(y)dy
$$
The operator norm satisfies:
$$
\|K\|_{op} \leq \left(\int_0^1 \int_0^1 |k(x,y)|^2 dx dy\right)^{1/2}
$$

### 3. Differential Operators
For \( D: C^1([0,1]) \to C([0,1]) \) with \(\|f\| = \sup |f(x)|\):
$$
\|D\|_{op} = \infty \quad \text{(unbounded operator)}
$$

## Computation Methods
| Space Type       | Common Technique                     |
|------------------|--------------------------------------|
| Finite-Dimensional | Singular Value Decomposition       |
| Hilbert Space    | Spectral Theorem                    |
| Banach Space     | Often requires explicit estimation |

> **Note**: For matrices, the operator norm coincides with the largest singular value (spectral norm).