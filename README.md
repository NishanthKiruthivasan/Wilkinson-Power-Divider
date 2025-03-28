# Wilkinson-Power-Divider

## Overview
This project involves the design and simulation of a 2 GHz, 50Ω Wilkinson power divider using Keysight ADS. The objective is to develop a two-metal layer PCB layout with copper as the conductive material and FR4 as the dielectric substrate (εr = 4.6). The design utilizes a 0402 footprint for isolating resistors and follows a methodical approach that includes impedance line calculations, schematic simulations, and electromagnetic (EM) simulations.

## Design Methodology
The design process is divided into four main phases:

### 1. Linecalc Analysis
- Defined substrate parameters:
  - Dielectric Constant (εr) = 4.6
  - Substrate Height (H) = 10 mils
  - Conductor Thickness (T) = 17 µm
  - Dielectric Loss Tangent (TanD) = 0.02
- Used Linecalc to determine exact transmission line dimensions:
  - 50Ω Line Width: 459.13 µm
  - 70.7Ω Line Width: 232.11 µm (length = 21.09 mm for λ/4)

### 2. Schematic Simulation
- Designed the schematic using T-line components and simulated for S-parameters.
- Key results:
  - S11, S22, and S33 below -15 dB indicating low reflection.
  - S21 and S31 close to 0 dB indicating minimal loss.

### 3. Piecewise EM Simulation
- Simulated individual segments of the Wilkinson power divider.
- Verified dimensions using Controlled Impedance Line Designer (CILD).
- Ensured accurate impedance matching with minimal losses.

### 4. Total EM Simulation
- Performed complete EM simulation of the final layout.
- Configured 100Ω isolation resistor ports and analyzed performance over a 1-3 GHz frequency range.

## Result Analysis
- **Return Loss (S11):** Below -20 dB at 2 GHz, indicating excellent impedance matching.
- **Insertion Loss (S21, S31):** Equal power division with insertion loss near -3 dB.
- **Isolation (S23):** High isolation between output ports with values below -20 dB.
- The results have been provided in the attached report

## Tools and Technologies Used
- **Keysight ADS** for schematic and EM simulation.
