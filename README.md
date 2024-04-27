# EX02 BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: Moenish Baalan G
RegisterNumber: 212223220057*/
``` 
module booleanfunction(A,B,C,D,F1); 
input A,B,C,D; 
output F1; 
wire x1,x2,x3,x4,x5; 
assign x1=(~A)&(~B)&(~C)&(~D); 
assign x2=(A)&(~C)&(~D); 
assign x3=(~B)&(C)&(~D); 
assign x4=(~A)&(B)&(C)&(D); 
assign x5=(B)&(~C)&(D); 
assign F1=x1|x2|x3|x4|x5; 
endmodule 
```
![326154818-0af426c0-a0bf-43c0-a4c4-828fcb18e5e1](https://github.com/MoenishBaalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473396/b60946bc-e224-4cae-8268-58b7d2d002d3)



**RTL realization**

![326154827-a527341a-95c6-4192-b655-fa28e4c36811](https://github.com/MoenishBaalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473396/2ef5e787-8c67-4beb-a373-45a712491f25)



**Output:**

![326154835-384344ad-76c8-4ca1-b7cd-717de6910ba1](https://github.com/MoenishBaalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473396/ec52b5f7-1b07-41b2-b2ba-900c18f72ba5)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
