# BOOLEAN_FUNCTION_MINIMIZATION
### NAME: S.NAVINKUMAR
### REG.NO: 24901075
### EXPERIMENT-2: BOOLEAN FUNCTION

#### AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

#### EQUIPMENT REQURIED:

Hardware – PCs, Cyclone II , USB flasher,
SOFTWARE-QUARTUS PRIME

#### THEORY:

#### LOGIC DIAGRAM:
![Screenshot 2024-11-04 164409](https://github.com/user-attachments/assets/1e71f893-9c6f-4f18-8fda-9c47bc835bfc)

![Screenshot 2024-11-04 164350](https://github.com/user-attachments/assets/488cdb05-9e50-4548-8021-4381ce8b1ca5)

#### PROCEDURE:

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


#### PROGRAM:
##### module BOOLEANFUNCTIONMINIMIZATION (a,b,c,d,w,x,y,z,f1,f2);
##### input a,b,c,d,w,x,y,z;
##### output f1,f2;
##### wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
##### assign x1=(~a)&(~b)&(~c)&(~d);
##### assign x2=(a)&(~c)&(~d);
##### assign x3=(~b)&(c)&(~d);
##### assign x4=(~a)&(b)&(c)&(d);
##### assign x5=(b)&(~c)&(d);
##### assign x6=(x)&(~y)&(z);
##### assign x7=(~x)&(~y)&(z);
##### assign x8=(~w)&(x)&(y);
##### assign x9=(w)&(~x)&(y);
##### assign x10=(w)&(x)&(y);
##### assign f1=x1|x2|x3|x4|x5;
##### assign f2=x6|x7|x8|x9|x10;
##### endmodule

#### RTL OUTPUT:
![Screenshot 2024-11-04 103309](https://github.com/user-attachments/assets/8ba8ab3d-29bd-415b-ac87-e0d700072add)

#### OUPUT WAVEFORM:
![Screenshot 2024-11-04 160947](https://github.com/user-attachments/assets/ddc50ce3-c8e1-466c-8af7-e409f5673f7f)

#### RESULT:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

