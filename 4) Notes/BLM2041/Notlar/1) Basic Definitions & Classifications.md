
Time: 02-04-2025 16.04

Tags: [[School]] | [[BLM2041]] 

## Definition of a System
- A **system** can be seen as an integrated set of components that accomplish a specific objective.
- **Inputs**, **processes**, and **outputs** are crucial; **feedback** (when present) further defines the system’s behavior.
![[Pasted image 20250402164701.png]]
## Types of Systems
- **Digital System**: Operates with discrete (often binary) inputs, system states, and outputs.
- **Analog System**: Deals with continuous signals.

## Signals
- A **signal** is an information-carrying variable represented by a physical quantity.
- In **digital signals**, values are discrete (e.g., 0/1).
- In **analog signals**, the variable is continuous and can take infinitely many values.

## Analog-to-Digital Conversion (ADC)
1. **Filtering** (limit signal bandwidth to avoid distortions).
2. **Sampling** (taking discrete measurements in time).
3. **Quantization** (mapping infinite amplitude values to a finite set of levels).
4. **Encoding** (assigning binary codes to each quantization level) 
![[Pasted image 20250402165614.png]]
### Sampling
- Done at intervals of $( T_s )$ seconds, so sampling rate/frequency is $f_{s} = 1/T_s$
- According to the **Nyquist Theorem**: $f_s \ge 2 f_{max}$
![[Pasted image 20250402170719.png]]
- Common sampling approaches: 
	- **Ideal:** Instantaneous sampling using impulses at specific time instants; not physically realizable.
    - **Natural:** Takes a short-duration sample of the actual signal amplitude; retains the signal’s shape during the pulse.
    - **Flattop:** Samples are held constant at a fixed amplitude level for the duration of the sampling pulse; used in most practical systems like ADCs.
    ![[Pasted image 20250402170523.png]]

### Quantization
- Divides the signal amplitude range into \( L \) discrete levels with width \( Delta \)
- Each sampled value is approximated to the midpoint of a level.
- **Quantization error** is the difference between the actual amplitude and the midpoint level.

### Encoding
- Each quantization level is mapped to a binary code.
- The required number of bits ( n ) for ( L ) levels: $( n = \log_2 L)$.

## Pulse Amplitude Modulation (PAM)
- **PAM** is a modulation technique where the **amplitude** of regularly spaced **pulses** is varied according to the **instantaneous amplitude** of the analog signal.
- It is used in the **sampling** process before analog-to-digital conversion.
- The outcome is a signal with **analog amplitude values** but occurring at **discrete time intervals**.
- Types of PAM based on sampling method:
  - **Natural PAM**: Pulses follow the shape of the signal during the pulse width.
  - **Flat-top PAM**: Pulses have constant amplitude (held value); more suitable for ADC.
- **Drawback**: Susceptible to noise affecting amplitude levels.
![[Pasted image 20250402173431.png]]

## Key Takeaways
- **Systems** transform inputs to outputs, potentially using feedback.
- **Signals** can be analog (continuous) or digital (discrete).
- **Sampling** and **quantization** inevitably introduce information loss and error.
- **Encoding** is essential to represent quantized levels in binary form for digital processing.


# References
[[1) SaS-01v2.pdf]]