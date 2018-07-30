----------------------------------------------------------------------------------
-- Company: 
-- Engineer: 
-- 
-- Create Date:    14:16:02 09/20/2016 
-- Design Name: 
-- Module Name:    one_bit_fulladder - Behavioral 
-- Project Name: 
-- Target Devices: 
-- Tool versions: 
-- Description: 
--
-- Dependencies: 
--
-- Revision: 
-- Revision 0.01 - File Created
-- Additional Comments: 
--
----------------------------------------------------------------------------------
library IEEE;
use IEEE.std_logic_1164.all;

--AND Gate
entity AND_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end AND_2;
Architecture AND2_str of AND_2 is
begin
	     out1 <= in1 and in2;
end AND2_str;

--OR GATE
library IEEE;
use IEEE.std_logic_1164.all;

entity OR_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end OR_2;
Architecture OR2_str of OR_2 is
begin
	     out1 <= in1 or in2;
end OR2_str;

--XOR GATE
library IEEE;
use IEEE.std_logic_1164.all;

entity XOR_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end XOR_2;

Architecture XOR2_str of XOR_2 is
begin
	     out1 <= in1 xor in2;
end XOR2_str;

-- ONE BIT FULL ADDER
library IEEE;
use IEEE.std_logic_1164.all;

entity FULL_ADDER is
	port(in1,in2, Cin: in std_logic; Cout, Sum: out std_logic);
end FULL_ADDER;

Architecture FULL_ADDER_STR of FULL_ADDER is
component AND_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end component;

component OR_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end component;

component XOR_2 is
	port(in1,in2: in std_logic; out1: out std_logic);
end component;
signal s1,s2,s3: std_logic;
begin
	A1: XOR_2 port map(in1, in2, s1);
	A2: AND_2 port map(in1, in2, s2);
	A3: XOR_2 port map(s1, Cin, Sum);
	A4: AND_2 port map(s1,Cin, S3);
	A5: OR_2 port map(s2,s3,Cout);
end FULL_ADDER_STR;


