# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![image](https://github.com/user-attachments/assets/0fdffebb-b32e-4f94-96c7-27d9b1418226)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Jisha Bossne SJ RegisterNumber: 24900154 */
```
module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=(a^b);
assign carry=(a&b);
endmodule
```
```
module hs(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=(~a&b);
endmodule
```
**RTL Schematic**

Half-adder:

![funct3](https://github.com/user-attachments/assets/0aa9f1fc-a7a1-4cac-bcd7-9581b8448a00)

Half-subtractor:

![funct4 rtl](https://github.com/user-attachments/assets/38648580-5509-49ff-b279-a91ee08d3642)

**Output/TIMING Waveform**

Half-adder:

![funct3 last op](https://github.com/user-attachments/assets/d0c86249-cb4b-48cf-afb0-eff61e3e1cea)

Half-subtractor:

![funct4](https://github.com/user-attachments/assets/49ddc961-45a4-48fd-bcbd-5de18177e965)


**Result:**

Half adder and half subtractor circuit and its truth table in Quartus using Verilog
programming is verified
