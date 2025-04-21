NAME: GOPIKA A 

REG NO: 212224100017

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

![Screenshot 2025-04-21 221754](https://github.com/user-attachments/assets/c96e5c5a-a91f-491e-8ae0-dd0d63208746)

![Screenshot 2025-04-21 221808](https://github.com/user-attachments/assets/65e61683-10ab-46da-9493-4365a8728a75)

**Program:**

```
module exp4(a,b,cin,c,d,bin,sum,cout,difference,bout); 
input a,b,cin,c,d,bin;
output sum, cout, difference, bout;
assign sum=a^b^cin;
assign cout=(a&b) | (b&cin) | (cin&a);
assign difference=a^b^bin;
assign bout=(~a&b) | (bin&(~a))| (bin&~b);
endmodule
```


**RTL Schematic**

![Screenshot (54)](https://github.com/user-attachments/assets/5d1fbca7-136b-4319-82a0-4df9d70e844b)


**Output Timing Waveform**

![Screenshot (55)](https://github.com/user-attachments/assets/5724b298-53b6-4d5f-85e9-58802d9955b4)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



