# Awesome FPGA

A curated, practical list of FPGA resources for engineers, students, and teams building real FPGA projects.

This list is optimized for application value: learning, RTL design, verification, toolchains, boards, reusable IP, communities, and vendors. It is intentionally selective; generic search links, unclear mirrors, abandoned stubs, and vendor names without useful public FPGA entry points are kept out.

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
| Learn FPGA basics | HDLBits, Nandland, Project F, fpga4fun, Bruno Levy learn-fpga |
| Write better RTL | 01signal, ZipCPU, Sunburst Design, ASIC-World, ChipVerify |
| Build verification habits | cocotb, VUnit, OSVVM, UVVM, Verible, GTKWave |
| Try open-source FPGA flow | Yosys, nextpnr, Project IceStorm, prjtrellis, F4PGA, openFPGALoader |
| Manage project workflow | FuseSoC, Edalize, RgGen, SiliconCompiler, Apio, FPGA Error Decoder |
| Pick reusable building blocks | LiteX, Analog Devices HDL, NEORV32, VexRiscv, SERV, ZipCPU |
| Choose a board or vendor | Board catalogs first, then vendor tools and device pages |

## Activity and status

| Status | Meaning |
| --- | --- |
| ![active][status-active] | Public project activity or source update within the last 18 months. |
| ![stable][status-stable] | Evergreen, authoritative, or vendor-maintained resource with no better public activity signal. |
| ![unknown][status-unknown] | Reachable and relevant, but public update activity is not clear. |
| ![legacy][status-legacy] | Useful for older flows, old devices, or historical context; not a first choice for new projects. |

`Activity` is always `YYYY-MM` when present. For GitHub repositories it is the repository `pushed_at` month. For articles, marketplaces, and regular websites it is used only when the source exposes a publication, release, or last-updated month. If no source-confirmed date can be extracted, the field is left empty. Manual audit dates are never used as activity dates. For this May 2026 audit, `active` means activity in `2024-11` or newer.

`Stars` is filled only for GitHub repositories, using the repository star count. Rows are ordered by status from active to stable to unknown to legacy, then by newest activity, stars, and name.

## Curation rules

- Prefer resources that help a reader do something concrete: simulate, synthesize, debug, select hardware, structure a project, or understand a design tradeoff.
- Prefer official documentation, active projects, maintained examples, and reproducible workflows.
- Keep descriptions short and decision-oriented.
- Avoid generic YouTube/search pages, personal contact noise, duplicate vendor landing pages, unsourced vendor names, and entries with unclear FPGA relevance.
- Keep old resources only when they still solve a recognizable problem or explain useful legacy context.

## Learning paths

