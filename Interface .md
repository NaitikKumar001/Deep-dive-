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

![Configuration of UART Before Transmission, UART Data Format, and Advantages](./file_00000000954c81fab1d0cd15f52d658b.png)

# 2. SPI (Serial Peripheral Interface)

1. SPI is a serial peripheral interface.
2. It is good in protocol speed and performance compared to UART.
3. It uses 4 wires

1. **SS/CS** →If multiple slaves connect with master, then for every slave, SS/CS line is separate.

2. **SCLK** → Serial clock to provide clock signals.
4. **MOSI** → Master Out Slave In  
   → Line to send data from Master.
   ![MOSI Communication](Screenshot_20261020_200030_YouTube.jpg)
6. **MISO** → Master In Slave Out  
   → Line to receive data from Slave.
   ![MISO Communication](Screenshot_20261020_200100_YouTube.jpg)

## Data Transfer

1. **Half Duplex:** One of them can send data to another at one time.

2. **Full Duplex:** Both of them can send data to each other at a time.

## Diagram

```text
          MOSI
Master ───────────────► Slave

          MISO
Master ◄─────────────── Slave

          SCLK
Master ───────────────► Slave

          SS/CS
Master ───────────────► Slave
```
5. Some SPI devices can operate at high speeds about 50 mbps.
6. We see it in:
   - SD cards
   - Flash memory
   - Display screens

7. Disadvantage:
   - To connect multiple devices, we need a separate CS (Chip Select) wire for each device.

8. When to use:
   - In a circuit board where fast speed is required but fewer devices are connected.

# 3. I²C (Inter-Integrated Circuit)

1. It removes the biggest disadvantage of SPI.
2. It uses only 2 wires:
   - SCL (Serial Clock Line)
   - SDA (Serial Data Line)

3. Over 127 devices can be connected using these 2 wires, depending on device addresses and bus configuration.

4. We use it in:
   - Temperature sensors
   - OLED displays
   - Gyroscopes
