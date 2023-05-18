# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodul.


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: jagadeeshreddy561
RegisterNumber: 212222240059 
*/

Half Subtractor program:
```python
module HalfSubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A ^ B);
assign Borrow = (~A & B);
endmodule
```
Full Subtractor program:
```python
module FullSubtractor(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule
```


## Output:

## Truthtable
Half Subtractor:

![4 5_halftable](https://github.com/jagadeeshreddy561/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120623104/38f8b878-0167-404e-bc1a-2164044aaf2f)

Full Subtractor:

![4 5_halftable (1)](https://github.com/jagadeeshreddy561/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120623104/cac59ae2-d3de-4041-a538-a0781b05832c)




##  RTL realization
Half Subtractor:

 file:///home/sec/Downloads/4.2_gate.png



Full Subtractor:

![4 3_gate](https://github.com/jagadeeshreddy561/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120623104/e352c31a-f5e7-40fa-a1a8-afbe64f74829)



## Timing diagram 
Half Subtractor:

![4 1_wave](https://github.com/jagadeeshreddy561/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120623104/c1161731-7dfe-4a45-8314-7be72651abbc)

Full subtractor:

![4 4_wave](https://github.com/jagadeeshreddy561/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120623104/69bddb79-3e11-438d-a181-d35713d82d2b)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
