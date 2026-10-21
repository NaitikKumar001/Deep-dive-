# Protocol Specification

Defines the meaning of signals and the rules for their timing and behaviour.

# RTL

Implements these rules in hardware, and the synthesised circuit produces and receives signals through physical connections.

# Protocols

## 1. UART (Universal Asynchronous Receiver-Transmitter)

1. Simplest way to communicate.
2. Uses only 2 wires to communicate.
3. Does not use any clock pulse, so devices rely on baud rate (e.g., 9600, 115200).
4. Used in:
   - Arduino Board
   - GPS
   - Bluetooth adapter cable
   - USB
5. Only connects two devices point-to-point.
6. No inbuilt error correction, so if data gets corrupted during transmission, no one knows until you check manually.
7. Easy to set up, so engineers use it everywhere.
