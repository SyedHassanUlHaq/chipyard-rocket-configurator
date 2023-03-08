# chipyard-rocket-configurator

This repo contains JSON parameters for configuring a chipyard rocket chip.

## What is chipyard?

Chipyard is an open source framework for agile development of Chisel-based systems-on-chip. It allows you to leverage the Chisel HDL, Rocket Chip SoC generator, and other Berkeley projects to produce a RISC-V SoC with everything from MMIO-mapped peripherals to custom accelerators.

## What is rocket chip?

Rocket Chip is a SoC generator initially developed by UC Berkeley and now mostly maintained by SiFive. The SoC can be configured with a single or multiple processor cores, such as the in-order Rocket cores or the out-of-order BOOM cores.

## How to use JSON parameters for configuration?

JSON parameters are used to specify various aspects of the SoC design, such as core type, frequency, cache size, memory map, etc. You can find some examples of JSON parameters in this repo. To use them, you need to pass them as an argument to the rocket-chip generator using `--config` option. For example:

```bash
make CONFIG=chipyard-rocket-configurator/MyConfig.json
```
This will generate a Verilog file for your SoC design based on your JSON parameters.

# How to run simulations and tests?
You can use various tools integrated with chipyard to run simulations and tests on your SoC design. For example, you can use Verilator for cycle-accurate simulation, FireSim for FPGA-accelerated simulation and benchmarking, or Hammer for VLSI implementation. Please refer to the chipyard documentation for more details.

# How to contribute?
If you have any suggestions or improvements for this repo, please feel free to open an issue or a pull request.😊
