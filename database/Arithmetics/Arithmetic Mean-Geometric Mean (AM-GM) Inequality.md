
## 1. Basic Statement
For non-negative real numbers \( x_1, x_2, ..., x_n \):
$$
\frac{x_1 + x_2 + \cdots + x_n}{n} \geq \sqrt[n]{x_1 x_2 \cdots x_n}
$$
Equality holds if and only if all \( x_i \) are equal.

## 2. Key Properties
- **Order Relationship**: Arithmetic mean ≥ Geometric mean
- **Homogeneity**: Scaling all variables preserves the inequality
- **Additivity**: Weighted versions exist for non-uniform distributions

## 3. Special Cases
### Two Variables:
$$
\frac{a + b}{2} \geq \sqrt{ab} \quad (a,b \geq 0)
$$

### Three Variables:
$$
\frac{a + b + c}{3} \geq \sqrt[3]{abc} \quad (a,b,c \geq 0)
$$

## 4. Proof Techniques
1. **Induction**: Classic proof for general \( n \)
2. **Cauchy's Forward-Backward Induction**: Elegant but technical
3. **Lagrange Multipliers**: For constrained optimization approach

## 5. Applications
| Field | Application |
|-------|-------------|
| Optimization | Finding minima/maxima |
| Probability | Bounding expectations |
| Geometry | Isoperimetric problems |
| Economics | Production efficiency |

## 6. Example Problems
1. **Minimization**:
   For ( x > 0 ), minimize ( x +1/x):
   $$ x + \frac{1}{x} \geq 2\sqrt{x \cdot \frac{1}{x}} = 2 $$

2. **Weighted Version**:
   For weights \( w_i \) with \( \sum w_i = 1 \):
   $$ \sum w_i x_i \geq \prod x_i^{w_i} $$

> **Historical Note**: First proven by Cauchy in 1821, with refinements by Hurwitz and others.