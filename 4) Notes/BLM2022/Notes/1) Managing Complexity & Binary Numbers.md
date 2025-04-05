
Time: 05-04-2025 17.04

Tags: [[BLM2022]]

## Managing Complexity
- **Key Question:** How to design complex systems?
- **Core Concepts:**
  - **Abstraction:** Hiding unnecessary details.
  - **Discipline:** Restricting design choices intentionally to simplify design (e.g., digital vs. analog).
  - **Hierarchy:** Systems divided into modules and submodules.
  - **Modularity:** Well-defined functions and clear interfaces.
  - **Regularity:** Uniformity for easy reuse.

## Number Systems
### Binary Numbers
- Binary digits (**Bits**): 0 or 1
- **Byte:** 8 bits, **Nibble:** 4 bits
- **Range & Capacity:**
  - N-bit binary can represent `2^N` values, ranging `[0, 2^N-1]`.

### Hexadecimal Numbers
- **Base-16** numbering system (digits: 0–9, A–F).
- Easy shorthand for binary (1 hex digit = 4 binary bits).
- **Conversions:**
  - **Hex → Binary:** Convert each hex digit to a 4-bit binary sequence.
  - **Hex → Decimal:** Multiply each digit by its hex weight (`16^n`) and sum.

### Addition
- Binary addition similar to decimal addition but only with digits 0 and 1.
- Overflow occurs when sum exceeds the number of bits.

### Signed Numbers
- **Sign/Magnitude:**
  - Most significant bit (MSB) represents sign (0=positive, 1=negative).
  - Two zeros issue (`+0` and `-0`); arithmetic problems.
- **Two’s Complement:**
  - Solves sign/magnitude issues (unique zero, arithmetic works easily).
  - Sign reversal: invert bits, then add 1.
  - Range for N-bits: `[−2^(N−1), 2^(N−1)−1]`.
### Extension
- **Sign-extension (Two’s Complement):** MSB copied to new bits.
- **Zero-extension (Unsigned):** Add zeros to higher-order bits.

# References
[[DDCArv_Ch1.pdf]]
