# VSDIAT Chip Design Program

This repository documents my hands-on learning journey through the **VSDIAT (VLSI System Design – Anurag Institute Chip Design Program)**. It includes my work on Verilog RTL design, simulation, synthesis, SKY130 technology mapping, timing analysis, and ASIC physical design.

The repository is organized by training day and includes practical exercises, implementation notes, debugging experiences, and my ongoing **BabySoC** project.

## Project Walkthrough Video

The video covers **Days 1–10** and the **BabySoC guided project**, including RTL design, synthesis, pre-layout STA, physical design, and post-route STA.

▶️ https://drive.google.com/file/d/1CoNw9tmedD7su3fJxhY0URSgDeSXODZo/view?usp=sharing

---

## Student Information

| Field      | Details                                  |
| ---------- | ---------------------------------------- |
| Name       | K. Vamshi Teja                           |
| University | Anurag University                        |
| Degree     | B.Tech                                   |
| Branch     | Electronics and Communication Engineering (ECE) |

---

## Development Environment and Tools

| Tool               | Purpose                          |
| ------------------ | -------------------------------- |
| Windows 11         | Host operating system            |
| Ubuntu VSDIAT VDI  | Linux development environment    |
| Oracle VirtualBox  | Virtualization                   |
| Icarus Verilog     | RTL and gate-level simulation    |
| GTKWave            | Waveform analysis                |
| Yosys              | RTL synthesis and optimization   |
| OpenLane           | ASIC implementation flow         |
| OpenSTA            | Static Timing Analysis           |
| OpenROAD           | Physical design                  |
| Magic              | Physical layout inspection       |
| SKY130 HD          | Standard-cell technology library |

---

## Repository Structure

```text
VLSI-Projects/
├── README.md
│
├── VLSI-Design-Workshop/
│   ├── README.md
│   ├── Module-1/
│   │   └── README.md
│   ├── Module-2/
│   │   └── README.md
│   ├── Module-3/
│   │   └── README.md
│   ├── Module-4/
│   │   └── README.md
│   ├── Module-5/
│   │   └── README.md
│   └── BabySoC/
│       ├── README.md
│       ├── rtl/
│       ├── testbench/
│       ├── synthesis/
│       └── results/
│
└── VLSI-Physical-Design/
    ├── README.md
    ├── Module-1/
    │   ├── README.md
    │   ├── OPENLANE NETLIST.png
    │   ├── OPENSTA.png
    │   ├── openlane statistics 2.png
    │   └── printing statistics openlane.png
    ├── Module-2/
    │   ├── README.md
    │   ├── FLOORPLANNING.png
    │   ├── PLACEMENT.png
    │   ├── design config tcl.png
    │   └── floorplan.png
    ├── Module-3/
    │   ├── README.md
    │   ├── inverter code magic t.png
    │   ├── inverter graph.png
    │   ├── inverter image.png
    │   └── inverter lef file pins.png
    ├── Module-4/
    │   ├── README.md
    │   ├── inverter m4.png
    │   ├── inverter lef file pins.png
    │   ├── pin placement1.png
    │   └── printing statistics m4.png
    └── Module-5/
        ├── README.md
        ├── DRC CLEAN.png
        ├── PARASITIC EXTRACTION.png
        ├── routing.png
        └── mage routing.png
```

> Physical-Design Module-5  contains **SKY130 Module 5**. The detailed module documentation and practical screenshots are maintained , rather than in this root README.

---

## Course Progress

| Day    | Topics                                          | Status       |
| ------ | ----------------------------------------------- | ------------ |
| Day 1  | Verilog RTL Design and Synthesis                | ✅ Completed |
| Day 2  | RTL Synthesis and Optimization                  | ✅ Completed |
| Day 3  | Combinational, Sequential, and Counter Optimization | ✅ Completed |
| Day 4  | RTL vs. Gate-Level Simulation                   | ✅ Completed |
| Day 5  | Verilog Coding and Hardware Inference           | ✅ Completed |
| Day 6  | Introduction to Physical Design and OpenLane    | ✅ Completed |
| Day 7  | Floorplanning and Placement                     | ✅ Completed |
| Day 8  | CMOS, Fabrication, SPICE, and SKY130            | ✅ Completed |
| Day 9  | Timing Analysis, CTS, and Post-CTS STA          | ✅ Completed |
| Day 10 | Routing, Power Distribution, and TritonRoute    | ✅ Completed |

