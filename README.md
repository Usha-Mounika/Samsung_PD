# Physical Design Training

A brief description of what this training summarizes : 

- [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)
- [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)

## [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)
 <details open>
<summary>dc_shell</summary>
<br>
  The dc_shell was setup.
  
![dc_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/693aa266-5775-42d6-adce-885437e43565)

- The Design compiler is an EDA tool in the field of Digital IC design. 
- It plays a crucial role in translating high-level hardware descriptive languages into optimized gate-level representation.
- Design Compiler employs sophisticated algorithms to reduce power consumption, enhance circuit speed, and minimize chip area utilization.
- This tool is essential for optimizing the design's power, performance, and area (PPA) metrics. 
</details>
<details open>
<summary>icc2_shell</summary>
<br>
  The icc2_shell was setup.
 
![icc2_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0a733004-dca6-412f-a94c-bc8608ecb36b)

- ICC2 (Integrated Circuit Compiler 2) Shell is a command-line interface that provides a powerful environment for managing various stages of the chip design process.
-  This command-line interface enables automation of complex design flows, making it easier to handle intricate VLSI projects.
-  Its features encompass logic synthesis, placement, routing, and clock tree synthesis, all orchestrated for optimal power, performance, and area (PPA) trade-offs. 
</details>
<details open>
<summary>pt_shell</summary>
<br>
  The pt_shell was setup.
 
 ![pt_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2e3efe8a-6aa3-4402-b3e4-542a4ac6b876)
</details>
<details open>
<summary>lc_shell</summary>
<br>
  The lc_shell was setup.
 
![lc_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/80feb4c1-1705-4ebb-8b10-a1593710dbc1)
</details>
 <details open>
<summary>Yosys</summary>
<br>
The yosys was setup.
  
<img width="568" alt="yosys" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/52c877f5-dda8-4fad-84ad-8697c30ddb68">
</details>
 <details open>
<summary>gtkwave</summary>
<br>
The gtkwave was setup.
   <img width="764" alt="gtkwave" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b53bb7d7-d3fe-4259-918e-6d348abef910">
</details>
  <details open>
<summary>iverilog</summary>
<br>
The iverilog was setup.
<img width="666" alt="iverilog" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e649c3c3-d141-48f9-83ee-03a9ad5a669d">
</details>

 ## [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)
 <details open>
<summary>Introduction to RTL Design and Synthesis</summary>
<br>
  
 - **RTL Design** : The RTL Design stands for **Register Transfer Language.**  It sits between the high-level system specification and the lower-level gate-level implementation. This is a design abstraction which models the flow of digital signals between hardware registers, and the logical operations performed on those signals.
  RTL is preferred because it is easy to understand and implement compared to structural and behavioral models.
 -  **HDL** : A hardware description language (HDL) enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit.
 - **Simulator** : Simulator is the tool used for checking adherence to the specification by simulating the design. iverilog is the tool used for RTL simulation. A simulator looks for change in the input signals and when no change in input, the output also doesn't change.
 - **Design** : Design is the actual verilog code or set of Verilog codeswhich has the intended functionality to meet the required specifications. Design may have one or more primary inputs or primary outputs.
    -RTL design is the behavioral representation of the required specification. The following code snippet is an example of Verilog HDL(RTL) code:

```vhdl
  module sample_code (
   input clk,rst,
   output result,done);

always @ (posedge clk ,posedgr rst)
 if(rst)
 ---
 else
 ----
 endmodule
---------------
---------------
```
 - **TestBench** : TestBench is the setup to apply stimulus to the design to check its functionality. TestBench doesn't have a primary input or primary output.

 ![testbench](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a057bfc6-029d-4cde-8549-3c33cb0a6001)

- **Logic Synthesis** : The Logic Synthesis involves following steps
  - Syntax Analysis: Takes input of HDL files and checks for syntax errors.The syntax analyzer breaks the code into tokens, then builds a parse tree, which is a graphical representation of the syntactic structure of the HDL file.
  - Library Definition: Provides and allocates standard cells and IP libraries.
  -  Elaboration and Binding: Translates RTL into the Boolean structure. Binds all cells and makes libraries available.
  - Constraint Definition: For building a customized and specific chip, we need to define constraints according to which the chip will function. For example, clock frequency, power efficiency, etc.
  - Pre-mapping Optimization: It performs mapping to generic cells in the library.
  - Technology Mapping: Performs mapping of the generic libraries to technology libraries.
  - Post-mapping Optimization: Changes gate designs to meet constraints.
  - Report and export: Give out the end results with reports on timings and export.
   
