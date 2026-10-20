# APB GPIO-Style Register: RTL Design and Simulation

We will design a simple APB-compatible hardware block using SystemVerilog RTL, simulate it, and verify its output using a testbench.

The hardware block will act as an 8-bit register that supports writing data through the APB interface and reading the stored data back.

# 1. Hardware Block Overview

—The design consists of two main components:

```APB Slave Register (apb_slave.sv):``` Implements the APB interface and stores 8-bit data.

```Testbench (testbench.v):```
Acts as an APB master, performs read and write transactions, and checks the output.
