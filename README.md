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

![image](https://github.com/user-attachments/assets/df7749f9-1c14-4bf1-bf69-37c0ea0fe47a)

![image](https://github.com/user-attachments/assets/031c35d6-eb65-478e-be66-c3f5aaccfce6)


**Procedure**
~~~
🔹 Full Adder Procedure
Inputs: A, B, Cin
Outputs: Sum, Cout

Sum = A ⊕ B ⊕ Cin

Cout = (A · B) + (B · Cin) + (Cin · A)

🔹 Full Subtractor Procedure
Inputs: A, B, Bin (borrow-in)
Outputs: Diff, Bout

Diff = A ⊕ B ⊕ Bin

Bout = (¬A · B) + (¬(A ⊕ B) · Bin)

~~~

Write the detailed procedure here

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Rihan Ahamed.S
RegisterNumber:212224040276


~~~
Program: FULL ADDRER:
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
FULL SUBTRACTOR:
module fsexp(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule




~~~
**RTL Schematic**

![image](https://github.com/user-attachments/assets/8d0a9779-6b57-4d7a-807c-b0fb767573ca)
![image](https://github.com/user-attachments/assets/fe18e03d-9ff3-4b4d-909f-abc05642ed20)


**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/056142ec-f487-4c81-b2bf-f765768fe735)
![image](https://github.com/user-attachments/assets/e91c9923-510e-411d-959d-f6ee47327571)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



