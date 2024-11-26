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

**Truthtable**
![WhatsApp Image 2024-11-25 at 23 18 12_7186f186](https://github.com/user-attachments/assets/733d7480-af0e-4086-b67f-eb67cbe6c09e)
![WhatsApp Image 2024-11-25 at 23 18 12_edcc2849](https://github.com/user-attachments/assets/35bfa8f0-2063-48f6-9796-1e635dc83926)

**Procedure**

Write the detailed procedure here

**Program:**
```
module exp41(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule

module exp42(df,bo,a,b,bin);

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
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
![Screenshot 2024-11-25 231314](https://github.com/user-attachments/assets/bf69d1b2-b2c9-4da8-96ed-665f438ff5bb)
![Screenshot 2024-11-25 232129](https://github.com/user-attachments/assets/8d1c17f2-f6ec-4e79-ad77-b23ec212bbb6)

**Output Timing Waveform**
![Screenshot 2024-11-25 231503](https://github.com/user-attachments/assets/4b2ac6f5-0d57-4204-8f71-ac9236e4c473)
![Screenshot 2024-11-25 232241](https://github.com/user-attachments/assets/983d8c16-460b-4725-9721-fa234552ae3b)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



