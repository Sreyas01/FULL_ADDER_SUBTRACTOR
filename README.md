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

Full Adder

![390651647-4d067f86-95f5-42ba-b297-7b0ac29da290](https://github.com/user-attachments/assets/6765608b-a132-49ed-9628-107448ee2882)

Full Subtractor

 ![390651696-00b5a05c-d04a-4a8f-b9e2-7f432ffade06](https://github.com/user-attachments/assets/4422c4e0-41ea-44cd-b45f-220840927242)
 
**Program:**

Full Adder

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

Full Subtractor

module de42(a, b, bin, difference, borrow);
input a, b, bin;
output difference, borrow;
xor(difference, (a ^ b), bin);
or(borrow, (a & b), (bin & (a | b)));
endmodule

Developed by:Sreyas Register number:24004091

**RTL Schematic**

Full Adder

![390650914-56271b1a-314b-4fbe-8abf-b46f6a7d8169](https://github.com/user-attachments/assets/cb7cb68e-999c-4b79-88e2-54a12a1e291d)

Full Subtractor

![390650979-6b6317bd-c0a7-4c72-8cac-ab1171771310](https://github.com/user-attachments/assets/3ae33556-a86b-4ca6-b171-3d7d0ce5a91d)


**Output Timing Waveform**

Full Adder

![390650638-d57f1ea2-7e03-4d6d-96a0-76de4d2adb99](https://github.com/user-attachments/assets/735864f1-c464-4004-8a46-ac4a60ac7fc2)

Full Subtractor

![390650808-58d21a4e-7c6b-40c2-8b47-cce04047ed36](https://github.com/user-attachments/assets/8eac7484-9f63-44e6-a2ac-f1f175c61a88)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



