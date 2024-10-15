# FULL_ADDER_SUBTRACTOR

### NAME : THARUN SRIDHAR 
### REGISTER NO : 212223230230

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

**DEVELOPED BY : THARUN SRIDHAR**
**REGISTER NO : 212223230230**

**FULL ADDER :**

```
module Exp4(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b) | (b&cin) | (cin&a));
endmodule
```

**FULL SUBTRACTOR :**

```
module exp42(a,b,bin,borr,diff);
input a,b,bin;
output borr,diff;
assign diff=(a^b^bin);
assign borr=((~a&b) | (b&bin) | (bin&~a));
endmodule
```

**RTL Schematic**

**FULL ADDER :**
![Screenshot (33)](https://github.com/user-attachments/assets/22148e0f-c140-414b-9067-5c9232ccae4a)

**FULL SUBTRACTOR :**
![Screenshot (35)](https://github.com/user-attachments/assets/53ccae34-1e46-4710-abfe-5f8ed4f54c5a)


**Output Timing Waveform**

**FULL ADDER :**
![Screenshot (34)](https://github.com/user-attachments/assets/36c30f2b-b3ee-4a07-9b89-9f113a678411)

**FULL SUBTRACTOR :**
![Screenshot (36)](https://github.com/user-attachments/assets/751f1f51-abe1-4685-8886-6e802607827a)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



