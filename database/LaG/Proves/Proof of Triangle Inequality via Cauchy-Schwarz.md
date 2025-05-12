## Theorem Statement
For any vectors $\mathbf{u}, \mathbf{v}$ in an inner product space:
$$
\|\mathbf{u} + \mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|
$$
where $\|\mathbf{x}\| := \sqrt{\langle \mathbf{x}, \mathbf{x} \rangle}$.

## Proof

### Step 1: Expand the Norm
Begin by squaring both sides:
$$
\|\mathbf{u} + \mathbf{v}\|^2 = \langle \mathbf{u}+\mathbf{v}, \mathbf{u}+\mathbf{v} \rangle
$$

### Step 2: Apply [[Inner Product]] Properties 
Using linearity of the inner product:
$$
= \langle \mathbf{u}, \mathbf{u} \rangle + 2\langle \mathbf{u}, \mathbf{v} \rangle + \langle \mathbf{v}, \mathbf{v} \rangle
$$
$$
= \|\mathbf{u}\|^2 + 2\langle \mathbf{u}, \mathbf{v} \rangle + \|\mathbf{v}\|^2
$$

### Step 3: Apply [[Cauchy-Schwarz inequality]]
By the Cauchy-Schwarz inequality:
$$
|\langle \mathbf{u}, \mathbf{v} \rangle| \leq \|\mathbf{u}\|\|\mathbf{v}\|
$$
Thus:
$$
2\langle \mathbf{u}, \mathbf{v} \rangle \leq 2|\langle \mathbf{u}, \mathbf{v} \rangle| \leq 2\|\mathbf{u}\|\|\mathbf{v}\|
$$

### Step 4: Combine Results
We now have:
$$
\|\mathbf{u} + \mathbf{v}\|^2 \leq \|\mathbf{u}\|^2 + 2\|\mathbf{u}\|\|\mathbf{v}\| + \|\mathbf{v}\|^2 = (\|\mathbf{u}\| + \|\mathbf{v}\|)^2
$$

### Step 5: Take Square Roots
Since norms are non-negative:
$$
\|\mathbf{u} + \mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|
$$

## Equality Condition
Equality holds iff $\mathbf{u}$ and $\mathbf{v}$ are linearly dependent (i.e., one is a non-negative scalar multiple of the other).

> **Visual Interpretation**: In $\mathbb{R}^2$, this states that the sum of two sides of a triangle is always greater than or equal to the third side.
