# Awesome FPGA

A curated, practical list of FPGA resources for engineers, students, and teams building real FPGA projects.

This list is optimized for application value: learning, RTL design, verification, toolchains, boards, reusable IP, communities, and vendors. It is intentionally selective; generic search links, unclear mirrors, abandoned placeholders, and vendor names without useful public FPGA entry points are kept out.

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

- `active` - public project activity or source update within the last 18 months.
- `stable` - evergreen, authoritative, or vendor-maintained resource with no better public activity signal.
- `legacy` - useful for older flows, old devices, or historical context; not a first choice for new projects.
- `unknown` - reachable and relevant, but public update activity is not clear.

For GitHub resources, the activity date is the latest observed push date where available. For regular websites, vendor pages, books, and tutorials without public version metadata, the date is the last manual check: `2026-05-19`.

## Curation rules

- Prefer resources that help a reader do something concrete: simulate, synthesize, debug, select hardware, structure a project, or understand a design tradeoff.
- Prefer official documentation, active projects, and examples that can be reproduced.
- Avoid generic YouTube/search pages, personal contact noise, unsourced vendor names, duplicate landing pages, and entries with unclear FPGA relevance.
- Keep descriptions short and decision-oriented.

## Learning paths

### Beginner path

- [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) - Hands-on Verilog exercises for syntax, FSMs, timing, and small digital blocks. Activity: 2026-05-19, stable.
- [Nandland](https://www.youtube.com/@nandland) - Beginner-friendly HDL and FPGA videos. Activity: 2026-05-19, stable.
- [Project F](https://projectf.io/) - Concise FPGA tutorials with graphics, timing, and small design examples. Activity: 2026-05-19, stable.
- [fpga4fun](https://www.fpga4fun.com/) - Small projects useful for first board experiments. Activity: 2026-05-19, stable.
- [FPGA Tutorial](https://www.fpgatutorial.com/) - Structured introductory material for HDL and FPGA fundamentals. Activity: 2026-05-19, stable.
- [SparkFun FPGA guide](https://www.sparkfun.com/fpga) - Beginner-oriented explanation of FPGA tradeoffs and first steps. Activity: 2026-05-19, stable.

### RTL design path

- [01signal](https://www.01signal.com/) - Practical notes on timing, CDC, reset strategy, constraints, and FPGA design pitfalls. Activity: 2026-05-19, stable.
- [ZipCPU](https://zipcpu.com/) - Deep RTL articles, formal methods, bus design, and CPU-oriented FPGA projects. Activity: 2025-12-08, active.
- [Sunburst Design](http://www.sunburst-design.com/) - Classic Verilog/SystemVerilog papers and design methodology material. Activity: 2026-05-19, stable.
- [ASIC-World](https://www.asic-world.com/) - Verilog/SystemVerilog reference material. Activity: 2026-05-19, stable.
- [ChipVerify](https://www.chipverify.com/) - Practical examples for Verilog, SystemVerilog, and verification concepts. Activity: 2026-05-19, stable.
- [Bruno Levy learn-fpga](https://github.com/BrunoLevy/learn-fpga) - Low-cost FPGA, Yosys, nextpnr, and RISC-V learning material. Activity: 2025-11-18, active.

### Verification path

- [EDA Playground](https://www.edaplayground.com/) - Browser-based HDL simulation and quick testbench experiments. Activity: 2026-05-19, stable.
- [cocotb](https://docs.cocotb.org/) - Python-based cosimulation for HDL verification. Activity: 2026-05-18, active.
- [VUnit](https://github.com/VUnit/vunit) - VHDL/SystemVerilog test automation framework. Activity: 2026-05-14, active.
- [OSVVM](https://github.com/OSVVM/OsvvmLibraries) - VHDL verification methodology and reusable verification libraries. Activity: 2026-05-16, active.
- [UVVM](https://github.com/UVVM/UVVM) - VHDL verification framework with BFMs and structured testbench patterns. Activity: 2026-04-22, active.
- [GTKWave](http://gtkwave.sourceforge.net/) - Waveform viewer for day-to-day simulation debug. Activity: 2026-04-21, active.

### Open-source FPGA flow path

- [Yosys](https://yosyshq.net/yosys/) - Open-source HDL synthesis. Activity: 2026-05-19, stable.
- [nextpnr](https://github.com/YosysHQ/nextpnr) - Open-source place-and-route for supported FPGA families. Activity: 2026-05-15, active.
- [Project IceStorm](http://www.clifford.at/icestorm/) - Open toolchain resources for Lattice iCE40. Activity: 2026-05-19, stable.
- [prjtrellis](https://github.com/YosysHQ/prjtrellis) - Lattice ECP5 bitstream and flow support. Activity: 2026-05-09, active.
- [F4PGA](https://f4pga.org/) - Umbrella project for open FPGA flows, formerly SymbiFlow. Activity: 2025-01-06, active.

## Knowledge and tutorials

- [VHDLwhiz](https://vhdlwhiz.com/) - VHDL-focused tutorials and courses. Activity: 2026-05-19, stable.
- [Beyond Circuits](https://www.beyond-circuits.com/) - FPGA and digital design articles. Activity: 2026-05-19, stable.
- [Adiuvo Engineering](https://www.adiuvoengineering.com/) - MicroZed Chronicles and FPGA/SoC engineering articles. Activity: 2026-05-19, stable.
- [ITSEmbedded](https://www.itsembedded.com/) - Practical RTL, Verilator, and scripted simulation workflows. Activity: 2026-05-19, stable.
- [FPGA4Student](https://fpga4student.com/) - FPGA projects and HDL examples. Activity: 2026-05-19, stable.
- [Numato Lab Knowledge Base](https://numato.com/kb/) - Board-oriented tutorials and examples. Activity: 2026-05-19, stable.
- [FPGA Academy](https://fpgacademy.org/) - Educational FPGA material and labs. Activity: 2026-05-19, stable.
- [Tang Nano Project Series](https://learn.lushaylabs.com/) - Practical Gowin/Tang Nano learning path. Activity: 2026-05-19, stable.
- [SparkFun "So You Want to Learn FPGAs"](https://news.sparkfun.com/1203) - Older but still useful discussion of the FPGA learning curve. Activity: 2013-08-27, legacy.

## Books and evergreen references

- *FPGA Prototyping by Verilog Examples* by Pong P. Chu - Practical Verilog projects for FPGA learning. Activity: 2008, stable.
- *FPGA Prototyping by VHDL Examples* by Pong P. Chu - Practical VHDL projects for FPGA learning. Activity: 2008, stable.
- *Verilog by Example* by Blaine C. Readler - Compact Verilog primer with FPGA-oriented examples. Activity: 2011, stable.
- *100 Power Tips for FPGA Designers* by Evgeni Stavinov - Practical FPGA design tips, scripts, and gotchas. Activity: 2011-06-17, stable.

## Languages and HDL frameworks

- [Verilog/SystemVerilog resources](https://www.chipverify.com/) - Practical language examples and verification-oriented explanations. Activity: 2026-05-19, stable.
- [VHDL resources](https://vhdlwhiz.com/) - Practical VHDL tutorials and design patterns. Activity: 2026-05-19, stable.
- [Chisel](https://www.chisel-lang.org/) - Scala-embedded hardware construction language. Activity: 2026-05-19, active.
- [SpinalHDL](https://spinalhdl.github.io/SpinalDoc-RTD/) - Scala-based hardware description language. Activity: 2026-05-09, active.
- [Amaranth HDL](https://amaranth-lang.org/) - Python-based HDL for FPGA and ASIC-oriented digital design. Activity: 2026-04-28, active.
- [PyMTL3](https://github.com/pymtl/pymtl3) - Python framework for hardware generation, simulation, and verification. Activity: 2026-04-05, active.
- [PyXHDL](https://github.com/davidel/pyxhdl) - Python frontend that generates SystemVerilog and VHDL. Activity: 2026-02-11, active.
- [FloPoCo](https://flopoco.org/) - Generator for fixed- and floating-point arithmetic cores. Activity: 2026-05-19, stable.
- [JSON-for-VHDL](https://github.com/Paebbels/JSON-for-VHDL) - Synthesizable VHDL package for JSON parsing and structured generics. Activity: 2023-07-17, stable.

## Simulation, verification, and debug

### Simulators

- [Icarus Verilog](https://github.com/steveicarus/iverilog) - Free Verilog simulator for quick command-line flows. Activity: 2026-05-17, active.
- [Verilator](https://verilator.org/) - High-performance SystemVerilog simulator and linting tool. Activity: 2026-05-19, active.
- [GHDL](https://ghdl.github.io/ghdl/) - Open-source VHDL analyzer, compiler, simulator, and experimental synthesizer. Activity: 2026-05-18, active.
- [NVC](https://github.com/nickg/nvc) - VHDL compiler and simulator. Activity: 2026-05-18, active.
- [EDA Playground](https://www.edaplayground.com/) - Online HDL simulation across multiple backends. Activity: 2026-05-19, stable.

### Verification frameworks and linting

- [cocotb](https://docs.cocotb.org/) - Python testbenches for HDL designs. Activity: 2026-05-18, active.
- [VUnit](https://github.com/VUnit/vunit) - Automated test runner and verification framework for VHDL/SystemVerilog. Activity: 2026-05-14, active.
- [OSVVM](https://github.com/OSVVM/OsvvmLibraries) - VHDL verification methodology, coverage, randomization, and utility libraries. Activity: 2026-05-16, active.
- [UVVM](https://github.com/UVVM/UVVM) - VHDL verification framework with reusable verification components. Activity: 2026-04-22, active.
- [Verible](https://chipsalliance.github.io/verible/) - SystemVerilog formatting, linting, parsing, and language tooling. Activity: 2026-03-13, active.
- [slang](https://github.com/MikePopoloski/slang) - SystemVerilog compiler and language services toolkit. Activity: 2026-05-18, active.
- [Surelog/UHDM](https://github.com/chipsalliance/Surelog) - SystemVerilog parser and UHDM-based frontend ecosystem. Activity: 2026-05-12, active.

### Debug and diagrams

- [GTKWave](http://gtkwave.sourceforge.net/) - Waveform viewing for VCD/FST traces. Activity: 2026-04-21, active.
- [WaveDrom](https://wavedrom.com/) - Timing diagrams for documentation and interface reviews. Activity: 2026-05-19, stable.
- [OpenOCD](https://openocd.org/) - JTAG access and board debug workflows. Activity: 2026-05-17, active.
- [Sigrok / PulseView](https://sigrok.org/wiki/Main_Page) - Logic analyzer and signal capture tooling. Activity: 2025-11-10, active.
- [FPGA Error Decoder](https://marketplace.visualstudio.com/items?itemName=fpgachat.fpga-error-decoder) - VS Code extension for faster FPGA build error triage. Activity: 2026-05-19, stable.

## Synthesis and implementation

- [Yosys](https://yosyshq.net/yosys/) - Synthesis framework used by many open FPGA flows. Activity: 2026-05-19, stable.
- [nextpnr](https://github.com/YosysHQ/nextpnr) - Place-and-route for iCE40, ECP5, Nexus, Gowin, and other supported targets. Activity: 2026-05-15, active.
- [F4PGA](https://f4pga.org/) - Open FPGA flow umbrella for supported vendor families. Activity: 2025-01-06, active.
- [Project IceStorm](http://www.clifford.at/icestorm/) - Reverse-engineered iCE40 bitstream tools. Activity: 2026-05-19, stable.
- [prjtrellis](https://github.com/YosysHQ/prjtrellis) - Open ECP5/XP2 tooling. Activity: 2026-05-09, active.
- [Verilog-to-Routing](https://verilogtorouting.org/) - Academic FPGA CAD flow and research platform. Activity: 2026-04-23, active.
- [VPR](https://docs.verilogtorouting.org/en/latest/vpr/) - Packing, placement, and routing engine from the VTR flow. Activity: 2026-04-23, active.
- [GHDL Yosys plugin](https://github.com/ghdl/ghdl-yosys-plugin) - VHDL frontend integration for Yosys. Activity: 2026-05-14, active.

## Project workflow and productivity

- [FuseSoC](https://github.com/olofk/fusesoc) - Package manager and build tool for reusable HDL projects. Activity: 2026-05-10, active.
- [Edalize](https://github.com/olofk/edalize) - Backend abstraction for EDA tools, often used with FuseSoC. Activity: 2026-04-24, active.
- [RgGen](https://github.com/rggen/rggen) - Register map generator for RTL, UVM RAL models, headers, and documentation. Activity: 2026-04-19, active.
- [Corsair](https://github.com/esynr3z/corsair) - Register map and RTL/header generator. Activity: 2025-05-24, active.
- [DigitalJS](https://digitaljs.tilk.eu/) - Digital logic simulator and Yosys netlist visualization support. Activity: 2026-05-19, stable.
- [HDLmake](https://hdl.github.io/awesome/items/hdlmake/) - Makefile/dependency workflow for HDL projects; useful mainly for legacy flows. Activity: 2026-04-23, legacy.
- [FPGAMAKE](https://github.com/cambridgehackers/fpgamake) - Vivado Makefile generation from the older Vitorian list. Activity: 2022-05-24, legacy.
- [AccelFury](https://accelfury.com/) - FPGA acceleration workflow and tooling ecosystem. Activity: 2026-05-19, stable.
- [AccelFury/af](https://github.com/AccelFury/af) - Open repository for the AccelFury toolchain. Activity: 2026-05-18, active.

## Vendor tools

- [AMD Vivado](https://www.xilinx.com/products/design-tools/vivado.html) - Primary AMD/Xilinx FPGA design suite. Activity: 2026-05-19, stable.
- [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html) - Intel FPGA design suite. Activity: 2026-05-19, stable.
- [Lattice Radiant](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/RadiantSoftwareSuite) - Lattice design suite for newer device families. Activity: 2026-05-19, stable.
- [Lattice Diamond](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/DIAMOND) - Lattice design suite for older families. Activity: 2026-05-19, stable.
- [Microchip Libero SoC](https://www.microchip.com/en-us/design-centers-and-tools/soc-design-support) - Microchip/Microsemi FPGA design environment. Activity: 2026-05-19, stable.
- [Efinix Efinity](https://www.efinixinc.com/support/) - Efinix FPGA design software. Activity: 2026-05-19, stable.
- [Gowin EDA](https://www.gowinsemi.com/en/support/home/) - Gowin FPGA design software. Activity: 2026-05-19, stable.
- [AMD FPGA devices](https://www.xilinx.com/products/silicon-devices/fpga.html) - Product navigation for AMD/Xilinx FPGA families. Activity: 2026-05-19, stable.
- [Intel FPGA product selector](https://www.intel.com/content/www/us/en/products/details/fpgas.html) - Product navigation for Intel FPGA families. Activity: 2026-05-19, stable.

## Boards and hardware ecosystems

- [Digilent FPGA boards](https://digilent.com/shop/fpga-development-boards-kits-from-digilent/) - Widely used education and prototyping boards. Activity: 2026-05-19, stable.
- [Terasic FPGA boards](https://www.terasic.com.cn/cgi-bin/page/archive.pl?Language=English) - Intel/Altera-oriented development boards. Activity: 2026-05-19, stable.
- [PYNQ](https://www.pynq.io/) - Python-centric Zynq board ecosystem. Activity: 2026-05-19, stable.
- [RocketBoards](https://www.rocketboards.org/) - Intel SoC FPGA board resources. Activity: 2026-05-19, stable.
- [AMD/Xilinx evaluation boards](https://www.xilinx.com/products/boards-and-kits/boards.html) - Official AMD/Xilinx board catalog. Activity: 2026-05-19, stable.
- [Intel FPGA development kits](https://www.intel.com/content/www/us/en/products/details/fpgas/development-kits.html) - Official Intel FPGA development kits. Activity: 2026-05-19, stable.
- [Lattice evaluation boards](https://www.latticesemi.com/Products/DevelopmentBoardsAndKits) - Official Lattice board catalog. Activity: 2026-05-19, stable.
- [FPGA Board Repository](https://boards.fpgadeveloper.com/) - Searchable FPGA board database. Activity: 2026-05-19, stable.
- [Second Life for FPGA boards](https://github.com/iDoka/awesome-fpga-boards) - Repurposed and surplus FPGA boards for hobby and lab use. Activity: 2021-01-12, legacy.

## Reusable IP and reference designs

- [OpenCores](http://opencores.org/) - Community repository of reusable digital IP. Activity: 2026-05-19, stable.
- [LiteX](https://github.com/enjoy-digital/litex) - SoC builder and ecosystem for FPGA systems. Activity: 2026-05-18, active.
- [ZipCPU](https://github.com/ZipCPU) - Open RTL, CPU, bus, and formal verification examples. Activity: 2025-12-08, active.
- [Project F examples](https://github.com/projf) - Compact FPGA projects and tutorial code. Activity: 2026-01-28, active.
- [MiSTer FPGA](https://github.com/MiSTer-devel) - Large open ecosystem for FPGA-based retro computing cores. Activity: 2026-05-19, active.
- [Digilent Vivado Library](https://github.com/Digilent/vivado-library) - Reusable IP and interface definitions for Vivado projects. Activity: 2026-05-19, active.

## Communities and source lists

- [fpga.chat](https://fpga.chat/) - Practical FPGA discussion community. Activity: 2026-05-19, stable.
- [Reddit r/FPGA](https://www.reddit.com/r/FPGA/) - Broad FPGA Q&A and project discussion. Activity: 2026-05-19, stable.
- [Electronics Stack Exchange: FPGA](https://electronics.stackexchange.com/questions/tagged/fpga) - Hardware-focused FPGA questions. Activity: 2026-05-19, stable.
- [Stack Overflow: FPGA](https://stackoverflow.com/questions/tagged/fpga) - Software/tooling-oriented FPGA questions. Activity: 2026-05-19, stable.
- [FPGA Systems list](https://github.com/FPGA-Systems/fpga-awesome-list) - Original community list used as a baseline for this curated English version. Activity: 2026-05-19, stable.
- [Awesome HDL tools](https://hdl.github.io/awesome/categories/tools/) - Source list for HDL/EDA tool discovery. Activity: 2026-05-15, active.
- [Vitorian awesome-fpga](https://github.com/Vitorian/awesome-fpga) - Older FPGA resource list used for durable legacy references. Activity: 2017-05-25, legacy.

## FPGA vendors

- [AMD/Xilinx](https://www.xilinx.com/) - High-end, mid-range, and SoC FPGA families. Activity: 2026-05-19, stable.
- [Intel FPGA](https://www.intel.com/content/www/us/en/products/details/fpgas.html) - Intel/Altera FPGA and SoC FPGA families. Activity: 2026-05-19, stable.
- [Lattice Semiconductor](https://www.latticesemi.com/) - Low-power and small/mid-range FPGA families. Activity: 2026-05-19, stable.
- [Microchip FPGA](https://www.microchip.com/en-us/products/fpgas-and-plds) - PolarFire, IGLOO, SmartFusion, and legacy Microsemi/Actel lines. Activity: 2026-05-19, stable.
- [Achronix](https://www.achronix.com/) - High-performance FPGA and embedded FPGA products. Activity: 2026-05-19, stable.
- [Efinix](https://www.efinixinc.com/) - Trion and Titanium FPGA families. Activity: 2026-05-19, stable.
- [Gowin Semiconductor](https://www.gowinsemi.com/) - Low-cost FPGA families and boards. Activity: 2026-05-19, stable.
- [QuickLogic](https://www.quicklogic.com/) - Low-power FPGA and eFPGA products. Activity: 2026-05-19, stable.
- [Anlogic](https://www.anlogic.com/) - FPGA vendor with regional device families and tools. Activity: 2026-05-19, stable.
- [Cologne Chip](https://www.colognechip.com/) - GateMate FPGA family. Activity: 2026-05-19, stable.
- [NanoXplore](https://nanoxplore.com/) - Radiation-tolerant FPGA products for space and high-reliability markets. Activity: 2026-05-19, stable.

## eFPGA vendors

- [Menta](https://www.menta-efpga.com/) - Embedded FPGA IP. Activity: 2026-05-19, stable.
- [Achronix eFPGA](https://www.achronix.com/) - Speedcore embedded FPGA IP. Activity: 2026-05-19, stable.
- [QuickLogic eFPGA IP](https://www.quicklogic.com/efpga-ip/) - Embedded FPGA hard IP and tools. Activity: 2026-05-19, stable.
- [AdicSys](https://www.adicsys.com/) - Embedded FPGA IP. Activity: 2026-05-19, stable.

## Contributing

Additions should explain why a resource belongs here. A good entry:

- solves a clear FPGA task,
- has a direct public URL,
- is active enough to be useful,
- and has a one-line description plus `Activity:` metadata that helps the reader decide quickly.

Avoid adding generic search pages, duplicate vendor landing pages, personal links without reusable technical value, and resources that only make sense for one private/internal workflow.

## License

MIT
