# Protocol Specification

Defines the meaning of signals and the rules for their timing and behaviour.

# RTL

Implements these rules in hardware, and the synthesised circuit produces and receives signals through physical connections.

# Protocols

## 1. UART (Universal Asynchronous Receiver-Transmitter)
![UART](./Screenshot_20261020_195115_YouTube.jpg)

1. Simplest way to communicate.
2. Uses only 2 wires to communicate.
   - Transmission wire [TX]
   - Receiver wire [RX]

   ![UART RX Signal](./Screenshot_20261020_195142_YouTube.jpg)
   
4. ASYNCHRONOUS :- Does not use any clock pulse, so devices rely on baud rate (e.g., 9600, 115200).
5. Used in:
   - Arduino Board
   - GPS
   - Bluetooth adapter cable
   - USB
6. Only connects two devices point-to-point.
7. No inbuilt error correction, so if data gets corrupted during transmission, no one knows until you check manually.
8. Easy to set up, so engineers use it everywhere.
