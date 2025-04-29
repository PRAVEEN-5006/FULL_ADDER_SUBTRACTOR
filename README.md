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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: PRAVEEN P B
RegisterNumber:212224050032
*/
```
module exp04(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor (sl,a,b);
and (cl,a,b);
xor (sum,sl,cin);
and (c2,sl,cin);
or (cout,c2,cl);
endmodule
```
```
module exp04(df,bo,a,b,bin);
input a,b,bin;
output df,bo;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

**RTL Schematic**
![Screenshot 2025-04-29 161300](https://github.com/user-attachments/assets/4321cca4-f5e7-4a4b-81be-d5a97e189ade)

![Screenshot 2025-04-29 161333](https://github.com/user-attachments/assets/0723ea93-6e12-45d9-a30e-843c28afb54d)


**Output Timing Waveform**
![Screenshot 2025-04-29 161355](https://github.com/user-attachments/assets/16a71dab-7d41-443c-8be2-4385c757f5c3)

![Screenshot 2025-04-29 161419](https://github.com/user-attachments/assets/76502a9a-aebf-4a6a-8b01-bf5619b309fb)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