---

## Day 1 – Verilog RTL Design and Synthesis

Day 1 introduced the RTL-to-synthesis workflow using a simple **2:1 multiplexer**. This exercise helped me understand how a Verilog design is simulated, synthesized, and mapped to standard cells.

### Topics Covered

- Verilog RTL design and testbench development
- Functional simulation using Icarus Verilog
- Waveform analysis using GTKWave
- Synthesis using Yosys
- Gate-level netlist generation
- SKY130 technology mapping

### Basic Workflow

```text
RTL Design
    ↓
Functional Simulation
    ↓
Synthesis
    ↓
Gate-Level Netlist
    ↓
Technology Mapping
```

---

## Day 2 – RTL Synthesis and Optimization

Day 2 focused on how different RTL coding styles affect the hardware produced by synthesis.

### Topics Covered

- Hierarchical and flat synthesis
- Flip-flop coding styles
- Synchronous and asynchronous resets
- Arithmetic optimization
- Boolean logic optimization
- Yosys synthesis analysis
- SKY130 technology mapping

These exercises helped me understand how synthesis tools transform RTL descriptions into optimized hardware structures.

---

## Day 3 – RTL Optimization and Sequential Logic

Day 3 continued the study of synthesis optimization, with a focus on combinational and sequential circuits.

### Topics Covered

- Combinational logic optimization
- Sequential logic optimization
- Flip-flop optimization
- Counter optimization
- Yosys synthesis analysis
- Gate-level netlist inspection
- Waveform analysis

The practical work helped me connect RTL coding decisions with the hardware structures generated during synthesis.

---

## Day 4 – RTL vs. Gate-Level Simulation

Day 4 focused on comparing RTL simulation with gate-level simulation (GLS) and understanding how synthesized hardware behaves.

### Topics Covered

- RTL and gate-level simulation
- Synthesis–simulation mismatches
- Blocking assignments
- Ternary operators
- Multiplexer synthesis
- Gate-level behavior
- Waveform comparison

The main objective was to check whether the synthesized implementation preserves the intended RTL functionality.

---

## Day 5 – Verilog Coding and Hardware Inference

Day 5 explored Verilog constructs that influence the hardware inferred by synthesis tools.

### Topics Covered

- `if` and `case` statements
- Incomplete assignments
- Latch inference
- MUX and DEMUX structures
- `generate` constructs
- Partial assignments
- Ripple-carry adder
- RTL hardware inference

This work highlighted the importance of writing complete and clear RTL code to obtain the intended hardware.

---

## Day 6 – Introduction to Physical Design and OpenLane

Day 6 marked the transition from RTL design and synthesis to ASIC physical design.

### Topics Covered

- ASIC design flow
- RTL-to-GDSII flow
- SKY130 PDK
- OpenLane and Yosys
- OpenSTA and OpenROAD
- Magic layout inspection
- Synthesis statistics
- Floorplanning and placement
- Clock Tree Synthesis (CTS)
- Routing and parasitic extraction
- Physical verification
- GDSII generation

### Practical Work

- Running synthesis and reviewing synthesis statistics
- Performing floorplanning
- Inspecting the physical layout using Magic

📄 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN/tree/main/MODULE%20-1

---

## Day 7 – Floorplanning and Placement

Day 7 explored the early stages of physical implementation and the physical factors that affect an ASIC design.

### Topics Covered

- Die and core concepts
- Floorplanning and aspect ratio
- Core utilization
- Standard-cell placement
- Cell and timing characterization
- Timing thresholds
- Input slew and output slew
- Static Timing Analysis fundamentals
- Power Distribution Network (PDN)
- IR drop and decoupling capacitors
- LEF and DEF formats
- Layout inspection using Magic

