# Hardware Accelerator for Runge-Kutta Solvers (RK2, RK3, RK4) on Zynq ZC702 FPGA

This repository presents the implementation of a hardware accelerator specifically designed to solve Ordinary Differential Equations (ODEs) using **Runge-Kutta numerical methods**. The accelerator is implemented using **VHDL** and deployed on the **Zynq ZC702 FPGA** evaluation board, with a focus on performance, efficiency, and scalability.

## Overview

Runge-Kutta methods, specifically **RK2**, **RK3**, and **RK4**, are widely used for solving ODEs in a variety of scientific and engineering applications. This work explores the hardware acceleration of these methods to improve computational speed and optimize resource usage. The methods were implemented on an FPGA, and the comparative analysis of these solvers highlights key factors such as:

- **Timing Performance**: Execution time for each solver.
- **Hardware Resource Utilization**: Usage of FPGA resources (e.g., logic cells, block RAM, DSP slices).
- **Power Consumption**: Analysis of total on-chip power consumption at a clock rate of 100 MHz.

### Experimental Findings

The experimental analysis found that the **fourth-order Runge-Kutta (RK4)** solver exhibits higher power consumption compared to the **second-order (RK2)** and **third-order (RK3)** solvers:

- **Power Consumption**: RK4 increased power consumption by **51.37%** compared to RK2 and **12.445%** compared to RK3 at a clock rate of 100 MHz.

This study contributes to the enhancement of **high-performance computing** applications by optimizing ODE solvers for FPGA acceleration.

This work was presented at **IEEE ICECCE 2023**. For more details, please refer to the paper: [IEEE ICECCE 2023 Paper](https://ieeexplore.ieee.org/document/10442325).

## Key Features

- **FPGA-based Hardware Acceleration**: Designed for the **Zynq ZC702 FPGA**.
- **Runge-Kutta Methods**: Implementations of **RK2**, **RK3**, and **RK4** solvers.
- **Floating-Point Operations**: Leverages **Xilinx Vivado’s IP cores** for single-precision floating-point operations.
- **Comparative Performance Analysis**: Detailed evaluation of performance, resource utilization, and power consumption.

## Hardware Resource Specifications

| ODE Solvers | FPU_ADD | FPU_SUB | FPU_MUL | MAC Units |
|-------------|---------|---------|---------|-----------|
| **RK2**     | 6       | 1       | 4       | X         |
| **RK3**     | 5       | 2       | 5       | 4         |
| **RK4**     | 7       | 1       | 2       | 4         |

## Setup Instructions

### Prerequisites
To get started, you will need to install the following:

1. **Xilinx Vivado** (for FPGA synthesis and simulation):
   - Download the latest version of **Xilinx Vivado** here: [Xilinx Vivado Documentation](https://docs.xilinx.com/r/2022.1-English/ug973-vivado-release-notes-install-license/Download-and-Installation)
   
2. **VHDL Tutorial** (for learning VHDL programming):
   - Get started with VHDL by reading this tutorial: [VHDL Tutorial](https://www.eecs.umich.edu/courses/doing_dsp/handout/vhdl-tutorial.pdf)

### Implementing the Design

This FPGA design uses Xilinx Vivado's **single precision floating point IP** to implement the **RK2**, **RK3**, and **RK4** solvers.
