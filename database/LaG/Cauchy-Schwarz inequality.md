## 1. Fundamental Statement
For any vectors **u**, **v** in an [[Inner Product]] space:

$$
|\langle \mathbf{u}, \mathbf{v} \rangle| \leq \|\mathbf{u}\| \cdot \|\mathbf{v}\|
$$

Equality holds if and only if **u** and **v** are linearly dependent.

## 2. Key Interpretations

### 2.1 Geometric Meaning
- Sets maximum value for inner product relative to vector lengths
- Generalizes the intuition $|\cos \theta| \leq 1$ from Euclidean space

### 2.2 Special Cases
- **Euclidean space** ($\mathbb{R}^n$):
  $$
  \left(\sum_{i=1}^n u_i v_i\right)^2 \leq \left(\sum_{i=1}^n u_i^2\right)\left(\sum_{i=1}^n v_i^2\right)
  $$
  
- **Function spaces** ($L^2$):
  $$
  \left|\int f(x)g(x)dx\right|^2 \leq \int |f(x)|^2 dx \cdot \int |g(x)|^2 dx
  $$

## 3. Proof Techniques

### 3.1 Quadratic Argument
Consider $p(t) = \|\mathbf{u} + t\mathbf{v}\|^2 \geq 0$ and analyze discriminant

### 3.2 Orthogonal Decomposition ([[LaG/Orthogonality in Math|Orthogonality in Math]])
Project **u** onto **v** and use Pythagorean theorem

## 4. Applications

### 4.1 Probability
- Covariance bound:
  $$
  |\text{Cov}(X,Y)| \leq \sqrt{\text{Var}(X)\text{Var}(Y)}
  $$

### 4.2 Physics
- Heisenberg Uncertainty Principle derivation

### 4.3 Machine Learning
- Regularization theory
- Kernel method error bounds

## 5. Related Inequalities
| Inequality | Relation                                                         |
| ---------- | ---------------------------------------------------------------- |
| Triangle   | $\|\mathbf{u}+\mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|$ |
| Hölder     | Generalization to $L^p$ spaces                                   |
| Bessel     | Orthogonal projection bounds                                     |

> **Historical Note**: First proved by Cauchy (1821) for finite sums, later generalized by Schwarz (1885) for integrals.