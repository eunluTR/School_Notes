## Frequency Components and Signal Decomposition

- Any signal can be represented as a **sum of sinusoidal components** with different frequencies, amplitudes, and phases.
- This concept is formalized through **Fourier Series** (for periodic signals) and **Fourier Transform** (for aperiodic signals).
- A complex signal is often composed of many **harmonic components**, each with its own frequency:
  $x(t) = \sum_{n=-\infty}^{\infty} C_n e^{j n \omega_0 t}$
  - Here, $C_n$ are complex Fourier coefficients.
  - $\omega_0$ is the fundamental angular frequency.
### Intuition
- Think of a complex waveform (e.g., a music note) as a blend of simpler sine and cosine waves.
- These simple waves "add up" (constructively and destructively) to form the final signal.
![[Pasted image 20250403173524.png]]

## Signal Classifications

### 1. Continuous-Time vs. Discrete-Time
- **Continuous-Time Signal**: Has a value at every real-numbered time.
- **Discrete-Time Signal**: Defined only at specific time intervals (usually equally spaced).
  - Often obtained by **sampling** a continuous-time signal.

### 2. Analog vs. Digital
- **Analog Signal**: Takes values from a continuous range.
- **Digital Signal**: Takes values from a discrete set (e.g., binary 0 or 1).

### 3. Periodic vs. Aperiodic
- **Periodic Signal**: Repeats after a fixed time period $T$.
  - Mathematically: $f(t) = f(t + T)$ for all $t$
- **Aperiodic Signal**: Does not repeat in a regular interval.

### 4. Causal, Anticausal, Noncausal
- **Causal**: $f(t) = 0$ for $t < 0$
- **Anticausal**: $f(t) = 0$ for $t > 0$
- **Noncausal**: Non-zero for both $t < 0$ and $t > 0$
![[Pasted image 20250403173725.png]]
### 5. Even vs. Odd
- **Even Signal**: $f(t) = f(-t)$ (symmetric about vertical axis)
- **Odd Signal**: $f(t) = -f(-t)$
- **Decomposition**:
  - Any signal can be written as:  
    $f(t) = \frac{f(t) + f(-t)}{2} + \frac{f(t) - f(-t)}{2}$
  - First term is even, second is odd.
![[Pasted image 20250403173639.png]]

### 6. Deterministic vs. Random
- **Deterministic Signal**: Defined precisely by an equation or rule.
- **Random Signal**: Contains some level of uncertainty or variability.
![[Pasted image 20250403173659.png]]