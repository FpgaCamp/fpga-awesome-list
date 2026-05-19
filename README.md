# Awesome FPGA

A curated, practical list of FPGA resources for engineers, students, and teams building real FPGA projects.

This list is optimized for application value: learning, RTL design, verification, toolchains, boards, reusable IP, communities, and vendors. It is intentionally selective; generic search links, unclear mirrors, abandoned stubs, and vendor names without useful public FPGA entry points are kept out.

## Contents

- [Start here](#start-here)
- [Activity legend](#activity-legend)
- [Curation rules](#curation-rules)
- [Learning paths](#learning-paths)
- [Knowledge and tutorials](#knowledge-and-tutorials)
- [Books and evergreen references](#books-and-evergreen-references)
- [Languages and HDL frameworks](#languages-and-hdl-frameworks)
- [Simulation, verification, and debug](#simulation-verification-and-debug)
- [Synthesis and implementation](#synthesis-and-implementation)
- [Project workflow and productivity](#project-workflow-and-productivity)
- [Vendor tools](#vendor-tools)
- [Boards and hardware ecosystems](#boards-and-hardware-ecosystems)
- [Reusable IP and reference designs](#reusable-ip-and-reference-designs)
- [Communities and source lists](#communities-and-source-lists)
- [FPGA vendors](#fpga-vendors)
- [eFPGA vendors](#efpga-vendors)
- [Contributing](#contributing)
- [License](#license)

## Start here

| Goal | Practical path |
| --- | --- |
| Learn FPGA basics | HDLBits, Nandland, Project F, fpga4fun, SparkFun |
| Write better RTL | 01signal, ZipCPU, Sunburst Design, ASIC-World, ChipVerify |
| Build verification habits | EDA Playground, cocotb, VUnit, OSVVM, GTKWave |
| Try open-source FPGA flow | Yosys, nextpnr, Project IceStorm, prjtrellis, F4PGA |
| Manage project workflow | FuseSoC, Edalize, RgGen, Verible, FPGA Error Decoder |
| Choose a board or vendor | Board catalogs first, then vendor tools and device pages |

## Activity legend

| Status | Meaning |
| --- | --- |
| ![active][status-active] | Public project activity or source update within the last 18 months. |
| ![stable][status-stable] | Evergreen, authoritative, or vendor-maintained resource with no better public activity signal. |
| ![legacy][status-legacy] | Useful for older flows, old devices, or historical context; not a first choice for new projects. |
| ![unknown][status-unknown] | Reachable and relevant, but public update activity is not clear. |

For GitHub resources, the activity month is the latest observed push month where available. For regular websites, vendor pages, books, and tutorials without public version metadata, the activity month is the last manual check: `2026-05`.

## Curation rules

- Prefer resources that help a reader do something concrete: simulate, synthesize, debug, select hardware, structure a project, or understand a design tradeoff.
- Prefer official documentation, active projects, and examples that can be reproduced.
- Avoid generic YouTube/search pages, personal contact noise, unsourced vendor names, duplicate landing pages, and entries with unclear FPGA relevance.
- Keep descriptions short and decision-oriented.

## Learning paths

### Beginner path

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) | Hands-on Verilog exercises for syntax, FSMs, timing, and small blocks. | ![stable][status-stable] | 2026-05 |
| [Nandland](https://www.youtube.com/@nandland) | Beginner-friendly HDL and FPGA videos. | ![stable][status-stable] | 2026-05 |
| [Project F](https://projectf.io/) | Concise FPGA tutorials with graphics, timing, and small examples. | ![stable][status-stable] | 2026-05 |
| [fpga4fun](https://www.fpga4fun.com/) | Small projects for first board experiments. | ![stable][status-stable] | 2026-05 |
| [FPGA Tutorial](https://www.fpgatutorial.com/) | Structured HDL and FPGA fundamentals. | ![stable][status-stable] | 2026-05 |
| [SparkFun FPGA guide](https://www.sparkfun.com/fpga) | Beginner-oriented FPGA tradeoffs and first steps. | ![stable][status-stable] | 2026-05 |

### RTL design path

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [01signal](https://www.01signal.com/) | Timing, CDC, resets, constraints, and design pitfalls. | ![stable][status-stable] | 2026-05 |
| [ZipCPU](https://zipcpu.com/) | Deep RTL, formal methods, buses, and CPU-oriented FPGA projects. | ![active][status-active] | 2025-12 |
| [Sunburst Design](http://www.sunburst-design.com/) | Classic Verilog/SystemVerilog papers and methodology material. | ![stable][status-stable] | 2026-05 |
| [ASIC-World](https://www.asic-world.com/) | Verilog and SystemVerilog reference material. | ![stable][status-stable] | 2026-05 |
| [ChipVerify](https://www.chipverify.com/) | Verilog, SystemVerilog, and verification examples. | ![stable][status-stable] | 2026-05 |
| [Bruno Levy learn-fpga](https://github.com/BrunoLevy/learn-fpga) | Low-cost FPGA, Yosys, nextpnr, and RISC-V learning. | ![active][status-active] | 2025-11 |

### Verification path

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [EDA Playground](https://www.edaplayground.com/) | Browser-based HDL simulation and quick testbench experiments. | ![stable][status-stable] | 2026-05 |
| [cocotb](https://docs.cocotb.org/) | Python-based cosimulation for HDL verification. | ![active][status-active] | 2026-05 |
| [VUnit](https://github.com/VUnit/vunit) | VHDL/SystemVerilog test automation. | ![active][status-active] | 2026-05 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | VHDL methodology and reusable verification libraries. | ![active][status-active] | 2026-05 |
| [UVVM](https://github.com/UVVM/UVVM) | VHDL BFMs and structured testbench patterns. | ![active][status-active] | 2026-04 |
| [GTKWave](http://gtkwave.sourceforge.net/) | Waveform viewing for day-to-day simulation debug. | ![active][status-active] | 2026-04 |

### Open-source FPGA flow path

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Yosys](https://yosyshq.net/yosys/) | Open-source HDL synthesis. | ![stable][status-stable] | 2026-05 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Open-source place-and-route for supported FPGA families. | ![active][status-active] | 2026-05 |
| [Project IceStorm](http://www.clifford.at/icestorm/) | Open toolchain resources for Lattice iCE40. | ![stable][status-stable] | 2026-05 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Lattice ECP5 bitstream and flow support. | ![active][status-active] | 2026-05 |
| [F4PGA](https://f4pga.org/) | Open FPGA flow umbrella, formerly SymbiFlow. | ![active][status-active] | 2025-01 |

## Knowledge and tutorials

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [VHDLwhiz](https://vhdlwhiz.com/) | VHDL-focused tutorials and courses. | ![stable][status-stable] | 2026-05 |
| [Beyond Circuits](https://www.beyond-circuits.com/) | FPGA and digital design articles. | ![stable][status-stable] | 2026-05 |
| [Adiuvo Engineering](https://www.adiuvoengineering.com/) | MicroZed Chronicles and FPGA/SoC engineering articles. | ![stable][status-stable] | 2026-05 |
| [ITSEmbedded](https://www.itsembedded.com/) | Practical RTL, Verilator, and scripted simulation workflows. | ![stable][status-stable] | 2026-05 |
| [FPGA4Student](https://fpga4student.com/) | FPGA projects and HDL examples. | ![stable][status-stable] | 2026-05 |
| [Numato Lab Knowledge Base](https://numato.com/kb/) | Board-oriented tutorials and examples. | ![stable][status-stable] | 2026-05 |
| [FPGA Academy](https://fpgacademy.org/) | Educational FPGA material and labs. | ![stable][status-stable] | 2026-05 |
| [Tang Nano Project Series](https://learn.lushaylabs.com/) | Practical Gowin/Tang Nano learning path. | ![stable][status-stable] | 2026-05 |
| [SparkFun "So You Want to Learn FPGAs"](https://news.sparkfun.com/1203) | Older but useful discussion of the FPGA learning curve. | ![legacy][status-legacy] | 2013-08 |

## Books and evergreen references

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| *FPGA Prototyping by Verilog Examples* by Pong P. Chu | Practical Verilog projects for FPGA learning. | ![stable][status-stable] | 2026-05 |
| *FPGA Prototyping by VHDL Examples* by Pong P. Chu | Practical VHDL projects for FPGA learning. | ![stable][status-stable] | 2026-05 |
| *Verilog by Example* by Blaine C. Readler | Compact Verilog primer with FPGA-oriented examples. | ![stable][status-stable] | 2026-05 |
| *100 Power Tips for FPGA Designers* by Evgeni Stavinov | Practical FPGA design tips, scripts, and gotchas. | ![stable][status-stable] | 2026-05 |

## Languages and HDL frameworks

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Verilog/SystemVerilog resources](https://www.chipverify.com/) | Practical language examples and verification explanations. | ![stable][status-stable] | 2026-05 |
| [VHDL resources](https://vhdlwhiz.com/) | Practical VHDL tutorials and design patterns. | ![stable][status-stable] | 2026-05 |
| [Chisel](https://www.chisel-lang.org/) | Scala-embedded hardware construction language. | ![active][status-active] | 2026-05 |
| [SpinalHDL](https://spinalhdl.github.io/SpinalDoc-RTD/) | Scala-based hardware description language. | ![active][status-active] | 2026-05 |
| [Amaranth HDL](https://amaranth-lang.org/) | Python-based HDL for FPGA and ASIC-oriented design. | ![active][status-active] | 2026-04 |
| [PyMTL3](https://github.com/pymtl/pymtl3) | Python hardware generation, simulation, and verification. | ![active][status-active] | 2026-04 |
| [PyXHDL](https://github.com/davidel/pyxhdl) | Python frontend that generates SystemVerilog and VHDL. | ![active][status-active] | 2026-02 |
| [FloPoCo](https://flopoco.org/) | Fixed- and floating-point arithmetic core generation. | ![stable][status-stable] | 2026-05 |
| [JSON-for-VHDL](https://github.com/Paebbels/JSON-for-VHDL) | Synthesizable VHDL package for JSON parsing and generics. | ![stable][status-stable] | 2023-07 |

## Simulation, verification, and debug

### Simulators

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Icarus Verilog](https://github.com/steveicarus/iverilog) | Free Verilog simulator for quick command-line flows. | ![active][status-active] | 2026-05 |
| [Verilator](https://verilator.org/) | High-performance SystemVerilog simulation and linting. | ![active][status-active] | 2026-05 |
| [GHDL](https://ghdl.github.io/ghdl/) | Open-source VHDL analysis, compilation, simulation, and synthesis experiments. | ![active][status-active] | 2026-05 |
| [NVC](https://github.com/nickg/nvc) | VHDL compilation and simulation. | ![active][status-active] | 2026-05 |
| [EDA Playground](https://www.edaplayground.com/) | Online HDL simulation across multiple backends. | ![stable][status-stable] | 2026-05 |

### Verification frameworks and linting

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [cocotb](https://docs.cocotb.org/) | Python testbenches for HDL designs. | ![active][status-active] | 2026-05 |
| [VUnit](https://github.com/VUnit/vunit) | Automated VHDL/SystemVerilog test running. | ![active][status-active] | 2026-05 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | VHDL verification, coverage, randomization, and utility libraries. | ![active][status-active] | 2026-05 |
| [UVVM](https://github.com/UVVM/UVVM) | VHDL verification components and structured tests. | ![active][status-active] | 2026-04 |
| [Verible](https://chipsalliance.github.io/verible/) | SystemVerilog formatting, linting, parsing, and language tooling. | ![active][status-active] | 2026-03 |
| [slang](https://github.com/MikePopoloski/slang) | SystemVerilog compiler and language services toolkit. | ![active][status-active] | 2026-05 |
| [Surelog/UHDM](https://github.com/chipsalliance/Surelog) | SystemVerilog parsing and UHDM frontend ecosystem. | ![active][status-active] | 2026-05 |

### Debug and diagrams

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [GTKWave](http://gtkwave.sourceforge.net/) | VCD/FST waveform viewing. | ![active][status-active] | 2026-04 |
| [WaveDrom](https://wavedrom.com/) | Timing diagrams for documentation and interface reviews. | ![stable][status-stable] | 2026-05 |
| [OpenOCD](https://openocd.org/) | JTAG access and board debug workflows. | ![active][status-active] | 2026-05 |
| [Sigrok / PulseView](https://sigrok.org/wiki/Main_Page) | Logic analyzer and signal capture tooling. | ![active][status-active] | 2025-11 |
| [FPGA Error Decoder](https://marketplace.visualstudio.com/items?itemName=fpgachat.fpga-error-decoder) | VS Code extension for FPGA build error triage. | ![stable][status-stable] | 2026-05 |

## Synthesis and implementation

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Yosys](https://yosyshq.net/yosys/) | Synthesis framework used by many open FPGA flows. | ![stable][status-stable] | 2026-05 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Place-and-route for iCE40, ECP5, Nexus, Gowin, and other targets. | ![active][status-active] | 2026-05 |
| [F4PGA](https://f4pga.org/) | Open FPGA flow umbrella for supported vendor families. | ![active][status-active] | 2025-01 |
| [Project IceStorm](http://www.clifford.at/icestorm/) | Reverse-engineered iCE40 bitstream tools. | ![stable][status-stable] | 2026-05 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Open ECP5/XP2 tooling. | ![active][status-active] | 2026-05 |
| [Verilog-to-Routing](https://verilogtorouting.org/) | Academic FPGA CAD flow and research platform. | ![active][status-active] | 2026-04 |
| [VPR](https://docs.verilogtorouting.org/en/latest/vpr/) | Packing, placement, and routing in the VTR flow. | ![active][status-active] | 2026-04 |
| [GHDL Yosys plugin](https://github.com/ghdl/ghdl-yosys-plugin) | VHDL frontend integration for Yosys. | ![active][status-active] | 2026-05 |

## Project workflow and productivity

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [FuseSoC](https://github.com/olofk/fusesoc) | Package management and builds for reusable HDL projects. | ![active][status-active] | 2026-05 |
| [Edalize](https://github.com/olofk/edalize) | Backend abstraction for EDA tools and FuseSoC flows. | ![active][status-active] | 2026-04 |
| [RgGen](https://github.com/rggen/rggen) | Register map generation for RTL, UVM RAL, headers, and docs. | ![active][status-active] | 2026-04 |
| [Corsair](https://github.com/esynr3z/corsair) | Register map and RTL/header generation. | ![active][status-active] | 2025-05 |
| [DigitalJS](https://digitaljs.tilk.eu/) | Digital logic simulation and Yosys netlist visualization. | ![stable][status-stable] | 2026-05 |
| [HDLmake](https://hdl.github.io/awesome/items/hdlmake/) | Makefile/dependency workflow for legacy HDL projects. | ![legacy][status-legacy] | 2026-04 |
| [FPGAMAKE](https://github.com/cambridgehackers/fpgamake) | Vivado Makefile generation from the older Vitorian list. | ![legacy][status-legacy] | 2022-05 |
| [AccelFury](https://accelfury.com/) | FPGA acceleration workflow and tooling ecosystem. | ![stable][status-stable] | 2026-05 |
| [AccelFury/af](https://github.com/AccelFury/af) | Open repository for the AccelFury toolchain. | ![active][status-active] | 2026-05 |

## Vendor tools

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [AMD Vivado](https://www.xilinx.com/products/design-tools/vivado.html) | Primary AMD/Xilinx FPGA design suite. | ![stable][status-stable] | 2026-05 |
| [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html) | Intel FPGA design suite. | ![stable][status-stable] | 2026-05 |
| [Lattice Radiant](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/RadiantSoftwareSuite) | Lattice design suite for newer device families. | ![stable][status-stable] | 2026-05 |
| [Lattice Diamond](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/DIAMOND) | Lattice design suite for older families. | ![stable][status-stable] | 2026-05 |
| [Microchip Libero SoC](https://www.microchip.com/en-us/design-centers-and-tools/soc-design-support) | Microchip/Microsemi FPGA design environment. | ![stable][status-stable] | 2026-05 |
| [Efinix Efinity](https://www.efinixinc.com/support/) | Efinix FPGA design software. | ![stable][status-stable] | 2026-05 |
| [Gowin EDA](https://www.gowinsemi.com/en/support/home/) | Gowin FPGA design software. | ![stable][status-stable] | 2026-05 |
| [AMD FPGA devices](https://www.xilinx.com/products/silicon-devices/fpga.html) | Product navigation for AMD/Xilinx FPGA families. | ![stable][status-stable] | 2026-05 |
| [Intel FPGA product selector](https://www.intel.com/content/www/us/en/products/details/fpgas.html) | Product navigation for Intel FPGA families. | ![stable][status-stable] | 2026-05 |

## Boards and hardware ecosystems

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Digilent FPGA boards](https://digilent.com/shop/fpga-development-boards-kits-from-digilent/) | Education and prototyping boards. | ![stable][status-stable] | 2026-05 |
| [Terasic FPGA boards](https://www.terasic.com.cn/cgi-bin/page/archive.pl?Language=English) | Intel/Altera-oriented development boards. | ![stable][status-stable] | 2026-05 |
| [PYNQ](https://www.pynq.io/) | Python-centric Zynq board ecosystem. | ![stable][status-stable] | 2026-05 |
| [RocketBoards](https://www.rocketboards.org/) | Intel SoC FPGA board resources. | ![stable][status-stable] | 2026-05 |
| [AMD/Xilinx evaluation boards](https://www.xilinx.com/products/boards-and-kits/boards.html) | Official AMD/Xilinx board catalog. | ![stable][status-stable] | 2026-05 |
| [Intel FPGA development kits](https://www.intel.com/content/www/us/en/products/details/fpgas/development-kits.html) | Official Intel FPGA development kits. | ![stable][status-stable] | 2026-05 |
| [Lattice evaluation boards](https://www.latticesemi.com/Products/DevelopmentBoardsAndKits) | Official Lattice board catalog. | ![stable][status-stable] | 2026-05 |
| [FPGA Board Repository](https://boards.fpgadeveloper.com/) | Searchable FPGA board database. | ![stable][status-stable] | 2026-05 |
| [Second Life for FPGA boards](https://github.com/iDoka/awesome-fpga-boards) | Repurposed and surplus FPGA boards. | ![legacy][status-legacy] | 2021-01 |

## Reusable IP and reference designs

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [OpenCores](http://opencores.org/) | Community repository of reusable digital IP. | ![stable][status-stable] | 2026-05 |
| [LiteX](https://github.com/enjoy-digital/litex) | SoC builder and ecosystem for FPGA systems. | ![active][status-active] | 2026-05 |
| [ZipCPU](https://github.com/ZipCPU) | Open RTL, CPU, bus, and formal verification examples. | ![active][status-active] | 2025-12 |
| [Project F examples](https://github.com/projf) | Compact FPGA projects and tutorial code. | ![active][status-active] | 2026-01 |
| [MiSTer FPGA](https://github.com/MiSTer-devel) | FPGA-based retro computing cores. | ![active][status-active] | 2026-05 |
| [Digilent Vivado Library](https://github.com/Digilent/vivado-library) | Reusable IP and interface definitions for Vivado projects. | ![active][status-active] | 2026-05 |

## Communities and source lists

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [fpga.chat](https://fpga.chat/) | Practical FPGA discussion community. | ![stable][status-stable] | 2026-05 |
| [Reddit r/FPGA](https://www.reddit.com/r/FPGA/) | Broad FPGA Q&A and project discussion. | ![stable][status-stable] | 2026-05 |
| [Electronics Stack Exchange: FPGA](https://electronics.stackexchange.com/questions/tagged/fpga) | Hardware-focused FPGA questions. | ![stable][status-stable] | 2026-05 |
| [Stack Overflow: FPGA](https://stackoverflow.com/questions/tagged/fpga) | Software/tooling-oriented FPGA questions. | ![stable][status-stable] | 2026-05 |
| [FPGA Systems list](https://github.com/FPGA-Systems/fpga-awesome-list) | Baseline community list for this curated English version. | ![stable][status-stable] | 2026-05 |
| [hdl/awesome](https://github.com/hdl/awesome) | Curated HDL design and verification source list. | ![active][status-active] | 2026-05 |
| [Awesome HDL tools](https://hdl.github.io/awesome/categories/tools/) | HDL/EDA tool discovery source list. | ![active][status-active] | 2026-05 |
| [Vitorian awesome-fpga](https://github.com/Vitorian/awesome-fpga) | Older FPGA list for durable legacy references. | ![legacy][status-legacy] | 2017-05 |

## FPGA vendors

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [AMD/Xilinx](https://www.xilinx.com/) | High-end, mid-range, and SoC FPGA families. | ![stable][status-stable] | 2026-05 |
| [Intel FPGA](https://www.intel.com/content/www/us/en/products/details/fpgas.html) | Intel/Altera FPGA and SoC FPGA families. | ![stable][status-stable] | 2026-05 |
| [Lattice Semiconductor](https://www.latticesemi.com/) | Low-power and small/mid-range FPGA families. | ![stable][status-stable] | 2026-05 |
| [Microchip FPGA](https://www.microchip.com/en-us/products/fpgas-and-plds) | PolarFire, IGLOO, SmartFusion, and legacy Microsemi/Actel lines. | ![stable][status-stable] | 2026-05 |
| [Achronix](https://www.achronix.com/) | High-performance FPGA and embedded FPGA products. | ![stable][status-stable] | 2026-05 |
| [Efinix](https://www.efinixinc.com/) | Trion and Titanium FPGA families. | ![stable][status-stable] | 2026-05 |
| [Gowin Semiconductor](https://www.gowinsemi.com/) | Low-cost FPGA families and boards. | ![stable][status-stable] | 2026-05 |
| [QuickLogic](https://www.quicklogic.com/) | Low-power FPGA and eFPGA products. | ![stable][status-stable] | 2026-05 |
| [Anlogic](https://www.anlogic.com/) | Regional FPGA device families and tools. | ![stable][status-stable] | 2026-05 |
| [Cologne Chip](https://www.colognechip.com/) | GateMate FPGA family. | ![stable][status-stable] | 2026-05 |
| [NanoXplore](https://nanoxplore.com/) | Radiation-tolerant FPGA products for high-reliability markets. | ![stable][status-stable] | 2026-05 |

## eFPGA vendors

| Resource | Use it for | Status | Activity |
| --- | --- | --- | --- |
| [Menta](https://www.menta-efpga.com/) | Embedded FPGA IP. | ![stable][status-stable] | 2026-05 |
| [Achronix eFPGA](https://www.achronix.com/) | Speedcore embedded FPGA IP. | ![stable][status-stable] | 2026-05 |
| [QuickLogic eFPGA IP](https://www.quicklogic.com/efpga-ip/) | Embedded FPGA hard IP and tools. | ![stable][status-stable] | 2026-05 |
| [AdicSys](https://www.adicsys.com/) | Embedded FPGA IP. | ![stable][status-stable] | 2026-05 |

## Contributing

Additions should explain why a resource belongs here. A good entry:

- solves a clear FPGA task,
- has a direct public URL,
- is active enough to be useful,
- and includes `Resource`, `Use it for`, `Status`, and `Activity` fields.

Avoid adding generic search pages, duplicate vendor landing pages, personal links without reusable technical value, and resources that only make sense for one private/internal workflow.

## License

MIT

[status-active]: https://img.shields.io/badge/-active-brightgreen
[status-stable]: https://img.shields.io/badge/-stable-blue
[status-legacy]: https://img.shields.io/badge/-legacy-orange
[status-unknown]: https://img.shields.io/badge/-unknown-lightgrey
