# FULL_ADDER_SUBTRACTOR

BLESSING S (24002843)

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

FULL ADDER:

![image](https://github.com/user-attachments/assets/b4ff5cba-86bf-418f-93df-ecbafe89af90)

FULL SUBTRACTOR:

![image](https://github.com/user-attachments/assets/803db6ad-ed68-4201-bb24-0b0cc3c8c1a6)

**Procedure**

Write the detailed procedure here

**Program:**

FULL ADDER:

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

FULL SUBTRACTOR:

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

**RTL Schematic**

FULL ADDER:

![image](https://github.com/user-attachments/assets/fae071af-75ba-4ad5-96fb-bd3e967a5168)

FULL SUBTRACTOR:

![image](https://github.com/user-attachments/assets/490226bd-ec89-4eba-9bcd-039f1d864927)

**Output Timing Waveform**

FULL ADDER:

![image](https://github.com/user-attachments/assets/99de6065-76f0-430f-a30a-09b47fb057ad)

FULL SUBTRACTOR:

![image](https://github.com/user-attachments/assets/a2297dcd-5a58-4b7f-a19a-763a3ed7d13e)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



