# 🚀 8-bit ALU Design (Verilog | Synthesis | Timing Analysis)

## 📌 Overview

This project implements an **8-bit Arithmetic Logic Unit (ALU)** using Verilog HDL.
The ALU performs multiple arithmetic and logical operations based on a control signal (opcode) and is verified through **simulation, synthesis, and timing analysis**.

The design follows a standard RTL-to-Gates flow used in VLSI design.

---

## ⚙️ Features

* Supports **8 operations**:

  * Arithmetic: ADD, SUB
  * Logical: AND, OR, XOR
  * Additional: NOT, SHIFT (if implemented)
* **Opcode-based control logic**
* Fully verified using **testbench simulation**
* Synthesized design with **timing and area reports**

---

## 🧠 Architecture

### Inputs:

* `A [7:0]` → Operand A
* `B [7:0]` → Operand B
* `opcode [2:0]` → Operation selector

### Output:

* `result [7:0]` → ALU output

### Operation Mapping (Example):

| Opcode | Operation |
| ------ | --------- |
| 000    | ADD       |
| 001    | SUB       |
| 010    | AND       |
| 011    | OR        |
| 100    | XOR       |
| 101    | NOT       |
| 110    | SHIFT L   |
| 111    | SHIFT R   |

---

## 📁 Folder Structure

```bash
RTL/         → Verilog design files  
tb/          → Testbench for functional verification  
synth/       → Synthesis scripts / netlist  
Constraints/ → Timing constraints (SDC/XDC)  
Reports/     → Timing and area reports  
```

---

## 🔬 Simulation

The design is verified using a testbench that applies multiple input combinations and validates ALU operations.

<img width="1920" height="444" alt="waveform png" src="https://github.com/user-attachments/assets/67ea29ec-a248-461d-843d-a77a94089958" />

```
![Waveform](waveform.png)
```

---

## 🏗️ Synthesis & Timing

* Synthesized using standard synthesis tools
* Timing constraints applied
* Reports generated for:

  * Area utilization
  * Timing (setup/hold)

---

## 🛠️ Tools Used

* Verilog HDL
* ModelSim / Vivado (Simulation)
* Synthesis Tool (Design Compiler / Vivado)

---

## 📊 Key Learnings

* RTL design and modular coding
* ALU architecture and control logic
* Testbench development and verification
* Synthesis flow and timing analysis

---

## 📌 Future Improvements

* Add pipeline stages for performance
* Extend to 16-bit / 32-bit ALU
* Integrate into a simple CPU datapath

---

## 👤 Author

**Pratyush Machcha**



