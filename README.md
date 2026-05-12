# Power over Ethernet(PoE) Development Board

A Power over Ethernet interface board for connecting an ESP32 development board to wired Ethernet using a W5500 Ethernet controller.

The board is designed to receive both power and network data through a single Cat5e Ethernet cable. The W5500 handles the Ethernet interface, while the ESP32 communicates with it over SPI.

## Project Status

In progress.

Current focus:
- Schematic design
- W5500 Ethernet interface
- ESP32 header pinout
- PoE MagJack integration
- SPI firmware bring-up

## System Overview

The Ethernet connector splits the design into two main paths:

```text
Cat5e Ethernet Cable
        |
        v
PoE-Compatible MagJack
        |
        +---- Ethernet Data Path ----> W5500 Ethernet Controller ----> ESP32 over SPI
        |
        +---- PoE Power Path --------> PoE 5 V Module ---------------> ESP32 5 V Input
