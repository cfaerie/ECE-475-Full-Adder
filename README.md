# ECE 475 Full Adder
Lab 1
Code Authors: Rachel & Danya

This lab served as an introduction to VHDL and using it within Xilinx. 
Students will also observe the RTL schematic that Xilinx generates based on the VHDL code.
The emphasis of this lab is on structural modeling.

We will design a full adder using structural modeling. 
Test the model by writing VHDL test bench code and generating a waveform of expected I/O.
Finally, we will load the code to the Xilinx development board and perform physical tests.

Equipment Used:
Xilinx ISE, iSim, iMPACT
ML501 Xilinx board with Virtex-5 LX Xilinx chip

Full Adder Truth table
INPUTS              OUTPUTS
cin in2 in1         cout  sum
0   0   0             0     0  
0   0   1             0     1 
0   1   0             0     1
0   1   1             1     0
1   0   0             0     1 
1   0   1             1     0
1   1   0             1     0 
1   1   1             1     1

These inputs and outputs must be mapped to switches and LEDs on the development board,
for the physical testing of the design.