### Practical Flow

```text
Synthesized Netlist
        ↓
    Floorplanning
        ↓
      Placement
        ↓
  Magic Layout Inspection
```

> Timing and cell characterization were also studied as theory. Numerical values in the training material are examples, not project measurements.

📄 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN/tree/main/MODULE%20-2

---

## Day 8 – CMOS Fundamentals, Fabrication, SPICE, and SKY130

Day 8 connected CMOS fundamentals and semiconductor fabrication concepts with practical standard-cell layout and SPICE simulation.

### Topics Covered

- SPICE deck basics
- CMOS robustness
- 16-mask CMOS fabrication process
- CMOS inverter
- SkyWater and SKY130 PDK
- Introduction to Magic
- Custom standard-cell inverter layout
- Layout-to-SPICE extraction
- Transient simulation using ngspice
- Waveform analysis

### Practical Flow

```text
CMOS Inverter
      ↓
Custom Standard-Cell Layout
      ↓
Magic Extraction
      ↓
SPICE Representation
      ↓
ngspice Transient Simulation
      ↓
Waveform Analysis
```

📄 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN/tree/main/MODULE%20-3

---

## Day 9 – SKY130 Module 4: Timing Analysis, CTS, and Post-CTS STA

Day 9 focused on timing analysis and clock distribution during physical design.

### Topics Covered

- Standard-cell timing models and delay tables
- Input slew and output load
- Cell and buffer delay
- Setup and hold timing
- Ideal-clock and real-clock analysis
- Clock Tree Synthesis (CTS)
- Clock distribution and buffering
- Clock skew and insertion delay
- Physical implementation effects
- Post-CTS timing analysis
- Static Timing Analysis (STA)
- Slack, WNS, and TNS
- Timing violations and timing closure

### Learning Flow

```text
Timing Models
      ↓
Setup and Hold Analysis
      ↓
Clock Tree Synthesis
      ↓
Physical Implementation
      ↓
Post-CTS Timing Analysis
      ↓
WNS / TNS Review
```

This module helped me understand how cell delays, clock distribution, and interconnect effects influence timing results.

📄 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN/tree/main/MODULE-%204

---

## Day 10 – SKY130 Module 5: Routing, Power Distribution, and TritonRoute

Day 10 focused on routing and related physical-design concepts, including power distribution and TritonRoute.

### SKY130_D5_SK1 – Routing and Design

- Introduction to maze routing
- Lee's routing algorithm
- Routing and parasitic extraction
- Routed-design inspection

### SKY130_D5_SK2 – Power Distribution

- Power Distribution Network concepts
- PDN generation and failure analysis
- OpenDB and OpenROAD investigation
- Power/ground BTerm handling
- Source-level debugging and patch development

### SKY130_D5_SK3 – TritonRoute Features

- Fast routing and detailed routing
- Preprocessed route guides
- Parallel and sequential panel routing
- Connectivity and access points
- Routing topology concepts

### Practical Routing Flow

```text
Floorplanning
      ↓
Placement
      ↓
CTS
      ↓
Routing
      ↓
Parasitic Extraction
      ↓
Routed DEF / SPEF
      ↓
Physical Layout Inspection
```

### Practical Progress and Debugging

The `picorv32a` routing stage completed successfully and produced routed design data, including **DEF** and **SPEF** files.

PDN generation was also investigated. In the original failing run, an existing power/ground BTerm was being recreated, causing a `NULL` object to reach `setSpecial`. A defensive source-level patch was developed to reuse an existing BTerm when one was already present.

> This documents the debugging and patch-development work. It does **not** establish that PDN generation completed successfully.

📄 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN/tree/main/MODULE%20-5

---

## BabySoC

**BabySoC** is the main SoC implementation. It brings together concepts from RTL design, simulation, synthesis, timing analysis, and physical design.

