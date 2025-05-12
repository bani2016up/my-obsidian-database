# Proof that $||\mathbf{x}|| = \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}$ Satisfies Norm Properties

## 1. Definition
Given an inner product space $(V, \langle \cdot, \cdot \rangle)$, we define:
$$
||\mathbf{x}|| := \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}
$$

## 2. Verification of Norm Axioms

### Axiom 1: Positive Definiteness [[Positive and Negative Definiteness]]
For any $\mathbf{x} \in V$:
1. $||\mathbf{x}|| = \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle} \geq 0$ (since $\langle \mathbf{x}, \mathbf{x} \rangle \geq 0$ by inner product properties)
2. $||\mathbf{x}|| = 0 \iff \langle \mathbf{x}, \mathbf{x} \rangle = 0 \iff \mathbf{x} = \mathbf{0}$

### Axiom 2: Absolute Homogeneity
For any scalar $\alpha$ and vector $\mathbf{x}$:
$$
||\alpha\mathbf{x}|| = \sqrt{\langle \alpha\mathbf{x}, \alpha\mathbf{x} \rangle} = \sqrt{|\alpha|^2 \langle \mathbf{x}, \mathbf{x} \rangle} = |\alpha| \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle} = |\alpha| \cdot ||\mathbf{x}||
$$

### Axiom 3: Triangle Inequality
Using [[Cauchy-Schwarz inequality]]):
$$
\begin{aligned}
||\mathbf{x} + \mathbf{y}||^2 &= \langle \mathbf{x}+\mathbf{y}, \mathbf{x}+\mathbf{y} \rangle \\
&= ||\mathbf{x}||^2 + 2\langle \mathbf{x}, \mathbf{y} \rangle + ||\mathbf{y}||^2 \\
&\leq ||\mathbf{x}||^2 + 2||\mathbf{x}|| \cdot ||\mathbf{y}|| + ||\mathbf{y}||^2 \quad \text{(by Cauchy-Schwarz)} \\
&= (||\mathbf{x}|| + ||\mathbf{y}||)^2
\end{aligned}
$$
Taking square roots preserves the inequality.

## 3. Conclusion
The function $||\mathbf{x}|| = \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}$ satisfies all norm axioms:
1. Positive definiteness
2. Absolute homogeneity  
3. Triangle inequality

Thus it is a valid norm on the inner product space.


# Related
1. [[Prove Norm Axioms]]
