# Enterprise VLSI Chip Design & Verification System

## Project Overview

The **Enterprise VLSI Chip Design & Verification System** is a 32-bit Single-Cycle Processor designed and implemented using **Verilog HDL**. The project demonstrates the complete RTL design flow, functional verification, and FPGA synthesis workflow for digital processor design.

The processor consists of a Program Counter, Instruction Memory, Register File, Arithmetic Logic Unit (ALU), Control Unit, Data Memory, and a Top-Level Processor module. Functional verification is performed using **ModelSim**, and synthesis is completed using **Quartus Prime Lite**.

---

# Project Objectives

- Design a 32-bit processor architecture
- Implement RTL using Verilog HDL
- Perform functional verification using ModelSim
- Synthesize the design using Quartus Prime Lite
- Analyze timing and FPGA resource utilization
- Demonstrate a complete VLSI RTL design workflow

---

# Processor Architecture

```
                 +----------------------+
                 | Program Counter (PC) |
                 +----------+-----------+
                            |
                            v
                 +----------------------+
                 | Instruction Memory   |
                 +----------+-----------+
                            |
                            v
                 +----------------------+
                 | Control Unit         |
                 +----------+-----------+
                            |
            --------------------------------------
            |            |            |           |
            v            v            v           v
      Register File   ALU Control  Memory Ctrl  Write Back
            |
            v
      +-------------+
      |     ALU     |
      +------+------+
             |
             v
      +-------------+
      | Data Memory |
      +------+------+
             |
             v
       Register File
```

---

# Processor Specifications

| Feature | Specification |
|----------|---------------|
| Architecture | Single-Cycle Processor |
| Word Size | 32-bit |
| Registers | 8 General Purpose Registers |
| Instruction Memory | 16 × 32-bit ROM |
| Data Memory | 16 × 32-bit RAM |
| HDL | Verilog HDL |
| Simulation Tool | ModelSim |
| Synthesis Tool | Quartus Prime Lite |

---

# Supported Instructions

| Opcode | Instruction | Description |
|---------|-------------|-------------|
| MOVI | Move Immediate | Load immediate value |
| ADD | Addition | Add two registers |
| SUB | Subtraction | Subtract two registers |
| AND | Logical AND | Bitwise AND |
| OR | Logical OR | Bitwise OR |
| LOAD | Load | Read data from memory |
| STORE | Store | Write data to memory |
| NOP | No Operation | Idle instruction |

---

# Project Structure

```
Enterprise_VLSI_Chip_Design/

├── rtl/
│   ├── program_counter.v
│   ├── instruction_memory.v
│   ├── register_file.v
│   ├── alu.v
│   ├── control_unit.v
│   ├── data_memory.v
│   └── processor.v
│
├── testbench/
│   ├── program_counter_tb.v
│   ├── instruction_memory_tb.v
│   ├── register_file_tb.v
│   ├── alu_tb.v
│   ├── control_unit_tb.v
│   ├── data_memory_tb.v
│   └── processor_tb.v
│
├── quartus/
│   ├── processor.qpf
│   ├── processor.qsf
│   ├── RTL_Viewer.png
│   ├── Technology_Map.png
│   ├── Compilation_Report.pdf
│   └── Timing_Report.pdf
│
├── simulation & waveforms/
│   ├── ProgramCounter.png
│   ├── InstructionMemory.png
│   ├── RegisterFile.png
│   ├── ALU.png
│   ├── ControlUnit.png
│   ├── DataMemory.png
│   └── Processor.png
│
├── report/
│   ├── Project_Report.pdf
│   ├── Verification_Report.pdf
│   └── Architecture.pdf
│
└── README.md
```

---

# Design Modules

## Program Counter

- Generates instruction addresses
- Increments by 4 every clock cycle
- Resets to address 0

---

## Instruction Memory

- Stores program instructions
- Fetches instruction using the Program Counter
- 16 × 32-bit ROM

---

## Register File

- Eight 32-bit general-purpose registers
- Two read ports
- One write port
- Synchronous write operation

---

## Arithmetic Logic Unit (ALU)

Supported operations:

- Addition
- Subtraction
- AND
- OR
- Pass Immediate
- Zero Flag Generation

---

## Control Unit

Generates control signals based on instruction opcode.

Signals include:

- RegWrite
- MemRead
- MemWrite
- ALUSrc
- MemToReg
- ALUControl

---

## Data Memory

- 16 × 32-bit RAM
- Supports LOAD
- Supports STORE

---

## Top Processor

Integrates:

- Program Counter
- Instruction Memory
- Register File
- ALU
- Control Unit
- Data Memory

into one complete processor.

---

# Verification

Each module is verified independently using dedicated ModelSim testbenches.

Verified modules include:

- Program Counter
- Instruction Memory
- Register File
- ALU
- Control Unit
- Data Memory
- Complete Processor

---

# Functional Verification Flow

```
RTL Design

↓

Compile

↓

Simulation

↓

Waveform Analysis

↓

Verification

↓

PASS
```

---

# FPGA Synthesis Flow

```
RTL Design

↓

Quartus Compilation

↓

Synthesis

↓

Placement

↓

Routing

↓

Timing Analysis

↓

Resource Utilization
```

---

# Quartus Outputs

The following reports are generated:

- RTL Viewer
- Technology Map Viewer
- Compilation Report
- Timing Report
- Resource Utilization

---

# Simulation

Simulation Tool:

**ModelSim**

Simulation verifies:

- Program Counter
- Instruction Fetch
- Register Operations
- ALU Operations
- Memory Operations
- Complete Processor Execution

---

# Applications

- Digital Processor Design
- FPGA Prototyping
- Embedded Systems
- Computer Architecture Education
- RTL Design and Verification
- VLSI Design Learning

---

# Future Enhancements

- Pipeline Processor
- Branch Instructions
- Jump Instructions
- Cache Memory
- Interrupt Handling
- Hazard Detection
- Forwarding Unit
- Branch Prediction
- Multi-Core Architecture

---

# Tools Used

- Verilog HDL
- ModelSim
- Quartus Prime Lite
- GitHub

---

# Learning Outcomes

This project demonstrates:

- RTL Design
- Processor Architecture
- Digital Logic Design
- Functional Verification
- FPGA Synthesis
- Timing Analysis
- Resource Utilization
- Verilog HDL Coding
- ModelSim Simulation
- Quartus Prime Lite Workflow

---

# Author

**K Murali**

Electronics and Communication Engineering

G. Pullaiah College of Engineering and Technology

---

# License

This project is developed for educational purposes as part of the **Cognify Technologies Internship**.
