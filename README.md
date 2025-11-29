# Asymmetric-CallStack-8bit-CPU
Turing-Complete 8-bit CPU from 12K+ NAND Gates: Asymmetric 10-bit Addressing &amp; 16-Level Call Stack with Full Toolchain – Solo Built by a 12-Year-Old in 4 Weeks

> **Repository Management Notice**
>
> This repository is maintained by the parent of the **12-year-old** creator. All technical content, architectural design, and implementation details were **100% independently completed** by the creator after 1.5 years of **self-directed learning through online video tutorials**, within just **4 weeks of after-school time**.
>
> Only the **compiler** framework was initially **AI-assisted**, but all logic, semantics, structure, and implementation issues were **independently debugged, refactored, and optimized by the creator himself**, ensuring complete understanding and full control over the entire CPU system.
>
> We sincerely invite **experts in computer architecture and digital logic design** to provide an objective assessment of this project's technical depth and academic merit. We would be deeply grateful for your professional guidance for the future development of this 12-year-old creator, **in English, Chinese, Japanese, or Korean**.
>
> * For project inquiries, please contact: yhc1930@gmail.com

---

## **Project Overview**

This project showcases an **8-bit Turing-Complete CPU** built entirely **bottom-up** from **NAND gates**. Implemented on the Digital Logic Sim platform, the total logic gate count exceeds **12,000+**.

Unlike traditional instructional 8-bit CPUs, this architecture overcomes conventional addressing limits by innovatively designing an **Asymmetric 10-bit Addressing System** and a **16-level Hardware Call Stack**. This design natively supports complex recursive calls and enables a larger instruction space. Beyond the hardware, the creator independently developed a **complete software toolchain**, including the Instruction Set Architecture (ISA) definition, Assembler, and a Compiler converting a high-level language to assembly.

**Global Rarity:** This is one of the few projects of its kind—a full-stack engineering practice from foundational logic gates to a complete computer system—completed **independently** by a **12-year-old** with **no external mentorship**, relying solely on 1.5 years of self-study and executed during **4 weeks of after-school** time.

<img width="2719" height="773" alt="YHC" src="https://github.com/user-attachments/assets/1353ea63-d480-4b93-aba4-b1e719f79fc7" />
Figure: Fibonacci & 5! = 120 ◎ Nov. 24, 2025

---

##  Turing Completeness Verification & Demos

The system has been validated through various complex algorithms, proving its Turing completeness and hardware stability.

| Verification Program | Date | Result / Performance | Key Technical Validation Points | Demo Video |
| :--- | :--- | :--- | :--- | :--- |
| **Fibonacci Sequence** | **Nov. 24, 2025** | Stable calculation in **39 seconds displayed on screen** | Recursive logic, addition operations, digital display driver | https://www.youtube.com/watch?v=GAZBIPB3BlA |
| **Factorial Calculation (5!)** | **Nov. 24, 2025** | Result **120** displayed on screen | Multiplication simulation (repeated addition), stack depth test | https://www.youtube.com/watch?v=ZgU1eWkcY8E |
| **Bubble Sort** | **Nov. 19, 2025** | **150 seconds** (8 numbers) | Nested loops, conditional branching, memory R/W stability | https://www.youtube.com/watch?v=A9nyPtnZRTs |
| **Graphics Display** | **Nov. 24, 2025** | 16x16 **"X-pattern"** | Memory-Mapped I/O (MMIO), bitwise operations, coordinate calculation | - |

---

## Core Architectural Innovations

### Breakthrough Design: Asymmetric 10-bit Call Stack Architecture
This is the most crucial technical highlight, resolving the engineering conflict between address expansion and performance in conventional 8-bit CPUs.

* **Technical Challenge** : A standard 8-bit CPU has an 8-bit data bus. To achieve addressing beyond 256 bytes (e.g., 1KB), it typically requires multiple memory access cycles or complex bank switching (paging), severely impacting performance.
* **Innovative Solution** :
    * **Separated Architecture** : The Arithmetic Logic Unit (ALU) remains **8-bit** for data processing efficiency, while the Address Bus and Program Counter (PC) are expanded to **10-bit**.
    * **10-bit Address Space** : Directly supports **1024 bytes (1KB)** of instruction memory space ($2^{10}$), eliminating the need for paging.
    * **Hardware-Level Recursion Support** : A specialized **16-level Hardware Call Stack** was designed. This stack saves the 10-bit return address in a single cycle, perfectly supporting deep recursive function calls and complex nesting.

This non-symmetric separation between **Data Word Width** and **Address Word Width** demonstrates the creator's profound understanding of the "von Neumann Bottleneck" and resource trade-offs in computer architecture.

