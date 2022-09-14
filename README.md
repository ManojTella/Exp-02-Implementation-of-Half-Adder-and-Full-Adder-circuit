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
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Manoj Guna Sundar Tella.
RegisterNumber:  212221240026.
*/
```
### HALF ADDER
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### FULL ADDER
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:
### RTL
![hl-1](https://user-images.githubusercontent.com/94883876/190230177-666b5e00-410d-4139-94e6-2e9b8e8e53ab.jpg)

### TIMING DIAGRAM
![hl-2](https://user-images.githubusercontent.com/94883876/190230203-1b99c1ef-334b-4d81-9504-4ab1902177d5.jpg)

### TRUTH TABLE
![hl-3](https://user-images.githubusercontent.com/94883876/190230483-953ecfa1-40b9-4341-ba3e-bf2c2238475b.jpg)

### RTL
![fl-1](https://user-images.githubusercontent.com/94883876/190229315-192e5020-1b50-4d63-b1a8-7978eada30c2.jpg)

### TIMING DIAGRAM
![fl-2-timing](https://user-images.githubusercontent.com/94883876/190229331-94358af3-95be-4e94-8c3c-260a5f35c826.jpg)
### TRUTH TABLE 
![fl-3](https://user-images.githubusercontent.com/94883876/190230261-295cdfe2-e828-4fb3-968e-1b4213547ad5.jpg)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