- **Synthesizer** : Synthesizer is the tool used for converting RTL to Netlist. Yosys is the tool used for synthesis and iverilog is the tool used to verify the synthesis. The RTL design is converted into gates and the connections are made between gates and netlist is given as an output file.

     ![Screenshot 2023-08-20 092650](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a775200f-0528-4b51-860f-73fadf6f2123)


- Netlist :  It is the representation of design in the form of Standard libs in the .lib. The set of inputs or outputs remain same between RTL design and Synthesized Netlist.

</details>
 <details open>
<summary>Introduction to Opensource simulator : iverilog gtkwave </summary>
<br>
  
- **iverilog** : iverilog is a compiler that translates Verilog source code into executable programs for simulation, or other netlist formats for further processing.
- **gtkwave** : GTKWave is an analysis tool used to perform debugging on Verilog or VHDL simulation models. It relies on a post-mortem approach through the use of
dumpfiles.

![iverilog simulation](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5ffc0f70-7a1a-494e-a025-81231cd1bc2f)

**Lab examples using iverilog and gtkwave**

![Lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d815c579-2efe-4303-9739-c9351e9663fb)

![Blank 2 Grids Collage (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/22fc7b31-23c7-4fe3-9352-51c6c2bfb5cc)

</details>
 <details open>
<summary> Introduction to Yosys and Logic Synthesis </summary>
<br>
  
 - **Yosys** : Yosys is a framework for Verilog RTL synthesis. It currently hasextensive Verilog-2005 support and provides a basic set of synthesis
algorithms for various application domains.
 - **Sky130PDK** : The SKY130 is a mature 180nm-130nm hybrid technology originally developed internally by Cypress Semiconductor before being spun out into SkyWater Technology and made accessible to general industry.

![yosys](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8879ae3b-8906-4c39-a5dd-bc9d869185f4)

  - .**lib** is the collection of logic modules that includes basic gates such as AND, OR etc.. and different flavors of same gate such as slow, medium, fast.
 ### Need for different flavors in design:
 The logic path consists of 3 stages: the launch flip-flop, the combinational delay, capture flip-flop.The combinational delay in a logic path decides the maximum speed of operation in a logic circuit. The **CLKtoQ period of  FFA**, **combinational delay** **setup time of FFB** are the factors to be considered for faster operation of a logic design. So the minimum clock period should be greater than this sum to ensure glitch free operation of design. This minimum period contributs to the higher speed and thus resulting in higher performance of the design.
 ![ffpath](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/22e9a0b2-6b04-44e5-972e-4bb9d25b0ec1)
 - **Setup time** determines the minimum amount of time the data input to a flip-flop must be stable before the clock edge arrives. 
 - **Hold time** refers to the minimum amount of time the data input to a flip-flop must be stable after the clock edge arrives.
 - ![hold eq](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f173f14a-bbc0-456d-8bbb-7e19eb6ac56a)

 - We need faster cells to meet setup requirement and slower cells to meet hold requirement.
 - The load in a digital design is **Capacitance**.  The cell delay is less when the capacitor charges or discharges faster. So it needs wider transistors that are capable of sourcing more current.
```celldelay
Wider Transistors => Less delay => More area and Power
Narrower Transistors => More delay => Less are and Power
```
  - The tradeoff of speed comes with area and power.
- **Selection of cells**: The use of faster cells consumes more area and power and causes hold violations. The use of slower cells makes the circuit sluggish and may not meet the performance. So, The synthesizer needs to be guided to select the flavor using **constraints**.
- This is a snippet example of how synthesis is being done from Behavioral code to gate level design.


 ![synthesis](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8b600c8f-e62a-4f45-84b0-02bb246a8b2d) 
 ### Lab using Yosys
</details>
