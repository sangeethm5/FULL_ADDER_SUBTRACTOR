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

 **FULL ADDER**
 
 
 <img width="733" height="706" alt="image" src="https://github.com/user-attachments/assets/c6a639c8-1704-47d3-bc69-87cc7c73f528" />
 


**FULL SUBTRACTOR**

<img width="654" height="667" alt="image" src="https://github.com/user-attachments/assets/93f3f148-a25b-45f2-9a09-80f737becd79" />


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sangeeth M
RegisterNumber:212225100043
*/
**FULL ADDER**
module exp4(df,bo,a,b,bin);
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

**FULL SUBTRACTOR**
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule


**RTL Schematic**

**FULL ADDER**

<img width="814" height="373" alt="image" src="https://github.com/user-attachments/assets/9edd69bd-0850-49d1-8e2b-7526bcbeda54" />

**FULL SUBTRACTOR**


<img width="807" height="384" alt="image" src="https://github.com/user-attachments/assets/69101578-a37c-46be-8355-2f8ee91ed5b8" />



**Output Timing Waveform**

**FULL ADDER**


<img width="1919" height="354" alt="image" src="https://github.com/user-attachments/assets/a43f9135-c7d2-4738-888e-4ba7e5cbe093" />


**FULL SUBTRACTOR**


<img width="823" height="432" alt="image" src="https://github.com/user-attachments/assets/2ae5be7c-04e5-4b84-b243-478e0f6929a5" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



