# Experiment--04-Half-Subtractor-and-Full-subtractor
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



Write the detailed procedure here 


## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SWETHA.S
RegisterNumber: 212222230155
Program for full subtractor:
module ex4(A,B,bin,diff,borrow);
input A,B,bin;
output diff,borrow;
assign diff= A^B^bin;
assign borrow = ((~A)&B)|(B&bin)|((~A)&bin);
endmodule
Program for half subtractor:
module ex4 (a,b,diff,borr) ;
input a,b ;
output diff,borr;
assign diff = (a^b) ;
assign borr = ((~a)&b) ;
endmodule
*/
```
## RTL realization:
HALF SUBTRACTOR:
![Screenshot 2023-09-13 230337](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/57b75e63-0ece-488f-a415-3b7d4b62632e)

FULL SUBTRACTOR:
![image](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/a021d435-8630-4dc1-95a1-f4dcfddfe704)

## Output Waveform:
![Screenshot 2023-09-13 230746](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/35cebaf3-d8e8-4d63-bed6-a747e560eb62)

![Screenshot 2023-09-13 231835](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/c1062f63-3401-49ef-b402-4c2711082e7b)

## Truthtable
![image](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/0d758131-9740-46d3-806c-a350af7a587c)

![image](https://github.com/swethaselvarajm/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119525603/50b3393b-9788-4eb6-ba13-8330c1b3f0bc) 

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
