# Experiment 04 Half Subtractor and Full subtractor
# NAME: DEEPAK
# REFERENCE NO: 23000154
## Implementation of Half subtractor and Full subtractor circuit
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

# Half Subtractor:

module halfsub(diff,carry,a,b);
input a,b;
output diff,carry;
xor(diff,a,b);
assign carry=(~a)&b;
endmodule

# Full Subtractor:

module fullsub(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule

## Truthtable
# HALF SUBTRACTOR:
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/9a9f573b-d78a-4f64-a106-deb96695006d)

# FULL SUBTRACTOR:
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/f96feddf-cd00-4c43-b927-4d3e6d4cabc7)


##  RTL realization:
# HALF SUBTRACTOR:
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/f8ba331b-0760-4a02-84e3-e08900a0a098)


# FULL SUBTRACTOR:
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/fb33dc6d-1d3a-4ee0-a958-86e408c32991)


## Timing diagram
# HALF SUBTRACTOR
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/a8205d52-6c9d-45a1-95b2-02f053c70cf9)


# FULL SUBTRACTOR
![image](https://github.com/deepak23000154/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151951350/e1cfc37a-b874-4361-b02e-7bb53974b79a)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
