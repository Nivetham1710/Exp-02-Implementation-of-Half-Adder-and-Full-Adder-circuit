# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Nivetha.M
RegisterNumber:  212221240034
*/
~~~
HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
~~~
### Logic symbol & Truthtable


### Output:
![image](https://user-images.githubusercontent.com/94155183/196036946-6e8c07c5-f387-460f-be37-4c12853522eb.png)

### RTL
![image](https://user-images.githubusercontent.com/94155183/196036954-8c4cc3c9-6aae-4a9c-8e6a-2ddb6df67c98.png)
![image](https://user-images.githubusercontent.com/94155183/196036965-c624b008-71c1-46f4-969f-1f7b503154f4.png)

### TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/94155183/196036976-663df978-992f-4567-a870-40d12c40aaa6.png)
### FULL ADDER:
![image](https://user-images.githubusercontent.com/94155183/196036989-fa0635e6-1ca8-43bf-8239-e90ff3408f82.png)



### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/94155183/196037042-ba81b09b-bf0d-40f6-ad29-759d9ad93d8b.png)

### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94155183/196037091-fd1d0fb7-2bd7-4d00-926e-d257fb5f4b7e.png)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
