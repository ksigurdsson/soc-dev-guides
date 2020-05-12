.. SoC Development Guides: Directory Structure

*******************
Directory Structure
*******************


Overview
========

This document provides a common directory structure intended to:

* Ensure a common directory layout


Design
======

Directory structure within the design directory:
*TBC*


Verification
============

Directory structure within the verif directory::

  verif/
  |-- cdc              Everything related to Clock Domain Crossing checks.
  |-- formal           Everything related to formal verification.
  |-- lint             Everything related to linting.
  |-- sva              Everything related to SystemVerilog Assertions.
  |-- models           [optional] Modules common between directed and mdv testbenches.
  |-- directed         Files specific to directed testing, usually written by designer.
  |                    It may have additional directories underneath similar to the mdv directory if desired.
  `-- mdv              Files specifit to Metric Driven Verification (typically UVM).
      |-- env          The environment and components that the tests use. In UVM, they would typically be extended from uvm_component or similar classes.
      |-- sequences    The sequences that the tests use. (Not more than one class per file please). In UVM, they would typically extend from uvm_sequence_item.
      |-- tests        The actual tests. In UVM, they would typically extend from uvm_test (or a base class that extends from uvm_test).
      |-- tbench       The testbench itself. Also any components, interfaces etc. that the testbench instances.
      |-- scripts      All scripts for simulation, coverage collection and processing, signal lists for waveform viewer etc.
      `-- sim          Simulation directory. Should not contain any files that are under version control, but rather is a dumping ground for temporary simulation files.


Build
=====

Directory structure within the build directory:
**TBC**


Naming Rules
============

**Needs moved to different section TBD**

* All SystemVerilog files that are ```included`` in packages etc must be suffixed ".svh"!
* All SystemVerilog files that are compiled directly (not ```included``) via a .f file
  or directly on the compiler's command line must be suffixed ".sv"!
