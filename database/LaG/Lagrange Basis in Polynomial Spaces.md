
## 1. Definition
The **Lagrange basis** is a set of polynomials $\{L_0(x), L_1(x), \dots, L_n(x)\}$ constructed for a given set of distinct points $\{x_0, x_1, \dots, x_n\}$. Each basis polynomial $L_i(x)$ satisfies:

$$
L_i(x_j) = \delta_{ij} = 
\begin{cases} 
1 & \text{if } i = j, \\
0 & \text{if } i \neq j,
\end{cases}
$$

where $\delta_{ij}$ is the [[Kronecker Delta Function]].

## 2. Explicit Construction
For points $\{x_0, \dots, x_n\}$, the $i$-th Lagrange polynomial is:

$$
L_i(x) = \prod_{\substack{j=0 \\ j \neq i}}^n \frac{x - x_j}{x_i - x_j}
$$

### Example (3 points: 0,1,2)
$$
\begin{aligned}
L_0(x) &= \frac{(x-1)(x-2)}{(0-1)(0-2)} = \frac{1}{2}(x^2-3x+2) \\
L_1(x) &= \frac{x(x-2)}{(1-0)(1-2)} = -x^2+2x \\
L_2(x) &= \frac{x(x-1)}{(2-0)(2-1)} = \frac{1}{2}(x^2-x)
\end{aligned}
$$

## 3. Key Properties
1. **Interpolation**: 
   - Any polynomial $p(x)$ of degree $\leq n$ can be written as:
     $$
     p(x) = \sum_{i=0}^n p(x_i) L_i(x)
     $$

1. **[[LaG/Orthogonality in Math|Orthogonality in Math]]**:
   - For discrete [[Inner Product]] of the form:
     $$
     \langle p, q \rangle = \sum_{k=0}^n p(x_k)q(x_k)
     $$
     the Lagrange basis is orthonormal:
     $$
     \langle L_i, L_j \rangle = \delta_{ij}
     $$

3. **Partition of Unity**:
   $$
   \sum_{i=0}^n L_i(x) = 1 \quad \forall x
   $$

## 4. Applications
1. **Polynomial Interpolation**:
   - Directly gives the interpolating polynomial through points $(x_i, y_i)$:
     $$
     p(x) = \sum_{i=0}^n y_i L_i(x)
     $$

2. **Numerical Analysis**:
   - Basis for finite element methods
   - Used in quadrature rules

3. **Signal Processing**:
   - Reconstruction of bandlimited signals

## 5. Advantages/Disadvantages
| Pros                             | Cons                                             |
| -------------------------------- | ------------------------------------------------ |
| Exact interpolation at nodes     | High computational cost for many points          |
| Numerically stable for small $n$ | Poor behavior between nodes (Runge's phenomenon) |
| Explicit formula available       | Degree grows with number of points               |

## 6. Connection to Other Concepts
- **Vandermonde Matrix**: Lagrange basis avoids solving Vandermonde systems
- **Bernstein Polynomials**: Alternative basis with better numerical stability
- **Orthogonal Polynomials**: Different approach using continuous inner products

> **Note**: For $n+1$ points, the Lagrange basis gives degree-$n$ polynomials that form a basis for $\mathbb{R}[x,n]$.