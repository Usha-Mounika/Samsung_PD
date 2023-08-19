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
  RTL is preferred because it is easy to understand and implement compared to structural and behavioral models
 -  **HDL** : A hardware description language (HDL) enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit.
 - **Simulator** : Simulator is the tool used for checking adherence to the specification by simulating the design. iverilog is the tool used for RTL simulation. A simulator looks for change in the input signals and when no change in input, the output also doesn't change.
 - **Design** : Design is the actual verilog code or set of Verilog codeswhich has the intended functionality to meet the required specifications. Design may have one or more primary inputs or primary outputs.
 - **TestBench** : TestBench is the setup to apply stimulus to the design to check its functionality. TestBench doesn't have a primary input or primary output.

 ![testbench](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a057bfc6-029d-4cde-8549-3c33cb0a6001)

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
  
- **Logic Synthesis** : 
- **Yosys** : Yosys is a framework for Verilog RTL synthesis. It currently hasextensive Verilog-2005 support and provides a basic set of synthesis
algorithms for various application domains.

</details>
