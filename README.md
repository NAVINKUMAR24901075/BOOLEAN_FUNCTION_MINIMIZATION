# BOOLEAN_FUNCTION_MINIMIZATION
### NAME: S.NAVINKUMAR
### REG.NO: 24901075
### EXPERIMENT-2: BOOLEAN FUNCTION IMPLEMENTATION

#### AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

𝐹1=𝐴′𝐵′𝐶′𝐷′+𝐴𝐶′𝐷′+𝐵′𝐶𝐷′+𝐴′𝐵𝐶𝐷+𝐵𝐶′𝐷

𝐹2=𝑥𝑦′𝑧+𝑥′𝑦′𝑧+𝑤′𝑥𝑦+𝑤𝑥′𝑦+𝑤𝑥𝑦
#### EQUIPMENT REQURIED:

* Hardware – PCs, Cyclone II , USB flasher
* Software - QUARTUS PRIME

#### THEORY:

Implementing Boolean functions in Quartus using Verilog programming involves a systematic approach to design, synthesize, and verify digital logic functions. Here, we’ll cover the theoretical background and implementation of Boolean functions using Verilog, focusing on the functions:

𝐹1=𝐴′𝐵′𝐶′𝐷′+𝐴𝐶′𝐷′+𝐵′𝐶𝐷′+𝐴′𝐵𝐶𝐷+𝐵𝐶′𝐷
𝐹2=𝑥𝑦′𝑧+𝑥′𝑦′𝑧+𝑤′𝑥𝑦+𝑤𝑥′𝑦+𝑤𝑥𝑦

Theory of Boolean Logic in Digital Circuits
In digital electronics, Boolean functions describe the relationships between inputs and outputs using binary logic (0s and 1s). These functions are often represented in Sum of Products (SOP) form, where each term (or "product") represents a specific combination of inputs that will produce a high (1) output. The SOP form uses the following logic operations:

AND Operation: Produces a high output only if all inputs are high.
OR Operation: Produces a high output if any of the inputs are high.
NOT Operation: Produces the opposite of the input (inverts it).

In SOP form, the function is an OR of multiple AND terms, with each AND term representing a unique combination of the inputs that yield a true (1) output.

Analyzing the Boolean Functions F1 and F2
Function F1 Analysis
The function F1 is given as:
    𝐹1=𝐴′𝐵′𝐶′𝐷′+𝐴𝐶′𝐷′+𝐵′𝐶𝐷′+𝐴′𝐵𝐶𝐷+𝐵𝐶′𝐷
Terms:
  * 𝐴′𝐵′𝐶′𝐷′:True when A,B,C,𝐷 are all zero.
  * AC′D′:True when A is 1, C and D are 0.
  * 𝐵′𝐶𝐷′:True when B is 0, C is 1, D is 0.
  * 𝐴′𝐵𝐶𝐷:True when A is 0, B,C, and D are 1.
  * 𝐵𝐶′𝐷:True when B is 1, C is 0, D is 1.
Each terms represents a specific input combination that yields an output of 1 for F1.
Function F2 Analysis
the function F2 given as:
   𝐹2=𝑥𝑦′𝑧+𝑥′𝑦′𝑧+𝑤′𝑥𝑦+𝑤𝑥′𝑦+𝑤𝑥𝑦
Terms:
  * xy'z:True when xix 1,y is 0,z is 1.
  * x'y'z:True when x andd y are 0, z is 1.
  * w'x'y:True when w is 0,x and y are 1.
  * wx'y:True when w,y are 1, and x is 0.
  * wxy:True when w,x,y are 1.
Each of these combination results in an output of 1 for F2.

Implementing Boolean Functions in Verilog
To implement these functions in Verilog, we use logical operators to replicate the behavior of AND, OR, and NOT operations.

AND is represented as &.
OR is represented as |.
NOT is represented as ~.

And start the verilog code for F1 and F2

Quartus Simulation and Verification
Once the Verilog code is written, we can verify the logic using Quartus, an FPGA design and simulation tool.

Steps in Quartus
* Create a New Project: Open Quartus, create a new project, and add the Verilog file.
* Compilation: Compile the Verilog code to synthesize it into logic gates. Quartus will map the Boolean functions to FPGA resources, ensuring that the code is correctly interpreted.
* Testing with a Testbench: To verify the function, create a testbench file that applies various combinations of inputs and observes the outputs F1 and F2.
* Simulation: Open the simulation tool in Quartus and select the testbench.Run the simulation and observe the waveforms. Each input combination should produce the expected result for F1 and F2 as per the truth table.
* Verify Results: Compare the output waveforms against the expected values to confirm correct operation.

* Conclusion:
  By using Quartus and Verilog programming, we can efficiently design, implement, and verify Boolean functions like F1 and 
F2. Quartus provides a platform for synthesizing the Verilog code into hardware, while simulation allows us to test and ensure that the functions behave as expected across all input combinations. This approach is essential for designing reliable digital systems.

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

#### TRUTH TABLE:
![Screenshot 2024-11-04 164409](https://github.com/user-attachments/assets/acb3ef21-0884-42b1-9755-9fd47eb97cab)

![Screenshot 2024-11-04 164350](https://github.com/user-attachments/assets/e58f150e-ae63-4f15-95cc-52d766062906)


#### RTL OUTPUT:
![Screenshot 2024-11-04 103309](https://github.com/user-attachments/assets/8ba8ab3d-29bd-415b-ac87-e0d700072add)

#### OUPUT WAVEFORM:
![Screenshot 2024-11-04 160947](https://github.com/user-attachments/assets/ddc50ce3-c8e1-466c-8af7-e409f5673f7f)

#### RESULT:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

