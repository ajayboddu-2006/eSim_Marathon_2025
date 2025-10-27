# A Low Power Dynamic Bitwidth-Adaptive Multiply Accumulate Unit for TinyML Accelerators using eSim

## Overview

This repository is part of the **eSim Marathon** organized by FOSSEE, IIT Bombay. It showcases the design and simulation of a low-power, dynamic bitwidth-adaptive 8-bit Multiply Accumulate (MAC) unit tailored for TinyML accelerators.

The MAC unit supports multiple mixed-precision modes including 2×2, 2×4, 2×8, 4×4, 4×8, and 8×8 with signed × unsigned operation. The architecture integrates several RTL-level optimizations to reduce power consumption and improve scalability for edge-constrained devices.

The design is modeled in Verilog HDL and verified using the open-source EDA tool **eSim** through mixed-signal simulation. Functional verification is performed using Icarus Verilog, and the design is integrated into a schematic using KiCad and simulated with NgSpice.

---

## Features

- Mixed-precision support: 2×2, 2×4, 2×8, 4×4, 4×8, 8×8
- Signed × Unsigned multiplication
- Shift-and-add based multiplier with partial product elimination
- Hybrid CLA-based accumulator with dynamic segment-wise activation
- Zero-aware gating and clock gating
- Verified using Icarus Verilog and NgSpice via eSim

---

## Architecture Summary

- **Multiplier**: Converts signed inputs to unsigned using 2's complement logic. Detects precision mode and generates partial products selectively.
- **Accumulator**: Uses 8 × 4-bit CLA blocks with enable signals based on operand width. Sign-extension ensures safe accumulation.
- **Gating Logic**: Implements zero-aware and clock gating to disable computation when inputs are zero.

---

## Simulation Flow

1. Functional verification using Icarus Verilog
2. RTL converted to NgVeri model and integrated into KiCad schematic in eSim
3. Mixed-signal simulation using NgSpice to verify waveform behavior

All simulation results and waveform outputs are documented in the attached PDF report.

## Reference

Boddu Ajay, Sumanto Kar, and Shyam Perika,  
*A Low Power Dynamic Bitwidth-Adaptive Multiply Accumulate Unit for TinyML Accelerators*,  
ICTACT Journal on Communication Technology, Vol. 16, No. 3, Sep. 2025.  
DOI: [10.21917/ijct.2025.0534](https://doi.org/10.21917/ijct.2025.0534)


## Repository Structure

