## 1. Definition
The notation $||\mathbf{x}||$ represents the **norm** (or length) of a vector $\mathbf{x}$ in a vector space. Formally, it's a function satisfying:

1. **Positive definiteness**([[Positive and Negative Definiteness]]): $||\mathbf{x}|| \geq 0$ with equality iff $\mathbf{x} = \mathbf{0}$
2. **Absolute homogeneity**: $||\alpha\mathbf{x}|| = |\alpha| \cdot ||\mathbf{x}||$
3. **Triangle inequality**: $||\mathbf{x}+\mathbf{y}|| \leq ||\mathbf{x}|| + ||\mathbf{y}||$

## 2. Common Norm Types

### 2.1 Euclidean Norm (ℓ²)
For $\mathbf{x} \in \mathbb{R}^n$:
$$
||\mathbf{x}||_2 = \sqrt{\sum_{i=1}^n x_i^2}
$$
- Induced by standard inner product: $||\mathbf{x}|| = \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}$

### 2.2 Manhattan Norm (ℓ¹)
$$
||\mathbf{x}||_1 = \sum_{i=1}^n |x_i|
$$

### 2.3 Maximum Norm (ℓ∞)
$$
||\mathbf{x}||_\infty = \max_{1 \leq i \leq n} |x_i|
$$

## 3. Geometric Interpretation
- Represents "length" of vector in abstract spaces
- Unit circle varies by norm type:
  - ℓ²: Perfect circle
  - ℓ¹: Diamond shape
  - ℓ∞: Square

## 4. Key Properties
1. **Normalization**: Any non-zero $\mathbf{x}$ can be scaled to unit vector $\frac{\mathbf{x}}{||\mathbf{x}||}$
2. **Orthogonality**: In inner product spaces, $||\mathbf{x}+\mathbf{y}||^2 = ||\mathbf{x}||^2 + ||\mathbf{y}||^2$ when $\mathbf{x} \perp \mathbf{y}$
3. **Continuity**: All norms are equivalent in finite dimensions

## 5. Applications
- **Machine Learning**: Regularization terms (L1/L2 norms)
- **Physics**: Magnitude of forces/fields
- **Optimization**: Convergence criteria

> **Note**: In function spaces, $||f||$ typically denotes the $L^p$ norm $\left(\int |f|^p dx\right)^{1/p}$