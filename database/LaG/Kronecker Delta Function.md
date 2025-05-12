## 1. Definition
The **Kronecker delta** is a function of two discrete variables, defined as:

$$
\delta_{ij} = 
\begin{cases} 
1 & \text{if } i = j, \\
0 & \text{if } i \neq j,
\end{cases}
$$

where \( i \) and \( j \) are typically indices (e.g., integers).

---

## 2. Key Properties
1. **Discrete Selector**:  
   Acts as an "identity" for discrete indices:
   $$
   \sum_{j} a_j \delta_{ij} = a_i
   $$

2. **Orthonormality**:  
   Encodes orthonormal basis conditions:
   $$
   \langle \mathbf{v}_i, \mathbf{v}_j \rangle = \delta_{ij}
   $$

3. **Matrix Representation**:  
   The identity matrix \( I_n \) can be written as:
   $$
   I_n = (\delta_{ij})_{1 \leq i,j \leq n}
   $$

---

## 3. Examples

### Example 1: [[Orthonormal Basis]]
For standard basis vectors \( \mathbf{e}_1, \mathbf{e}_2 \) in \( \mathbb{R}^2 \):
$$
\langle \mathbf{e}_1, \mathbf{e}_1 \rangle = 1 = \delta_{11}, \quad
\langle \mathbf{e}_1, \mathbf{e}_2 \rangle = 0 = \delta_{12}
$$

### Example 2: Summation Simplification
Given a vector \( \mathbf{x} = (x_1, x_2, x_3) \):
$$
\sum_{j=1}^3 x_j \delta_{2j} = x_2
$$

---

## 4. Applications
1. **Linear Algebra**:  
   - Defines orthonormal bases.  
   - Simplifies tensor notation.

2. **Signal Processing**:  
   - Used in discrete-time impulse responses.

3. **Quantum Mechanics**:  
   - Represents orthogonality of eigenstates.

4. **Computer Science**:  
   - Appears in algorithm design (e.g., dynamic programming).

---

## 5. Kronecker Delta vs. [[Dirac Delta Function]]

| Feature          | Kronecker Delta \( \delta_{ij} \)       | Dirac Delta \( \delta(x) \)         |
|------------------|----------------------------------------|-------------------------------------|
| **Domain**       | Discrete indices \( (i,j) \)           | Continuous variable \( x \in \mathbb{R} \) |
| **Value**        | 1 or 0                                 | \( \infty \) at \( x=0 \), else 0  |
| **Normalization**| \( \sum_j \delta_{ij} = 1 \)           | \( \int_{-\infty}^\infty \delta(x)dx = 1 \) |
