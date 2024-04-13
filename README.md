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

