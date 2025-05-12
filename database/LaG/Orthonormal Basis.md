
## 1. Definition

A set of vectors $$ \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\} $$ in an inner product space is called an **orthonormal basis** if:

$$
\langle \mathbf{v}_i, \mathbf{v}_j \rangle = \delta_{ij} = 
\begin{cases} 
1 & \text{if } i = j, \\
0 & \text{if } i \neq j,
\end{cases}
$$

where $$ \langle \cdot, \cdot \rangle $$ is the [[Inner Product]], and $$ \delta_{ij} $$ is the [[Kronecker Delta Function]]. 

---

## 2. Key Properties

1. **Normality**: $$ \|\mathbf{v}_i\| = 1 $$ for all $$ i $$
2. **[[LaG/Orthogonality in Math|Orthogonality in Math]]**: $$ \mathbf{v}_i \perp \mathbf{v}_j $$ for $$ i \neq j $$
3. **Coordinates**: Any vector $$ \mathbf{x} $$ can be expressed as:
   $$
   \mathbf{x} = \sum_{i=1}^n \langle \mathbf{x}, \mathbf{v}_i \rangle \mathbf{v}_i
   $$

---

## 3. Construction via Gram-Schmidt Process

Given a basis $$ \{\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_n\} $$, construct an orthonormal basis:

1. **Normalize the first vector**:
   $$
   \mathbf{v}_1 = \frac{\mathbf{u}_1}{\|\mathbf{u}_1\|}
   $$
2. **Iterative orthogonalization** for $$ k = 2, \dots, n $$:
   $$
   \mathbf{v}_k = \frac{\mathbf{u}_k - \sum_{i=1}^{k-1} \langle \mathbf{u}_k, \mathbf{v}_i \rangle \mathbf{v}_i}{\left\| \mathbf{u}_k - \sum_{i=1}^{k-1} \langle \mathbf{u}_k, \mathbf{v}_i \rangle \mathbf{v}_i \right\|}
   $$

---

## 4. Example in $$ \mathbb{R}^3 $$

### Given basis:
$$
\mathbf{u}_1 = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}, \quad
\mathbf{u}_2 = \begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix}, \quad
\mathbf{u}_3 = \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}
$$

### Step 1: Normalize $$ \mathbf{u}_1 $$
$$
\mathbf{v}_1 = \frac{\mathbf{u}_1}{\|\mathbf{u}_1\|} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}
$$

### Step 2: Orthogonalize ([[LaG/Orthogonality in Math|Orthogonality in Math]])$$ \mathbf{u}_2 $$
$$
\mathbf{v}_2' = \mathbf{u}_2 - \langle \mathbf{u}_2, \mathbf{v}_1 \rangle \mathbf{v}_1 = \begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix} - \frac{1}{2} \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} \\ -\frac{1}{2} \\ 1 \end{pmatrix}
$$
$$
\mathbf{v}_2 = \frac{\mathbf{v}_2'}{\|\mathbf{v}_2'\|} = \frac{1}{\sqrt{\frac{3}{2}}} \begin{pmatrix} \frac{1}{2} \\ -\frac{1}{2} \\ 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{\sqrt{6}} \\ -\frac{1}{\sqrt{6}} \\ \frac{2}{\sqrt{6}} \end{pmatrix}
$$

### Step 3: Orthogonalize ([[LaG/Orthogonality in Math|Orthogonality in Math]])$$ \mathbf{u}_3 $$
$$
\mathbf{v}_3' = \mathbf{u}_3 - \langle \mathbf{u}_3, \mathbf{v}_1 \rangle \mathbf{v}_1 - \langle \mathbf{u}_3, \mathbf{v}_2 \rangle \mathbf{v}_2
$$
After calculations:
$$
\mathbf{v}_3 = \begin{pmatrix} -\frac{1}{\sqrt{3}} \\ \frac{1}{\sqrt{3}} \\ \frac{1}{\sqrt{3}} \end{pmatrix}
$$

### Final orthonormal basis:
$$
\mathbf{v}_1 = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} \\ 0 \end{pmatrix}, \quad
\mathbf{v}_2 = \begin{pmatrix} \frac{1}{\sqrt{6}} \\ -\frac{1}{\sqrt{6}} \\ \frac{2}{\sqrt{6}} \end{pmatrix}, \quad
\mathbf{v}_3 = \begin{pmatrix} -\frac{1}{\sqrt{3}} \\ \frac{1}{\sqrt{3}} \\ \frac{1}{\sqrt{3}} \end{pmatrix}
$$

---

## 5. Applications

1. **Fourier Series**:  
   Basis $$ \left\{ \frac{1}{\sqrt{2\pi}}, \frac{\cos nx}{\sqrt{\pi}}, \frac{\sin nx}{\sqrt{\pi}} \right\} $$ for $$ L^2([-\pi, \pi]) $$.

2. **Quantum Mechanics**:  
   Eigenvectors of Hermitian operators form orthonormal bases.

3. **PCA (Principal Component Analysis)**:  
   Covariance matrix eigenvectors are orthonormal.