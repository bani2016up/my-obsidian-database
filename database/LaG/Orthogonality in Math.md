## 1. Fundamental Definition
Two vectors **u** and **v** in an inner product space are **orthogonal** if:

$$
\langle \mathbf{u}, \mathbf{v} \rangle = 0
$$

where $\langle \cdot, \cdot \rangle$ is the [[Inner Product]] of the space.

## 2. Key Concepts

### 2.1 Geometric Interpretation
- In $\mathbb{R}^2$/$\mathbb{R}^3$: Orthogonal vectors are perpendicular (90° angle)
- Generalization: The angle $\theta$ between vectors satisfies:
  $$
  \cos \theta = \frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\|\mathbf{u}\|\|\mathbf{v}\|}
  $$

### 2.2 Orthogonal Sets
A set $\{\mathbf{v}_1, ..., \mathbf{v}_n\}$ is:
- **Orthogonal** if $\langle \mathbf{v}_i, \mathbf{v}_j \rangle = 0$ for all $i \neq j$
- **Orthonormal** if also $\|\mathbf{v}_i\| = 1$ for all $i$

## 3. Important Examples

### 3.1 Vector Spaces
- Standard basis in $\mathbb{R}^n$: $\mathbf{e}_i \cdot \mathbf{e}_j = \delta_{ij}$
- Fourier basis: $\{1, \cos x, \sin x, \cos 2x, ...\}$ under $L^2$ inner product

### 3.2 Function Spaces
Legendre polynomials $P_n(x)$ on $[-1,1]$:
$$
\int_{-1}^1 P_m(x)P_n(x)dx = \frac{2}{2n+1}\delta_{mn}
$$

### 3.3 Matrix Algebra
- Orthogonal matrices: $Q^TQ = I$
- SVD: $U$ and $V$ contain orthogonal vectors

## 4. Core Properties

1. **Pythagorean Theorem**:
   $$
   \|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2 \iff \mathbf{u} \perp \mathbf{v}
   $$

2. **Linear Independence**:
   Any orthogonal set of non-zero vectors is linearly independent

3. **Orthogonal Complement**:
   For subspace $W$, $W^\perp = \{\mathbf{v} : \mathbf{v} \perp \mathbf{w}\ \forall \mathbf{w} \in W\}$

## 5. Applications

### 5.1 Signal Processing
- Walsh/Haar functions for signal decomposition
- Noise removal via orthogonal projections

### 5.2 Quantum Mechanics
- Orthogonal eigenstates in Hilbert spaces
- Commuting observables have orthogonal eigenvectors

### 5.3 Machine Learning
- PCA finds orthogonal directions of maximum variance
- Orthogonal weight initialization in neural networks

## 6. Computational Aspects
| Operation | Complexity | Example |
|-----------|------------|---------|
| Gram-Schmidt | $O(n^3)$ | QR decomposition |
| Checking orthogonality | $O(n^2)$ | Matrix multiplication |
| Projection | $O(n)$ | $\frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\langle \mathbf{v}, \mathbf{v} \rangle}\mathbf{v}$ |

> **Note**: Orthogonality generalizes perpendicularity to abstract spaces while preserving its geometric intuition.