## Problem Statement
Prove:
$$
ab + bc + ac \leq a^2 + b^2 + c^2 \quad \forall a,b,c \in \mathbb{R}
$$

## Proof

1. **Define Vectors**:
   Let $\mathbf{u} = (a,b,c)$ and $\mathbf{v} = (b,c,a)$ in $\mathbb{R}^3$ with standard dot product.

2. **Apply [[Cauchy-Schwarz inequality]]:
   $$
   |\mathbf{u} \cdot \mathbf{v}| \leq \|\mathbf{u}\|\|\mathbf{v}\|
   $$
   $$
   |ab + bc + ca| \leq \sqrt{a^2 + b^2 + c^2} \cdot \sqrt{b^2 + c^2 + a^2} = a^2 + b^2 + c^2
   $$

3. **Conclusion**:
   Since $x \leq |x|$ and $\|\mathbf{u}\| = \|\mathbf{v}\|$:
   $$
   ab + bc + ca \leq a^2 + b^2 + c^2
   $$

## Equality Condition
Holds iff $\mathbf{u} \parallel \mathbf{v}$, i.e., when $a = b = c$.