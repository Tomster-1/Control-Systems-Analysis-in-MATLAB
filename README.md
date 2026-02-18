# Control-Systems-Analysis-in-MATLAB

MATLAB implementation covering closed-loop control analysis, time-domain responses, pole–zero maps, and stability assessment for multiple feedback systems.

---

## Overview

This repository contains the MATLAB code implementing **Exercises 1–3** exactly as specified in the practical sheet.

The script performs system modelling, stability analysis, and time-domain simulation using standard Control System Toolbox functions:
`tf`, `feedback`, `pole`, `pzmap`, `step`, `impulse`, `lsim`, `isstable`.

The code is written as a **single, linear MATLAB script**, reflecting the structure of an academic practical submission rather than a modular software package.

---

## Contents Overview

### Exercise 1 — Closed-Loop Control with Gain Variation

Exercise 1 constructs a nested feedback control system and forms the closed-loop transfer function for an arbitrary gain:

```math
K
```

For the specific gain cases:
- ```math
  K = 10
  ```
  The script computes poles/zeros and generates impulse, step, and ramp responses.
- ```math
  K \in \{50,\ 100,\ 150\}
  ```
  Step responses are compared on a single figure to show gain effects on rise time, overshoot, and damping.
- ```math
  K = -100
  ```
  Instability is demonstrated via a divergent step response.

A sinusoidal input is also applied using `lsim` to demonstrate response to a periodic signal.

Pole–zero maps are plotted with explicit legends, and the time-domain responses are used to interpret damping behaviour, overshoot, and closed-loop stability.

---

### Exercise 2 — Stability of Interconnected Systems

Exercise 2 forms the closed-loop transfer function between the reference input and the output:

```math
\frac{y}{r}
```

using a given pair of transfer functions:

```math
G_1(s),\; G_2(s)
```

The script computes the resulting poles and zeros, checks stability using `isstable`, and visualises the pole–zero map to confirm that all poles lie in the left-half plane (or to highlight any unstable behaviour).

---

### Exercise 3 — Transfer Function Manipulation and Analysis

Exercise 3 starts from a given plant and feedback transfer function:

```math
G(s),\; H(s)
```

The poles of:

```math
G(s)
```

are extracted and reported.

The characteristic equation of the feedback transfer function is obtained from its denominator. In general, if:

```math
H(s)=\frac{N_H(s)}{D_H(s)}
```

then the characteristic equation is:

```math
D_H(s)=0
```

The composite system is then constructed:

```math
J(s)=\frac{G(s)}{H(s)}
```

and analysed.

The script generates a pole–zero map of:

```math
J(s)
```

computes the unit-step response, and comments on pole locations, dominant dynamics, and decay behaviour. This includes identifying whether poles are purely real, repeated, or complex, and what that implies for the presence or absence of oscillations.

---

## Output and Reporting

All required figures (pole–zero maps and time responses) are generated automatically.

At the end of the script, a clean **PRINT BLOCK** is printed to the MATLAB command window. This block summarises the key analytical results for each exercise, including transfer functions, poles and zeros, stability conclusions, and the required written observations.
