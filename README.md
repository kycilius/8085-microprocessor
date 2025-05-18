## 🧠 8085 Microprocessor Development Kit

This project is a full schematic of an **8085-based microprocessor system**, built using EasyEDA. It includes a working setup with memory, address decoding, IO ports, and timing circuitry — designed as an educational kit or foundation for further expansion (e.g., display, keypad, or other peripherals).

### 🔧 Features

* **8085 CPU (U1)**
  Central processor that drives instruction execution.

* **2732 EPROM (U3)**
  Used for storing permanent programs/code. Address decoding enables program memory mapping.

* **HM6116 SRAM (U4)**
  2K RAM chip for general data storage.

* **74LS373 (U5)**
  Latch used to separate multiplexed address/data bus from 8085.

* **74LS138 (U6)**
  3-to-8 decoder for address decoding: selects ROM, RAM, and Port space.

* **8155 (or External Ports - P1, P3, P4)**
  Provides I/O lines for user interaction or peripherals.

* **CD4040 (U7)**
  Binary counter, used here to generate timing pulses or signals.

* **LM7805 (U8)**
  Power regulation: provides +5V supply to the circuit.

* **XTAL + Capacitors**
  Provides 6.144 MHz clock frequency to the CPU for stable operation.

---

### 🗺️ Block Diagram Overview

```
    +---------+     +----------+     +---------+
    |         |     |          |     |         |
    |  8085   +---> |  Latch   +---> | Address |
    |         |     |  74LS373 |     |  Lines  |
    +----+----+     +----+-----+     +----+----+
         |               |                |
         |               |                |
         v               v                v
     Multiplexed     Control         Decoder (74LS138)
     AD0–AD7 Bus     Signals          /    |    \
                                     ROM  RAM  IO Ports
```

---

### ⚙️ Schematic

The full schematic is built in **EasyEDA** and includes:

* All IC connections
* Power routing
* Control signals (`RD`, `WR`, `IO/M`, `ALE`, `RESET`, `INT`, etc.)
* Address & data bus routing
* Decoder enable logic
* Program storage in ROM
* RAM for data

🖼️ Preview available in repository:

> ![image](https://github.com/user-attachments/assets/197faf21-f8ff-49a8-8e10-535b17d48585)

🖼️ Preview also available in EasyEDA:

 https://oshwlab.com/sufyannadeem240/microprocessor-8085
---

### 🛠️ To-Do (Future Improvements)

* Add 7-Segment display or LCD output
* Integrate 8255 or 8155 for IO control
* Add keypad input interface
* Program and burn HEX code to EPROM
* Design PCB layout based on schematic

---

### ❌ Why Simulation Doesn't Work

EasyEDA **does not support microprocessor simulation** for full systems. The schematic is meant for:

* **PCB manufacturing**
* **Reference**
* **Educational design**

If you want to simulate logic or partial sections:

* Use **Logisim** for logic gates and decoder testing
* Use **Proteus** for full 8085 CPU-level simulation (commercial)

---

### 📂 Repository Structure

```
/8085-dev-kit
├── schematic/
│   └── 8085_microprocessor.json (EasyEDA project)
├── images/
│   └── 8085_schematic.png
├── README.md
└── LICENSE
```

---

### 📜 License

MIT License – Feel free to use, modify, or build upon this project. Give credit where due! 👍

---
