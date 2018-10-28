# Design Your Own Computer #

Welcome to this series where you will learn how to *Design Your Own Computer* on an FPGA!

## Overview of series ##

In the first few episodes we'll be focussing on the VGA output, essentially
building a (small) GPU. The reason is that this will give us excellent 
possibilities later on to view the internal state of the CPU.

Later we'll design and implement the 6502 processor. This is the same processor
that was used in e.g. the Commodore 64 computer from the 1980's. There is
an abundance of information on this processor on the Internet. In later episodes
I'll provide more links.

In the end I would like to build an online multi-player game that can run on this computer.

Of course, the ultimate goal is to have fun building stuff!

## Overall design ##

The computer we're building will be running on an FPGA board, and inside the FPGA there will be:
* VGA interface (GPU)
* Memory (RAM and ROM)
* 6502 CPU
* Keyboard interface
* Ethernet interface

We will be designing and building these blocks roughly in the above order.

## List of episodes: ##
### VGA ###
### Memory ###
### CPU ###
### VGA part 2 ###
### Keyboard ###
### Ethernet ###
### VGA part 3 ###

More to come soon...

## Prerequisites ##

### FPGA board ###

To get started you need an FPGA board. There are many possibilities, e.g.
* [Nexys 4 DDR](https://reference.digilentinc.com/reference/programmable-logic/nexys-4-ddr/start)
(from Digilent). This is the one I am using (but somewhat of an overkill for this project).
* [Basys 3](https://reference.digilentinc.com/reference/programmable-logic/basys-3/start)
(from Digilent). Less expensive.
* [Go board](https://www.nandland.com/goboard/introduction.html)
(from Nandland). Even less expensive.

Make sure that the FPGA board you buy has (at least) the following features:
* VGA connector
* USB input connector (for keyboard)
* Crystal oscillator
* Ethernet PHY (optional)

### FPGA toolchain (software) ###

You need a tool chain for programming the FPGA. There are three major FPGA vendors:
* Xilinx
* Intel (formerly Altera)
* Lattice

The Nexys 4 DDR board uses a Xilinx FPGA, and the toolchain is called
[Vivado](https://www.xilinx.com/support/download.html).
Use the Webpack edition, because it is free to use.

## Recommended additional information ##

I recommend watching the video series 
[Building an 8-bit breadboard computer!](https://www.youtube.com/playlist?list=PLowKtXNTBypGqImE405J2565dvjafglHU)
by Ben Eater. He goes into great depth explaining the concepts and elements in
a computer. The design we're building will be somewhat more elaborate and have
more features. This is largely due to the many possibilities of using FPGAs.

I also recommend watching (at least the first half of) the video series
[Computation Structures](https://www.youtube.com/playlist?list=PLqAMlAbd8sIuiuk_yJeqCWWxe7jxWgswj)
from MIT. These are university lectures explaining very clearly the concepts involved in digital design.

I will in this series assume you are at least a little familiar with logic
gates and digital electronics.

I will also assume you are comfortable in at least one other programming
language, e.g. C, C++, Java, or similar.

## About me ##

I'm currently working as a professional FPGA developer, but have previously
been teaching the subjects mathematics, physics, and programming in High School.
Before that I've worked for twelve years as a software developer.

As a child I used to program in assembler on the Commodore 64. This "heritage"
is reflected in some of the design choices for the present project, e.g.
choosing the 6502 processor.

