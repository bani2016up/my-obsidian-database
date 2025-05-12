## Definition
Fourier coefficients are the set of coefficients obtained when expressing a periodic function as a linear combination of sine and cosine functions (or complex exponentials), forming its Fourier series expansion. For a \(2\pi\)-periodic function \(f(x)\), the Fourier coefficients provide the weight of each harmonic frequency component.

## Explicit Construction
Given a function \(f: \mathbb{R} \to \mathbb{C}\) with period \(2\pi\), the complex Fourier coefficients \(c_n\) are defined by:

$$
c_n = \frac{1}{2\pi} \int_{-\pi}^{\pi} f(x) e^{-inx} \, dx, \quad n \in \mathbb{Z}
$$

In the real form, the Fourier coefficients \(a_n\) and \(b_n\) in the expansion

$$
f(x) \sim \frac{a_0}{2} + \sum_{n=1}^{\infty} \left( a_n \cos nx + b_n \sin nx \right)
$$

are given by

$$
a_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos nx \, dx, \quad n \geq 0
$$

$$
b_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin nx \, dx, \quad n \geq 1
$$

## Key Properties
- **Orthogonality:** The sine and cosine functions form an orthogonal system under the inner product

  $$
  \langle f, g \rangle = \int_{-\pi}^\pi f(x) \overline{g(x)} \, dx.
  $$

- **Uniqueness:** If \(f\) is piecewise continuous and integrable over \([-\pi, \pi]\), the Fourier coefficients uniquely determine \(f\) almost everywhere.

- **Parseval's Identity:**

  $$
  \frac{1}{2\pi} \int_{-\pi}^\pi |f(x)|^2 dx = \sum_{n=-\infty}^{\infty} |c_n|^2
  $$

- **Linearity:** The Fourier coefficient operator is linear: the Fourier coefficient of a sum is the sum of Fourier coefficients.

- **Decay behavior:** Smoothness in \(f\) correlates with rapid decay of its Fourier coefficients.

## Examples
- For the square wave \(f(x) = \operatorname{sgn}(\sin x)\), the coefficients \(b_n\) are

  $$
  b_n = \frac{4}{\pi n} \quad \text{for odd } n, \quad b_n = 0 \quad \text{for even } n,
  $$

  with all \(a_n = 0\).

- For \(f(x) = x\) defined on \([-\pi, \pi]\), the coefficients are

  $$
  a_0 = 0, \quad a_n = 0, \quad b_n = \frac{2(-1)^{n+1}}{n}.
  $$

## Applications
- **Signal processing:** Fourier coefficients encode frequency components critical to filtering and compression.

- **Partial differential equations:** Solutions of heat, wave, and Laplace's equations often utilize Fourier series expansions.

- **Approximation theory:** Fourier coefficients provide best approximations of functions via trigonometric polynomials in \(L^2\) spaces.

- **Quantum mechanics:** Fourier coefficients relate to wavefunction decompositions in momentum space.

- **Numerical analysis:** Fast Fourier Transform (FFT) algorithms compute discrete analogs of Fourier coefficients efficiently.

## Related Topics
- See [[LaG/Orthonormal Basis.md|Orthonormal Basis]] for the notion of orthogonality underpinning Fourier expansions.
- Relations with [[LaG/Inner Product.md|Inner Product]] spaces clarify the integral-based coefficient definitions.
- Parseval's identity connects with norms, further explained in [[LaG/Norms in Inner Product Spaces.md|Norms in Inner Product Spaces]].
- The concept of convergence and orthogonality is also related to [[LaG/Orthogonality in Math.md|Orthogonality in Math]].

---
This note integrates crucial insights on Fourier coefficients with foundational concepts from linear algebra and functional analysis to support deeper mathematical study or applications.
