# 32-Bit CPU Design in VHDL

A 32-bit CPU designed and implemented in VHDL as part of the COE608 Computer Organization and Architectures course. The project integrates the processor's datapath, control unit, ALU, registers, reset circuitry, and instruction memory into a complete CPU system.

The processor was assembled and tested using Intel Quartus through timing simulation to verify instruction execution and data processing.

## Project Overview

The project builds a complete CPU by integrating several processor components developed in VHDL.

The CPU includes:

- 32-bit datapath
- Control unit
- Arithmetic Logic Unit (ALU)
- Program Counter (PC)
- 32-bit registers
- Instruction/system memory
- Reset circuitry
- Multiplexers
- Supporting arithmetic and logic components
- CPU simulation and testbench files

## CPU Architecture

The complete processor combines three major subsystems:

### Datapath

The datapath handles the movement and processing of data throughout the CPU. It connects components such as the ALU, registers, multiplexers, and Program Counter.

### Control Unit

The control unit generates the control signals required to coordinate CPU operations and instruction execution.

### Reset Circuit

The reset circuit initializes the processor before normal operation begins. It clears the Program Counter and controls the CPU startup sequence so that the system can stabilize before instruction execution.

## Main Components

| File | Purpose |
| --- | --- |
| `cpu1.vhd` | Top-level CPU design |
| `Data_Path.vhd` | CPU datapath |
| `Control_New.vhd` | CPU control unit |
| `alu.vhd` | Arithmetic Logic Unit |
| `register32.vhd` | 32-bit register |
| `pc.vhd` | Program Counter |
| `reset_circuit.vhd` | CPU reset circuitry |
| `data_mem.vhd` | Data memory |
| `system_memory.vhd` | System/instruction memory |
| `system_memory.mif` | Memory initialization data |
| `mux2to1.vhd` | 2-to-1 multiplexer |
| `mux4to1.vhd` | 4-to-1 multiplexer |
| `adder4.vhd` | 4-bit adder |
| `adder16.vhd` | 16-bit adder |
| `adder32.vhd` | 32-bit adder |
| `fulladd.vhd` | Full-adder component |
| `LZE.vhd` | Supporting datapath component |
| `RED.vhd` | Supporting datapath component |
| `UZE.vhd` | Supporting datapath component |
| `cpu_test_sim.vhd` | CPU simulation/test file |
| `cpu_test_sim.vwf` | CPU simulation waveform |
| `reset_circuit.vwf` | Reset circuit simulation waveform |
| `lab6.qpf` | Quartus project file |
| `lab6.qsf` | Quartus project settings |

## Reset Operation

When the reset signal is asserted, the CPU is placed into its initial state and the Program Counter is cleared.

After the reset signal is released, the reset circuitry delays normal CPU operation for several clock cycles, allowing the system signals to stabilize before instruction execution begins.

## Simulation and Testing

The processor was tested using timing simulation.

Testing was used to verify that the complete CPU could:

- Load instructions and data from memory
- Execute processor operations
- Perform arithmetic operations such as addition
- Execute load-upper-immediate operations
- Reset and initialize correctly
- Coordinate the datapath and control unit during instruction execution

Waveform files are included for testing the complete CPU and the reset circuitry.

## Tools and Technologies

- VHDL
- Intel Quartus
- FPGA/RTL design
- Digital logic design
- CPU architecture
- Timing simulation

## Course

**COE608 – Computer Organization and Architectures**

**Project:** Lab 6 – The Complete CPU (Overall Project)

## Author

**Akarshan R Singh**
