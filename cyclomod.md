# Notes for use with CycloMod

This is intended to be used with the CycloMod board:
[https://github.com/gsteiert/cyclomod](https://github.com/gsteiert/cyclomod)

## Pins
| Define       | GPIO | Connection | Notes |
| ------------ |:----:|:----------:| ----- | 
| PIN_TDI      | 7    | FPGA TDI   | 
| PIN_TDO      | 4    | FPGA TDO   | 
| PIN_TCK      | 6    | FPGA TCK   | 
| PIN_TMS      | 5    | FPGA TMS   | 
| PIN_RST      | 2    | NC         | Not used
| PIN_TRST     | 3    | NC         | Not used
| PIN_LED      | 28   | NC         | Not used
| PIN_UART0_TX | 12   | FPGA B4    | FPGA RX 
| PIN_UART0_RX | 13   | FPGA A5    | FPGA TX
| PIN_UART1_TX | 26   | M.2 A0     | External UART
| PIN_UART1_RX | 27   | M.2 A1     | External UART
| PIN_CLK_OUT  | 21   | FPGA B8    | 12MHz Clock

* The JTAG is connected directly to the FPGA.  RST and TRST are unused.
* UART0 is connected to the FPGA, UART1 is connected to A0 and A1.
* *Turn off UART1 if you connect analog signals to A0 or A1*
* The 12MHz oscilator is output on CLOCK0 to provide a reference clock for the FPGA.  
* The schematic shows pin definitions for the 10CL16, but the initial batch is populated with 10CL10.  FPGA pin B8 is not a clock input on 10CL10.
