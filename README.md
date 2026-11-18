# Numerical-Modelling-of-Bolt-Loosening-
# Why Does a Bolt Loosen Under Vibration?

### Junker Test, Bolt Mechanics, Preload, and Axial vs. Transverse Vibrational Loading

## Overview

This project investigates the mechanical mechanisms responsible for **bolt loosening under vibrational loading**, with particular attention to the influence of preload, frictional contact, material properties, and excitation direction.

The work combines a theoretical investigation of vibration-induced self-loosening with nonlinear Finite Element (FE) simulations aimed at reproducing the main features of a Junker-type vibration test.

The project was developed as part of the **Laboratory of Aerospace Structures** final project.

## Objectives

The main objectives of this study are:

- Understand the mechanical fundamentals of preloaded bolted joints.
- Investigate the physical mechanisms responsible for vibration-induced loosening.
- Analyse the Junker test and its relevance in evaluating fastener locking performance.
- Develop and compare different 3D finite element models of bolted connections.
- Evaluate the influence of preload magnitude and clamped-part material properties.
- Compare the effects of axial and transverse vibrational excitation.
- Identify possible engineering strategies to mitigate bolt loosening.

## Theoretical Background

The theoretical part focuses on the relationship between preload, friction, and relative motion at the contact interfaces.

Particular attention is given to:

- Bolt and clamped-member stiffness.
- Torque–tension relationship and preload variability.
- Frictional resistance and contact slip.
- Rotational and non-rotational loosening mechanisms.
- Transverse versus axial vibrational excitation.
- Junker test principles and standardization (DIN 65151 and ISO 16130).

## Finite Element Analysis

Nonlinear implicit finite element simulations were performed using **MSC Patran / MSC Nastran (SOL 400)**.

Three different geometric configurations were investigated, progressively increasing the level of detail used to represent the bolted connection.

The final analyses focused on a multi-body configuration in which the bolt, nut, and clamped plates were modelled as separate components.

### Simulation setup

The main characteristics of the numerical model include:

| Parameter | Description |
|---|---|
| Solver | MSC Nastran – SOL 400 |
| Analysis type | Nonlinear implicit FE analysis |
| Bolt material | Steel |
| Plate materials | Aluminium / Steel |
| Bolt nominal diameter | 10 mm (M10) |
| Bolt under-head length | 50 mm |
| Friction coefficient (plates) | 0.3 |
| Friction coefficient (nut–bolt) | 0.1 |
| Excitation frequency | 12.5 Hz |
| Applied loading | Sinusoidal |

### Investigated configurations

The following parameters were varied throughout the simulations:

- **Preload magnitude:** 450 N, 900 N and 1500 N, depending on the simulation case.
- **Material properties:** Aluminium and steel clamped plates.
- **Excitation direction:** Transverse and axial loading.
- **Vibrational amplitude:** Different force amplitudes to investigate the onset and evolution of loosening.

The applied excitation was defined through a sinusoidal time-dependent load:

\[
F(t)=F_0\sin(2\pi f t)
\]

where \(F_0\) is the force amplitude and \(f\) is the excitation frequency.

## Main Results

The numerical analyses highlighted several important aspects of bolt loosening under vibration:

**1. Influence of modelling assumptions**

The simplified model, in which the bolt and nut were represented as a single solid body, showed a significantly more stable response. Modelling the components separately allowed additional contact interactions and provided a more realistic representation of the joint behaviour.

**2. Influence of preload**

Increasing the initial preload reduced the loss of effective clamp force under transverse vibrational loading. However, preload must be optimized within the mechanical strength limits of the fastener and the joint.

**3. Influence of material properties**

Steel clamped plates exhibited a more stable response than aluminium plates under the same nominal preload and excitation conditions. This behaviour was associated with their higher stiffness and reduced transverse compliance.

**4. Influence of excitation direction**

Transverse excitation produced a progressive reduction in the axial constraint reaction, consistent with a loss of effective clamp force.

Under axial zero-mean excitation, the reaction force instead exhibited periodic oscillations around an approximately constant mean value. Increasing preload reduced the amplitude of these oscillations.

## Conclusions

The project demonstrates how vibration-induced bolt loosening is governed by the interaction between preload, frictional contact, joint stiffness, and excitation direction.

The results emphasize the importance of:

- Choosing an appropriate initial preload.
- Accurately representing contact interfaces in numerical models.
- Considering the stiffness and material properties of the clamped components.
- Distinguishing between axial and transverse vibrational loading.
- Evaluating clamp-force evolution rather than relying exclusively on the applied loading conditions.

Overall, the study highlights the importance of combining theoretical mechanics and nonlinear finite element analysis to understand the behaviour and reliability of bolted joints subjected to dynamic loading.

## Tools and Software

- **MSC Patran** – Geometric modelling, preprocessing, meshing, and post-processing.
- **MSC Nastran** – Nonlinear implicit finite element analysis (SOL 400).
- **Finite Element Method (FEM)** – Structural and contact mechanics analysis.

## Project Information

**Course:** Laboratory of Aerospace Structures  
**Academic Year:** 2025–2026

**Authors:**
- Jesmin Idrizi
- Marco Mattiuzzo
- Andrea Ramogida

---

*This repository contains the final project report documenting the theoretical investigation, finite element modelling, simulation methodology, and results of the study.*