---

## Technical Specifications & Hardware Implementation

### System Specifications Table

| Specification | Parameter Details |
| :--- | :--- |
| **Base Logic Gates** | 12,000+ (NAND/NOR/XOR/NOT, etc.) |
| **Data Word Width** | 8-bit (General-purpose registers and ALU) |
| **Address Word Width** | 10-bit (Asymmetric design, supporting 1KB space) |
| **Register File** | 16 x 8-bit General-Purpose Registers (R0-R15) |
| **Call Stack** | **16-level Hardware Stack** (16 x 10-bit) for return addresses |
| **Instruction Set (ISA)** | Custom ISA (includes arithmetic, logic, jump, and stack operations) |
| **Clock Frequency** | 1000 Hz (Simulation Environment Setting) |
| **Peripherals** | 16x16 Pixel Graphics Display + 3 x 7-segment Digital Displays |

### Bottom-Up Construction Layers
1.  **Fundamental Gates**: Manually built NAND, NOR, XOR, AND, NOT.
2.  **Combinational Logic**: Built 8-bit Adders, Comparators, Multiplexers (MUX).
3.  **Custom Components**:
    * **XORS Gate**: Creator-designed special logic gate (see `XORS.json`) for optimizing specific computation paths.
    * **ALU (Arithmetic Logic Unit)**: Supports addition/subtraction, bitwise operations, and a custom `**Cancler**` logic.
4.  **Sequential Logic**: Latches → Registers → Program Counter (PC).
5.  **Core Integration**: ALU + Register File + Control Unit + 16-level Call Stack = **Complete CPU Core**.

---

## Software Toolchain

The creator not only built the **hardware** but also implemented a complete **software** development ecosystem:

### 1. Instruction Set Architecture (ISA)
A fixed 16-bit instruction format was defined, including:
* **Data Transfer**: `LDI` (Load Immediate), `STR` (Store)
* **Arithmetic**: `ADD`, `DEC` (Decrement)
* **Logic/Control**: `CMP` (Compare), `JMP`, `BRH` (Conditional Branch)
* **Subroutine Control**: `CAL` (Call), `RET` (Return - works with the hardware stack)

### 2. Assembler
Independently written, responsible for symbol parsing, label address allocation, and machine code generation.

### 3. Compiler
* **Development History**: The initial framework was AI-generated (approx. 2000 lines), but significant logical flaws and inoperability were found.
* **Independent Refactoring**: The creator completely discarded the unusable code and **rewrote(AI), debugged, and optimized** the core logic, resulting in 1257 lines of efficient code (Assembly Language → High-level Language).
* **Functionality**: Successfully translates high-level language logic into custom assembly instructions with optimized code generation efficiency.

---

## Parent's Note & Acknowledgement

As parents, the **happiest moment** was seeing the **pure joy on our child's face after solving a stubborn problem**. In his own words: "**I finally succeeded after so, so many failures**."

We **witnessed** his **complete dedication** over these four weeks: whether walking, eating, or even in his sleep, his brain was racing, designing the circuit logic.

Honestly, **we know nothing** about CPU hardware design. It wasn't until **November 16, 2025**, that he excitedly rushed over, yelling: "**Dad, Dad, I did it! I made a Turing-complete CPU, come look!**" We stared at the complex wiring on the screen, completely clueless about what it meant. Out of curiosity, during a relaxed Sunday, I took a screenshot and asked an AI, "**What is this?**"

In that moment, I felt like I had opened a door to a **new universe**. To truly understand our child's world, I also spent **a week** catching up on computer organization and architecture. And that is how this GitHub repository came to be.

This project might be naive, but it embodies the **PUREST PASSION** and **persistence** of a 12-year-old heart. **We kindly ask for the patience and guidance of experts and scholars**.

### Acknowledgements (Credits)
* **Platform Tool**: Digital Logic Sim
* **Assisted Tool**: AI (for initial compiler framework generation and conceptual explanations)
* **Special Thanks**: We are grateful to all experts and scholars willing to stop by, review, and offer professional assessment and advice. **Your every suggestion will be a precious lighthouse for his future path**.

---

## Contact Information

* **Project/Academic Consultation**: yhc1930@gmail.com
* **Technical Discussion**: Welcome to raise questions or suggestions via Issues.
* **License**: MIT License

**🌟 If this 8-bit world, independently built by a 12-year-old, brought you a spark of surprise, a Star of support is greatly appreciated! 🌟**

*Built with passion, logic gates, and countless hours of debugging by a 12-year-old dreamer.*
