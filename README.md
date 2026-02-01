# Control-Systems-Analysis-in-MATLAB
MATLAB implementation covering closed-loop control analysis, time-domain responses, pole–zero maps, and stability assessment for multiple feedback systems.

This repository contains the MATLAB code implementing Exercises 1–3 exactly as specified in the practical sheet.
The script performs system modelling, stability analysis, and time-domain simulation using standard Control System Toolbox functions (tf, feedback, pole, pzmap, step, impulse, lsim).

The code is written as a single, linear MATLAB script, reflecting the structure of an academic practical submission rather than a modular software package.

Contents Overview
Exercise 1 – Closed-Loop Control with Gain Variation

Construction of a nested feedback control system

Closed-loop transfer function generation for arbitrary gain K

Analysis for:

K = 10: poles, zeros, impulse, step, and ramp responses

K = 50, 100, 150: step-response comparison

K = -100: instability demonstration

Sinusoidal input response using lsim

Pole–zero maps with explicit legends

Time-domain interpretation of damping, overshoot, and stability

Exercise 2 – Stability of Interconnected Systems

Formation of the closed-loop transfer function y / r

Pole–zero analysis of the resulting system

Stability verification using isstable

Visual confirmation via pole–zero mapping

Exercise 3 – Transfer Function Manipulation and Analysis

Pole extraction of a given plant G(s)

Derivation of the characteristic equation of H(s)

Construction of the composite system J(s) = G(s) / H(s)

Pole–zero analysis and unit-step response of J(s)

Interpretation of dominant poles and decay behaviour

Output and Reporting

All required figures generated automatically

A clean “PRINT BLOCK” at the end of the script summarising:

Transfer functions

Poles and zeros

Stability conclusions

Required observations for each exercise
