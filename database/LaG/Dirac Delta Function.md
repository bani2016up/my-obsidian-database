
## 1. Definition
The **Dirac delta function** $\delta(x)$ is a generalized function (or distribution) with the following defining properties:

1. **Point Concentration**:
   $$
   \delta(x) = \begin{cases}
   +\infty & \text{if } x = 0 \\
   0 & \text{if } x \neq 0
   \end{cases}
   $$

2. **Normalization**:
   $$
   \int_{-\infty}^\infty \delta(x) \, dx = 1
   $$

3. **Sifting Property** (most important):
   $$
   \int_{-\infty}^\infty f(x)\delta(x-a) \, dx = f(a)
   $$

## 2. Key Properties

### A. Scaling
$$
\delta(kx) = \frac{1}{|k|}\delta(x) \quad (k \neq 0)
$$

### B. Composition with Functions
For $g(x)$ with simple zeros at $x_i$:
$$
\delta(g(x)) = \sum_i \frac{\delta(x-x_i)}{|g'(x_i)|}
$$

### C. Derivative
The derivative $\delta'(x)$ satisfies:
$$
\int_{-\infty}^\infty f(x)\delta'(x) \, dx = -f'(0)
$$

## 3. Common Representations

### A. Limit of Gaussian Functions
$$
\delta(x) = \lim_{\sigma\to 0} \frac{1}{\sigma\sqrt{2\pi}} e^{-x^2/(2\sigma^2)}
$$

### B. Limit of Rectangular Pulses
$$
\delta(x) = \lim_{\epsilon\to 0} \frac{1}{\epsilon}\text{rect}\left(\frac{x}{\epsilon}\right)
$$
where $\text{rect}(x) = 1$ for $|x| < 1/2$, $0$ otherwise.

## 4. Physical Interpretation

- Models **point masses** in mechanics
- Represents **impulse forces** (infinite force over infinitesimal time)
- Describes **point charges** in electromagnetism

## 5. Relationship to Kronecker Delta

| Property         | Dirac Delta $\delta(x)$       | Kronecker Delta $\delta_{ij}$ |
|------------------|------------------------------|------------------------------|
| Domain           | Continuous ($x\in\mathbb{R}$) | Discrete ($i,j\in\mathbb{Z}$) |
| Integration      | $\int \delta(x)dx = 1$        | $\sum_j \delta_{ij} = 1$      |
| Sampling        | $\int f(x)\delta(x)dx=f(0)$  | $\sum_j a_j \delta_{ij}=a_i$ |

## 6. Applications

### A. Signal Processing
- Represents ideal impulse response
- Used in convolution: $f(t)*\delta(t-t_0) = f(t-t_0)$

### B. Quantum Mechanics
- Position eigenstates: $\langle x|x'\rangle = \delta(x-x')$
- Momentum eigenstates: $\langle p|p'\rangle = \delta(p-p')$

### C. Electromagnetism
- Point charge density: $\rho(\mathbf{r}) = q\delta(\mathbf{r}-\mathbf{r}_0)$

## 7. Important Notes

1. **Not a True Function**:
   The Dirac delta is a *distribution* that only makes sense under an integral.

2. **Engineering Approximation**:
   In practice, very narrow, tall pulses approximate $\delta(x)$.

3. **Multidimensional Form**:
   In 3D space: $\delta^3(\mathbf{r}) = \delta(x)\delta(y)\delta(z)$