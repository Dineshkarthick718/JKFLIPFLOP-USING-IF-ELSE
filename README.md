# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1.Open Quartus II software.
2.Create a new project using New Project Wizard.
3.Create a Verilog HDL / Block Diagram file and save it as the top-level entity.
4.Write the JK flip-flop logic and save the file.
5.Compile the design using Start Compilation.
6.Create a University Program VWF file.
7.Insert input and output nodes (J, K, CLK, Q).
8.Apply a clock waveform to the CLK input.
9.Set input values for J and K as 0 or 1.
10.Run Functional Simulation and observe the output. 

**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming.
module jk(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
q=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule

Developed by:R Dinesh Karthick
RegisterNumber: 25018555

**RTL LOGIC FOR FLIPFLOPS**
<img width="1776" height="711" alt="image" src="https://github.com/user-attachments/assets/d763a578-b62f-484e-ba06-abf1b17f2269" />

**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1883" height="566" alt="image" src="https://github.com/user-attachments/assets/544ab9ed-e328-4d6b-b249-0b5263303a8f" />

**RESULTS**
Hence JK FlipFlop using if else program is executed and the output is verified
