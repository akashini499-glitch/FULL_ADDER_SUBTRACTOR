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

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule



Developed by:AKASHINI V
RegisterNumber:25016886
*/

**RTL Schematic**
<img width="706" height="317" alt="Screenshot 2025-11-26 185548" src="https://github.com/user-attachments/assets/c6f4dae9-cec8-4049-873e-396010c91de9" />
<img width="892" height="439" alt="Screenshot 2025-11-26 205903" src="https://github.com/user-attachments/assets/0fd9aa7a-9047-46c0-86b9-56da5a84e1f1" />


**Output Timing Waveform**
<img width="1919" height="1022" alt="Screenshot 2025-11-26 185735" src="https://github.com/user-attachments/assets/c117e87a-a359-413e-ba69-c5f9f877f514" />
<img width="1919" height="1025" alt="Screenshot 2025-11-26 210155" src="https://github.com/user-attachments/assets/ffb6273d-5d75-4a11-80bd-5e394a5c530c" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



