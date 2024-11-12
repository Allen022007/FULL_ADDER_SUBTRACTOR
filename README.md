# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable** :

![WhatsApp Image 2024-11-12 at 13 49 12_c2f2d3d0](https://github.com/user-attachments/assets/15e43241-c655-4831-b0b6-0832a062b562)

![WhatsApp Image 2024-11-12 at 13 49 13_3287dede](https://github.com/user-attachments/assets/ca9d7422-fc09-4062-98e3-13dc6e3e2142)

**Procedure**

Write the detailed procedure here

**Program:**
~~~
//full adder
module Exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(C1,a,b);
xor(sum,s1,cin);
or(cout,c2,c1);
endmodule
~~~

~~~
module EXP_4 (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
~~~


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: W Allen Johnston Ozario
RegisterNumber: 24900645
*/

**RTL Schematic :**

![Exp4](https://github.com/user-attachments/assets/44f58eb0-0898-47b6-b28f-9934229309ef)

![Exp4 subtractor](https://github.com/user-attachments/assets/042a54a6-14c6-40e6-8e18-67730860d37e)

**Output Timing Waveform :**

![waveform](https://github.com/user-attachments/assets/2854343a-3833-4635-81d4-a2047d2ae091)

![waveform subtractor](https://github.com/user-attachments/assets/fea10aa6-fd3e-4e62-bbf1-7a5c6b21d99f)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



