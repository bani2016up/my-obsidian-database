
Method: 1. Take partial derivative for each var. and build n x n matrix from it (Jacobian Matrix) 2. Tale a second partial derivative from each element as follows: fxx, fxy, …


#  Step 1: Define the Bilinear Form  
The quadratic form $f$ corresponds to a symmetric bilinear form $\langle \mathbf{u}, \mathbf{v} \rangle$, defined as:  

$$
\langle \mathbf{u}, \mathbf{v} \rangle = u_1v_1 + 2u_2v_2 + 3u_3v_3 + \frac{1}{2}u_1v_2 + \frac{1}{2}u_2v_1 + u_1v_3 + u_3v_1 + \frac{1}{2}u_2v_3 + \frac{1}{2}u_3v_2.
$$

---

# Step 2: Choose the Standard Basis  
Let $\mathcal{B} = \{\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3\}$ be the standard basis of $\mathbb{R}^3$:  

$$
\mathbf{e}_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad 
\mathbf{e}_2 = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}, \quad 
\mathbf{e}_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}.
$$

---

# Step 3: Compute the Gram Matrix  
The Gram matrix $G$ has entries $G_{ij} = \langle \mathbf{e}_i, \mathbf{e}_j \rangle$:  

1. **Diagonal Entries:**  
   $$
   \begin{aligned}  
   G_{11} &= \langle \mathbf{e}_1, \mathbf{e}_1 \rangle = 1, \\  
   G_{22} &= \langle \mathbf{e}_2, \mathbf{e}_2 \rangle = 2, \\  
   G_{33} &= \langle \mathbf{e}_3, \mathbf{e}_3 \rangle = 3.  
   \end{aligned}
   $$

2. **Off-Diagonal Entries:**  
   $$
   \begin{aligned}  
   G_{12} &= \langle \mathbf{e}_1, \mathbf{e}_2 \rangle = \frac{1}{2}, \\  
   G_{13} &= \langle \mathbf{e}_1, \mathbf{e}_3 \rangle = 1, \\  
   G_{23} &= \langle \mathbf{e}_2, \mathbf{e}_3 \rangle = \frac{1}{2}.  
   \end{aligned}
   $$

3. **Resulting Gram Matrix:**  
   $$
   G = \begin{pmatrix}
   1 & \frac{1}{2} & 1 \\
   \frac{1}{2} & 2 & \frac{1}{2} \\
   1 & \frac{1}{2} & 3
   \end{pmatrix}
   $$