# Name: HAREESH R
# Roll No: 23013706
# Experiment 03: Implementation of Half Adder and Full Adder circuit
# AIM
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.
# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime
# Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

# Procedure

Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.






# Program:
### Half adder
module HalfAdder(a,b,sum,carry);

input a,b;

output sum,carry;

assign sum=a^b;

assign carry=a&b;

endmodule

### Full adder
module Fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum=((a^b)^c);

assign carry=((a&b) | (b&c) | (c&a));

endmodule

# RTL realization
### Half adder
![halfadder rtl](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/6a1abfba-62c2-4c48-baa3-91a0a2303638)


### Full adder
![full rtl](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/c46541cb-e9e1-433c-a345-6a2181213eec)



# Truth Table
### Half adder
![half truth](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/5afacc88-ff73-4fcf-9059-072464d87532)


### Full adder

![full truth](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/b4d85508-9990-4a85-93f6-51dd397e6c33)

# Timing Diagram
### Half adder

![half timing](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/8010b863-164c-4143-9d19-95a71ba0a9e2)

### Full adder
![full timing](https://github.com/HareeshrajaR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870459/4b432e84-c16b-4c5a-9820-82b23994d4ad)

# Result
Hence, the output is verified successfully.
