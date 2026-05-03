🚀 8-bit ALU Design (Verilog | Synthesis | Timing)

📌 Overview
This project implements an 8-bit Arithmetic Logic Unit (ALU) using Verilog HDL.  
The design supports multiple arithmetic and logical operations and is validated through simulation, synthesis, and timing analysis.

⚙️ Features
- 8 operations:
  - ADD, SUB
  - AND, OR, XOR
  - NOT
  - SHIFT LEFT, SHIFT RIGHT
  - Fully combinational design
  - Verified using testbench and     waveform analysis
  - Synthesized using Yosys
  - Basic timing analysis with constraints (SDC)

🧠 Architecture
- All operations are computed in parallel
- Output is selected using a multiplexer ($pmux)
- Select signal (`sel`) is decoded using comparators

---

## 🧪 Simulation

- Tool: **Icarus Verilog**
- Waveform: **GTKWave**

### 🔹 Waveform Output
![Waveform](reports/waveform.png)

✔ Verified all operations:
- ADD → 15  
- SUB → 5  
- AND → 0  
- OR → 15  
- XOR → 15  
- NOT → F5  
- SHIFT operations correct  

📊 Synthesis

- Tool: Yosys
- Cells: 15
- No latches or flip-flops inferred (pure combinational design)

🔹 Synthesized Netlist
![Schematic](reports/alu_schematic.png)

🔹 Key Components
- `$add`, `$sub` → Arithmetic
- `$and`, `$or`, `$xor`, `$not` → Logic
- `$pmux` → Output selection
- `$eq` → Select decoding

⏱️ Timing Analysis

👉 Critical Path: 
ADD → MUX → OUTPUT
Estimated Delay: ~6.5 ns
Required Time: 10 ns
Slack: +3.5 ns
Status: Timing Met 
 
📌 Note: Timing is estimated based on architecture.  
Full STA requires tools like OpenSTA or PrimeTime.

🛠 Tools Used
- Verilog HDL  
- Yosys (Synthesis)  
- Icarus Verilog (Simulation)  
- GTKWave (Waveform Viewer)  

🧠 Key Learnings
- RTL to Gate-Level conversion  
- Multiplexer-based ALU design  
- Understanding `$pmux`, `$eq` cells  
- Critical path and timing concepts  
- Writing synthesis scripts (Yosys)

📌 Future Improvements
- Add status flags (Carry, Zero, Overflow)  
- Pipeline design for performance  
- Area optimization  
- Perform real STA using OpenSTA  

👤 Author
Pratyush Machcha
