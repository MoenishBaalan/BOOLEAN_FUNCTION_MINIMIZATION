**EX.NO:2**

# BOOLEAN_FUNCTION_MINIMIZATION

**DATE:**

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

Developed by: MOENISH BAALAN G
RegisterNumber:212223220057

```
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
  not(adash,a);
  not(bdash,b);
  not(cdash,c);
  not(ddash,d);
  and(p,bdash,ddash);
  and(q,adash,b,d);
  and(r,a,b,cdash);
  or(f1,p,q,r);
//type code for f2 as like f1
 not(ydash,y);
 and(s,x,y);
 and(t,ydash,z);
 and(u,w,y);
 or(f2,s,t,u);
endmodule
```
**RTL realization**
![329143729-eb08f007-dbc2-4c95-a37e-b5427cafab4f](https://github.com/MoenishBaalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473396/2ad3fd59-6fc0-4e0d-ad97-dd02f7f09f46)




**Timing Diagram**
![329143792-69bde7e8-330a-4d10-b6a1-c06948315ba0](https://github.com/MoenishBaalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473396/5763ccc5-ac68-4656-aec4-90d4aea2c121)



**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
