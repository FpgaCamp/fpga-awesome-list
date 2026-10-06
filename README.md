# Awesome FPGA

Resources for learning RTL, testing designs, building bitstreams, choosing boards, and reusing FPGA IP.

## Contents

- [Start here](#start-here)
- [Activity and status](#activity-and-status)
- [Curation rules](#curation-rules)
- [Learning paths](#learning-paths)
- [Knowledge and tutorials](#knowledge-and-tutorials)
- [Books and evergreen references](#books-and-evergreen-references)
- [Languages and HDL frameworks](#languages-and-hdl-frameworks)
- [Simulation, verification, and debug](#simulation-verification-and-debug)
- [Synthesis, implementation, and programming](#synthesis-implementation-and-programming)
- [Project workflow and productivity](#project-workflow-and-productivity)
- [Vendor tools](#vendor-tools)
- [Boards and hardware ecosystems](#boards-and-hardware-ecosystems)
- [Reusable IP and reference designs](#reusable-ip-and-reference-designs)
- [Communities and source lists](#communities-and-source-lists)
- [FPGA vendors](#fpga-vendors)
- [eFPGA vendors](#efpga-vendors)
- [Source audit](#source-audit)
- [Contributing](#contributing)
- [License](#license)

## Start here

| Goal | Practical path |
| --- | --- |
| Learn FPGA basics | HDLBits exercises, then Nandland or Project F board projects. |
| Write RTL that meets timing | 01signal for CDC and resets; AMD UG903/UG906 for Vivado constraints and timing reports. |
| Test an RTL block | Pick a simulator, use cocotb or VUnit, inspect waveforms with GTKWave or Surfer. |
| Try an open-source FPGA flow | OSS CAD Suite, Yosys, nextpnr, and openFPGALoader; check exact chip and board support first. |
| Automate builds and registers | FuseSoC/Edalize for builds; PeakRDL or RgGen for register maps. |
| Assemble a soft-core SoC | LiteX or NEORV32; check peripheral, memory PHY, and board support. |
| Choose hardware | Confirm tool edition, license, OS support, and required I/O before buying a board. |

## Activity and status

| Status | Meaning |
| --- | --- |
| ![active][status-active] | Source-confirmed activity within the last 18 months, without an explicit retirement notice. |
| ![stable][status-stable] | Useful older project, durable reference, or official resource without a dated update. |
| ![unknown][status-unknown] | Relevant source with unclear update activity or incomplete access verification. |
| ![legacy][status-legacy] | Useful for older flows, old devices, or historical context; not a first choice for new projects. |

Metadata and links checked on **2026-10-06**. `Activity` is the GitHub repository's `pushed_at` month, or a publication, release, or last-updated month exposed by the linked source. Missing dates stay blank; the check date is not an activity date. The active window starts on 2025-04-06. Archived repositories and explicit maintenance notices override recency. A recent push does not prove a release, device support, or design correctness.

`Stars` is filled only for GitHub repositories, using the repository star count. Rows are ordered by status from active to stable to unknown to legacy, then by newest activity, stars, and name.

## Curation rules

- Link to documentation, source code, exercises, or a hardware catalog with a clear FPGA use.
- Check upstream content and maintenance notices before adding an entry.
- State relevant device, tool, licensing, or experimental limitations.
- Skip duplicate landing pages, generic search indexes, dead mirrors, and contact-only pages.
- Keep older material when its RTL, exercises, or device-specific instructions are still useful.

## Learning paths

### Beginner path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Project F](https://projectf.io/) | Build display controllers, sprites, fixed-point arithmetic, and other Verilog examples. | ![active][status-active] | 2026-09 |  |
| [FPGA-ASIC Roadmap](https://github.com/m3y54m/FPGA-ASIC-Roadmap) | Plan study topics from digital logic through RTL and verification; includes ASIC material. | ![active][status-active] | 2026-05 | 703 |
| [Bruno Levy learn-fpga](https://github.com/BrunoLevy/learn-fpga) | Build Verilog circuits and a RISC-V CPU with Yosys/nextpnr on supported boards. | ![active][status-active] | 2025-11 | 3718 |
| [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) | Solve automatically checked Verilog exercises on combinational logic, registers, and FSMs. | ![stable][status-stable] | 2024-10 |  |
| [fpga4fun](https://www.fpga4fun.com/) | Try UART, video, audio, and other small circuits; many tool instructions use ISE or Quartus II. | ![stable][status-stable] | 2024-03 |  |
| [Nandland](https://nandland.com/) | Learn Verilog/VHDL basics and work through UART and Go Board examples. | ![stable][status-stable] | 2023-12 |  |
| [SparkFun "So You Want to Learn FPGAs"](https://news.sparkfun.com/1203) | Read a 2013 introduction to the learning curve; not a current board or tool recommendation. | ![legacy][status-legacy] | 2013-07 |  |

### RTL design path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [ZipCPU](https://github.com/ZipCPU/zipcpu) | Study pipelined CPU RTL, Wishbone interfaces, and formal properties in a working soft core. | ![active][status-active] | 2026-09 | 1589 |
| [01signal](https://www.01signal.com/) | Work through CDC, reset strategy, FIFOs, signed arithmetic, and timing constraints. | ![stable][status-stable] |  |  |
| [ASIC-World](https://www.asic-world.com/) | Look up HDL syntax and small circuit/testbench examples. | ![stable][status-stable] |  |  |
| [ChipVerify](https://www.chipverify.com/) | Look up SystemVerilog constructs, assertions, and UVM testbench examples. | ![stable][status-stable] |  |  |
| [Cliff Cummings / Sunburst papers](https://www.paradigm-works.com/technical-library) | Read papers on nonblocking assignments, CDC, asynchronous FIFOs, and SystemVerilog coding. | ![stable][status-stable] |  |  |

### Verification path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [cocotb](https://github.com/cocotb/cocotb) | Write Python tests that drive and check HDL signals in a supported simulator. | ![active][status-active] | 2026-10 | 2534 |
| [VUnit](https://github.com/VUnit/vunit) | Compile HDL dependencies, run self-checking VHDL/SystemVerilog tests, and collect results. | ![active][status-active] | 2026-10 | 847 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | Add VHDL random stimulus, functional coverage, scoreboards, and protocol verification components. | ![active][status-active] | 2026-10 | 88 |
| [GTKWave](https://github.com/gtkwave/gtkwave) | Inspect VCD/FST simulation waveforms and save signal layouts. | ![active][status-active] | 2026-09 | 1030 |
| [UVVM](https://github.com/UVVM/UVVM) | Drive interfaces with VHDL BFMs and coordinate transactions through verification components. | ![active][status-active] | 2026-04 | 465 |
| [EDA Playground](https://www.edaplayground.com/) | Run and share small HDL/testbench examples in a browser; backend access varies by account. | ![stable][status-stable] |  |  |

### Open-source FPGA flow path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Yosys](https://github.com/YosysHQ/yosys) | Synthesize RTL into netlists for supported FPGA targets. | ![active][status-active] | 2026-10 | 4790 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Place and route Yosys netlists; select the backend for your FPGA family. | ![active][status-active] | 2026-10 | 1766 |
| [OSS CAD Suite](https://github.com/YosysHQ/oss-cad-suite-build) | Install prebuilt Yosys, nextpnr, formal, and simulation tools; packages vary by OS. | ![active][status-active] | 2026-10 | 1749 |
| [Project IceStorm](https://github.com/YosysHQ/icestorm) | Pack, unpack, and program supported Lattice iCE40 bitstreams. | ![active][status-active] | 2026-10 | 1189 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Use the Lattice ECP5 device database and bitstream tools with nextpnr. | ![active][status-active] | 2026-09 | 473 |
| [F4PGA](https://github.com/chipsalliance/f4pga) | Use configured open FPGA flows; check the project's supported devices and installation instructions. | ![stable][status-stable] | 2025-01 | 451 |

## Knowledge and tutorials

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [VHDLwhiz](https://vhdlwhiz.com/) | Learn VHDL through circuit examples and simulation exercises; some courses require payment. | ![active][status-active] | 2026-10 |  |
| [AMD UG903: Using Constraints](https://docs.amd.com/r/en-US/ug903-vivado-using-constraints) | Define clocks, I/O delays, and timing exceptions in Vivado XDC; match the guide to your tool version. | ![active][status-active] | 2026-07 |  |
| [AMD UG906: Design Analysis and Closure](https://docs.amd.com/r/en-US/ug906-vivado-design-analysis) | Interpret timing, utilization, and congestion reports and work toward Vivado timing closure. | ![active][status-active] | 2026-06 |  |
| [FPHD](https://github.com/lpacher/fphd) | Follow VHDL labs, Vivado exercises, and course notes on FPGA design. | ![active][status-active] | 2025-07 | 28 |
| [Tang Nano Project Series](https://learn.lushaylabs.com/) | Build UART, SPI, displays, and other projects on Gowin Tang Nano boards. | ![stable][status-stable] | 2024-03 |  |
| [ITSEmbedded](https://www.itsembedded.com/) | Build C++ Verilator testbenches and scripted simulation flows; examples use older tool versions. | ![stable][status-stable] | 2022-04 |  |
| [Beyond Circuits](https://www.beyond-circuits.com/wordpress/) | Study RAM inference, synthesis/simulation differences, and Verilog tutorials; tool examples are older. | ![stable][status-stable] | 2019-10 |  |
| [Adiuvo Engineering](https://www.adiuvoengineering.com/) | Read MicroZed Chronicles on Zynq, Vivado IP integration, and embedded FPGA systems. | ![stable][status-stable] |  |  |
| [FPGA Academy](https://fpgacademy.org/) | Use digital-logic labs and board-specific tutorials for teaching FPGA design. | ![stable][status-stable] |  |  |
| [FPGA4Student](https://fpga4student.com/) | Browse Verilog/VHDL circuit and testbench examples; check board and tool assumptions. | ![stable][status-stable] |  |  |
| [Numato Lab Knowledge Base](https://numato.com/kb/) | Find setup, programming, and peripheral examples for specific Numato boards. | ![stable][status-stable] |  |  |

## Books and evergreen references

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [*FPGA Prototyping by Verilog Examples*](https://onlinelibrary.wiley.com/doi/book/10.1002/9780470374283) by Pong P. Chu | Learn RTL through counters, FSMs, UART, and VGA projects; hardware examples target Spartan-3. | ![stable][status-stable] | 2008-06 |  |
| [*FPGA Prototyping by VHDL Examples*](https://www.wiley-vch.de/en/areas-interest/engineering/fpga-prototyping-by-vhdl-examples-978-0-470-18531-5) by Pong P. Chu | Work through VHDL circuit and peripheral exercises; this edition targets Spartan-3. | ![stable][status-stable] | 2008-03 |  |
| *100 Power Tips for FPGA Designers* by Evgeni Stavinov (ISBN 9781461186298) | Review design, timing, and build-script tips; older tool examples and an unavailable companion site. | ![stable][status-stable] |  |  |
| [*Verilog by Example*](https://www.readler.com/books2.html) by Blaine C. Readler (ISBN 9780983497301) | Learn Verilog syntax, FSMs, FPGA memories, and simulation through worked examples. | ![stable][status-stable] |  |  |

## Languages and HDL frameworks

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Chisel](https://github.com/chipsalliance/chisel) | Generate parameterized RTL from Scala hardware descriptions. | ![active][status-active] | 2026-10 | 4807 |
| [Veryl](https://github.com/veryl-lang/veryl) | Write typed HDL that compiles to SystemVerilog; language design is still exploratory. | ![active][status-active] | 2026-10 | 1042 |
| [Amaranth HDL](https://github.com/amaranth-lang/amaranth) | Describe, simulate, and build synchronous circuits in Python. | ![active][status-active] | 2026-09 | 2102 |
| [SpinalHDL](https://github.com/SpinalHDL/SpinalHDL) | Generate Verilog/VHDL from Scala and use bus, stream, and CDC libraries. | ![active][status-active] | 2026-09 | 2051 |
| [MyHDL](https://github.com/myhdl/myhdl) | Simulate Python hardware models and convert supported constructs to Verilog/VHDL. | ![active][status-active] | 2026-09 | 1131 |
| [PyMTL3](https://github.com/pymtl/pymtl3) | Model and simulate hardware in Python and translate RTL to Verilog; beta software. | ![active][status-active] | 2026-09 | 468 |
| [PyXHDL](https://github.com/davidel/pyxhdl) | Generate SystemVerilog or VHDL from Python circuit descriptions. | ![active][status-active] | 2026-05 | 31 |
| [FloPoCo](https://flopoco.org/) | Generate arithmetic operators in VHDL with chosen precision and target frequency. | ![stable][status-stable] |  |  |
| [Migen](https://github.com/m-labs/migen) | Maintain Python-generated RTL, including LiteX dependencies; archived GitHub mirror moved upstream to git.m-labs.hk. | ![legacy][status-legacy] | 2026-01 | 1330 |

## Simulation, verification, and debug

### Simulators

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Verilator](https://github.com/verilator/verilator) | Compile Verilog/SystemVerilog into C++/SystemC simulations and lint RTL; check supported constructs. | ![active][status-active] | 2026-10 | 3984 |
| [Icarus Verilog](https://github.com/steveicarus/iverilog) | Compile and run Verilog testbenches from the command line; SystemVerilog support is incomplete. | ![active][status-active] | 2026-10 | 3667 |
| [GHDL](https://github.com/ghdl/ghdl) | Analyze, elaborate, and simulate VHDL; synthesis support is experimental. | ![active][status-active] | 2026-10 | 2899 |
| [NVC](https://github.com/nickg/nvc) | Compile and simulate VHDL, especially VHDL-2008 testbenches. | ![active][status-active] | 2026-10 | 889 |
| [EDA Playground](https://www.edaplayground.com/) | Compare small HDL examples across simulators without a local installation; account restrictions apply. | ![stable][status-stable] |  |  |

### Verification, formal, and language tooling

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [cocotb](https://github.com/cocotb/cocotb) | Drive HDL simulations with Python tests; requires a supported simulator. | ![active][status-active] | 2026-10 | 2534 |
| [slang](https://github.com/MikePopoloski/slang) | Parse, type-check, and elaborate SystemVerilog; a compiler library, not a simulator. | ![active][status-active] | 2026-10 | 1155 |
| [VUnit](https://github.com/VUnit/vunit) | Automate HDL compilation, test discovery, parameterized runs, and CI reports. | ![active][status-active] | 2026-10 | 847 |
| [VHDL LS](https://github.com/VHDL-LS/rust_hdl) | Add VHDL diagnostics, completion, and navigation to an LSP-capable editor. | ![active][status-active] | 2026-10 | 513 |
| [Surelog/UHDM](https://github.com/chipsalliance/Surelog) | Preprocess, parse, and elaborate SystemVerilog into UHDM for downstream tools. | ![active][status-active] | 2026-10 | 475 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | Use VHDL coverage, constrained random stimulus, scoreboards, and interface models. | ![active][status-active] | 2026-10 | 88 |
| [Verible](https://github.com/chipsalliance/verible) | Format and lint SystemVerilog and integrate language tools into editors or CI. | ![active][status-active] | 2026-09 | 1950 |
| [svls](https://github.com/dalance/svls) | Add SystemVerilog diagnostics and completion to an editor through LSP. | ![active][status-active] | 2026-09 | 585 |
| [SymbiYosys / SBY](https://github.com/YosysHQ/sby) | Run bounded/unbounded property checks and cover statements using Yosys and solver backends. | ![active][status-active] | 2026-09 | 555 |
| [cocotbext-axi](https://github.com/alexforencich/cocotbext-axi) | Test AXI, AXI-Lite, AXI-Stream, and APB interfaces with cocotb bus models; not synthesizable IP. | ![active][status-active] | 2026-08 | 362 |
| [JSON-for-VHDL](https://github.com/Paebbels/JSON-for-VHDL) | Read and query JSON configuration files in VHDL testbenches using file I/O. | ![active][status-active] | 2026-07 | 87 |
| [sv-parser](https://github.com/dalance/sv-parser) | Build Rust tooling that parses SystemVerilog; not a simulator or synthesis frontend. | ![active][status-active] | 2026-06 | 482 |
| [UVVM](https://github.com/UVVM/UVVM) | Coordinate VHDL bus transactions with BFMs, sequencers, and verification components. | ![active][status-active] | 2026-04 | 465 |
| [svlint](https://github.com/dalance/svlint) | Check SystemVerilog against configurable coding rules from the command line. | ![active][status-active] | 2025-11 | 393 |

### Debug and diagrams

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [OpenOCD](https://github.com/openocd-org/openocd) | Access supported JTAG adapters and FPGA/SoC targets; requires target and adapter configuration. | ![active][status-active] | 2026-10 | 2345 |
| [GTKWave](https://github.com/gtkwave/gtkwave) | Inspect VCD/FST waveforms from simulations and compare signal timing. | ![active][status-active] | 2026-09 | 1030 |
| [WaveDrom](https://github.com/wavedrom/wavedrom) | Draw interface timing diagrams from text descriptions; not a waveform simulator. | ![active][status-active] | 2026-08 | 3502 |
| [FPGA Error Decoder](https://marketplace.visualstudio.com/items?itemName=fpgachat.fpga-error-decoder) | Turn EDA build logs into VS Code Problems and reports; does not run tools or validate timing closure. | ![active][status-active] | 2026-05 |  |
| [Sigrok / PulseView](https://github.com/sigrokproject/pulseview) | Capture board signals with supported logic analyzers and decode protocols. | ![active][status-active] | 2025-11 | 797 |
| [Surfer](https://surfer-project.org/) | Inspect simulation waveforms with a native or browser viewer; the browser version has fewer features. | ![stable][status-stable] |  |  |

## Synthesis, implementation, and programming

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Yosys](https://github.com/YosysHQ/yosys) | Synthesize RTL and map logic to supported FPGA primitives; language support depends on the frontend. | ![active][status-active] | 2026-10 | 4790 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Place and route supported iCE40, ECP5, Nexus, Gowin, and other devices; check backend coverage. | ![active][status-active] | 2026-10 | 1766 |
| [OSS CAD Suite](https://github.com/YosysHQ/oss-cad-suite-build) | Download a bundled Yosys/nextpnr/formal/simulation toolchain; check platform-specific contents. | ![active][status-active] | 2026-10 | 1749 |
| [openFPGALoader](https://github.com/trabucayre/openFPGALoader) | Load bitstreams into SRAM or flash on supported boards and adapters. | ![active][status-active] | 2026-10 | 1745 |
| [Verilog-to-Routing](https://github.com/verilog-to-routing/vtr-verilog-to-routing) | Evaluate FPGA architectures, packing, and routing algorithms; not a generic vendor-board bitstream flow. | ![active][status-active] | 2026-10 | 1274 |
| [Project IceStorm](https://github.com/YosysHQ/icestorm) | Pack and unpack supported Lattice iCE40 bitstreams and access the device database. | ![active][status-active] | 2026-10 | 1189 |
| [OpenFPGA](https://github.com/lnis-uofu/OpenFPGA) | Generate FPGA fabric RTL and evaluate custom architectures; not a programmer for off-the-shelf boards. | ![active][status-active] | 2026-10 | 1158 |
| [Apicula](https://github.com/YosysHQ/apicula) | Pack Gowin bitstreams and use device data with Yosys/nextpnr; only documented chips are supported. | ![active][status-active] | 2026-10 | 692 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Use the Lattice ECP5 bitstream database and tools with nextpnr. | ![active][status-active] | 2026-09 | 473 |
| [GHDL Yosys plugin](https://github.com/ghdl/ghdl-yosys-plugin) | Synthesize supported VHDL through GHDL into Yosys; experimental integration. | ![active][status-active] | 2026-09 | 370 |
| [Project Oxide](https://github.com/gatecat/prjoxide) | Use bitstream tools and device data for supported Lattice Nexus parts; coverage is incomplete. | ![active][status-active] | 2026-07 | 155 |
| [F4PGA](https://github.com/chipsalliance/f4pga) | Run open FPGA build flows for documented targets; device support is not vendor-wide. | ![stable][status-stable] | 2025-01 | 451 |

## Project workflow and productivity

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [SiliconCompiler](https://github.com/siliconcompiler/siliconcompiler) | Orchestrate tool runs and collect build metrics through Python-defined ASIC/FPGA flows. | ![active][status-active] | 2026-10 | 1224 |
| [Apio](https://github.com/FPGAwars/apio) | Install tool packages and build, simulate, or upload projects on supported FPGA boards. | ![active][status-active] | 2026-10 | 1012 |
| [FuseSoC](https://github.com/olofk/fusesoc) | Describe HDL cores, dependencies, and build targets in reusable core files. | ![active][status-active] | 2026-09 | 1469 |
| [Edalize](https://github.com/olofk/edalize) | Configure and invoke EDA tools through a shared Python build interface, including FuseSoC backends. | ![active][status-active] | 2026-09 | 802 |
| [RgGen](https://github.com/rggen/rggen) | Generate register RTL, UVM models, C headers, and documentation from a register specification. | ![active][status-active] | 2026-09 | 471 |
| [PeakRDL](https://github.com/SystemRDL/PeakRDL) | Generate CSR RTL, headers, docs, and UVM models from SystemRDL using exporter plugins. | ![active][status-active] | 2026-09 | 218 |
| [AccelFury/af](https://github.com/AccelFury/af) | Generate project manifests and FuseSoC/LiteX/IP-XACT wrappers; alpha CLI requiring external EDA tools. | ![active][status-active] | 2026-09 | 1 |
| [Icestudio](https://github.com/FPGAwars/icestudio) | Connect visual logic blocks and build designs for supported open-tool boards. | ![active][status-active] | 2026-08 | 1941 |
| [Corsair](https://github.com/esynr3z/corsair) | Generate register RTL, headers, and docs from JSON/YAML; upstream has frozen version 1.x. | ![legacy][status-legacy] | 2025-05 | 149 |
| [FPGAMAKE](https://github.com/cambridgehackers/fpgamake) | Generate Vivado Makefiles for older projects; check compatibility with your Vivado version. | ![legacy][status-legacy] | 2022-05 | 101 |

## Vendor tools

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Lattice Radiant](https://www.latticesemi.com/Products/DesignSoftwareAndIP/FPGAandLDS/Radiant) | Build supported Nexus, Avant, and iCE40 UltraPlus designs; check the device/license matrix. | ![active][status-active] | 2026-06 |  |
| [Lattice Diamond](https://www.latticesemi.com/Products/DesignSoftwareAndIP/FPGAandLDS/LatticeDiamond) | Build ECP5, MachXO2/3, and other listed families; free licenses exclude some devices. | ![stable][status-stable] | 2025-04 |  |
| [Altera Quartus Prime](https://www.altera.com/products/development-tools/quartus) | Build Altera FPGA designs; choose Pro, Standard, or Lite by device family and license requirements. | ![stable][status-stable] |  |  |
| [AMD Vivado](https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/vivado.html) | Synthesize, implement, and debug supported AMD FPGA/SoC designs; check device support and licensing. | ![stable][status-stable] |  |  |
| [Efinix Efinity](https://www.efinixinc.com/products-efinity.html) | Build Trion, Titanium, and Topaz designs; free license requests and downloads require registration. | ![stable][status-stable] |  |  |
| [Gowin EDA](https://www.gowinsemi.com/en/support/home/) | Download Gowin implementation tools and device documentation; check license and edition support. | ![stable][status-stable] |  |  |
| [Microchip Libero SoC](https://www.microchip.com/en-us/products/fpgas-and-plds/fpga-and-soc-design-tools/fpga-software-downloads) | Download Microchip implementation tools; match release and license to the target device. | ![stable][status-stable] |  |  |

## Boards and hardware ecosystems

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [PYNQ](https://github.com/Xilinx/PYNQ) | Control FPGA overlays from Python notebooks on supported Zynq-based boards. | ![active][status-active] | 2026-09 | 2365 |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Compare Lattice boards and their open-tool support; verify stock and exact FPGA part. | ![active][status-active] | 2026-09 | 363 |
| [RocketBoards](https://www.rocketboards.org/foswiki/Main/WebHome) | Find Altera SoC FPGA Linux, bootloader, and board bring-up documentation. | ![active][status-active] | 2025-08 |  |
| [Altera development kits](https://www.altera.com/products/development-kits) | Compare official Altera kits and their memory, transceiver, and expansion interfaces. | ![stable][status-stable] |  |  |
| [AMD evaluation boards](https://www.amd.com/en/products/adaptive-socs-and-fpgas/evaluation-boards.html) | Compare official boards by FPGA/SoC, memory, connectors, and included tools. | ![stable][status-stable] |  |  |
| [Digilent FPGA boards](https://digilent.com/shop/fpga-development-boards-kits-from-digilent/) | Compare education/prototyping boards and find board manuals and peripheral options. | ![stable][status-stable] |  |  |
| [FPGA Board Repository](https://boards.fpgadeveloper.com/) | Filter boards by device and hardware features; confirm specifications with the manufacturer. | ![stable][status-stable] |  |  |
| [Lattice evaluation boards](https://www.latticesemi.com/Products/DevelopmentBoardsAndKits) | Find official Lattice kits, schematics, user guides, and reference designs. | ![stable][status-stable] |  |  |
| [Terasic FPGA boards](https://www.terasic.com.tw/en/index.html) | Find Altera-based boards, manuals, and demos; HTTPS certificate verification failed in the automated check. | ![unknown][status-unknown] |  |  |
| [Second Life for FPGA boards](https://github.com/iDoka/awesome-fpga-boards) | Identify surplus boards and reverse-engineering notes; programming access and schematics vary. | ![legacy][status-legacy] | 2021-01 | 105 |

## Reusable IP and reference designs

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [NEORV32](https://github.com/stnolting/neorv32) | Integrate a configurable VHDL RISC-V MCU-style SoC with peripherals and software examples. | ![active][status-active] | 2026-10 | 2284 |
| [Analog Devices HDL](https://github.com/analogdevicesinc/hdl) | Integrate ADI converter/transceiver IP and reference designs; match release to board and tool version. | ![active][status-active] | 2026-10 | 2022 |
| [LiteX](https://github.com/enjoy-digital/litex) | Assemble FPGA SoCs with soft CPUs, buses, memory, and peripherals; requires Migen and external tools. | ![active][status-active] | 2026-09 | 4147 |
| [VexRiscv](https://github.com/SpinalHDL/VexRiscv) | Generate a plugin-configured RISC-V CPU from SpinalHDL with optional caches and MMU. | ![active][status-active] | 2026-09 | 3281 |
| [ZipCPU](https://github.com/ZipCPU/zipcpu) | Integrate a Wishbone-connected soft CPU with its own ISA, not RISC-V; GPLv3. | ![active][status-active] | 2026-09 | 1589 |
| [LitePCIe](https://github.com/enjoy-digital/litepcie) | Add PCIe endpoints, DMA, and host access to LiteX systems on supported FPGA hard blocks. | ![active][status-active] | 2026-09 | 732 |
| [LiteDRAM](https://github.com/enjoy-digital/litedram) | Add SDR/DDR controllers to LiteX or generate Verilog; check supported PHY, FPGA, and memory combinations. | ![active][status-active] | 2026-09 | 557 |
| [SERV](https://github.com/olofk/serv) | Use a bit-serial RISC-V CPU when area matters more than throughput. | ![active][status-active] | 2026-08 | 1898 |
| [Taxi](https://github.com/fpganinja/taxi) | Reuse SystemVerilog AXI/APB, Ethernet, and PCIe components; under development, CERN-OHL-S-2.0 or commercial license. | ![active][status-active] | 2026-08 | 962 |
| [Digilent Vivado Library](https://github.com/Digilent/vivado-library) | Reuse Digilent peripheral IP and bus interface definitions in Vivado projects. | ![active][status-active] | 2025-12 | 703 |
| [Corundum](https://github.com/corundum/corundum) | Build a 10/25/100G FPGA NIC with PCIe DMA and a Linux driver on supported boards. | ![stable][status-stable] | 2024-07 | 2484 |
| [verilog-pcie](https://github.com/alexforencich/verilog-pcie) | Use PCIe-to-AXI/AXI-Lite bridges and DMA with supported FPGA PCIe hard interfaces. | ![stable][status-stable] | 2024-04 | 1666 |
| [OpenCores](https://opencores.org/) | Find community IP; check each core's license, verification, and maintenance before reuse. | ![stable][status-stable] |  |  |
| [verilog-ethernet](https://github.com/alexforencich/verilog-ethernet) | Maintain existing Ethernet designs; upstream directs new development to Taxi and promises no further fixes here. | ![legacy][status-legacy] | 2025-02 | 3114 |

## Communities and source lists

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Find Lattice boards, device notes, and open-tool links. | ![active][status-active] | 2026-09 | 363 |
| [drom/awesome-hdl](https://github.com/drom/awesome-hdl) | Compare HDL languages, compilers, and simulation tools. | ![active][status-active] | 2026-07 | 1177 |
| [aolofsson/awesome-opensource-hardware](https://github.com/aolofsson/awesome-opensource-hardware) | Find open EDA tools and hardware designs; includes substantial non-FPGA material. | ![active][status-active] | 2026-03 | 2437 |
| [ben-marshall/awesome-open-hardware-verification](https://github.com/ben-marshall/awesome-open-hardware-verification) | Find testbench, simulator, and formal-verification projects for open hardware. | ![active][status-active] | 2026-01 | 628 |
| [FPGA-Systems/fpga-awesome-list](https://github.com/FPGA-Systems/fpga-awesome-list) | Consult the original broad FPGA list; check linked projects individually. | ![active][status-active] | 2025-10 | 185 |
| [coderonion/awesome-fpga](https://github.com/coderonion/awesome-fpga) | Find FPGA/HDL projects and other lists; verify maintenance and remove duplicates before reuse. | ![stable][status-stable] | 2024-07 | 6 |
| [Electronics Stack Exchange: FPGA](https://electronics.stackexchange.com/questions/tagged/fpga) | Ask about digital logic, timing, board interfaces, and electrical design. | ![stable][status-stable] |  |  |
| [Reddit r/FPGA](https://www.reddit.com/r/FPGA/) | Discuss boards, projects, tool problems, and FPGA engineering work. | ![stable][status-stable] |  |  |
| [Stack Overflow: FPGA](https://stackoverflow.com/questions/tagged/fpga) | Ask focused HDL, scripting, and FPGA software-tool questions. | ![stable][status-stable] |  |  |
| [hdl/awesome](https://github.com/hdl/awesome) | Browse HDL/EDA references; the maintainer explicitly reports no active maintenance. | ![legacy][status-legacy] | 2026-10 | 178 |
| [open-source-fpga-resource](https://github.com/os-fpga/open-source-fpga-resource) | Find older OSFPGA links to tools, cores, and educational projects. | ![legacy][status-legacy] | 2022-11 | 466 |
| [awesome-fpga-programming](https://github.com/emanueledelsozzo/awesome-fpga-programming) | Compare older FPGA programming languages, DSLs, and HLS projects. | ![legacy][status-legacy] | 2022-06 | 76 |
| [VHDL/awesome-vhdl](https://github.com/VHDL/awesome-vhdl) | Find VHDL libraries and tools in an archived index; follow links to current upstreams. | ![legacy][status-legacy] | 2020-02 | 85 |
| [Vitorian awesome-fpga](https://github.com/Vitorian/awesome-fpga) | Find older tutorials and build tools; many links need rechecking. | ![legacy][status-legacy] | 2017-05 | 400 |

## FPGA vendors

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Achronix](https://www.achronix.com/) | Find Speedster FPGA specifications, ACE tools, and accelerator-board documentation. | ![stable][status-stable] |  |  |
| [Altera](https://www.altera.com/fpga) | Compare Agilex, Stratix, Arria, Cyclone, and MAX families and their tool requirements. | ![stable][status-stable] |  |  |
| [AMD](https://www.amd.com/en/products/adaptive-socs-and-fpgas.html) | Compare FPGA/adaptive SoC families and find device documentation and tool support. | ![stable][status-stable] |  |  |
| [Anlogic](https://www.anlogic.com/) | Find device data and Tang Dynasty tool information; much of the site is in Chinese. | ![stable][status-stable] |  |  |
| [Cologne Chip](https://www.colognechip.com/) | Find GateMate device data, development boards, and toolchain information. | ![stable][status-stable] |  |  |
| [Efinix](https://www.efinixinc.com/index.html) | Compare Trion, Titanium, and Topaz devices and find Efinity and board documentation. | ![stable][status-stable] |  |  |
| [Gowin Semiconductor](https://www.gowinsemi.com/en/) | Find Gowin device data, EDA downloads, and supported peripheral IP. | ![stable][status-stable] |  |  |
| [Lattice Semiconductor](https://www.latticesemi.com/) | Compare Lattice families and find device data, Diamond/Radiant support, and reference designs. | ![stable][status-stable] |  |  |
| [Microchip FPGA](https://www.microchip.com/en-us/products/fpgas-and-plds) | Find PolarFire/PolarFire SoC, RTG4, SmartFusion, and IGLOO device and tool documentation. | ![stable][status-stable] |  |  |
| [NanoXplore](https://nanoxplore.com/) | Find radiation-hardened FPGA families, development boards, and design-tool information. | ![stable][status-stable] |  |  |
| [QuickLogic](https://www.quicklogic.com/) | Find low-power programmable devices, evaluation kits, and open-tool support information. | ![stable][status-stable] |  |  |

## eFPGA vendors

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Achronix Speedcore](https://www.achronix.com/product/speedcore) | Evaluate configurable logic, DSP, and RAM fabrics for integration into an ASIC or SoC. | ![stable][status-stable] |  |  |
| [AdicSys](https://www.adicsys.com/) | Evaluate customizable embedded FPGA soft IP and its ASIC integration requirements. | ![stable][status-stable] |  |  |
| [Menta](https://www.menta-efpga.com/) | Evaluate embedded FPGA IP and the associated implementation tools for an ASIC design. | ![stable][status-stable] |  |  |
| [QuickLogic eFPGA IP](https://www.quicklogic.com/efpga-ip/) | Evaluate process-specific embedded FPGA IP and its design tools; not board-level FPGA hardware. | ![stable][status-stable] |  |  |

## Source audit

`use_as_seed` means inspect linked candidates, not import the list. `manual_review` means filter for a specific task. `monitor_only` means retain the audit record without using it as a current source. Search indexes appear here only, not among recommended resources. Some vendor and community sites restrict automated access; a blocked request alone is not evidence that a resource is dead.

| Source | Use it for | Action | Status | Activity | Stars |
| --- | --- | --- | --- | --- | --- |
| [kitspace/awesome-electronics](https://github.com/kitspace/awesome-electronics) | General electronics; retain only links needed for FPGA board work. | monitor_only | ![active][status-active] | 2026-09 | 8190 |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Lattice boards and open tools; verify each board's exact device and availability. | use_as_seed | ![active][status-active] | 2026-09 | 363 |
| [FPGA Tutorial: SystemVerilog loops](https://www.fpgatutorial.com/systemverilog-loops/) | Contains examples to review: the stated 10 MHz clock uses a 500 ns half-period, which produces 1 MHz. | manual_review | ![active][status-active] | 2026-09 |  |
| [Awesome-EDA](https://github.com/ishandutta2007/Awesome-EDA) | Mixed PCB/ASIC/FPGA tools; check that each candidate can handle RTL or FPGA builds. | manual_review | ![active][status-active] | 2026-08 | 11 |
| [drom/awesome-hdl](https://github.com/drom/awesome-hdl) | HDL languages and tools; check compiler outputs and supported targets. | use_as_seed | ![active][status-active] | 2026-07 | 1177 |
| [awesome-formal-verification](https://github.com/ElNiak/awesome-formal-verification) | Software/hardware formal methods; inspect only hardware-relevant tool links. | monitor_only | ![active][status-active] | 2026-06 | 186 |
| [FPGA-ASIC-Roadmap](https://github.com/m3y54m/FPGA-ASIC-Roadmap) | Study sequence; select FPGA exercises rather than importing the ASIC syllabus. | manual_review | ![active][status-active] | 2026-05 | 703 |
| [suryakantamangaraj/awesome-riscv](https://github.com/suryakantamangaraj/awesome-riscv) | RISC-V cores and SoCs; select implementations with FPGA build instructions. | manual_review | ![active][status-active] | 2026-04 | 391 |
| [RDSik/FPGA-Awesome-list](https://github.com/RDSik/FPGA-Awesome-list) | Russian/English material; select resources usable without regional social accounts. | manual_review | ![active][status-active] | 2026-04 | 11 |
| [aolofsson/awesome-opensource-hardware](https://github.com/aolofsson/awesome-opensource-hardware) | Open EDA and hardware designs; filter out PCB-only and ASIC-only tools. | use_as_seed | ![active][status-active] | 2026-03 | 2437 |
| [ben-marshall/awesome-open-hardware-verification](https://github.com/ben-marshall/awesome-open-hardware-verification) | Simulation, testbenches, and formal tools; check simulator and language compatibility. | use_as_seed | ![active][status-active] | 2026-01 | 628 |
| [FPGA-Systems/fpga-awesome-list](https://github.com/FPGA-Systems/fpga-awesome-list) | Original FPGA list; remove dead links, duplicates, and contact-only entries. | use_as_seed | ![active][status-active] | 2025-10 | 185 |
| [C8Costa/Edge-Ai-Resources](https://github.com/C8Costa/Edge-Ai-Resources) | Edge AI; FPGA-specific build and deployment information is secondary. | monitor_only | ![active][status-active] | 2025-08 | 2 |
| [lpacher/fphd](https://github.com/lpacher/fphd) | VHDL/Vivado course; select labs matching the reader's board and tool version. | manual_review | ![active][status-active] | 2025-07 | 28 |
| [TM90/awesome-hwd-tools](https://github.com/TM90/awesome-hwd-tools) | Hardware-design tools; deduplicate against the language and verification lists. | monitor_only | ![active][status-active] | 2025-06 | 91 |
| [coderonion/awesome-fpga](https://github.com/coderonion/awesome-fpga) | Broad FPGA links; check upstream maintenance, language, and duplicate entries. | manual_review | ![stable][status-stable] | 2024-07 | 6 |
| [suryavanshi/awesome-hardware](https://github.com/suryavanshi/awesome-hardware) | General hardware; no automatic transfer into the FPGA list. | monitor_only | ![stable][status-stable] | 2024-06 | 2 |
| [awesome.ecosyste.ms FPGA topic](https://awesome.ecosyste.ms/lists?topic=fpga) | Discovery index; returned HTTP 402 during this check, so no candidates were imported. | monitor_only | ![unknown][status-unknown] |  |  |
| [AwesomeOpenSource: sjinzh awesome-fpga-list](https://awesomeopensource.com/project/sjinzh/awesome-fpga-list) | Mirror whose GitHub slug now redirects to coderonion/awesome-cuda-and-hpc; exclude as an FPGA source. | monitor_only | ![unknown][status-unknown] |  |  |
| [fpga.chat](https://fpga.chat/) | Now an EDA log-analysis product, not the discussion community previously listed. | monitor_only | ![unknown][status-unknown] |  |  |
| [Terasic catalog](https://www.terasic.com.tw/en/index.html) | Canonical catalog found, but automated HTTPS verification fails; the old .com.cn archive URL serves an error page. | manual_review | ![unknown][status-unknown] |  |  |
| [hdl/awesome](https://github.com/hdl/awesome) | HDL/EDA index; upstream says it is not actively maintained despite recent pushes. | manual_review | ![legacy][status-legacy] | 2026-10 | 178 |
| [awesome-opensource-asic-resources](https://github.com/mattvenn/awesome-opensource-asic-resources) | Older ASIC index; inspect only shared RTL/EDA tooling. | monitor_only | ![legacy][status-legacy] | 2023-04 | 414 |
| [drom/awesome-riscv](https://github.com/drom/awesome-riscv) | Older CPU index; confirm FPGA implementations at their upstream repositories. | monitor_only | ![legacy][status-legacy] | 2023-03 | 149 |
| [open-source-fpga-resource](https://github.com/os-fpga/open-source-fpga-resource) | Older OSFPGA index; recheck tools, cores, and tutorials individually. | manual_review | ![legacy][status-legacy] | 2022-11 | 466 |
| [Hands-on-FPGA-class](https://github.com/tinyvision-ai-inc/Hands-on-FPGA-class) | Older board-based class; select exercises with usable hardware/tool instructions. | manual_review | ![legacy][status-legacy] | 2022-09 | 57 |
| [awesome-fpga-programming](https://github.com/emanueledelsozzo/awesome-fpga-programming) | Older languages/DSLs/HLS index; check whether each compiler still builds. | manual_review | ![legacy][status-legacy] | 2022-06 | 76 |
| [awesome-digital-ic](https://github.com/qninth/awesome-digital-ic) | Broad digital-IC links and topic searches; not used to import FPGA entries. | monitor_only | ![legacy][status-legacy] | 2022-05 | 172 |
| [awesome-hardware-tools](https://github.com/jpc-lip6/awesome-hardware-tools) | Older open-hardware tool index; check projects individually rather than trusting list activity. | manual_review | ![legacy][status-legacy] | 2022-04 | 0 |
| [awesome-dv](https://github.com/troyguo/awesome-dv) | ASIC verification index; inspect only testbench/formal tools applicable to FPGA RTL. | monitor_only | ![legacy][status-legacy] | 2022-02 | 368 |
| [Awesome-FPGA-ASIC-RISC-V](https://github.com/TouchSky-Lab/Awesome-FPGA-ASIC-RISC-V) | Older FPGA/ASIC/RISC-V papers; not a source of tested build flows. | monitor_only | ![legacy][status-legacy] | 2022-02 | 6 |
| [awesome-fpga-boards](https://github.com/iDoka/awesome-fpga-boards) | Surplus boards; confirm schematics, programming access, and device identity. | manual_review | ![legacy][status-legacy] | 2021-01 | 105 |
| [VHDL/awesome-vhdl](https://github.com/VHDL/awesome-vhdl) | Archived VHDL index; follow library links to current upstreams. | manual_review | ![legacy][status-legacy] | 2020-02 | 85 |
| [clin99/awesome-eda](https://github.com/clin99/awesome-eda) | Year-indexed EDA history; not an actively curated project source. | monitor_only | ![legacy][status-legacy] | 2019-06 | 103 |
| [Vitorian/awesome-fpga](https://github.com/Vitorian/awesome-fpga) | Older FPGA tutorials and tools; retain only still-readable references and usable legacy flows. | manual_review | ![legacy][status-legacy] | 2017-05 | 400 |
| [hdl/awesome tools category](https://hdl.github.io/awesome/categories/tools/) | Generated duplicate of an unmaintained index; prefer canonical project repositories. | monitor_only | ![legacy][status-legacy] |  |  |

## Contributing

For an addition or update:

- Explain the FPGA task and any device, license, or experimental limitation.
- Link to a public primary source and check its content, not just its HTTP status.
- Use the existing table columns and status badges.
- Read upstream maintenance/deprecation notices before assigning a status.
- Use GitHub `pushed_at` for repository activity and the source's own date elsewhere; leave unknown dates blank.
- Fill `Stars` only for specific GitHub repositories and sort by status, activity, stars, then name.
- Keep repeated entries consistent; repeat only for a distinct task or the source audit, not as duplicate landing pages within a section.

Avoid adding generic search pages, duplicate vendor landing pages, personal links without reusable technical value, and resources that only make sense for one private/internal workflow.

## License

MIT

[status-active]: https://img.shields.io/badge/-active-brightgreen
[status-stable]: https://img.shields.io/badge/-stable-blue
[status-legacy]: https://img.shields.io/badge/-legacy-orange
[status-unknown]: https://img.shields.io/badge/-unknown-lightgrey
