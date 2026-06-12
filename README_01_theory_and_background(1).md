# README 01: Theory and Background

This document explains the engineering theory behind the **Frequency Response Structural Dynamics Platform**.

The project focuses on structural dynamics, modal analysis, frequency response analysis, damping behavior, vibro-acoustic response, and SEA concepts.

---

## 1. Structural Dynamics Equation

The general equation of motion for a linear structural system is:

```text
[M]{x''} + [C]{x'} + [K]{x} = {F(t)}
```

Where:

| Symbol | Meaning |
|---|---|
| `[M]` | Mass matrix |
| `[C]` | Damping matrix |
| `[K]` | Stiffness matrix |
| `{x}` | Displacement vector |
| `{x'}` | Velocity vector |
| `{x''}` | Acceleration vector |
| `{F(t)}` | Applied force vector |

This equation is the foundation for modal analysis and frequency response simulation.

---

## 2. Modal Analysis

Modal analysis identifies the natural frequencies and mode shapes of a structure.

For free undamped vibration:

```text
[M]{x''} + [K]{x} = 0
```

Assuming harmonic motion:

```text
{x} = {phi} sin(omega t)
```

The system becomes an eigenvalue problem:

```text
[K]{phi} = omega^2 [M]{phi}
```

Where:

- `omega` is the natural circular frequency
- `{phi}` is the mode shape
- `omega^2` is the eigenvalue

Natural frequency in Hz:

```text
f_n = omega_n / (2*pi)
```

---

## 3. Frequency Response Analysis

For harmonic excitation:

```text
{F(t)} = {F}e^(j omega t)
```

The frequency-domain equation becomes:

```text
([K] - omega^2[M] + j omega[C]){X} = {F}
```

The matrix:

```text
[D(omega)] = [K] - omega^2[M] + j omega[C]
```

is called the **dynamic stiffness matrix**.

The response is:

```text
{X} = [D(omega)]^-1 {F}
```

This response is calculated over a frequency sweep to create the Frequency Response Function.

---

## 4. Frequency Response Function

The Frequency Response Function, or FRF, describes how much a structure responds at each excitation frequency.

For a single degree-of-freedom system:

```text
H(omega) = 1 / (k - m omega^2 + j c omega)
```

At resonance, the excitation frequency is close to the natural frequency and the response amplitude becomes large.

---

## 5. Damping Concepts

Damping controls how sharp or broad the resonance peaks are.

This project considers:

- Viscous damping
- Modal damping
- Proportional damping
- Loss-factor damping

Increasing damping generally:

- Reduces resonance peak amplitude
- Broadens the resonance curve
- Improves numerical stability
- Represents real energy dissipation

---

## 6. FEA Concepts Used

The project uses finite element analysis concepts without depending entirely on a commercial FEA tool.

Important FEA concepts include:

- Mass matrix assembly
- Stiffness matrix assembly
- Damping matrix definition
- Boundary condition application
- Degree-of-freedom handling
- Eigenvalue solution
- Harmonic response solution

In a full FEA model, the mass and stiffness matrices come from discretizing the structure into finite elements.

---

## 7. Vibro-Acoustic Interpretation

Structural vibration can radiate sound when vibrating surfaces interact with surrounding air.

The project connects structural frequency response to vibro-acoustic behavior by studying:

- Surface velocity response
- Vibration amplitude vs frequency
- Resonance-driven acoustic radiation
- Transmission loss trends
- Coupled structure-acoustic interpretation

---

## 8. SEA Concepts

Statistical Energy Analysis is useful for high-frequency vibro-acoustic systems where deterministic modal simulation becomes expensive.

SEA concepts used in this project include:

- Modal density
- Subsystem energy
- Coupling loss factor
- Damping loss factor
- Energy flow between structural and acoustic systems
- Transmission loss interpretation

SEA was applied conceptually to connect deterministic modal analysis with high-frequency energy-based modeling.
