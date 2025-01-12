# TV80

Source: https://opencores.org/ocsvn/tv80/tv80/trunk 


## Description

The TV80 is an 8-bit Z80-compatible microprocessor core, written in Verilog. It is based on Daniel Wallner's VHDL T80 core.

## Features

- executes 8080/Z80 instruction set
- cycle timing is similar to original Z80
- small die area
- sample peripheral with GMII interface
- Optional Wishbone wrapper for TV80 core now available

## T80 Overview

### Description

Configurable cpu core that supports Z80, 8080 and gameboy instruction sets. Z80 and 8080 compability have been proven by numerous implementations of old computer and arcade systems. It is used in the zxgate project, a zx81, zx spectrum, trs80 and Jupiter ACE clone project. And also in the FPGA Arcade project. A Z80 SoC debug system with ROM, RAM and two 16450 UARTs is included in the distribution. It is possible to run the NoICE debugger on this system. Batch files for runnning XST and Leonardo synthesis can be found in syn/xilinx/run/. Check these scripts to see how to use the included VHDL ROM generators. Before you can run the scripts you need to compile hex2rom and xrom or download binaries from here. You must also replace one of the hex files in sw/ or change the batch files to use another hex file. The z88dk C compiler can be used with T80. The "embedded" configuration can be used with the debug system without modifications. Browse source code here. Download latest tarball here. Thanks to MikeJ for some serious debugging and to the zxgate project members for invaluable Z80 information.

### Features

- Technology independent
- Up to 35MHz clock in Spartan2 -5 using XST synthesis
- 10k gates and up to 100MHz in 0.18 CMOS
- Supports all undocumented Z80 instructions
- Supports all Z80 interrupt modes
- Correct R register behaviour
- Correct Z80 instruction timing
- Almost 100% correct behavior of the undocumented Z80 flags
- Both a synchronous (for implementation) and an asynchronous (for board level simulations) Z80 top level
- Only a synchronous 8080 top level

### Status

- Z80 compability and functionality thoroughly verified in FPGA
- The gameboy mode is experimental
- No gameboy top level
