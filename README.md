##  RVCE FPGA Workshop Repository

Welcome to the official repository for the **RVCE Hands-on Workshop on FPGA, UART, and RISC-V**. This repo contains all the source code, examples, and instructions for the sessions conducted by [Kunal ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/).


###  Workshop Objectives

- Blink LEDs using Verilog and FPGA toolchain

- Communicate via UART using `picocom`

- Perform UART loopback tests

- Interface real-time sensors 

- Explore minimal RISC-V processor integration

***
###  Requirements

Install the following tools:


####  Toolchain Setup (Linux)

```
sudo apt update
sudo apt install -y git build-essential yosys nextpnr-ice40 icestorm picocom
```
####  To verify installation:

```
yosys -V
nextpnr-ice40 --version
```

***
###  Cloning the Repo
```
git clone https://github.com/Skandakm29/rvce_workshop.git
cd rvce_workshop
```

***
###  How to Use Each Project

####  LED Blinking

```
cd led_blinking
make flash
```
####  UART Loopback
```
cd uart_loopback
make flash
sudo make terminal
```
####  UART Transmit/Receive

```
cd uart
make flash
sudo make terminal
```
####  Sensor Interface

```
cd Real-Time-Sensor-Data-Acquisition-and-Transmission-System
make flash
sudo make terminal
```
***


###  UART Terminal

To test UART using `picocom`:

```
sudo picocom -b 9600 /dev/ttyUSB0 --echo
```
You can type characters to send and receive (loopback).


