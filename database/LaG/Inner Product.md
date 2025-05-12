## 1. Definition
An **inner product** on a real vector space $V$ is a function $\langle \cdot, \cdot \rangle: V \times V \to \mathbb{R}$ satisfying for all $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ and $a \in \mathbb{R}$:

1. **Symmetry**:  
   $$\langle \mathbf{u}, \mathbf{v} \rangle = \langle \mathbf{v}, \mathbf{u} \rangle$$

2. **Linearity**:  
   $$\langle a\mathbf{u} + \mathbf{v}, \mathbf{w} \rangle = a\langle \mathbf{u}, \mathbf{w} \rangle + \langle \mathbf{v}, \mathbf{w} \rangle$$

3. **Positive Definiteness**:  ([[Positive and Negative Definiteness]])
   $$\langle \mathbf{u}, \mathbf{u} \rangle \geq 0 \text{, with equality iff } \mathbf{u} = \mathbf{0}$$

---

## 2. Standard Examples

### Euclidean Inner Product (Dot Product)
For $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$:
$$
\langle \mathbf{u}, \mathbf{v} \rangle = \mathbf{u} \cdot \mathbf{v} = \sum_{i=1}^n u_i v_i
$$

### Weighted Inner Product
Given positive weights $w_i$:
$$
\langle \mathbf{u}, \mathbf{v} \rangle_w = \sum_{i=1}^n w_i u_i v_i
$$

### Function Space Inner Product
For $f, g \in C([a,b])$:
$$
\langle f, g \rangle = \int_a^b f(x)g(x) \, dx
$$

---

## 3. Key Properties

1. **Cauchy-Schwarz Inequality**:  
   $$|\langle \mathbf{u}, \mathbf{v} \rangle| \leq \|\mathbf{u}\| \|\mathbf{v}\|$$

2. **Induced Norm**:  
   $$\|\mathbf{u}\| = \sqrt{\langle \mathbf{u}, \mathbf{u} \rangle}$$

3. **Angle Between Vectors**:  
   $$\theta = \cos^{-1}\left(\frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\|\mathbf{u}\| \|\mathbf{v}\|}\right)$$

4. **[[LaG/Orthogonality in Math|Orthogonality in Math]]**: 
   $\mathbf{u}$ and $\mathbf{v}$ are orthogonal if $\langle \mathbf{u}, \mathbf{v} \rangle = 0$

---

## 4. Matrix Representation
For a basis $\mathcal{B} = \{\mathbf{b}_1, \dots, \mathbf{b}_n\}$, the Gram matrix $G$ encodes the inner product:
$$
G_{ij} = \langle \mathbf{b}_i, \mathbf{b}_j \rangle
$$

- If $\mathcal{B}$ is orthonormal, $G = I_n$ (identity matrix)
- For vectors $\mathbf{u}, \mathbf{v}$ expressed in $\mathcal{B}$:
  $$\langle \mathbf{u}, \mathbf{v} \rangle = [\mathbf{u}]_\mathcal{B}^T G [\mathbf{v}]_\mathcal{B}$$

---

## 5. Applications

1. **Geometry**:  
   - Lengths and angles in vector spaces
   - Projections: $\text{proj}_{\mathbf{v}} \mathbf{u} = \frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\langle \mathbf{v}, \mathbf{v} \rangle} \mathbf{v}$

2. **Signal Processing**:  
   - Correlation as inner product

3. **Quantum Mechanics**:  
   - Probability amplitudes $\langle \psi|\phi \rangle$

4. **Machine Learning**:  
   - Kernel methods use generalized inner products