### Beginner path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [FPGA-ASIC Roadmap](https://github.com/m3y54m/FPGA-ASIC-Roadmap) | Structured path through FPGA/ASIC learning topics and references. | ![active][status-active] | 2026-05 | 591 |
| [Bruno Levy learn-fpga](https://github.com/BrunoLevy/learn-fpga) | Low-cost FPGA, Yosys, nextpnr, graphics, and RISC-V learning. | ![active][status-active] | 2025-11 | 3516 |
| [FPGA Tutorial](https://www.fpgatutorial.com/) | Structured HDL and FPGA fundamentals. | ![stable][status-stable] |  |  |
| [fpga4fun](https://www.fpga4fun.com/) | Small projects for first board experiments. | ![stable][status-stable] |  |  |
| [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) | Hands-on Verilog exercises for syntax, FSMs, timing, and small blocks. | ![stable][status-stable] |  |  |
| [Nandland](https://www.youtube.com/@nandland) | Beginner-friendly HDL and FPGA videos. | ![stable][status-stable] |  |  |
| [Project F](https://projectf.io/) | Concise FPGA tutorials with graphics, timing, and small examples. | ![stable][status-stable] |  |  |
| [SparkFun "So You Want to Learn FPGAs"](https://news.sparkfun.com/1203) | Older but useful discussion of the FPGA learning curve. | ![legacy][status-legacy] | 2013-08 |  |

### RTL design path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [ZipCPU](https://github.com/ZipCPU/zipcpu) | CPU-oriented RTL, buses, and formal verification examples. | ![active][status-active] | 2025-12 | 1542 |
| [01signal](https://www.01signal.com/) | Timing, CDC, resets, constraints, and design pitfalls. | ![stable][status-stable] |  |  |
| [ASIC-World](https://www.asic-world.com/) | Verilog, VHDL, and SystemVerilog reference material. | ![stable][status-stable] |  |  |
| [ChipVerify](https://www.chipverify.com/) | Verilog, SystemVerilog, UVM, and verification examples. | ![stable][status-stable] |  |  |
| [Sunburst Design](http://www.sunburst-design.com/) | Classic Verilog/SystemVerilog papers and methodology material. | ![stable][status-stable] |  |  |

### Verification path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [cocotb](https://github.com/cocotb/cocotb) | Python-based cosimulation and reusable HDL testbenches. | ![active][status-active] | 2026-05 | 2375 |
| [VUnit](https://github.com/VUnit/vunit) | VHDL/SystemVerilog test automation. | ![active][status-active] | 2026-05 | 826 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | VHDL methodology, coverage, randomization, and reusable verification libraries. | ![active][status-active] | 2026-05 | 77 |
| [GTKWave](https://github.com/gtkwave/gtkwave) | Waveform viewing for day-to-day simulation debug. | ![active][status-active] | 2026-04 | 974 |
| [UVVM](https://github.com/UVVM/UVVM) | VHDL BFMs and structured testbench patterns. | ![active][status-active] | 2026-04 | 429 |
| [EDA Playground](https://www.edaplayground.com/) | Browser-based HDL simulation and quick testbench experiments. | ![stable][status-stable] |  |  |

### Open-source FPGA flow path

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Yosys](https://github.com/YosysHQ/yosys) | Open-source HDL synthesis. | ![active][status-active] | 2026-05 | 4451 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Open-source place-and-route for supported FPGA families. | ![active][status-active] | 2026-05 | 1670 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Lattice ECP5 bitstream and flow support. | ![active][status-active] | 2026-05 | 459 |
| [Project IceStorm](https://github.com/YosysHQ/icestorm) | Open toolchain resources for Lattice iCE40. | ![active][status-active] | 2026-02 | 1161 |
| [F4PGA](https://github.com/chipsalliance/f4pga) | Open FPGA flow umbrella, formerly SymbiFlow. | ![active][status-active] | 2025-01 | 437 |

## Knowledge and tutorials

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [FPHD](https://github.com/lpacher/fphd) | Vivado and VHDL course notes with virtual labs. | ![active][status-active] | 2025-07 | 21 |
| [Adiuvo Engineering](https://www.adiuvoengineering.com/) | MicroZed Chronicles and FPGA/SoC engineering articles. | ![stable][status-stable] |  |  |
| [Beyond Circuits](https://www.beyond-circuits.com/) | FPGA and digital design articles. | ![stable][status-stable] |  |  |
| [FPGA Academy](https://fpgacademy.org/) | Educational FPGA material and labs. | ![stable][status-stable] |  |  |
| [FPGA4Student](https://fpga4student.com/) | FPGA projects and HDL examples. | ![stable][status-stable] |  |  |
| [ITSEmbedded](https://www.itsembedded.com/) | Practical RTL, Verilator, and scripted simulation workflows. | ![stable][status-stable] |  |  |
| [Numato Lab Knowledge Base](https://numato.com/kb/) | Board-oriented tutorials and examples. | ![stable][status-stable] |  |  |
| [Tang Nano Project Series](https://learn.lushaylabs.com/) | Practical Gowin/Tang Nano learning path. | ![stable][status-stable] |  |  |
| [VHDLwhiz](https://vhdlwhiz.com/) | VHDL-focused tutorials and courses. | ![stable][status-stable] |  |  |

## Books and evergreen references

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| *100 Power Tips for FPGA Designers* by Evgeni Stavinov | Practical FPGA design tips, scripts, and gotchas. | ![stable][status-stable] |  |  |
| *FPGA Prototyping by Verilog Examples* by Pong P. Chu | Practical Verilog projects for FPGA learning. | ![stable][status-stable] |  |  |
| *FPGA Prototyping by VHDL Examples* by Pong P. Chu | Practical VHDL projects for FPGA learning. | ![stable][status-stable] |  |  |
| *Verilog by Example* by Blaine C. Readler | Compact Verilog primer with FPGA-oriented examples. | ![stable][status-stable] |  |  |

## Languages and HDL frameworks

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Chisel](https://github.com/chipsalliance/chisel) | Scala-embedded hardware construction language. | ![active][status-active] | 2026-05 | 4662 |
| [SpinalHDL](https://github.com/SpinalHDL/SpinalHDL) | Scala-based hardware description language. | ![active][status-active] | 2026-05 | 1988 |
| [Veryl](https://github.com/veryl-lang/veryl) | Modern SystemVerilog-compatible hardware description language and tooling. | ![active][status-active] | 2026-05 | 937 |
| [PyXHDL](https://github.com/davidel/pyxhdl) | Python frontend that generates SystemVerilog and VHDL. | ![active][status-active] | 2026-05 | 27 |
| [Amaranth HDL](https://github.com/amaranth-lang/amaranth) | Python-based HDL for FPGA and ASIC-oriented design. | ![active][status-active] | 2026-04 | 2012 |
| [PyMTL3](https://github.com/pymtl/pymtl3) | Python hardware generation, simulation, and verification. | ![active][status-active] | 2026-04 | 453 |
| [JSON-for-VHDL](https://github.com/Paebbels/JSON-for-VHDL) | Synthesizable VHDL package for JSON parsing and generics. | ![active][status-active] | 2026-02 | 84 |
| [MyHDL](https://github.com/myhdl/myhdl) | Python hardware description and conversion flow. | ![active][status-active] | 2025-04 | 1117 |
| [FloPoCo](https://flopoco.org/) | Fixed- and floating-point arithmetic core generation. | ![stable][status-stable] |  |  |
| [Verilog/SystemVerilog resources](https://www.chipverify.com/) | Practical language examples and verification explanations. | ![stable][status-stable] |  |  |
| [VHDL resources](https://vhdlwhiz.com/) | Practical VHDL tutorials and design patterns. | ![stable][status-stable] |  |  |
| [Migen](https://github.com/m-labs/migen) | Python-based HDL/toolbox still relevant for older LiteX-era code. | ![legacy][status-legacy] | 2026-01 | 1323 |

## Simulation, verification, and debug

### Simulators

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Verilator](https://github.com/verilator/verilator) | High-performance SystemVerilog simulation and linting. | ![active][status-active] | 2026-05 | 3621 |
| [Icarus Verilog](https://github.com/steveicarus/iverilog) | Free Verilog simulator for quick command-line flows. | ![active][status-active] | 2026-05 | 3452 |
| [GHDL](https://github.com/ghdl/ghdl) | Open-source VHDL analysis, compilation, simulation, and synthesis experiments. | ![active][status-active] | 2026-05 | 2819 |
| [NVC](https://github.com/nickg/nvc) | VHDL compilation and simulation. | ![active][status-active] | 2026-05 | 817 |
| [EDA Playground](https://www.edaplayground.com/) | Online HDL simulation across multiple backends. | ![stable][status-stable] |  |  |

### Verification, formal, and language tooling

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [cocotb](https://github.com/cocotb/cocotb) | Python testbenches for HDL designs. | ![active][status-active] | 2026-05 | 2375 |
| [slang](https://github.com/MikePopoloski/slang) | SystemVerilog compiler and language services toolkit. | ![active][status-active] | 2026-05 | 1039 |
| [VUnit](https://github.com/VUnit/vunit) | Automated VHDL/SystemVerilog test running. | ![active][status-active] | 2026-05 | 826 |
| [SymbiYosys / SBY](https://github.com/YosysHQ/sby) | Frontend for formal verification flows around Yosys. | ![active][status-active] | 2026-05 | 509 |
| [VHDL LS](https://github.com/VHDL-LS/rust_hdl) | VHDL language server and analysis library. | ![active][status-active] | 2026-05 | 483 |
| [Surelog/UHDM](https://github.com/chipsalliance/Surelog) | SystemVerilog parsing and UHDM frontend ecosystem. | ![active][status-active] | 2026-05 | 460 |
| [OSVVM](https://github.com/OSVVM/OsvvmLibraries) | VHDL verification, coverage, randomization, and utility libraries. | ![active][status-active] | 2026-05 | 77 |
| [svls](https://github.com/dalance/svls) | SystemVerilog language server. | ![active][status-active] | 2026-04 | 575 |
| [UVVM](https://github.com/UVVM/UVVM) | VHDL verification components and structured tests. | ![active][status-active] | 2026-04 | 429 |
| [Verible](https://github.com/chipsalliance/verible) | SystemVerilog formatting, linting, parsing, and language tooling. | ![active][status-active] | 2026-03 | 1846 |
| [sv-parser](https://github.com/dalance/sv-parser) | SystemVerilog parser library. | ![active][status-active] | 2026-03 | 471 |
| [svlint](https://github.com/dalance/svlint) | SystemVerilog linter. | ![active][status-active] | 2025-11 | 383 |

### Debug and diagrams

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [OpenOCD](https://github.com/openocd-org/openocd) | JTAG access and board debug workflows. | ![active][status-active] | 2026-05 | 2198 |
| [FPGA Error Decoder](https://marketplace.visualstudio.com/items?itemName=fpgachat.fpga-error-decoder) | VS Code extension for FPGA build error triage. | ![active][status-active] | 2026-05 |  |
| [WaveDrom](https://github.com/wavedrom/wavedrom) | Timing diagrams for documentation and interface reviews. | ![active][status-active] | 2026-04 | 3404 |
| [GTKWave](https://github.com/gtkwave/gtkwave) | VCD/FST waveform viewing. | ![active][status-active] | 2026-04 | 974 |
| [Sigrok / PulseView](https://github.com/sigrokproject/pulseview) | Logic analyzer and signal capture tooling. | ![active][status-active] | 2025-11 | 735 |

## Synthesis, implementation, and programming

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Yosys](https://github.com/YosysHQ/yosys) | Synthesis framework used by many open FPGA flows. | ![active][status-active] | 2026-05 | 4451 |
| [nextpnr](https://github.com/YosysHQ/nextpnr) | Place-and-route for iCE40, ECP5, Nexus, Gowin, and other targets. | ![active][status-active] | 2026-05 | 1670 |
| [openFPGALoader](https://github.com/trabucayre/openFPGALoader) | Programming many FPGA boards from one command-line tool. | ![active][status-active] | 2026-05 | 1635 |
| [Verilog-to-Routing](https://github.com/verilog-to-routing/vtr-verilog-to-routing) | Academic FPGA CAD flow and architecture research platform. | ![active][status-active] | 2026-05 | 1226 |
| [OpenFPGA](https://github.com/lnis-uofu/OpenFPGA) | FPGA architecture generation and CAD research framework. | ![active][status-active] | 2026-05 | 1102 |
| [prjtrellis](https://github.com/YosysHQ/prjtrellis) | Open ECP5/XP2 tooling. | ![active][status-active] | 2026-05 | 459 |
| [GHDL Yosys plugin](https://github.com/ghdl/ghdl-yosys-plugin) | VHDL frontend integration for Yosys. | ![active][status-active] | 2026-05 | 361 |
| [Project IceStorm](https://github.com/YosysHQ/icestorm) | Reverse-engineered iCE40 bitstream tools. | ![active][status-active] | 2026-02 | 1161 |
| [F4PGA](https://github.com/chipsalliance/f4pga) | Open FPGA flow umbrella for supported vendor families. | ![active][status-active] | 2025-01 | 437 |

## Project workflow and productivity

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [FuseSoC](https://github.com/olofk/fusesoc) | Package management and builds for reusable HDL projects. | ![active][status-active] | 2026-05 | 1417 |
| [SiliconCompiler](https://github.com/siliconcompiler/siliconcompiler) | Python-based build orchestration for ASIC and FPGA tool flows. | ![active][status-active] | 2026-05 | 1158 |
| [Apio](https://github.com/FPGAwars/apio) | Open-source command-line workflow for supported FPGA boards. | ![active][status-active] | 2026-05 | 981 |
| [AccelFury/af](https://github.com/AccelFury/af) | Open repository for the AccelFury toolchain. | ![active][status-active] | 2026-05 | 1 |
| [Edalize](https://github.com/olofk/edalize) | Backend abstraction for EDA tools and FuseSoC flows. | ![active][status-active] | 2026-04 | 770 |
| [RgGen](https://github.com/rggen/rggen) | Register map generation for RTL, UVM RAL, headers, and docs. | ![active][status-active] | 2026-04 | 455 |
| [Icestudio](https://github.com/FPGAwars/icestudio) | Visual FPGA IDE for open-source boards and educational flows. | ![active][status-active] | 2026-02 | 1907 |
| [Corsair](https://github.com/esynr3z/corsair) | Register map and RTL/header generation. | ![active][status-active] | 2025-05 | 136 |
| [AccelFury](https://accelfury.com/) | FPGA acceleration workflow and tooling ecosystem. | ![stable][status-stable] |  |  |
| [FPGAMAKE](https://github.com/cambridgehackers/fpgamake) | Vivado Makefile generation from the older Vitorian list. | ![legacy][status-legacy] | 2022-05 | 99 |

## Vendor tools

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [AMD Vivado](https://www.xilinx.com/products/design-tools/vivado.html) | Primary AMD/Xilinx FPGA design suite. | ![stable][status-stable] |  |  |
| [Efinix Efinity](https://www.efinixinc.com/support/) | Efinix FPGA design software. | ![stable][status-stable] |  |  |
| [Gowin EDA](https://www.gowinsemi.com/en/support/home/) | Gowin FPGA design software. | ![stable][status-stable] |  |  |
| [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html) | Intel FPGA design suite. | ![stable][status-stable] |  |  |
| [Lattice Diamond](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/DIAMOND) | Lattice design suite for older families. | ![stable][status-stable] |  |  |
| [Lattice Radiant](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/RadiantSoftwareSuite) | Lattice design suite for newer device families. | ![stable][status-stable] |  |  |
| [Microchip Libero SoC](https://www.microchip.com/en-us/design-centers-and-tools/soc-design-support) | Microchip/Microsemi FPGA design environment. | ![stable][status-stable] |  |  |

## Boards and hardware ecosystems

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Lattice boards that can be used with open tools. | ![active][status-active] | 2026-04 | 354 |
| [PYNQ](https://github.com/Xilinx/PYNQ) | Python-centric Zynq and Zynq UltraScale+ board ecosystem. | ![active][status-active] | 2026-03 | 2303 |
| [AMD/Xilinx evaluation boards](https://www.xilinx.com/products/boards-and-kits/boards.html) | Official AMD/Xilinx board catalog. | ![stable][status-stable] |  |  |
| [Digilent FPGA boards](https://digilent.com/shop/fpga-development-boards-kits-from-digilent/) | Education and prototyping boards. | ![stable][status-stable] |  |  |
| [FPGA Board Repository](https://boards.fpgadeveloper.com/) | Searchable FPGA board database. | ![stable][status-stable] |  |  |
| [Intel FPGA development kits](https://www.intel.com/content/www/us/en/products/details/fpgas/development-kits.html) | Official Intel FPGA development kits. | ![stable][status-stable] |  |  |
| [Lattice evaluation boards](https://www.latticesemi.com/Products/DevelopmentBoardsAndKits) | Official Lattice board catalog. | ![stable][status-stable] |  |  |
| [RocketBoards](https://www.rocketboards.org/) | Intel SoC FPGA board resources. | ![stable][status-stable] |  |  |
| [Terasic FPGA boards](https://www.terasic.com.cn/cgi-bin/page/archive.pl?Language=English) | Intel/Altera-oriented development boards. | ![stable][status-stable] |  |  |
| [Second Life for FPGA boards](https://github.com/iDoka/awesome-fpga-boards) | Repurposed and surplus FPGA boards. | ![legacy][status-legacy] | 2021-01 | 104 |

## Reusable IP and reference designs

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [LiteX](https://github.com/enjoy-digital/litex) | SoC builder and ecosystem for FPGA systems. | ![active][status-active] | 2026-05 | 3887 |
| [NEORV32](https://github.com/stnolting/neorv32) | VHDL RISC-V processor and microcontroller-style SoC. | ![active][status-active] | 2026-05 | 2065 |
| [Analog Devices HDL](https://github.com/analogdevicesinc/hdl) | FPGA reference designs and IP for Analog Devices platforms. | ![active][status-active] | 2026-05 | 1925 |
| [LitePCIe](https://github.com/enjoy-digital/litepcie) | PCIe core and integration blocks from the LiteX ecosystem. | ![active][status-active] | 2026-05 | 695 |
| [VexRiscv](https://github.com/SpinalHDL/VexRiscv) | Configurable SpinalHDL RISC-V CPU core. | ![active][status-active] | 2026-02 | 3144 |
| [SERV](https://github.com/olofk/serv) | Tiny serial RISC-V CPU for area-constrained FPGA projects. | ![active][status-active] | 2026-02 | 1799 |
| [ZipCPU](https://github.com/ZipCPU/zipcpu) | Open soft CPU core with extensive design notes. | ![active][status-active] | 2025-12 | 1542 |
| [Digilent Vivado Library](https://github.com/Digilent/vivado-library) | Reusable IP and interface definitions for Vivado projects. | ![active][status-active] | 2025-12 | 682 |
| [verilog-ethernet](https://github.com/alexforencich/verilog-ethernet) | Ethernet components for FPGA designs. | ![active][status-active] | 2025-02 | 2961 |
| [Corundum](https://github.com/corundum/corundum) | FPGA-based NIC and network datapath platform. | ![stable][status-stable] | 2024-07 | 2329 |
| [verilog-pcie](https://github.com/alexforencich/verilog-pcie) | PCIe components for FPGA designs. | ![stable][status-stable] | 2024-04 | 1597 |
| [OpenCores](http://opencores.org/) | Community repository of reusable digital IP. | ![stable][status-stable] |  |  |

## Communities and source lists

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [hdl/awesome](https://github.com/hdl/awesome) | Curated HDL design, verification, and EDA source list. | ![active][status-active] | 2026-05 | 173 |
| [drom/awesome-hdl](https://github.com/drom/awesome-hdl) | HDL language and tool discovery list. | ![active][status-active] | 2026-04 | 1149 |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Lattice FPGA board and open-tool discovery. | ![active][status-active] | 2026-04 | 354 |
| [aolofsson/awesome-opensource-hardware](https://github.com/aolofsson/awesome-opensource-hardware) | Open-source hardware, EDA, and reusable design discovery. | ![active][status-active] | 2026-03 | 2338 |
| [ben-marshall/awesome-open-hardware-verification](https://github.com/ben-marshall/awesome-open-hardware-verification) | Focused verification source list for open hardware. | ![active][status-active] | 2026-01 | 607 |
| [FPGA-Systems/fpga-awesome-list](https://github.com/FPGA-Systems/fpga-awesome-list) | Baseline community list for this curated English version. | ![active][status-active] | 2025-10 | 180 |
| [coderonion/awesome-fpga](https://github.com/coderonion/awesome-fpga) | Broad discovery list that needs filtering before reuse. | ![stable][status-stable] | 2024-07 | 4 |
| [Electronics Stack Exchange: FPGA](https://electronics.stackexchange.com/questions/tagged/fpga) | Hardware-focused FPGA questions. | ![stable][status-stable] |  |  |
| [fpga.chat](https://fpga.chat/) | Practical FPGA discussion community. | ![stable][status-stable] |  |  |
| [hdl/awesome tools category](https://hdl.github.io/awesome/categories/tools/) | Generated tool category page from the hdl/awesome ecosystem. | ![stable][status-stable] |  |  |
| [Reddit r/FPGA](https://www.reddit.com/r/FPGA/) | Broad FPGA Q&A and project discussion. | ![stable][status-stable] |  |  |
| [Stack Overflow: FPGA](https://stackoverflow.com/questions/tagged/fpga) | Software/tooling-oriented FPGA questions. | ![stable][status-stable] |  |  |
| [awesome.ecosyste.ms FPGA topic](https://awesome.ecosyste.ms/lists?topic=fpga) | Index of FPGA-related awesome lists. | ![unknown][status-unknown] |  |  |
| [open-source-fpga-resource](https://github.com/os-fpga/open-source-fpga-resource) | Open-source FPGA resource index from OSFPGA. | ![legacy][status-legacy] | 2022-11 | 455 |
| [awesome-fpga-programming](https://github.com/emanueledelsozzo/awesome-fpga-programming) | Older FPGA programming source list. | ![legacy][status-legacy] | 2022-06 | 74 |
| [VHDL/awesome-vhdl](https://github.com/VHDL/awesome-vhdl) | Archived VHDL source list for older references. | ![legacy][status-legacy] | 2020-02 | 85 |
| [Vitorian awesome-fpga](https://github.com/Vitorian/awesome-fpga) | Older FPGA list for durable legacy references. | ![legacy][status-legacy] | 2017-05 | 389 |

## FPGA vendors

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Achronix](https://www.achronix.com/) | High-performance FPGA and embedded FPGA products. | ![stable][status-stable] |  |  |
| [AMD/Xilinx](https://www.xilinx.com/) | High-end, mid-range, and SoC FPGA families. | ![stable][status-stable] |  |  |
| [Anlogic](https://www.anlogic.com/) | Regional FPGA device families and tools. | ![stable][status-stable] |  |  |
| [Cologne Chip](https://www.colognechip.com/) | GateMate FPGA family. | ![stable][status-stable] |  |  |
| [Efinix](https://www.efinixinc.com/) | Trion and Titanium FPGA families. | ![stable][status-stable] |  |  |
| [Gowin Semiconductor](https://www.gowinsemi.com/) | Low-cost FPGA families and boards. | ![stable][status-stable] |  |  |
| [Intel FPGA](https://www.intel.com/content/www/us/en/products/details/fpgas.html) | Intel/Altera FPGA and SoC FPGA families. | ![stable][status-stable] |  |  |
| [Lattice Semiconductor](https://www.latticesemi.com/) | Low-power and small/mid-range FPGA families. | ![stable][status-stable] |  |  |
| [Microchip FPGA](https://www.microchip.com/en-us/products/fpgas-and-plds) | PolarFire, IGLOO, SmartFusion, and legacy Microsemi/Actel lines. | ![stable][status-stable] |  |  |
| [NanoXplore](https://nanoxplore.com/) | Radiation-tolerant FPGA products for high-reliability markets. | ![stable][status-stable] |  |  |
| [QuickLogic](https://www.quicklogic.com/) | Low-power FPGA and eFPGA products. | ![stable][status-stable] |  |  |

## eFPGA vendors

| Resource | Use it for | Status | Activity | Stars |
| --- | --- | --- | --- | --- |
| [Achronix eFPGA](https://www.achronix.com/) | Speedcore embedded FPGA IP. | ![stable][status-stable] |  |  |
| [AdicSys](https://www.adicsys.com/) | Embedded FPGA IP. | ![stable][status-stable] |  |  |
| [Menta](https://www.menta-efpga.com/) | Embedded FPGA IP. | ![stable][status-stable] |  |  |
| [QuickLogic eFPGA IP](https://www.quicklogic.com/efpga-ip/) | Embedded FPGA hard IP and tools. | ![stable][status-stable] |  |  |

## Source audit

| Source | Use it for | Action | Status | Activity | Stars |
| --- | --- | --- | --- | --- | --- |
| [FPGA-ASIC-Roadmap](https://github.com/m3y54m/FPGA-ASIC-Roadmap) | FPGA/ASIC learning roadmap; useful education map, but add only focused learning entries. | manual_review | ![active][status-active] | 2026-05 | 591 |
| [hdl/awesome](https://github.com/hdl/awesome) | HDL design, verification, tools, IP, and libraries; strong source for modern tool and framework discovery. | use_as_seed | ![active][status-active] | 2026-05 | 173 |
| [drom/awesome-hdl](https://github.com/drom/awesome-hdl) | HDL languages, simulators, transpilers, and meta-HDL; dedupe against hdl/awesome before adding. | use_as_seed | ![active][status-active] | 2026-04 | 1149 |
| [awesome-latticeFPGAs](https://github.com/kelu124/awesome-latticeFPGAs) | Lattice FPGA boards for open tools; required source for board and open-tool Lattice discovery. | use_as_seed | ![active][status-active] | 2026-04 | 354 |
| [suryakantamangaraj/awesome-riscv](https://github.com/suryakantamangaraj/awesome-riscv) | RISC-V cores, SoCs, and FPGA targets; use only for reusable soft CPU/RISC-V references. | manual_review | ![active][status-active] | 2026-04 | 351 |
| [RDSik/FPGA-Awesome-list](https://github.com/RDSik/FPGA-Awesome-list) | Russian/English FPGA materials; add only English-usable or broadly useful resources. | manual_review | ![active][status-active] | 2026-04 | 10 |
| [aolofsson/awesome-opensource-hardware](https://github.com/aolofsson/awesome-opensource-hardware) | Open-source hardware tools and reusable designs; high-signal open-source EDA/tooling source. | use_as_seed | ![active][status-active] | 2026-03 | 2338 |
| [awesome-formal-verification](https://github.com/ElNiak/awesome-formal-verification) | Formal verification across software and hardware; use only for hardware-specific formal resources. | monitor_only | ![active][status-active] | 2026-03 | 134 |
| [Awesome-EDA](https://github.com/ishandutta2007/Awesome-EDA) | EDA tools across PCB, FPGA, ASIC, and VLSI; secondary source that requires manual filtering. | manual_review | ![active][status-active] | 2026-02 | 7 |
| [kitspace/awesome-electronics](https://github.com/kitspace/awesome-electronics) | General electronics resource index; use only for cross-list discovery. | monitor_only | ![active][status-active] | 2026-01 | 7695 |
| [ben-marshall/awesome-open-hardware-verification](https://github.com/ben-marshall/awesome-open-hardware-verification) | Open hardware verification; strong source for cocotb, formal, and testbench tooling. | use_as_seed | ![active][status-active] | 2026-01 | 607 |
| [FPGA-Systems/fpga-awesome-list](https://github.com/FPGA-Systems/fpga-awesome-list) | General FPGA list used as the baseline seed; clean contact noise, generic links, and stale entries before reuse. | use_as_seed | ![active][status-active] | 2025-10 | 180 |
| [C8Costa/Edge-Ai-Resources](https://github.com/C8Costa/Edge-Ai-Resources) | Edge AI and hardware acceleration; too broad for the main list because FPGA relevance is secondary. | monitor_only | ![active][status-active] | 2025-08 | 2 |
| [lpacher/fphd](https://github.com/lpacher/fphd) | FPGA programming course using Vivado and VHDL; useful VHDL/Vivado education resource. | manual_review | ![active][status-active] | 2025-07 | 21 |
| [TM90/awesome-hwd-tools](https://github.com/TM90/awesome-hwd-tools) | Hardware design tools; secondary tooling source mostly covered by stronger lists. | monitor_only | ![active][status-active] | 2025-06 | 88 |
| [coderonion/awesome-fpga](https://github.com/coderonion/awesome-fpga) | Broad FPGA, HDL, tools, IP, and source-list discovery; useful but noisy, so select maintained English-usable resources only. | use_as_seed | ![stable][status-stable] | 2024-07 | 4 |
| [suryavanshi/awesome-hardware](https://github.com/suryavanshi/awesome-hardware) | Generic hardware resources; weak FPGA signal, useful only as a secondary search trail. | monitor_only | ![stable][status-stable] | 2024-06 | 1 |
| [hdl/awesome tools category](https://hdl.github.io/awesome/categories/tools/) | Generated HDL/EDA tools category; use hdl/awesome GitHub metadata for project activity. | use_as_seed | ![stable][status-stable] |  |  |
| [awesome.ecosyste.ms FPGA topic](https://awesome.ecosyste.ms/lists?topic=fpga) | FPGA-related awesome-list discovery index; not a source of activity metadata for individual resources. | monitor_only | ![unknown][status-unknown] |  |  |
| [AwesomeOpenSource: sjinzh awesome-fpga-list](https://awesomeopensource.com/project/sjinzh/awesome-fpga-list) | AwesomeOpenSource mirror page; Cloudflare-gated during audit and GitHub slug redirects to an unrelated CUDA/HPC repo. | monitor_only | ![unknown][status-unknown] |  |  |
| [awesome-opensource-asic-resources](https://github.com/mattvenn/awesome-opensource-asic-resources) | Open-source ASIC resources; use only for OSS CAD Suite/open-silicon overlap. | monitor_only | ![legacy][status-legacy] | 2023-04 | 395 |
| [drom/awesome-riscv](https://github.com/drom/awesome-riscv) | RISC-V implementations; compact soft CPU source, but less current than alternatives. | monitor_only | ![legacy][status-legacy] | 2023-03 | 143 |
| [open-source-fpga-resource](https://github.com/os-fpga/open-source-fpga-resource) | Open-source FPGA projects; useful OSFPGA/open-tool index, but stale. | use_as_seed | ![legacy][status-legacy] | 2022-11 | 455 |
| [Hands-on-FPGA-class](https://github.com/tinyvision-ai-inc/Hands-on-FPGA-class) | Hands-on FPGA class; good beginner angle, but add only durable exercises. | manual_review | ![legacy][status-legacy] | 2022-09 | 58 |
| [awesome-fpga-programming](https://github.com/emanueledelsozzo/awesome-fpga-programming) | FPGA programming languages and DSLs; useful for HLS/DSL discovery, but stale. | use_as_seed | ![legacy][status-legacy] | 2022-06 | 74 |
| [awesome-digital-ic](https://github.com/qninth/awesome-digital-ic) | Digital IC, ASIC, and FPGA resources; mixed Chinese/English source that requires strict filtering. | manual_review | ![legacy][status-legacy] | 2022-05 | 154 |
| [awesome-hardware-tools](https://github.com/jpc-lip6/awesome-hardware-tools) | Open-source hardware tools; secondary tooling source included in audit but not main list due low signal. | use_as_seed | ![legacy][status-legacy] | 2022-04 | 0 |
| [awesome-dv](https://github.com/troyguo/awesome-dv) | ASIC design verification; use only for FPGA-relevant verification resources. | monitor_only | ![legacy][status-legacy] | 2022-02 | 357 |
| [Awesome-FPGA-ASIC-RISC-V](https://github.com/TouchSky-Lab/Awesome-FPGA-ASIC-RISC-V) | FPGA/ASIC/RISC-V papers; weak curation, not used as a seed. | monitor_only | ![legacy][status-legacy] | 2022-02 | 6 |
| [awesome-fpga-boards](https://github.com/iDoka/awesome-fpga-boards) | Repurposed FPGA boards; niche board list kept as a legacy board resource. | manual_review | ![legacy][status-legacy] | 2021-01 | 104 |
| [VHDL/awesome-vhdl](https://github.com/VHDL/awesome-vhdl) | VHDL IP, frameworks, tools, and resources; archived, useful for older VHDL references only. | manual_review | ![legacy][status-legacy] | 2020-02 | 85 |
| [clin99/awesome-eda](https://github.com/clin99/awesome-eda) | Year-indexed open-source EDA projects; historical index, not an active source list. | monitor_only | ![legacy][status-legacy] | 2019-06 | 99 |
| [Vitorian/awesome-fpga](https://github.com/Vitorian/awesome-fpga) | General FPGA tutorials and references; historical source for durable references and legacy tools. | manual_review | ![legacy][status-legacy] | 2017-05 | 389 |

## Contributing

Additions should explain why a resource belongs here. A good entry:

- solves a clear FPGA task,
- has a direct public URL,
- is reachable and useful for the public FPGA community,
- uses the table columns `Resource`, `Use it for`, `Status`, `Activity`, and `Stars`,
- leaves `Activity` blank unless a source-confirmed `YYYY-MM` date is available,
- and fills `Stars` only for GitHub repositories.

Avoid adding generic search pages, duplicate vendor landing pages, personal links without reusable technical value, and resources that only make sense for one private/internal workflow.

## License

MIT

[status-active]: https://img.shields.io/badge/-active-brightgreen
[status-stable]: https://img.shields.io/badge/-stable-blue
[status-legacy]: https://img.shields.io/badge/-legacy-orange
[status-unknown]: https://img.shields.io/badge/-unknown-lightgrey