For detailed documentation, architecture, RTL, testbench, synthesis results, and physical-design evidence, see the https://github.com/vamshiteja10/VLSI-DESIGN-WORKSHOP/tree/main/SUMMARY.

### BabySoC Architecture

The top-level module is `vsdbabysoc`. The design contains three main blocks:

```text
                     ┌──────────────┐
 ENb_CP ────────────►│              │
 ENb_VCO ───────────►│   AVSDPLL    │
 REF ───────────────►│     PLL      │─── CLK ───┐
 VCO_IN ────────────►│              │           │
                     └──────────────┘           ▼
                                           ┌──────────┐
                                    reset ►│  RVMyth  │
                                           │   CPU    │
                                           └────┬─────┘
                                                │
                                           RV_TO_DAC[9:0]
                                                │
                                                ▼
                                           ┌──────────┐
                                    VREFH ►│ AVSDDAC  │
                                           │   DAC    │
                                           └────┬─────┘
                                                │
                                                ▼
                                               OUT
```

### Main Blocks

- **RVMyth** – RISC-V-based digital processor core.
- **AVSDPLL** – PLL block used for clock generation.
- **AVSDDAC** – DAC block that converts the processor's digital output.

### BabySoC ASIC Flow

```text
RTL Design
    ↓
Pre-Synthesis Simulation
    ↓
Logic Synthesis
    ↓
SKY130 Technology Mapping
    ↓
Gate-Level Netlist
    ↓
Post-Synthesis Simulation
    ↓
Pre-Layout Static Timing Analysis
    ↓
Floorplanning
    ↓
Placement
    ↓
Clock Tree Synthesis
    ↓
Routing
    ↓
Post-Route Static Timing Analysis
    ↓
Further Physical Verification and Closure
```

- Pre-layout STA
- Floorplanning
- Placement
- Clock Tree Synthesis
- Routing
- Post-route STA
- Overall Physical-Design README

> **Note on results:** STA results must be interpreted alongside the timing constraints, corner definitions, units, and source reports. Negative slack indicates a timing violation for the relevant path under the analyzed constraints. The available routing DRC evidence includes short violations, so the design should not be described as DRC-clean based on the current evidence.
>
> Similarly, executing post-route STA does not prove that all timing corners pass, that LVS is clean, or that a final signoff-ready GDSII has been generated.

---

## What I Learned

### RTL and Digital Design

- Verilog HDL and RTL design
- Testbench development
- Functional simulation
- Combinational and sequential logic
- Digital hardware inference

### Synthesis

- Yosys synthesis and logic optimization
- Technology mapping
- Standard-cell libraries
- Gate-level netlist generation and inspection

### ASIC Physical Design

- OpenLane and the SKY130 PDK
- Floorplanning and placement
- Clock Tree Synthesis
- Routing and parasitic extraction
- Static Timing Analysis
- Power Distribution Network concepts
- Physical verification and GDSII flow

### Practical Engineering

- Linux command-line workflow
- EDA tool usage
- Simulation and waveform analysis
- Netlist and physical layout inspection
- Git and GitHub documentation
- OpenROAD/OpenDB debugging
- Timing and physical-design report analysis

---

## Overall Learning Journey

```text
Digital Design
      ↓
Verilog RTL
      ↓
Simulation
      ↓
Synthesis and Optimization
      ↓
Technology Mapping
      ↓
Gate-Level Simulation
      ↓
ASIC Physical Design
      ↓
Floorplanning and Placement
      ↓
Clock Tree Synthesis
      ↓
Routing and Parasitic Extraction
      ↓
Timing Analysis
      ↓
Physical Verification and Further Closure
```

This repository reflects my progress from basic RTL design and simulation to more advanced ASIC implementation concepts. It also documents practical debugging experiences and the stages that still require further verification.

---

## Author

**K. Vamshi Teja**
B.Tech – Electronics and Communication Engineering
Anurag University

## Repositories

🔗 https://github.com/vamshiteja10/VLSI-DESIGN-WORKSHOP
🔗 https://github.com/vamshiteja10/VLSI-PHYSICAL_DESIGN
