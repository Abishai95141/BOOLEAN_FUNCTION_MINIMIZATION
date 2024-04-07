# BOOLEAN_FUNCTION_MINIMIZATION

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

```

module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule

Developed by: ABISHAI K C
Register Number:212223240002
``` 

Developed by:ABISHAI K C RegisterNumber:212223240002


**RTL realization**
![image](https://github.com/Abishai95141/BOOLEAN_FUNCTION_MINIMIZATION/assets/139335314/71b570c3-2545-48a7-8bc2-69fe5b2302b8)


**LOGIC AND TRUTH TABLE**
![image](https://github.com/Abishai95141/BOOLEAN_FUNCTION_MINIMIZATION/assets/139335314/7e738141-1d51-418c-b175-8bf4bdfda5e2)

![image](https://github.com/Abishai95141/BOOLEAN_FUNCTION_MINIMIZATION/assets/139335314/aa0a40f4-3590-4bc6-aac0-ff5f584c2153)

**RTL**
![image](https://github.com/Abishai95141/BOOLEAN_FUNCTION_MINIMIZATION/assets/139335314/0ca6e231-2428-4595-bfbd-ecb1447b2704)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

