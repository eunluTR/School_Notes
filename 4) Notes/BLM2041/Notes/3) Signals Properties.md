
Time: 03-04-2025 21.04

Tags: [[BLM2041]]

## Signal Operations and Special Signals

### 1. Basic Signal Operations

- **Amplitude Scaling:**
  - Multiplies the signal by a constant factor $A$.
  - $y(t) = A \cdot x(t)$.
  - Changes the signal’s amplitude without affecting its shape or duration.

- **Time Scaling:**
  - Compresses or expands the signal in time domain.
  - $y(t) = x(a t)$:
    - $a > 1$: compression (faster).
    - $0 < a < 1$: expansion (slower).

- **Time Reversal:**
  - Reflects the signal around the vertical axis.
  - $y(t) = x(-t)$.

- **Time Shift:**
  - Moves signal forward or backward in time.
  - $y(t) = x(t - t_0)$ shifts right by $t_0$.
  - $y(t) = x(t + t_0)$ shifts left by $t_0$.

---

### 2. Periodic Signals
- Signals repeating after a fixed period $T$:
  - $x(t) = x(t + T)$ for all $t$.
- Example: Sinusoidal signals, square waves.

---

### 3. Complex Signals & Complex Plane
- Signals with real and imaginary parts: $x(t) = a(t) + jb(t)$.
- Represented in a complex plane (real-imaginary axis).
- Widely used in modulation and frequency analysis.

---

### 4. Signal Energy and Power
- **Signal Energy** (finite energy signals):
  - Defined for signals where the integral is finite.
  - $E = \int_{-\infty}^{\infty} |x(t)|^2 dt$.
  - Typically non-periodic signals.

- **Signal Power** (finite power signals):
  - Average energy per unit time (usually periodic signals).
  - $P = \lim_{T→∞} \frac{1}{2T}\int_{-T}^{T}|x(t)|^2 dt$.
  - Often infinite energy but finite power (e.g., sinusoidal signals).

---

### 5. Sinusoidal Signals
- Fundamental periodic signals: 
  - $x(t) = A\cos(\omega t + \phi)$.
  - $A$: amplitude, $\omega$: angular frequency, $\phi$: phase shift.
- Basis for Fourier analysis (all signals can be represented as sum of sinusoids).

---

### 6. Exponential Signals
- Commonly encountered signals:
  - $x(t) = Ae^{\alpha t}$.
  - $α$: rate of growth (α > 0) or decay (α < 0).
- Exponential signals are important for solving differential equations.

---

### 7. Unit Step and Unit Functions
- **Unit Step Function** ($u(t)$):
  $$
  u(t) = \begin{cases}
  1, & t ≥ 0 \\[6pt]
  0, & t < 0
  \end{cases}
  $$
![[Pasted image 20250404112827.png]]
- **Significance**:
  - Used to represent switching on/off processes.
  - Often used in signal decomposition.

- **Other Unit functions**:
  - Unit Ramp ($r(t) = t \cdot u(t)$)
  - Rectangular pulse, triangular pulse functions.

---

### 8. Impulsive Signals
- Idealized signals with infinite amplitude at a specific instant (Dirac delta δ(t)):
  - $\delta(t) = 0$ for all $t ≠ 0$ and $\int_{-\infty}^{\infty}\delta(t)dt = 1$.
- Used extensively in system characterization (impulse response).

---

### 9. Integrals and Derivatives of Signals
- Useful in system analysis (especially linear systems).
- **Differentiation**:
  - Indicates the rate of change of a signal.
  - $y(t) = \frac{dx(t)}{dt}$.

- **Integration**:
  - Accumulates the signal’s past values.
  - $y(t) = \int_{-\infty}^{t}x(\tau)d\tau$.
- Used in system descriptions, e.g., integrators, differentiators.

# References
[[3) SaS-03.pdf]]