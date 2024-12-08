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

FULL ADDER

![IMG-20241208-WA0007](https://github.com/user-attachments/assets/c0ec2f9a-6d17-40f9-9f54-11d11549471b)

FULL SUBTRACTOR
![IMG-20241208-WA0010](https://github.com/user-attachments/assets/dbcb7421-2702-4424-94f6-5cb105d6012a)
**Procedure**

1 Type the program in Quartus software.

2 Compile and run the program.

3 Generate the RTL schematic and save the logic diagram.

4 Create nodes for inputs and outputs to generate the timing diagram.

5 For different input combinations generate the timing diagram


**Program:**
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule

```
Developed by:latchaya priyan S

RegisterNumber:24900388


**RTL Schematic**

FULL ADDER
![IMG-20241208-WA0009](https://github.com/user-attachments/assets/a0a840fe-0a5c-4afb-8a87-d6b4ecc52678)

FULL SUBTRACTOR

![IMG-20241208-WA0008](https://github.com/user-attachments/assets/b68fa72f-1b6e-4919-a6cc-28cbfe6b2caf)


**Output Timing Waveform**

FULL ADDER
![IMG-20241208-WA0011](https://github.com/user-attachments/assets/c053d43c-12f2-405f-8fbb-0b94fb624234)

FULL SUBTRACTOR
![IMG-20241208-WA0012](https://github.com/user-attachments/assets/076a7bdb-f8c4-447a-a95b-5709ebd47916)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



