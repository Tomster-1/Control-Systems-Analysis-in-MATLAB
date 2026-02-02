# Control-Systems-Analysis-in-MATLAB

MATLAB implementation covering closed-loop control analysis, time-domain responses, pole–zero maps, and stability assessment for multiple feedback systems.

---

## Overview

This repository contains the MATLAB code implementing Exercises 1–3 exactly as specified in the practical sheet.

The script performs system modelling, stability analysis, and time-domain simulation using standard Control System Toolbox functions (`tf`, `feedback`, `pole`, `pzmap`, `step`, `impulse`, `lsim`).

The code is written as a single, linear MATLAB script, reflecting the structure of an academic practical submission rather than a modular software package.

---

## Contents Overview

### Exercise 1 – Closed-Loop Control with Gain Variation

Exercise 1 constructs a nested feedback control system and forms the closed-loop transfer function for an arbitrary gain \(K\).

For \(K = 10\), the script computes the poles and zeros and generates impulse, step, and ramp responses.  
For \(K = 50, 100, 150\), it compares the step responses on a single figure to illustrate how increasing gain affects rise time, overshoot, and damping.  
For \(K = -100\), it shows the resulting instability and divergent step response.  
A sinusoidal input is also applied using `lsim` to demonstrate the response to a periodic signal.

Pole–zero maps are plotted with explicit legends, and the time-domain responses are used to interpret damping behaviour, overshoot, and closed-loop stability.

---

### Exercise 2 – Stability of Interconnected Systems

Exercise 2 forms the closed-loop transfer function between the reference input \(r\) and the output \(y\), denoted \(y/r\), using a given pair of transfer functions \(G_1(s)\) and \(G_2(s)\).

The script computes the resulting poles and zeros, checks stability using `isstable`, and visualises the pole–zero map to confirm that all poles lie in the left-half plane (or to highlight any unstable behaviour).

---

### Exercise 3 – Transfer Function Manipulation and Analysis

Exercise 3 starts from a given plant \(G(s)\) and feedback transfer function \(H(s)\).

The poles of \(G(s)\) are extracted and reported.  
The characteristic equation of \(H(s)\) is obtained from its denominator and written explicitly.  
The composite system \(J(s) = G(s) / H(s)\) is then constructed, simplified, and analysed.

The script generates a pole–zero map of \(J(s)\), computes the unit-step response, and comments on the pole locations, dominant dynamics, and decay behaviour. This includes identifying whether poles are purely real, repeated, or complex, and what that implies for the presence or absence of oscillations.

---

## Output and Reporting

All required figures (pole–zero maps and time responses) are generated automatically.

At the end of the script, a clean “PRINT BLOCK” is printed to the MATLAB command window. This block summarises the key analytical results for each exercise, including transfer functions, poles and zeros, stability conclusions, and the required written observations.
