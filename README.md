# Relative Humidity Monitoring System COMSOL Simulation

This repository contains the **COMSOL Multiphysics simulation** of the **Dual Loop Rejoin Sensing (LRS)** setup for relative humidity (RH) and dew point (DP) monitoring. The simulation supports the design, optimization, and calibration of the RH monitoring system.

---

## Overview

The ITk detector requires extremely low humidity levels to ensure safe operation of sensitive electronics and mitigate galvanic corrosion. The dew point inside the detector barrel must be maintained below **−60°C**, achieved by flushing the volumes with dry nitrogen.

The **Dual Loop Rejoin Sensing (LRS)** system allows accurate and auto-regulated sampling of the nitrogen flow for DP/RH measurement. The COMSOL model reproduces:

- Laminar nitrogen flow in the main and sampling branches
- Convection–diffusion transport of water vapor
- Steady-state sensor response as a function of flow fraction
- Calibration of the RH measurement accounting for flow splitting effects

The model is based on the **convection–diffusion partial differential equation** and empirical calibration derived from laboratory experiments.

---

## Repository Contents

- `Double_LRS.mph` – COMSOL Multiphysics model file
- `README.md` – Scientific description and usage instructions
  
---

## Model Description

1. **Geometry**: Includes the main flushing line and sampling branches forming the dual LRS loop. Typical branch length is ~40 cm.
2. **Physics**:
   - Turbulent SST model Flow
   - Water vapor insertion through pipe walls
   - Stationary convection–diffusion transport
   - Transport of Diluted Species

---

## Usage Instructions

1. Open `Double_LRS.mph` in **COMSOL Multiphysics**.
2. Inspect the **Model Builder** for geometry, materials, and physics definitions.
3. Run the **Study** to obtain steady-state or transient solutions.
4. Extract results for:
   - Flow rates in the main and sampling branches
   - Dew point and RH profiles along the pipes
