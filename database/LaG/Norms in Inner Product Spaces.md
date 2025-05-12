
## Definition
Given an inner product space $(V, \langle \cdot, \cdot \rangle)$, the **corresponding norm** is defined as:
$$
\|\mathbf{x}\| := \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}
$$

## Key Properties
1. **Positive definiteness**: 
   $$\|\mathbf{x}\| \geq 0 \text{ with equality iff } \mathbf{x} = \mathbf{0}$$

2. **Absolute homogeneity**: 
   $$\|\alpha\mathbf{x}\| = |\alpha|\|\mathbf{x}\|$$

3. **Triangle inequality**: 
   $$\|\mathbf{x}+\mathbf{y}\| \leq \|\mathbf{x}\| + \|\mathbf{y}\|$$

## Examples

### 1. Euclidean Norm ($\mathbb{R}^n$)
For standard [[Inner Product]] $\langle \mathbf{x}, \mathbf{y} \rangle = \sum_{i=1}^n x_i y_i$:
$$
\|\mathbf{x}\|_2 = \sqrt{\sum_{i=1}^n x_i^2}
$$

### 2. $L^2$ Function Norm
For $f \in C([a,b])$ with $\langle f,g \rangle = \int_a^b f(x)g(x)dx$:
$$
\|f\|_2 = \sqrt{\int_a^b |f(x)|^2 dx}
$$

### 3. Weighted Norm
Given positive weights $w_i$ and $\langle \mathbf{x}, \mathbf{y} \rangle_w = \sum_{i=1}^n w_i x_i y_i$:
$$
\|\mathbf{x}\|_w = \sqrt{\sum_{i=1}^n w_i x_i^2}
$$

## Applications
- **Geometry**: Measures vector length
- **Optimization**: Used in regularization
- **Physics**: Represents energy in quantum systems

> **Note**: All norms induced by inner products satisfy the parallelogram law:
> $$\|\mathbf{x}+\mathbf{y}\|^2 + \|\mathbf{x}-\mathbf{y}\|^2 = 2(\|\mathbf{x}\|^2 + \|\mathbf{y}\|^2)$$

# Related
1. [[Notm of a Vector]]