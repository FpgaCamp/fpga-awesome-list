# Awesome FPGA

Practical, English-speaking resource list for people building FPGA projects: study, design, verify, implement, and deploy.

This list is structured for actual engineering workflows, not just bookmarks.
Primary flow: **learn → build RTL → verify → implement → hardware bring-up → productionize**.

## Table of Contents

- [How to use this list](#how-to-use-this-list)
- [Learning paths](#learning-paths)
- [Knowledge and tutorials](#knowledge-and-tutorials)
- [Tools and toolchains](#tools-and-toolchains)
- [Verification and debug](#verification-and-debug)
- [Reference designs and reusable IP](#reference-designs-and-reusable-ip)
- [Boards and ecosystems](#boards-and-ecosystems)
- [Communities](#communities)
- [Vendors](#vendors)
- [eFPGA vendors](#efpga-vendors)
- [Contributing](#contributing)
- [License](#license)

## How to use this list

- If you are new: start with **Learning paths** and build one small project in the first week.
- If you are already coding HDL: use **Tools and toolchains** + **Verification and debug** to optimize your workflow.
- If you are planning a new platform: check **Boards and ecosystems** before choosing a vendor.

Use the short one-line descriptions to pick practical options for your context (cost, openness, complexity, and support).

## Learning paths

### Beginner path (first FPGA project)

- [FPGA Tutorial](https://www.fpgatutorial.com/) – structured fundamentals and first design ideas.
- [Nandland](https://www.youtube.com/@nandland) – practical HDL examples in clear sequence.
- [fpga4fun](https://www.fpga4fun.com/) – many small projects for initial hands-on learning.
- [Project F](https://projectf.io/) – compact practical examples and clear architecture notes.
- [ZipCPU](https://zipcpu.com/) – project-oriented notes and RTL patterns.

### RTL-first path

- [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) – exercises for syntax, FSMs, timing, interfaces.
- [ASIC-World](https://www.asic-world.com/) – Verilog/SystemVerilog reference material.
- [chipverify](https://www.chipverify.com/) – practical HDL design and language references.
- [VHDLwhiz](https://vhdlwhiz.com/) – practical VHDL-based learning.
- [Project F: FPGA Design](https://projectf.io/) – design-focused tutorials and practical use cases.

### Verification-first path

- [Edaplayground](https://www.edaplayground.com/) – run HDL simulations quickly in browser.
- [Verification Guide](https://www.verificationguide.com/) – methodical SystemVerilog verification notes.
- [Testbench.in](https://testbench.in/) – practical verification articles and examples.
- [Verification Academy](https://www.verificationacademy.com/) – practical verification course material.

### Open-source flow path

- [Yosys](https://yosyshq.net/yosys/) – open HDL synthesis.
- [NextPNR](https://github.com/YosysHQ/nextpnr) – open P&R for supported FPGA families.
- [SymbiFlow](https://symbiflow.github.io/) – open FPGA implementation ecosystem.
- [Project IceStorm](http://www.clifford.at/icestorm/) – toolchain resources for Lattice ICE.
- [prjtrellis](https://github.com/YosysHQ/prjtrellis) – open flows for Lattice ECP5.

## Knowledge and tutorials

- [FPGA Tutorial - YouTube](https://www.youtube.com/results?search_query=FPGA+Tutorial) – broad video entry point.
- [ITSEmbedded](https://www.itsembedded.com/) – practical workflow and simulation examples.
- [Numato Lab](https://numato.com/blog/) – hardware-oriented learning projects.
- [Learn FPGA easily](https://www.learn-fpga-easily.com/) – practical introduction portal.

### Books

- *FPGA Prototyping by Verilog Examples* (Pong Chu)
- *FPGA Prototyping by VHDL Examples* (Pong Chu)

## Tools and toolchains

### Vendor tools

- [AMD/Xilinx Vivado](https://www.xilinx.com/products/design-tools/vivado.html)
- [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html)
- [Intel Quartus Prime Pro](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime-pro.html)
- [Lattice Radiant](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/RadiantSoftwareSuite)
- [Microchip Libero SoC](https://www.microchip.com/en-us/design-centers-and-tools/soc-design-support)
- [Lattice Diamond](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/DesignSoftware/DIAMOND)

### Open-source tools

- [Yosys](https://yosyshq.net/yosys/)
- [Icarus Verilog](https://github.com/steveicarus/iverilog)
- [GHDL](https://ghdl.github.io/)
- [Verilator](https://verilator.org/)
- [NVC](https://github.com/nickg/nvc)
- [Verible](https://chipsalliance.github.io/verible/)
- [FuseSoC](https://github.com/olofk/fusesoc)
- [CocoTB](https://docs.cocotb.org/)
- [Tensil](https://www.tensil.ai/)
- [Testonica](https://qi.testonica.com/)
- [DigitalJS](https://digitaljs.tilk.eu/)
- [AccelFury](https://accelfury.com/) – hardware acceleration and FPGA workflow tooling.
- [AccelFury/af](https://github.com/AccelFury/af) – repository for the AccelFury FPGA toolchain ecosystem.

### Utility and productivity

- [Verilator docs](https://verilator.org/guide/latest/) – practical guidance on fast simulation workflows.
- [OpenROAD](https://theopenroadproject.org/) – broader open tooling for implementation research.
- [OpenOCD](http://openocd.org/) – JTAG/debug programming support.
- [FuseSoC docs](https://fusesoc.readthedocs.io/) – package/dependency flow for HDL components.
- [FPGA Error Decoder](https://marketplace.visualstudio.com/items?itemName=fpgachat.fpga-error-decoder) – VS Code extension for faster FPGA build error triage.

## Verification and debug

- [GTKWave](http://gtkwave.sourceforge.net/) – waveform inspection and signal debugging.
- [WaveDrom](https://wavedrom.com/) – timing diagrams and wave visualization.
- [cocotb](https://docs.cocotb.org/) – Python-based verification.
- [GHDL + GTKWave stack](https://github.com/ghdl/ghdl) – VHDL simulation with practical debug.
- [cocotb simulator support matrix](https://docs.cocotb.org/en/stable/simulator_support.html) – compare supported simulators.

## Reference designs and reusable IP

- [OpenCores](https://opencores.org/) – reusable IP blocks and community projects.
- [ZipCPU](https://zipcpu.com/) – RTL project source material with practical engineering notes.
- [opencores projects](https://opencores.org/projects) – indexed reusable IP discovery.

## Boards and ecosystems

- [Digilent](https://digilent.com/) – broad educational and hobby FPGA boards.
- [PYNQ](https://www.pynq.io/) – Python-centric development boards and ecosystem.
- [RocketBoards](https://www.rocketboards.org/) – Intel-aligned reference platforms.
- [Xilinx Evaluation Boards](https://www.xilinx.com/products/boards-and-kits/boards.html)
- [Intel FPGA boards](https://www.intel.com/content/www/us/en/products/details/fpgas.html)

## Communities

- [Reddit - FPGA](https://www.reddit.com/r/FPGA/)
- [Stack Overflow - FPGA](https://stackoverflow.com/questions/tagged/fpga)
- [Electronics Stack Exchange - FPGA](https://electronics.stackexchange.com/questions/tagged/fpga)
- [fpga4student](https://fpga4student.com/)
- [fpga.chat](https://fpga.chat/) – practical FPGA discussion community.

## Vendors

- [AMD/Xilinx](https://www.xilinx.com/)
- [Intel](https://www.intel.com/)
- [Lattice](https://www.latticesemi.com/)
- [Microchip](https://www.microchip.com/)
- [Achronix](https://www.achronix.com/)
- [Efinix](https://www.efinixinc.com/)
- [Anlogic](https://www.anlogic.com/)
- [QuickLogic](https://www.quicklogic.com/)
- [GoWin](https://www.gowinsemi.com/)
- [Renesas/Dialog](https://www.renesas.com/us/en/)

## eFPGA vendors

- [Menta](https://www.menta-efpga.com/)
- [Flex Logix](https://www.flex-logix.com/)
- [Achronix](https://www.achronix.com/)
- [AdicSys](https://www.adicsys.com/)

## Contributing

This list is intended to stay practical. Priorities for additions:

- Use clear English one-line descriptions.
- Prefer official documentation over mirrors.
- Prefer actively maintained projects with visible examples and community use.
- Add links that help users go from reading to implementation quickly.

Please open an issue or PR with:

- short context (what problem it helps solve),
- placement suggestion (which section),
- and one-line description updated to this style.

## License

MIT
