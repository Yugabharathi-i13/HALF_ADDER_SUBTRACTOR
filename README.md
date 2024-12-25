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

![392014798-2dd87981-402e-4350-9314-e2a47670baca](https://github.com/user-attachments/assets/bbadb8e7-546c-4fdf-beed-7ecec7666a71)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module HALFADDER(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum = a^b;
assign carry = a & b;
endmodule

module SUB(a,b,D,Bo);
input a,b;
output D,Bo; 
assign D = a ^ b;
assign Bo = ~a & b;
endmodule
```


Developed by:Yugabharathi .T RegisterNumber:24900006

**RTL Schematic**

![394198583-f40e2a4e-a6c8-4bd5-8ec6-4c5f9dfa8c43](https://github.com/user-attachments/assets/7bc9c1a0-0e3f-496d-9d4f-840c2d9b8a5f)
![394198783-aec2a8f7-a4a3-4e77-8392-db1220f583b4](https://github.com/user-attachments/assets/b5339af5-c6c0-430e-87f3-4635306bb9d5)

**Output/TIMING Waveform**
![392015423-bd3bffbb-9acd-4c36-ac75-bc913fca618b](https://github.com/user-attachments/assets/94129fcf-f1be-44bc-b135-12cdef79a02c)
![392016705-c921e6c7-cf3b-48db-85f9-c97b50ed478c](https://github.com/user-attachments/assets/82389943-e071-44d0-aa62-ba13c786eda9)

**Result:**
Thus the half adder and half subtractor are designed and their truth table is verified.
