## NAME:V.SHREYA
## REG NO:24000632
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

![Screenshot 2024-12-08 204714](https://github.com/user-attachments/assets/eb374568-42b4-43ca-9024-97d3f5599cf2)
![Screenshot 2024-12-08 204722](https://github.com/user-attachments/assets/48f2c20a-1631-4842-aa3a-79a338d81f38)

**Procedure**

1.A combinational circuit that performs the addition of 2 bits is called the half adder

2.A half adder has 2 inputs and 2 outputs. The output variables produce the sum and carry

3.In full adder two input variables A and B represents the two significant bits to be added. The third input C represents the carry from the previous lower significant position

4.A half subtractor is a combinational circuit that subtracts two bits. Ithas two inputs and two outputs. The output variables produce difference and borrow.

5.A full subtractor is a combinational circuit that performs subtraction between two bits taking into account one mayhave been borrowed by a lower significant stage

**Program:**

module full(a,b,cin,bin,sum,carry,difference,borrow);

input a,b,cin,bin;

output sum,carry,difference,borrow;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule

**RTL Schematic**

![Screenshot (169)](https://github.com/user-attachments/assets/3d56ba4d-2435-44c8-ae26-4546a79aa03a)

**Output Timing Waveform**

![Screenshot (170)](https://github.com/user-attachments/assets/3116e981-cfcc-45dd-b64f-94122e4ad571)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



