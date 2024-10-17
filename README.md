# FULL_ADDER_SUBTRACTOR

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

**FULL ADDER:**

![DE E-4 truthtable](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/7116d2bf-8e90-4e96-bfd5-d62af11a317a)

**FULL SUBTRACTOR:**

![DE E-4 subtractor truth table](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/33d8ba16-9169-40b0-8696-3bb8e5c3a0b7)


**Procedure**

**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.


**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Implementation-of-Full-Adder-and-Full-subtractor-circuit

```
Developed by: DHARMALINGAM S
RegisterNumber: 212223040037
```
```
## Full_adder
module DE4(sum,carry,a,b,c);
input a,b,c;
output sum,carry;
wire w1,w2,w3;       
xor(w1,a,b);
xor(sum,w1,c);        

and(w2,a,b);
and(w3,w1,c);

or(carry,w2,w3);
endmodule

## Full_subtractor
module fullsub(diff,borrow,a,b,bin);
input a,b,bin;
output diff,borrow;
wire w1,w2,w3,w4,w5;
xor (w1,a,b);
xor(diff,w1,bin);
not(w2,a);
not(w3,w1);
and(w4,w2,b);
and(w5,w3,bin);
or(borrow,w4,w5);
endmodule

```

**RTL Schematic**
FULL ADDER
![Screenshot 2024-10-17 104232](https://github.com/user-attachments/assets/29dcd690-aea7-4e29-acab-4973fe98ffd4)


FULL SUBTRACTOR
![Screenshot 2024-10-17 110736](https://github.com/user-attachments/assets/446734dc-2c05-4c6f-a6e5-5b3b56b4d394)


**Output Timing Waveform**

**FULL ADDER**

![Screenshot 2024-10-17 104013](https://github.com/user-attachments/assets/ce34373f-e41f-4d35-942e-f5e485fa94b6)

**FULL SUBTRACTOR**

![Screenshot 2024-10-17 111038](https://github.com/user-attachments/assets/777905e9-844b-475b-a557-873a6f3ced9d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

