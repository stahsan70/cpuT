# cpuT
This repository contains a **partial implementation of a 32-bit RISC-V processor based on the RV32I ISA**, developed as part of an ongoing processor design project. The design currently supports a subset of **RV32I integer instructions** along with **selected RV32M (multiplication/division) instructions**. 

# RV32I RISC-V Processor (Partial Implementation)

The processor is intended for **educational and experimental purposes**, focusing on instruction decoding, ALU design, and datapath/control integration.

---

## 📌 Features Implemented

- **ISA Base**: RISC-V RV32I  
- **Word Length**: 32-bit  
- **Architecture Style**: Single-cycle  
- **Design Level**: Schematic-based  

---

## ✅ Instruction Support

A total of **22 ALU-related instructions** have been implemented.

### RV32I Integer Instructions (19)

#### R-type Instructions
- `ADD`
- `SUB`
- `AND`
- `OR`
- `XOR`
- `SLL`
- `SRL`
- `SRA`
- `SLT`
- `SLTU`

#### I-type Instructions
- `ADDI`
- `ANDI`
- `ORI`
- `XORI`
- `SLLI`
- `SRLI`
- `SRAI`
- `SLTI`
- `SLTIU`

### RV32M Extension (3)
- `MUL`
- `DIVU`
- `REMU`

---

## 🧠 Processor Datapath Overview

The processor consists of the following major components:

- Instruction Memory Interface  
- Register File (32 × 32-bit)  
- ALU with RV32I and partial RV32M support  
- Immediate Generator  
- ALU Control Unit  

---

## 🖼️ Circuit Diagrams

### Top-Level Processor Architecture
![Top-Level Processor](images/main-circuit.png)
<img width="832" height="538" alt="main-circuit" src="https://github.com/user-attachments/assets/84958a69-5e72-460d-bace-822be152d960" />

### ALU Design
![ALU View 1](images/ALU_view1.png)  
<img width="710" height="638" alt="ALU_view1" src="https://github.com/user-attachments/assets/3cf2574b-3f73-4238-9e77-bdc200ca92f3" />

![ALU View 2](images/ALU_view2.png)
<img width="570" height="658" alt="ALU_view2" src="https://github.com/user-attachments/assets/f96fb187-06ea-4186-9d5e-5c5a6c81642c" />


### ALU Control Unit
![ALU Control Logic 1](images/ALU-Control-Logic_view1.png)  
<img width="1188" height="606" alt="ALU-Control-Logic_view1" src="https://github.com/user-attachments/assets/aede6018-5a7c-4cd5-9caf-1a4f008b553f" />

![ALU Control Logic 2](images/ALU-Control-Logic_view2.png)  
<img width="1186" height="632" alt="ALU-Control-Logic_view2" src="https://github.com/user-attachments/assets/c148da88-cb30-4940-af57-063cb7d72ffa" />


### Register File Unit
![Register File 1](images/Reg-file_view1.png)  
<img width="1168" height="624" alt="Reg-file_view1" src="https://github.com/user-attachments/assets/dacbe267-fdf6-4889-83ad-8e33790a5cbb" />

![Register File 2](images/Reg-file_view2.png)  
<img width="1088" height="654" alt="Reg-file_view2" src="https://github.com/user-attachments/assets/81dfff03-605e-4d55-84a0-a0df6db18bb2" />

![Register File 3](images/Reg-file_view3.png)
<img width="1168" height="640" alt="Reg-file_view3" src="https://github.com/user-attachments/assets/ccc9575d-4f99-4b37-ba68-95c0f856b4f4" />


### Instruction Memory Unit
![Instruction Memory](images/IMEM.png)
<img width="690" height="212" alt="IMEM" src="https://github.com/user-attachments/assets/98af5a53-772a-4e34-89a0-774fa0d02dbe" />


### Immediate Generation Unit
![Immediate Generator](images/Imm-Gen.png)
<img width="602" height="158" alt="Imm-Gen" src="https://github.com/user-attachments/assets/c71c1c1b-daef-475a-9091-0ab9baf5555e" />


---

## 🧪 Verification & Testing

- Instruction-level testing performed using:
  - Hand-written RISC-V assembly programs
  - ALU operation test cases
- **Simulation environment**: Logisim  
- A sample assembly test-code file is included in the repository.
[test-code-22Inst.docx](https://github.com/user-attachments/files/24845458/test-code-22Inst.docx)


Further testing and full ISA coverage are planned.

---

## 🚧 Current Limitations

- Load/store instructions not yet implemented  
- Branch and jump instructions not included  
- CSR support and exception handling not present  
- Pipeline implementation not included  
- Not yet fully RV32I-compliant  

---

## 🔮 Future Work

Planned extensions include:

- Load and store instructions (`LW`, `SW`, etc.)
- Branch and jump instructions (`BEQ`, `JAL`, `JALR`)
- Full RV32M support
- Pipelined implementation
- Hazard detection and forwarding
- Compliance testing with official RISC-V test suites

---

## 📁 Repository Structure

```text
.
├── src/
│   └── cpuT_22inst.circ      # Logisim processor project file
├── images/                  # Processor and circuit diagrams
├── test/                    # Assembly test code
└── README.md
