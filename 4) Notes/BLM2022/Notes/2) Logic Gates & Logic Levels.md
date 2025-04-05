
Time: 05-04-2025 17.04

Tags: [[BLM2022]]

## Logic Gates
- Implement logical functions in digital circuits.

**Basic Gates:**
- **NOT**: Inverts input  
  - `Y = ¬A`
- **AND**: Outputs 1 only if all inputs are 1  
  - `Y = A·B`
- **OR**: Outputs 1 if at least one input is 1  
  - `Y = A+B`

**Extended Gates:**
- **NAND** (NOT AND): Universal gate, all logic functions can be built using NAND.
  - `Y = ¬(A·B)`
- **NOR** (NOT OR): Universal gate.
  - `Y = ¬(A+B)`
- **XOR** (Exclusive OR): Outputs 1 if inputs differ.
- **XNOR** (Exclusive NOR): Outputs 1 if inputs are the same.

## Logic Levels
- Digital systems represent binary values using discrete voltage levels.

**Standard Voltage Levels:**
- `HIGH (logic 1)` usually close to VDD (e.g., 5V, 3.3V, 1.8V)
- `LOW (logic 0)` typically near ground (0V)
*VDD:* Voltage Drain Drain

**Voltage Thresholds:**
- **VOH (Output High Voltage):** Min output voltage to be considered logic HIGH.
- **VOL (Output Low Voltage):** Max output voltage to be considered logic LOW.
- **VIH (Input High Voltage):** Min input voltage recognized as logic HIGH.
- **VIL (Input Low Voltage):** Max input voltage recognized as logic LOW.

## Noise Margin
- Defines tolerance for voltage fluctuations (noise).
- **High noise margin (NMH)**: `VOH - VIH`
- **Low noise margin (NML)**: `VIL - VOL`

## Static Discipline
- Ensures valid logical outputs for valid logical inputs by clearly defined voltage ranges.
- Prevents ambiguity by defining a forbidden zone (between `VIH` and `VIL`).
---
![[Pasted image 20250405172918.png]]
# References
[[DDCArv_Ch1.pdf]]
