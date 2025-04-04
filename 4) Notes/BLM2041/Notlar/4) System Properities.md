
Time: 04-04-2025 11.04

Tags: [[School]] | [[BLM2041]]

## Properties of Systems

### 1. Discrete-Time Systems
- A discrete-time system transforms input sequences $x[n]$ into output sequences $y[n]$.
- Often represented using **difference equations**.
**SISO:** Single input, single output systems.
### 2. Linearity
- A system is **linear** if it satisfies two conditions:
  - **Additivity**:  
    $x_1(t) + x_2(t) \rightarrow y_1(t) + y_2(t)$
  - **Homogeneity (Scaling)**:  
    $a \cdot x(t) \rightarrow a \cdot y(t)$ for any scalar $a$
- Combined test: If $x(t) = a x_1(t) + b x_2(t)$, then output must be $y(t) = a y_1(t) + b y_2(t)$.

### 3. Memory vs. Memoryless Systems
- **Memory System**: Output depends on past or future input values (e.g., systems with energy storage like capacitors).
- **Memoryless System**: Output at time $t$ depends only on the input at the same instant $t$.

### 4. Causality
- A system is **causal** if its output at time $t$ depends only on current and past inputs, never on future inputs.
  - Mathematically: output $y(t)$ depends on inputs $x(\tau)$ only for $\tau \leq t$.

### 5. Time-Invariance
- A system is **time-invariant** if a shift in the input causes an identical shift in the output.
- Mathematically:  
  If $x(t) \rightarrow y(t)$, then for any time shift $t_0$:  
  $x(t - t_0) \rightarrow y(t - t_0)$.

### 6. Invertibility
- A system is **invertible** if the input can be uniquely determined from the output.
- If system $S$ is defined as $y(t) = S\{x(t)\}$, an inverse system exists such that $x(t) = S^{-1}\{y(t)\}$.
- Not all systems are invertible (some may lose information during transformation).

# References
