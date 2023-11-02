# Physical Design Training

A brief description of what this training summarizes : 

- [Day0 : Setup Check](https://github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#day0setupcheck)
- [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day1)
- [Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day2)
-  [Day3 : Combinational and Sequential Optimizations](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day3)
-  [Day4 : GLS,blocking vs non-blocking and Synthesis Simulation mismatch](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day4)
-  [Day5 : DFT](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day5)
-  [Day6 : Introduction to Logic Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day6)
-  [Day7 : Basic SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day7)
-  [Day8 : Advanced SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day8)
-  [Day9 : Optimization in Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day9)
-  [Day10 : QOR](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day10)
-  [Day11 : Introduction to BabySoC](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day11)
-  [Day12 : BabySoC Modelling](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day12)
-  [Day13 : Post-Synthesis Simulation](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day13)
-  [Day14 : Synopsys DC and timing analysis](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day14)
-  [Day15 : Inception of EDA and PDK](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day15)
-  [Day16 : Good Floorplan vs Bad Floorplan](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day16)
-  [Day17 : Std Cell Characterize experiment](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day17)
-  [Day18 : Pre-layout STA and importance of good clock tree](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day18)
-  [Day19 : Final steps for RTL2GDS](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day19)
-  [Day20 : Floorplanning and Powerplanning Labs](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day20)
-  [Day21 : Placement and CTS Labs](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day21)
-  [Day22 : CTS analysis Labs](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day22)
-  [Day23 : Clock Gating Technique](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day23)
-  [Day24 : Timing violations and ECO](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day24)
-  [Day26 : Introduction to mixed signal flow](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day26)
-  [Day27 : Introduction to crosstalk - glitch and delta delay](https://www.github.com/Usha-Mounika/Samsung_PD/blob/master/README.md#Day24)



## Day0 : Setup Check

<details>
<summary>dc_shell</summary>
<br>	 
	
  The dc_shell was setup.

![dc_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5846b160-d888-454e-a1b0-d492b2137f36)

- The Design compiler is an EDA tool in the field of Digital IC design. 
- It plays a crucial role in translating high-level hardware descriptive languages into optimized gate-level representation.
- Design Compiler employs sophisticated algorithms to reduce power consumption, enhance circuit speed, and minimize chip area utilization.
- This tool is essential for optimizing the design's power, performance, and area (PPA) metrics.
</details>

<details>
<summary>icc2_shell</summary>
<br>
  The icc2_shell was setup.
 
 ![icc2_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/83cf9480-5e09-4635-80eb-ec4656bbc3f9)


- ICC2 (Integrated Circuit Compiler 2) Shell is a command-line interface that provides a powerful environment for managing various stages of the chip design process.
-  This command-line interface enables automation of complex design flows, making it easier to handle intricate VLSI projects.
-  Its features encompass logic synthesis, placement, routing, and clock tree synthesis, all orchestrated for optimal power, performance, and area (PPA) trade-offs. 
</details>
<details >
<summary>pt_shell</summary>
<br>
  The pt_shell was setup.

 ![pt_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c3d81adc-1013-4c30-9ac6-e6acf001c965)

- **PrimeTime** analyzes the timing behavior of a digital circuit by considering signal propagation delays, clock cycles, and other factors. It helps identify critical paths and timing violations.
-  It can estimate power consumption based on the circuit's activity and help designers optimize power usage.
-  It also provides signal integrity analysis, variability analysis, clock tree synthesis and design optimization.
</details>
<details>
<summary>lc_shell</summary>
<br>
  The lc_shell was setup.
 
![lc_shell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4b61b75b-95a2-4f85-b1ff-4d8593bdc86d)

- **Library Compiler** refers to a tool that generates optimized cell libraries for use in digital integrated circuit designs.
-  These libraries contain pre-characterized cells (logic gates, flip-flops, etc.) that have been characterized for various operating conditions, such as process corners and temperature ranges.
-  It is used for ndm generation from cell libraries and technology files.
</details>
 <details>
<summary>Yosys</summary>
<br>
The yosys was setup.
  
<img width="568" alt="yosys" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/52c877f5-dda8-4fad-84ad-8697c30ddb68">
</details>
 <details>
<summary>gtkwave</summary>
<br>
The gtkwave was setup.
   <img width="764" alt="gtkwave" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b53bb7d7-d3fe-4259-918e-6d348abef910">
</details>
  <details>
<summary>iverilog</summary>
<br>
The iverilog was setup.
<img width="666" alt="iverilog" src="https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e649c3c3-d141-48f9-83ee-03a9ad5a669d">
</details>

 ## Day1 : Introduction to Verilog RTL Design and Synthesis
 
 <details>
<summary>Introduction to RTL Design and Synthesis</summary>
<br>
  
 - **RTL Design** : The RTL Design stands for **Register Transfer Language.**  It sits between the high-level system specification and the lower-level gate-level implementation. This is a design abstraction which models the flow of digital signals between hardware registers, and the logical operations performed on those signals.
  RTL is preferred because it is easy to understand and implement compared to structural and behavioral models.
 -  **HDL** : A hardware description language (HDL) enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit.
 - **Simulator** : Simulator is the tool used for checking adherence to the specification by simulating the design. **iverilog** is the tool used for RTL simulation. A simulator looks for change in the input signals and when no change in input, the output also doesn't change.
 - **Design** : Design is the actual verilog code or set of verilog codes which has the intended functionality to meet the required specifications. Design may have one or more primary inputs or primary outputs.
    - RTL design is the behavioral representation of the required specification. The following code snippet is an example of Verilog HDL(RTL) code:

```verilog
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

![testbench](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7748b0a1-356e-4c61-9a20-6ecc8fc37989)

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


![Screenshot 2023-08-20 092650](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/99486688-b0bd-4313-9489-b6a2df52844e)


- Netlist :  It is the representation of design in the form of Standard libs in the .lib. The set of inputs or outputs remain same between RTL design and Synthesized Netlist.

</details>
 <details>
<summary>Introduction to Opensource simulator : iverilog gtkwave </summary>
<br>
  
- **iverilog** : iverilog is a compiler that translates Verilog source code into executable programs for simulation, or other netlist formats for further processing.
- **gtkwave** : GTKWave is an analysis tool used to perform debugging on Verilog or VHDL simulation models. It relies on a post-mortem approach through the use of
dumpfiles.

![iverilog simulation](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e1cff27a-9006-4f26-ab04-9729c58bfcad)


**Lab examples using iverilog and gtkwave**

![Lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2b68d5f3-44c4-4fe3-8e9b-eb5e8b83bc24)

The following image shows the a good D-latch operation with gtkwave
![Blank 2 Grids Collage (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d2827e98-29c8-4a06-b291-47b8615cb700)
The following is the verilog code for good latch:
```verilog
module good_latch (input clk , input reset , input d , output reg q);
always @ (clk,reset,d)
begin
	if(reset)
		q <= 1'b0;
	else if(clk)
		q <= d;
end
```
The following is the test bench code for good latch:
```verilog
`timescale 1ns / 1ps
module tb_good_latch;
	// Inputs
	reg clk, reset, d;
	// Outputs
	wire q;

        // Instantiate the Unit Under Test (UUT)
	good_latch uut (
		.clk(clk),
		.reset(reset),
		.d(d),
		.q(q)
	);

	initial begin
	$dumpfile("tb_good_latch.vcd");
	$dumpvars(0,tb_good_latch);
	// Initialize Inputs
	clk = 0;
	reset = 1;
	d = 0;
	#300 $finish;
	end

always #20 clk = ~clk;
always #23 d = ~d;
always	#15 reset=0;
```

</details>
 <details>
<summary> Introduction to Yosys and Logic Synthesis </summary>
<br>
  
 - **Yosys** : Yosys is a framework for Verilog RTL synthesis. It currently hasextensive Verilog-2005 support and provides a basic set of synthesis
algorithms for various application domains.
 - **Sky130PDK** : The SKY130 is a mature 180nm-130nm hybrid technology originally developed internally by Cypress Semiconductor before being spun out into SkyWater Technology and made accessible to general industry.
![yosys](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c82f157a-23b7-46f8-896d-9738096d55c7)

  - .**lib** is the collection of logic modules that includes basic gates such as AND, OR etc.. and different flavors of same gate such as slow, medium, fast.
 ### Need for different flavors in design:
 The logic path consists of 3 stages: the launch flip-flop, the combinational delay, capture flip-flop.The combinational delay in a logic path decides the maximum speed of operation in a logic circuit. The **CLKtoQ period of  FFA**, **combinational delay** **setup time of FFB** are the factors to be considered for faster operation of a logic design. So the minimum clock period should be greater than this sum to ensure glitch free operation of design. This minimum period contributes to the higher speed and thus resulting in higher performance of the design.

 - **Setup time** determines the minimum amount of time the data input to a flip-flop must be stable before the clock edge arrives. 
 - **Hold time** refers to the minimum amount of time the data input to a flip-flop must be stable after the clock edge arrives.
 - ![hold eq](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c1daa786-52eb-4180-8403-0314b3a713ca)
![ffpath](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c01d6e7d-6a41-463b-8dc6-165cc2051dc4)

 - We need faster cells to meet setup requirement and slower cells to meet hold requirement.
 - The load in a digital design is **Capacitance**.  The cell delay is less when the capacitor charges or discharges faster. So it needs wider transistors that are capable of sourcing more current.
```celldelay
Wider Transistors => Less delay => More area and Power
Narrower Transistors => More delay => Less are and Power
```
  - The tradeoff of speed comes with area and power.
- **Selection of cells**: The use of faster cells consumes more area and power and causes hold violations. The use of slower cells makes the circuit sluggish and may not meet the performance. So, The synthesizer needs to be guided to select the flavor using **constraints**.
- This is a snippet example of how synthesis is being done from Behavioral code to gate level design.
![synthesis](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/23da17a0-4bc5-474b-a1a2-ed3ca0cd5091)


 
 ### Lab using Yosys
 The following images show the synthesis of a 2x1 multiplexer from verilog code to its gate level netlist. 
 ![first](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/17e30794-3b9c-4471-bc8c-aa2abaf70309)
![n-1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1863611f-76e7-45e8-aac5-b8a1d22fe965)
![last](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/faa7c01b-34ee-4b64-9c5b-80d6c5534a81)
This following snippet shows the steps to generate RTL to netlist using Yosys tool.
```yosys
$ yosys
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> read_verilog good_mux.v 
yosys> synth -top good_mux 
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show

yosys> write_verilog good_mux_netlist.v 
yosys> !gvim good_mux_netlist.v 

yosys> write_verilog -noattr good_mux_netlist.v
yosys> !gvim good_mux_netlist.v 

```
The following snap is the behavioral design in the code
![good_mux logic](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9aa1e911-7623-4b2b-9dc5-47d00f85de78)
The following code snippet is the generated netlist without switch (on left) and with switch (right image).
![Blank 2 Grids Collage (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9ed09f75-fd13-4bbe-998e-b50b5feede37)

</details>

## Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles
 <details>
<summary>Introduction to timing .libs</summary>
<br>
	 
The Library includes the various parameters to be defined for a design such as units of voltage, resistance, capacitance and type of technology used, delay model used, input transition etc... 

![pvt ss](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c2a92802-ed80-4573-a126-ded39bf7bee1)

The library name (as follows) explains about **PVT conditions** of a .lib file.The following library is a 130 nm technology with tt (process), 1.8V (voltage), 25c (temperature).
- The **process variation** defines the change in parameters due to fabrication. In other words, two wafers made at same instant with same material may have different specifications. The process can be **slow(ss), typical(tt), fast(ff)**.
	 
- The **voltage variation** and **temperature variation** effect the operation of circuit in the design.
![PVT cond](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b5055b4f-dc7e-4482-840d-199287b2a70e)

The cell information in a library gives about the leakage power for different combinations (for example, for 2 input gate the power information of all 4 combinations are given) of inputs, area, power port information and various information associated with each pin.
 - The following comparison shows that the same **AND gate** has three diferent flavors.
  - The wider transistor (and2_4) has less delay and consumes more area and power.
  - The moderate wide transistor (and2_2) has moderate delay and consumes moderate power and moderate area.
  - The narrower transistor (and2_0) has more delay and consumes less area and power.
In the following 2-input AND gate, you can also see the 4. combinations of inputs as in the truth table and the power associated with those inputs.
![comparison](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/90583d7a-8474-43bf-90c1-ae69a4d250c5)

</details>
 <details>
<summary>Hierarchical Synthesis and Flat Synthesis</summary>
<br>

Let us consider a module having two submodules as following code and schematic for understanding hierarchical synthesis and flat synthesis.
```verilog
module sub_module2 (input a, input b, output y);
	assign y = a | b;
endmodule

module sub_module1 (input a, input b, output y);
	assign y = a&b;
endmodule


module multiple_modules (input a, input b, input c , output y);
	wire net1;
	sub_module1 u1(.a(a),.b(b),.y(net1));  //net1 = a&b
	sub_module2 u2(.a(net1),.b(c),.y(y));  //y = net1|c ,ie y = a&b + c;
endmodule
```

![Schematic](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a08c9ee6-8c23-435b-896d-092bc9b3f25f)

Now inorder to synthesize a netlist from RTL code, we follow these steps using yosys:

 **Step-1**: Load the yosys tool by giving yosys command
```bash
$yosys
```
**Step-2**: Inorder to run yosys, we need two inputs verilog file and .lib file. So, These inputs were given using read_verilog and read_liberty thus successfully finishing frontend
```bash
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog multiple_modules.v
```
**Step-3**: Inorder to synthesize the netlist, we use **synth -top** command to synthesize the toplevel module. This gives the count of no. of bits, wires, inputs,cells etc...
```bash
yosys> synth -top multiple_modules
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
![cell design](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6cd3bd1b-b089-4205-b776-2decaf2ee594)

Here, the **show** command must specify the name, as there are multiple modules. The **multiple_modules** here specify the top_level.
In this output, there are two sub_modules specified as blackbox without any idea of the logic in it. The circuit gives information only about inputs and outputs.
The final schematic of the multiple_module is as:
![out1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1d01c03e-354b-405e-9992-710195736d34)

Step-4:Finally, by using the write_verilog command it converts the behavioral code into the gate-level netlist as following:
```bash
yosys> write_verilog -noattr multiple_modules_hier.v
yosys> !gvim multiple_modules_hier.v
```
So, The hierarchical Synthesized netlist is as follows:
```verilog
module multiple_modules(a, b, c, y);
  input a;
  input b;
  input c;
  wire net1;
  output y;
  sub_module1 u1 (
    .a(a),
    .b(b),
    .y(net1)
  );
  sub_module2 u2 (
    .a(net1),
    .b(c),
    .y(y)
  );
endmodule

module sub_module1(a, b, y);
  wire _0_;
  wire _1_;
  wire _2_;
  input a;
  input b;
  output y;
  sky130_fd_sc_hd__and2_0 _3_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
  assign _1_ = b;
  assign _0_ = a;
  assign y = _2_;
endmodule

module sub_module2(a, b, y);
  wire _0_;
  wire _1_;
  wire _2_;
  input a;
  input b;
  output y;
  sky130_fd_sc_hd__or2_0 _3_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
  assign _1_ = b;
  assign _0_ = a;
  assign y = _2_;
endmodule
```
The flattened nelist is the netlist where the hierarchies (or submodules) are replaced by the actual gates logic present in those sub modules. Inorder to generate the flattened netlist the first 3 steps were same. In the step-4,
```bash
yosys> flatten
yosys> write_verilog -noattr multiple_modules_flat.v
```
The output of the flattened synthesis is:
```verilog
module multiple_modules(a, b, c, y);
  wire _0_;
  wire _1_;
  wire _2_;
  wire _3_;
  wire _4_;
  wire _5_;
  input a;
  input b;
  input c;
  wire net1;
  wire \u1.a ;
  wire \u1.b ;
  wire \u1.y ;
  wire \u2.a ;
  wire \u2.b ;
  wire \u2.y ;
  output y;
  sky130_fd_sc_hd__and2_0 _6_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
  sky130_fd_sc_hd__or2_0 _7_ (
    .A(_4_),
    .B(_3_),
    .X(_5_)
  );
  assign _4_ = \u2.b ;
  assign _3_ = \u2.a ;
  assign \u2.y  = _5_;
  assign \u2.a  = net1;
  assign \u2.b  = c;
  assign y = \u2.y ;
  assign _1_ = \u1.b ;
  assign _0_ = \u1.a ;
  assign \u1.y  = _2_;
  assign \u1.a  = a;
  assign \u1.b  = b;
  assign net1 = \u1.y ;
endmodule
```
In this figure, there are no hierarchies such as u1, u2 and we have the gate logic present in it such as AND, OR.
![flatshow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fa852f0d-91f5-4991-bcfc-a81fe5fbd647)


Inorder to generate a submodule only, we give the sub-module name(sub_module1) with **synth -top** command
The following image shows the synthesized circuit of **sub_module1**. The submodules can be generated 
- whenever there are multiple instances of same module in the design
- To stitch various modules when there are massive designs 
![mod](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/540f7b2f-7ce0-4a0a-a195-3464987eecf9)

</details>
<details>
<summary>Flop coding Styles</summary>
<br>	
	
#### Why flops?
In a combinational logic design, the change in input is seen at the output after the propagation delay. During the propagation of data, if there are more cells of different delays, this might cause a glitch in the output. If this combinational logic has more cells, this would cause an unstable output.In order to avoid these glitches, the flops are used between the combinational design.

The flip-flop is a single bit storage device used between the combinational circuit to avoid glitches in the output.When a flop is used, the output of the previous stage is stored until there is a posedge or negedge triggered at the clock so the combinational circuit avoids glitches at the output as each stage is sort of shielded from input to output by the clock.

The signals such as set or reset are used to initialise the flops otherwise any (previous value) garbage value could be propagated to next stage. These signals can be asynchronous or synchronous.

### Lab on flop synthesis:
Inorder to generate the gtkwave using iverilog, the following sequence of steps are followed:
```bash
$iverilog dff_asyncres.v tb_asyncres.v
$./a.out
$gtkwave tb_dff_asyncres.vcd
```
The **./a.out** generates a vcd output file that can be viewed with gtkwave
Inorder to generate the synthesized circuit, the following sequence of steps are followed:
```bash
$yosys
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_asyncres.v
yosys> synth -top dff_asyncres
yosys> dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show
```
**Asynchronous reset**: The asynchronous reset is the input of the flop, which shifts the output to 0 irrespective of the clock or the input signal D on the flop. 
The Behavioral code of asynchronous reset is as follows:
```verilog
module dff_asyncres ( input clk ,  input async_reset , input d , output reg q );
always @ (posedge clk , posedge async_reset)
begin
	if(async_reset)
		q <= 1'b0;
	else	
		q <= d;
end
endmodule
```
This can be visualised as on gtkwave as follows:
![dff_asyncres gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cabb77e7-d1b5-4bb0-bf5e-799489f1063d)

The synthesized circuit for asynchronous reset is:
![dff_asyncres show](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d5a6ee70-2b29-4fe3-8a46-5b31c39fa8b5)
***Asynchronous set**: The output of the flop changes to 1 irrespective of the clock edge or the input signal of D on the flop. 
The Behavioral code of asynchronous set is:
```verilog
module dff_async_set ( input clk ,  input async_set , input d , output reg q );
always @ (posedge clk , posedge async_set)
begin
	if(async_set)
		q <= 1'b1;
	else	
		q <= d;
end
endmodule
```
The gtkwave output is as follows:
![dff_asyncset gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/edac6109-0013-415c-afab-13aac0f146fd)

The synthesized circuit is as follows:
![dff_ayncset show](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f3ef913e-eac7-4bb5-87f6-9f7fee21eeb3)

**Synchronous reset**: The Behavioral code of synchronous reset is as follows:
```verilog
module dff_syncres ( input clk , input async_reset , input sync_reset , input d , output reg q );
always @ (posedge clk )
begin
	if (sync_reset)
		q <= 1'b0;
	else	
		q <= d;
end
endmodule
```
The synthesized circuit is as follows:
![dff_syncres show](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f475f1b5-2d30-4f13-98b3-b1a1c662d7c8)

The simulated wave is as follows:
![dff_syncres gtkwave](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/36a5b560-4d83-4c30-a400-b4121ef23aef)
</details>
<details>
<summary>Coding optimizations</summary>
<br>	
	
Some circuits may not need any standard cells like multiplication by 2. These circuits doesn't need **'abc -liberty'** command. 
Let us consider multiplication by 2 and multiplication by 9. In binary number system, when a number is multiplied by 2, the number can be appended by 0 at the end. In other words, When a number multiplied by 2^n, the number shifts n digits to left. 
For example, Let us consider the truth table of 2:

![image](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dbb265c6-cce2-4f80-9cbf-1db1bc1491da)

The behavioral code is as follows:

```verilog
module mul2 (input [2:0] a, output [3:0] y);
	assign y = a * 2;
endmodule
```
The simulated circuit and the synthesized netlist are as follows:
![mul2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0d59f15c-afbd-49b5-a18a-0d20a8bf1ac5)
**Multiplication by 9**: When a number is multiplied by 9, the number gets repeated itself. This can be as illustrated:
![mul9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c895c83a-e8f3-4037-b4f6-a26f78244692)

The behavioral code is
```verilog
module mult8 (input [2:0] a , output [5:0] y);
	assign y = a * 9;logic to m
endmodule
```

The synthesized circuit and netlist are:
![mult8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7d5c17b6-ade6-45c6-a4ce-69276fa44568)

</details>

## Day3 : Combinational and Sequential Optimizations

<details>
<summary> Combinational Optimization with examples </summary>
<br>
The Combinational Logic Optimization is nothing but squeezing the logic to get the most optimized design thus reducing area and power.  The techniques used for Combinational Optimization are:
	
  ### Constant propagation, which is a direct optimization technique 
  The following image is an example of constant propagation. When A is tied down to ground (logic 0), the output will be the inversion of C input. In the MOS Transistor implementation, the combinational logic would occupy 2 gates with 3 inputs. As the input A is constant, it can be reduced to 2 transistor logic (inverter) with single input, which occupies less space and reduces power consumption.
  ![comb opt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2db5e402-17b0-4e0f-b678-98dbba29d69d)
 ### Boolean Logic Optimization, can be done by using K-Map or Quine McKluskey Method
 Let us consider an example statement **assign y=a?(b?c:(c?a:0)):(!c)**. The following expression is using ternary operation, that can be realised by using multiplexers as shown. The logic can be reduced as following by using laws of boolean algebra such that a series of multiplexers got reduced to an xnor gate.
 ![bool opt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5a31fb1e-e10b-4b94-bee1-8ab0ea16ce80)

 ### Lab examples on combinational Optimization
 The command to do optimizations is **opt_clean -purge**,  which is executed after *synth -top* command.
 #### Example-1:
 The behavioral code is:
 ```verilog
module opt_check (input a , input b , output y);
	assign y = a?b:0;
endmodule
```
![opt1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8a0a38b1-3edc-497c-9091-2cdbf15bc05f)

The synthesized circuit is:
![optcheck](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bcafa937-84d2-4444-95be-bcad2b0989a3)
 #### Example-2:
  The behavioral code is:
 ```verilog
module opt_check2 (input a , input b , output y);
	assign y = a?1:b;
endmodule
```
![opt2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fd0d7987-44df-4b30-86f4-e224b10e5ee8)

The synthesized circuit is:
![optcheck2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fab49fd2-c826-43fa-807f-f33984095616)

#### Example-3:
  The behavioral code is:
```verilog
module opt_check3 (input a , input b, input c , output y);
	assign y = a?(c?b:0):0;
endmodule
```
![optcheck3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/efae5e77-ba90-44e3-aef1-d7a298710589)

The synthesized circuit is:
![opt3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a1f65ca2-e5ab-41c4-b72c-e2fd884e3f3d)

#### Example-4:
  The behavioral code is:
```verilog
module opt_check4 (input a , input b , input c , output y);
 assign y = a?(b?(a & c ):c):(!c);
 endmodule
```

![exp4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ab808849-18d1-4f7c-978d-51e2140794e6)

The synthesized circuit is:
![optcheck4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/eaf3960a-2a41-43a0-9104-114186a0379b)

#### Example-5:
The multiple modules are being synthesized from RTL code to netlist. So, The following sequence of steps are followed:
```bash
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> read_verilog multiple_module_opt.v
yosys> synth -top multiple_module_opt2
yosys> opt_clean -purge
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> flatten
yosys> show
yosys> write_verilog -noattr multiple_module_opt_net.v
```
 The behavioral code is:
```verilog
module sub_module1(input a , input b , output y);
 assign y = a & b;
endmodule


module sub_module2(input a , input b , output y);
 assign y = a^b;
endmodule

module multiple_module_opt(input a , input b , input c , input d , output y);
wire n1,n2,n3;

sub_module1 U1 (.a(a) , .b(1'b1) , .y(n1));
sub_module2 U2 (.a(n1), .b(1'b0) , .y(n2));
sub_module2 U3 (.a(b), .b(d) , .y(n3));

assign y = c | (b & n1); 


endmodule
```
The synthesized circuit is:

**Before flatten**:
![multimod1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b38aadf5-d636-401b-a9e4-e486fa8a271b)
**After flatten**:
![multimod1after](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/36200cdd-09b4-4c27-87f0-8da253653e0b)
#### Example-6: 
The behavioral code is:
```verilog
module sub_module(input a , input b , output y);
 assign y = a & b;
endmodule



module multiple_module_opt2(input a , input b , input c , input d , output y);
wire n1,n2,n3;

sub_module U1 (.a(a) , .b(1'b0) , .y(n1));
sub_module U2 (.a(b), .b(c) , .y(n2));
sub_module U3 (.a(n2), .b(d) , .y(n3));
sub_module U4 (.a(n3), .b(n1) , .y(y));


endmodule
```

![exp6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/23b3e55f-9bc5-456d-9625-6e0716b75282)

The synthesized circuit is :

**Before flatten**:

![opt2before](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/03222a2d-1bb6-4a6f-b6a5-63520af9a964)

**After flatten**:
![mod2after](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/145d3633-a910-4e3e-b5da-3d9919566a89)
</details>	
<details>
<summary>Sequential Optimization with examples</summary>
<br>
The various Sequential Optimisation techniques are:
	
- Sequential Constant Propagation
- State Optimization
- Retiming
- Sequential Logic Cloning
  ### Sequential Constant Propagation
  The sequential propagation occurs when there is no change in output irrespective of the inputs or clock being applied. For example, In the following circuit, the D is tied down to ground, the output is always 0 whatever may be the reset condition. But This will not continue to next sequential stages. The output of next sequential stage may or may not vary. The output of this NAND gate will be 1 as Q is always 0.
  
![seqconstpropaga](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ef9c7d52-fede-4ac8-b52d-721d8a88b7a0)

Let us consider the set with D flip-flop. In the following example, the output is high when set is applied and low when no set condition. But it cannot be interpreted as set inverted condition. Considering the set to be asynchronous (change in state before clock edge), but the output still does not change until the clock edge. So, This type of circuits cannot be optimized and they are retained in the design.

![set seq](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3b68c3c6-edcb-44d3-9805-ca320bc1abda)

**State Optimization**

The state optimization is the optimization of unused states. Depending upon states, we can get the most optimized finite machine.

**Cloning**

  Cloning is done with *Physical aware synthesis*. This can be explained through an example. Let us consider 3 flipflops A,B,C, which are far from each other with more routing length. Let A be the launching flop of both B and C capture flops. Assuming that the positive slack is high, The A flop is cloned to two different points on the net length such that the distance between launch and capture is reduced, thus reducing the delay of the circuit. The cloning implies that the flop is copied to two distinct points where it is not present. This is an advanced optimization technique.
  
  **Retiming**
  
  Retiming is done to improve the performance of a circuit. When two consecutive combinational stages operate at different frequencies(that is have different combinational delay), some of the logic is moved to the next flop, thus reducing the delay at each stage and improving the frequency of operation without any change in the logic of the design.  This involves scrutinizing the existing schedule, pinpointing bottlenecks, reordering for better efficiency, integrating alterations, and validating the resultant performance enhancements.
 ### Lab examples on Sequential Optimization
 #### Example-1
 
 The behavioral code is:
 ```verilog
module dff_const1(input clk, input reset, output reg q);
always @(posedge clk, posedge reset)
begin
	if(reset)
		q <= 1'b0;
	else
		q <= 1'b1;
end

endmodule
```
The following code shows the synchronous reset condition. The D input is always connected to 1. So, when reset is high, output is 0. when reset is low, output is high after the arrival of next clock edge.

The Synthesized circuit is:
![dfffcionst1ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9d03e2b2-4a00-4d18-8615-38c344a26922)

The simulated output is:
![dffconst1gtkwave](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/145f35d2-2b2f-4259-91f9-da202042deaa)

#### Example-2
 The behavioral code is:
 ```verilog
module dff_const2(input clk, input reset, output reg q);
always @(posedge clk, posedge reset)
begin
	if(reset)
		q <= 1'b1;
	else
		q <= 1'b1;
end

endmodule
```
The following code shows constant propagation of logic 1. Here, the reset input is considered to be set condition. WHen reset is high, output is high. When reset is low, output is high till next clock edge. After next clock edge, the output is high as D input is connected to logic 1. So, no flipflop is required after optimization.

The Synthesized circuit is:

![dffconst2ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/66ef2acd-de11-4ed5-b63c-883a1401265a)

The simulated output is:

![dffconst2gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bdb3ef18-e296-4dc8-8b9e-de3bb8eeccda)

#### Example-3
 The behavioral code is:
 ```verilog
module dff_const3(input clk, input reset, output reg q);
reg q1;

always @(posedge clk, posedge reset)
begin
	if(reset)
	begin
		q <= 1'b1;
		q1 <= 1'b0;
	end
	else
	begin
		q1 <= 1'b1;
		q <= q1;
	end
end

endmodule
```
This is a 2 flipflop reset-set circuit. Here, The output of q1 is low when reset is high. The output of q1 is high after next clock edge when reset is low. The output of q is only low at the instant of change in reset condition, else it is always high. This happens due to the *clk-q delay* present in the q1 flipflop output. SO, the state goes low for this cycle, and retains to 1 from next clock edge.
The Synthesized circuit is:

![dffconst3ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4b85033a-7982-49bc-9318-f209481c42e1)

The simulated output is:

![dffconst3gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2fc92814-54ba-4742-ae52-53e60c5eedff)

#### Example-4
 The behavioral code is:
 ```verilog
module dff_const4(input clk, input reset, output reg q);
reg q1;

always @(posedge clk, posedge reset)
begin
	if(reset)
	begin
		q <= 1'b1;
		q1 <= 1'b1;
	end
	else
	begin
		q1 <= 1'b1;
		q <= q1;
	end
end

endmodule
```
In this circuit, there is no need of flipflops as the outputs q1 and q are high irrespective of clock edge or reset condition.

The Synthesized circuit is:

![dffconst4ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d9b32810-11a2-4f59-bf5a-a327f4f76731)

The simulated output is:

![dffconst4gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a0d5c25f-61d2-4765-a562-165850ecac7b)

#### Example-5
 The behavioral code is:
 ```verilog
module dff_const5(input clk, input reset, output reg q);
reg q1;

always @(posedge clk, posedge reset)
begin
	if(reset)
	begin
		q <= 1'b0;
		q1 <= 1'b0;
	end
	else
	begin
		q1 <= 1'b1;
		q <= q1;
	end
end

endmodule
```
Here, q is the primary output and q1 is the intermediate output. This is similar to synchronous reset condition. But the output changes after one more clock cycle as there are two flipflops.

The Synthesized circuit is:

![dffconst5ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/94277438-1d08-4f43-a0f9-ecb8c061025b)

The simulated output is:

![dffconst5gtk](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/48730d06-a8a9-4f5d-a3f4-eb8e6baf4483)

</details>	
<details>
<summary>Sequential Optimization of unused outputs</summary>
<br>
The Sequential circuit having unused outputs( that is the outputs are not required) can be optimised.	

#### Example-1:	
Let us see an example of 3-bit counter. The Behavioral code is:
```verilog
module counter_opt (input clk , input reset , output q);
reg [2:0] count;
assign q = count[0];

always @(posedge clk ,posedge reset)
begin
	if(reset)
		count <= 3'b000;
	else
		count <= count + 1;
end

endmodule
```
In the following ocde, the q takes count[0] and count[1] and count[2] are unused. The counter resets to 0 if reset is high else it increments the value of counter. We know, the incrementing of counter of LSB  toggles output for each clock cycl, which is independent on other output states. So, this can be optimized by using a single toggle flipflop instead of 3 flipflops, that changes output for every clock cycle.

![tff](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6484b782-9163-46bc-a3d5-b17d72b6fb45)

This can be viewd by synthesis. The reset is active low so an inverterr is connected as we defined reset active high. The ouput of flipflop is given to an inverter and back to D flipflop which gives the toggle flipflop output.

The synthesized circuit is:

![countckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cb2998da-0aaf-4124-81a5-3452acdc0232)

#### Example-2: 
Now Let us see an example that uses the 3 flipflops. The Behavioral code is:

```verilog
module counter_opt (input clk , input reset , output q);
reg [2:0] count;
assign q = count[2:0] == 3'b100;

always @(posedge clk ,posedge reset)
begin
	if(reset)
		count <= 3'b000;
	else
		count <= count + 1;
end

endmodule
```

In this example, the q is assigned the 3 bit value 100, so this can be obtained using NOR gate as follows:

![count2 logic](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1ce167d2-da5b-44cf-b470-ffed1c36f997)

Here, the 3 flipflops are required as output is a 3 bit data so all the flipflops are retained and the combinational logic specifies the adder logic, incrementing the counter upon each clock cycle. 

The synthesized circuit is:

![countopt2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dc92ffa7-18b5-46f2-8349-1511c70718d7)

</details>	

## Day4 : GLS,blocking vs non-blocking and Synthesis Simulation mismatch
<details>
<summary> GLS and Synthesis-simulation mismatch </summary>
<br>
	
#### What is GLS?
GLS stands for Gate Level Simulation. GLS is obtaining the simulated output by running testbench with netlist as design under test (DUT). Before, the simulation is done with RTL code as DUT, and the testbench providing stimulus to code as per the specifications.

The Netlist is logically same as the RTL code. So, same testbench goes with the netlist as specifications are same.The netlist is plugged in place of RTL file and simulation is run by invoking simulator with testbench.

#### Why GLS?
The GLS is done to verify the logical correctness of the design. When simulation is done in RTL, there is no notion of timing. To ensure timig is met, GLS needs to be run with delay annotation.

The following image shows the iverilog flow of the process. The iverilog takes an extra input, that is gate level verilog models to generate GLS simulated output. If these gate level models are delay annotated, then this GLS can be used for timing validation.

![gls iverilog flow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7290001b-5c45-4390-8093-9d39346542bb)

In this design, let us assume the following state is defined, the subsequent netlist is obtained as shown. The files that define the behaviour of **and** and **or** in the netlist are the gate level verilog models. The gate level verilog models can be timing aware (both timing and logic is ckecked) or functional (only logic benaviour is checked).
![ex](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/337ba22f-7372-4647-ae10-218fbeffdbe3)

#### Synthesis Simulation Mismatch:
The reasons for synthis simulation mismatches can be:
- Missing Sensitivity List
- Blocking vs Non-Blocking Assignments
- Non Standard Verilog Coding

**Missing Sensitivty List:**

 A Simulator works based on the activity. When there is a change in input, then only output changes. Let us consider an example of 2x1 multiplexer. The bahavioral code on left only considers sel as input. So when sel changes, the output is evaluated at that instant and corresponding io or i1 is captured at that instant and  it continues at output until there is next change in sel irrespective of changes in io or i1.
 In constrant to this, the behavioral code on right, evaluates the change in every signal( which can be sel or i0 or i1).

![sensit exp](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/553f59ed-8e78-4e67-8083-eeba7440ef95)

**Blocking and Non-Blocking Statements in Verilog:**

A Blocking Statement evaluates statements in the order they are written inside the always block. The Blocking Statements use **=** for assigning values.
A Non-BLocking Statement evaluates all the assigning variables at once on the RHS and assign to those on LHS when it enters always block. The Non-Blocking Statements use **<=** for assigning values.

Nonblocking assignments are only made to register data types and are therefore only permitted inside of procedural blocks, such as initial blocks and always blocks. Nonblocking assignments are not permitted in
continuous assignments.

This improper assignment sometimes cause mismatches due to improper use of blocking Statements.

- Combinational (always@*) →blocking (=) assignment.
- Sequential (always@posedge) → non-blocking (<=) assignment
- Always separate sequential and combinational logic

**Caveats with Blocking Statements**:
In this example, the flip flop assignment varies the number of flipflops dimulated in the circuit. These caveats can be avoided by using Non-Blocking Statements.

![caveat1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ba593e92-d9bc-4229-af7d-322b1ac3e9fc)

In this example, the synthesis yields the same circuit as shown, but the simulation gives different behaviour. This causes Synthesis-Simulation mismatch.

![caveat2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/93704ba6-37e2-4635-9255-455587abd8cf)

 Due to such issues, it becomes paramount importance to run GLS on netlist and match the behaviour of output simulated and expected. So, This is why we run GLS.
 </details>

<details>
<summary> Labs on GLS and Synthesis-simulation mismatch </summary>
<br>

#### Example-1
A Ternary operator takes 3 operands. It is in the form of **<condition>?<True>:<False>**. When the condition is true, the first part is executed and if the condition is false, the second part is executed.
The behavioral code is :
```verilog
module ternary_operator_mux (input i0 , input i1 , input sel , output y);
	assign y = sel?i1:i0;
	endmodule
```

The RTL simulated output is:
![rtlexxp1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/68b78ddd-d67f-4458-88a9-c0ddec5baf4c)

The RTL synthesized circuit is:
![exp1ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c4720c7b-4cf6-4da1-bb0f-de5f1254d1ca)

The GLS simulated output is:
This is simulated using the RTL netlist, testbench, and the verilog models by giving to iverilog. Then the vcd file is dumped and viewed using gtkwave.
![glsexp1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/864d3fa6-5db6-46bd-8ebe-0213200141e5)

#### Example-2
Now let us look at the example of a bad_mux. 
The Behavioral code is:
```verilog
module bad_mux (input i0 , input i1 , input sel , output reg y);
always @ (sel)
begin
	if(sel)
		y <= i1;
	else 
		y <= i0;
end
endmodule
```
The synthesized circuit is:

The circuit is a 2x1 multiplexer, although the behaviour mimics a dual-edge triggered flipflop.
![showex2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/392c28b9-173c-43fc-a00f-5b16bdfc47cf)

The simulated output is:

Here, the top image shows RTL simulation and bottom image shows GLS simulation. The above image didn't reflect the changes in input at the output after the select line edge, but below image reflected the corresponding changes in input at the output through select line. The GLS can be inferred as there are extra inputs as _1_,_2_,_3_..., which are absent in RTL simulated output. So, This is a *synthesis-simulation mismatch* as the generated output differs between RTL and GLS.
![outex2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/08607860-45eb-42cd-a005-4763261e9837)

#### Example-3
Now let us look at another caveat explained.
The behavioral code is:
```verilog
module blocking_caveat (input a , input b , input  c, output reg d); 
reg x;
always @ (*)
begin
	d = x & c;
	x = a | b;
end
endmodule
```

The synthesized circuit is:
This circuit mimics a flop, but there is no flop in the synthesized circuit.
![lastexp](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/11735cfc-2338-4ce7-bd36-b9b35154686f)
The simulated output is:
![rtl3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0b5d7cd2-1818-4bed-8057-3380837b2f20)

In the RTL simulated output, though a or b is low, the output is high when c is high. This occurs due to the usage of blocking statements. The previous value of a|b  is used to and with c. So, the x mimics a flipflop. In the GLS si,ulated output, the output is clearly dependent only on the present inputs.
</details>

## Day5 : DFT
<details>
<summary>DFT</summary>
<br>	
	
### Design for Testability

DFT is a technique which facilitates a design to become testable after production or adding an extra design for an existing design to make sure it can be tested after being fabricated. DFT makes testing easy for post-production process. There are 3 main levels of testing chips after being fabricated i.e., chip-level(die-level), board level, system-level. DFT is also done due to market and economical needs.
**Testability**: If a design is well-controllable and well-observable, it is said to be testable. There are different DFT techniques such as MBist Logic (Memory Built-in Self test), scan chains (for flops), test patterns (combinational circuits). DFT insertion is done during synthesis. 
The DFT reduces tester complexity, tester time and reduces faulty devices, although it adds complications to design flow. The scan chain insertion may cause more setup and hold violations increasing design time and power,area.
#### Basic Terminology:
- Controllability : A point is said to be controllable if both ‘0’ and ‘1’ can be propagated through scan patterns. The controllability can be achieved by using mux or any other selector switch. This may icrease area, power in design
- Observability : The ability to measure the state of a logic signal. When we say that a node is observable, we mean that the value at the node can be shifted out through scan patterns and can be observed through scan out ports.
- Stuck at-fault: It is a physical damage/defect compared to the good system, which may or may not cause system failure.
- Error: An error is caused by a fault because of which system went to erroneous state.
- Failure: failure is when the system is not providing the expected service. A fault causes an error which leads to the system failure.
- Fault Coverage: Percentage of the total number of logical faults that can be tested using a given test set.
- Defect Level: Refers to the fraction of shipped parts that are defective. In the other words, the proportion of the faulty chip in which fault isn’t detected and has been classified as good.

There are two main techniques of DFT.
-**Adhoc Technique**:
Rules:
○ Avoid combinational feedback
○ All flip flops must be initializable
○ Partition a large circuit into small blocks.
○ Provide test control for the signals which are not controllable
○ While designing test logic we have to consider the ATE requirements
-**Structured Technique**:
 - In this, we use a new kind of flipflop called scan flipflop. An extra combinational design added to flipflop.
 - Boundary scan is the scan done by limiting number of devices to be scanned.Bist can be LBist or MBist.
![scanflop](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1fd9c312-c10c-494b-b6a7-c4d80cf9cfe0)

**Scan Chain Technique**:
Scan chains are the elements in scan-based designs that are used to shift-in and shift-out test data.
- Scan chain technique can be explained as:
   - Specifying the scan constraint
   - Specifying Scan ports and scan enbles
   - compiling dft
   - identify number of scan chains
- A scan chain is formed by a number of flops connected back to back in a chain with the output of one flop connected to another flop.
- The input of first flop is connected to the input pin of the chip (called scan-in) from where scan data is fed. The output of the last flop is connected to the output pin of the chip (called scan-out) which is used to take the shifted data out.
- Scan flops are used to test stuck-at faults and test path delays in thew design.
- Number of cycles required to run a pattern = Length of largest scan chain in design.
- Smaller chain length means more number of input/output ports is needed as scan_inand scan_out ports.
              -  Number of ports required = 2 X Number of scan chain
  There are 3 types of scan flip-flops configurations namely multiplexed, clocked, lssd (latch sensitive scan design).
  The overview of DFT compiler is as follows:
  ![dft compiler](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bcf89ce1-e198-425c-8d73-bfd7621c2531)
  
  Steps followed to draw scan chain:
1. Assert scan_enable (make it high) so as to enable (SI -> Q) path for each flop
2. Keep shifting in the scan data until the intended values at intended nodes are reached
3. De-assert scan_enable (for one pulse of clock in case of stuck-at testing and two or more cycles in case of transition testing) to enable D->Q path so that the combinational cloud output can be captured at the next clock edge.
4. Again assert scan_enable and shift out the data through scan_out
</details>

## Day6 : Introduction to Logic Synthesis
<details>
<summary>Basics of Digital Logic design and RTL Synthesis</summary>
<br>	 
	
### Basics of Digital Design
Digital Logic is a switching function which is powerful in automation and decision making. Most of the automation involves decision making circuits. These specifications are mentioned as the behavioral design, written in HDLs. The famous HDL are VHDL, Verilog.
	
-  Every design starts with a target specification. This decides the architecture of the chip. This representation is done in a programming language (RTL).
-  The RTL is the behavioral code. We require the actual gates i.e., gates, flops etc..
![Screenshot 2023-09-02 150858](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/064d5a33-aec1-4792-a3d7-5c5efaa5438d)

-  The RTL code is translated into gate level netlist by Synthesis. The synthesis tool takes .lib and verilog file as input and gives netlist as output.
- .lib is a collection of different logical modules(AND, OR, NOT, NAND...) with different flavors(Fast, typical, slow). We need faster cells to meet setup (also for higher performance) and slower cells to meet hold requirements.
- The hold time implies that the data to capture flop shouldn't be changed during this window. The data should arrive only after the hold window and before the setup window. The intermediate period is the combinational period which determines the speed of circuit.
![launch capture](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/31c1abe5-32bd-40ba-a4ae-ddb21000cdaa)

- From the MOSFET drain current equation, we know, drain current is proportional to the width to length ratio. As width of transistor increases, the current capacity increases, thus faster charge/discharge and vice-versa.
- The Synthesizer is guided to select the flavor of cells that are optimum for implementation of logic circuit. This guidance is referred as constraints.

### Logic Synthesis
 - Logic Synthesis tries to achieve a working digital circuit which is logically and electrically correct by meeting the timing specifications.
 ![lc](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/356b01c0-1aa4-44fa-a784-b38a80b285fc)

  Let us consider an example to understand.
![exlogic synth](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f979159f-71af-4e41-9e3d-cb9f14d799bf)
In this example, let us assume the behavioural code of 3-bit carry adder logic (i.e., ab+bc+ca). So, this logic can be implemented in many ways using the basic logic gates. Consider the following values of delay and area for the standard cells (logic gates) used in the implementation. When the delay of each implementation is considered as the following table, the third implementation gives the least delay and consumes less area. But, if the path where logic is present is a hold-sensitive path, we need to use either second or first implementation depending on the requirement to meet the violation it might cause.

- *The constraints are the guide to synthesizer to pick the correct library cells which are appropriate for optimum design*.
</details>

<details>
<summary>Introduction to DC Shell</summary>
<br>	

The Design Compiler is a synthesis tool targeted for ASIC flow from Synopsys.

#### Features:

- Established as a premium synthesis tool across semiconductor industry
- Interoperabilty with various backend tools from Synopsys
- Has the ability to perform DFT Scan stitch
- Can handle huge designs with extreme complexity and provide very good QoR
  
### Common Terminology associated with DC:

- *Synopsys Design Constraints*(SDC) : These are the design constraints which are supplied to DC to enable appropriate optimization suitable for achieving the best implementation.
- *.lib* : Design Library which contains the Standard cells.
- *.db* : Same as .lib but in a different format. DC understands libraries in .db format
- *.ddc* : Synopsys propreitary format for storing the design information. DC can write out and read in DDC.
- *Design* : RTL files which has the behavioral model of the design. 

#### SDC : Synopsys Design Constraints

- The SDC format specifies the design intent in terms of **timing, power and area** constraints. Power is specified interms of UPF. UPF can be read through SDC commands.
- Supported by different EDA tools across semiconductor Industry.
- SDC is based on Tool Command Language (Tcl).

#### DC Setup:

The dc setup takes the RTL files and .lib files (as in yosys) and also SDC to generate the gate-level netlist, ddc format file and synthesis reports as outputs.

![dcsetup](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c124c265-17b5-46d8-95a5-b256299f303c)

The ASIC flow is the steps involved in converting RTL to the physical database(GDS). The Application Specific IC flow is as follows:

The RTL is the behavioral code of design. It is synthesized into logical netlist (consists of gates). After DFT, it is placed after proper floor plan  and synthesis of clock tree.Then final database i.e., physical netlist is obtained.

![asic flow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ecc17f1e-49b8-4b65-a90b-28eb5add0113)

The DC Synthesis flow can be illustated as follows:
Here, the *Design.lib* is a design library, not the standard .lib or technology library, which can be a third-party IP that can be a readymade design available. The DC ensures that the outputs and inputs of this module are properly connected to design and appropriately optimizing the logic.

The Design Compiler reads the verilog files of design and standard library files and constraints and generates reports after linking and synthesizing the design. It finally writes out a netlist as output.

![dcsynth flow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cbb90ec5-53bc-4d7e-8379-c889c566de76)

#### Invoking dc basic setup
The .lib file is for user reference and .db file is for DC reference. The DC understands .db format, not .lib format. The contents of .lib file are as follows:
![lib](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5e1d27ef-53bc-47eb-8619-c6ce86b5abbe)

We know that the library name consists of the information such as PVT (Process, Voltage, temperature) conditions of design. Every electronic circuit operation is a function of voltage, temperature and process.
The .lib is specified for each PVT corner.This PVT corner is a typical, 25c temperature and 1.8V. This .lib file gives information such as units of R,L,C, time & type of technology used and the various flavors of each cell etc... 
The dc shell is invoked using following commands:
```bash
$ csh
$ dc_shell
dc_shell> 
```
We need to enable cshell and then invoke DC shell. The DC shell checks the license of various compilers like VHDL compiler,HDL compiler(to understand the verilog or any other HDLs), DFT compiler(as DC enables scan stitich), Design vision(graphical version of DC), Power Compiler(as it is power aware synthesis) etc... This can be illustrated as follows:

![dc_shell (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/45410227-54db-4905-b9ef-3d8e37c12a80)

```bash
dc_shell> echo $target_library
 your_library.db
dc_shell> echo $link_library
 * your_library.db
```
In DC, the technology file is in the form of target library or link library. These both libraries are used by DC shell to pick standard cells. 
**your_library.db** is an imaginary non-existent library, just pointed for dummy purpose.
```bash
dc_shell> read_verilog DC_WORKSHOP/verilog_files/lab1_flop_with_en.v
dc_shell> write -f verilog -out lab1_flop_net.v
dc_shell> sh gvim lab1_net.v &
```
We give the input verilog file (RTL code) to read and write the verilog file as read by the design. The file editor can't be opened with gvim in shell. We need to use the above **sh gvim <file_name> &** inorder to open a file editor with shell.
The Behavioral code of the design being read is :
```verilog
module lab1_flop_with_en ( input res , input clk , input d , input en , output reg q);
always @ (posedge clk , posedge res)
begin
	if(res)
		q <= 1'b0;
	else if(en)
		q <= d;	
end
endmodule
```
The expected behavior is:
![behave](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b82f913b-ea18-4616-bda3-99dd4ad90dcb)

But the out netlist file doesn't have any libs read. So, the dc shell reads lib files in .db format. 
```bash
dc_shell> read_db ~/DC_WORKSHOP/lib/sky130_fd_sc_hd_tt_025c_1v80.db
dc_shell> write -f verilog -out lab1_db_net.v
dc_shell> sh gvim lab1_db_net.v &
```

The cells are in SEQGEN but not as sky130 cells format. This happens because target & link library not assigned any file.
**gtech** is the virtual library in DC's memory to understand the design.
The following steps are proper sequence to write gate level netlist from the behavioral code:
```bash
dc_shell> set target_library /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd_tt_025c_1v80.db
dc_shell> set link_library {* <path to standardcell library> }
dc_shell> read_verilog DC_WORKSHOP/verilog_files/lab1_flop_with_en.v
dc_shell> read_db ~/DC_WORKSHOP/lib/sky130_fd_sc_hd_tt_025c_1v80.db
dc_shell> link
dc_shell> compile
dc_shell> write -f verilog -out lab1_flop_net.v
```

In the following image, you can clearly observe the SEQGEN cells changed to sky130 cells after proper linking & compiling.Now the outnetlist obtained is as follows:
![netlist out](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7bfa7e9f-bd79-4e1b-ada2-e5e24f53d454)

Now by assigning the files to the libraries, the design is linked and compiled as follows. Here, the link_library is assigned such inorder to append to the pre-existing list data without overwriting it.
The highlighted area are the commands used as above. 
![steps1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ffa4d3a4-98b2-4e37-87ab-f050a40d19a6)
After linking, it is showing the db linked ad the cell count and other design information after compiling.
![steps2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/12092d52-11f0-4741-892c-ccc4a7596bcb)
After succesful compilation, the output netlist is as shown above, the netlist now consists of sky130 cells.
![steps3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cf9203d5-e9ba-47f9-89be-37bb2bdd75a1)

#### Lab on ddc gui with design_vision
Inorder to launch the design vision, we again load cshell and **design_vision** command. This will launch the gui format of DC shell called design_vision. 
The command to write out a ddc file as output of dc_shell after writing out netlist is:
```bash
dc_shell> write -f ddc -out lab1_flop.ddc
```
The following image shows the design_vision loaded with gui. If the gui is not opened, you can use *start_gui* command. Design vision is internally compiled with dc shell.
![ddc](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f6a828c7-9f86-4afe-b4fe-2bb82d2fe4d6)

The ddc automatically loads the technology file and current design without specifying. ddc stores all the information in the tool memory in that particular session. But, ddc is a synopsys proprietary format, i.e., it can only be understood by Synopsys tools. The main advantage of ddc is all the information loaded in one tool can be saved and used in another tool with one command *read_ddc*.*read_verilog* reads only the verilog file. 
The following image shows the loaded read_ddc and read_verilog command. In the *read_ddc*, you can find the .db file loaded without specifying whereas, *read_verilog* command loads only the design data.
![ddccomp](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fef0344c-fa45-4f14-b4cc-719f42f7d615)

The schematic view of the scan flipflop is :
![ddcschem](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/489c2c53-fbe9-4cf0-9bcb-cba430bead36)

By clicking on this flop, the detailed behavior can be viewed.
The final behavior of the circuit is as follows (displayed with ddc gui) is:
![schem](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2cf101cd-c9db-42a3-a19f-82e43dbe0986)

 
#### Lab on .synopsys dc setup
Invoking the dc shell using csh, dc_shell commands. When a session is loaded, the target_library and link_library variables must be set everytime. In the real-time scenario, we will have multiple .db files for a design and we cannot miss them.
So, Setting these both variables everytime would be cumbersome and error-prone. This can be overcome by **.synopsys_dc.setup**.
DC reads .synopsys_dc.setup files in order:
- Synopsys installation directory (all user projects)
- User home directory (all projects for this user)
- Current project directory 
The order of priority is, if file exists in user_home_directory, will be picked and the installed (default) is ignored. If not found, then installed one is picked.
All repetitive tasks which are needed for tool setup can be pointed in this file (mainly target_library, link_library).When the tasks are defined in this file, the tool automatically picks these values and load it in tool memory.
So, This can be done by creating a file with this name and loading the shell as follows:
```bash
$ gvim .synopsys_dc.setup
$dc_shell
dc_shell> echo $target_library
```
The same can be illustrated as follows:
![syndcset](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/27803167-efb6-43af-b93e-6eb384f8c147)

</details>

<details>
<summary>TCL Scripting</summary>
<br>	
Tool Command Language is used for writing SDCs.
	
### Basic commands in TCL

- The tcl is typed language i.e., all gaps and paranthesis should be properly followed.
- The wildcard (*) is used for bigger data-sets.
- $ symbol is used for referring a variable, not for assigning.

```tcl
  set
  ```
   - It is used for creating and assigning any variable.
   - For example, **set a 5** --> a=5
   -    set a \[expr $a+$b\] --> a=a+b
   - The square brackets are used for nesting the commands in TCL.
     
  ```tcl
  if {condition} {
  statements if true
  } else {
  statements if false
  }
   ```

The condition must always be specified in curly braces only. The $ sign is used when the value of variable is being used, not when it is being assigned(with set).

For example,

```tcl
if {$a < 10} {
echo "$a is less than 10"
}else {
echo "$a is greater than 10"
}
```

- echo is the command used in tcl for displaying (same as linux).
	     
  ```tcl
  echo
  ```
     
 ```tcl
  while {condition} {
  statements
  }
 ```
For example,

```tcl
set i 0
while {$i < 10} {
  echo $i;
 incr i;
}
```
   - The **incr** is same as **set i \[expr $i+1\]** or **i=i+1**.
   - Wrong manipulation of variables could lead to infinite loops.
   - The incr is given with variable directly, not value of variable($i).

The following image shows the output and syntax of while loop. Though incr replaced with $i+1, the output didn't change.
![tcl2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/284a26a4-a2f4-4548-bcc2-de7a15820d75)

 
  ```tcl
  for {looping var} {condition} {looping var modification} {
  statements
  }
```

For example,
	  
```tcl
  for {set i 0} {$i < 10} {incr i} {
  echo $i;
  }
```
The following image shows the usage of for command and its syntax and using basic commands set (for assignment), incr (incrementing).
![tcl1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/adb24bb5-8057-4c07-bb82-c75341b74f09)


-  foreach is a general tcl statement.
```tcl
  foreach var list {
  statements
  }
```
	  
For example,

```tcl
set my_design_list [list u_top/u_mod1 \
			 u_top/u_mod3 ]
foreach my_module $my_design_list {
set_size_only $my_module;
  }
```

 - Here, **my_design_list** is the name of the list. List is similar to arrays in C.
 - \ is used as line breaker i.e., next line is continuation of the present command. 
 - The loop iterates for every element of the list. 
 - **set_size_only** is a DC specific command. 
- foreach_in_collection is a DC specific command

 The following image shows the usage of dc_specific command "get_lib_cells". In this image, the cellnames is a collection as it is closed with curly braces. 
 A list is generally closed with square braces.
 ![tcl3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/64e6b2d2-004b-47b3-83a9-246e1316da64)

```tcl
foreach_in_collection var collection {
   statements
 }
```
- The foreach command is used for lists and foreach_in_collection is a dc specific command used for collections.
![foreach ex](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8095eadc-d52b-42ca-bd4a-f341afb2e06e)

In the above example, the nesting of commands can be seen. The output of one variable is used to obtain another variable output.

The following image shows the usage of dc specific command "get_object_name". If get_object_name is not used, the shells gives a pointer as output such as "_sel3". So, now all the names of lib cells are printed as follows:
![tcl4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/749a1381-9ce5-4b38-886e-782dbb6f11e7)
The following code can also be written in a file editor and it can be executed using source command i.e.,
```bash
dc_shell> source abc.tcl
```
The tcl script in the gvim file is:
```tcl
foreach_in_collection my_var [get_lib_cells */*and*]  {
set my_var_name [get_object_name $my_var];
echo $my_var_name;
}

echo "Printing Multiplication table"
set i 5;
set j 1;
while {$j < 21} {
echo "$i x $j = [expr $i*$j]";
incr j;
}

set mylist [list a b c d e f g];
foreach myvar $mylist {
echo $myvar;
}
echo $mylist;
```

Now the output of the code is as follows:
![tcl5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1a03ec29-8276-4d2a-a97d-236e7748d527)

</details>

## Day7 : Basic SDC Constraints
<details>
<summary>Introduction to STA </summary>
<br>	

STA stands for Static Timing Analysis. 
- Every path has delay constraints, the maximum delay constraint (setup condition) and minimum delay constraint (hold condition). 
- The setup condition states the maximim delay the combinational circuit can have. The hold condition defines the minimum combinational delay.
- The clock period is fixed as it is defined as per our requirements. The clock-to-q delay and setup, hold values are specific for flipflops. So, The parameter that can be varied is combinational delay. So, the setup and hold equations can be written as follows: 
![equations](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9cd6be7b-7d60-437f-8311-8fb013db5448)

- This defines the minimum and maximum constraint on the combinational delay so that neither setup nor hold is violated.

Let us consider an example of combinational delay being 8ns and clock period of 5 ns, then the clock delay to capture flop is increased the adding delay to the clock path of capture clock. This causes a waveform as below. 

Now, the required time is increased (the period from 1st cycle of launch flop to 2nd cycle of capture flop). 
There comes a repercussion of minimum delay on this circuit. When the clock is pushed, the hold window of capture flop moves with it. So, data cannot arrive before the hold window. 
The new hold equation includes the push period as shown.In the following figure, data from launch cannot arrive before the hold window of capture flop as follows:
![clock push](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d3ae021f-486f-44f8-8d65-0a7441be496b)

#### Water Bucket Analogy :
Let us consider two taps having different inflow. The faster inflow fills the bucket in less time than that of slower inflow.So, the less inflow causes more delay and more inflow results less delay. Hence, delay is a function of inflow. Here, inflow of water translates to inflow of current(input transition). So, faster current sourcing (faster rise) will have less delay and vice-versa.

Although inflow of taps are same, when the size of buckets vary (i.e., 5 and 25 gallons) then the larger bucket takes more time to fill than smaller bucket. So, Delay is a function of bucket size (which is analogous to load capacitance).

So, *Delay of a cell is a fuction of input transition*(inflow) *and output load*(bucket size).

Let us assume two gates in a design are far from each other (say long net length from gate1 to gate2). This long net causes more capacitance.Thus, the delay of gate1 will increase due to load capacitance. The output load can be high not only due to long nets but also due to large number of loads connected(high fanout). The capacitance of all these load pins are summed and causes high output capacitance at the gate resulting more delay.

### Timing Arcs
It contains the delay information of every input pin to every output pin that it can control. 

In a combinational circuit, 
- In a 2x1 multiplexer, the output may change due to change in sel though no change in i0 or i1. Similarly, the change in i0 or i1 causes change in output. So, the timing arcs are from i0-->y, i1-->y or  sel -->y. The timing arc contain delay information in these arcs.
- In an AND gate, the output may change due to change in A or B.So, the timing arcs are from A-->y or B-->y.
  
In a sequential circuit,
- The D flipflop have the timing arc clock to q (as the output changes after occurence of clock edge) and clock to D (for setup and hold).
- The D latch has delay from clock to q, clock to D, D to q(This is because the latch works on levels, onelevel makes flop transparent and other makes it opaque. Though clock is constant, change in D causes change in Q for a latch).
The following table shows the occurence of flop/Latch and the timing arc taken occurence of flop/latch i.e., positive edge/level or negative edge/level. Setup/Hold is around the sampling point of clock.
![info](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e97903c2-bc1b-4af2-abb7-90a0c13d2a4b)

- The D to Q delay is not required in  flipflop as the change in D is not captured until clock is arrived. In a latch, D-to-Q delay must be known as the change in data for a level changes output (the transparent level).
- The clock-to-Q delay occurs with respect to the edge that is being considered in both latch and flop. Because data capturing is done at this instant.
- The Setup time requires data to arrive before its active clock edge. For a flipflop, it is with respect to triggering edge. For a latch, it is with repect to next edge(the transparent level changes to opaque level, so the last data change occurs at this instant for this cycle).
-  The Hold time requires data to arrive after this clock edge. For a flipflop, it is with respect to triggering edge. For a latch, it is with repect to next edge(the transparent level changes to opaque level, so the last data change occurs at this instant for this cycle).
</details>
<details>
<summary> Constraints </summary>
<br>
	
### Timing Paths
A Critical Path is the path that gives the maximum delay in a circuit. It determines the speed of the operation of the circuit. By reducing the cell delay in a critical path, the frequency of operation of the circuit can be done. This reduction in cell delay is nothing but making the tool pick faster cells. This can be done by defining constraints. This can be illustrated with the following example of timing path:

A Timing Path can be defined by the Start point and the endpoint. The Startpoint and Endpoint of a timing path are the points, within the delays are being calculated.
A Startpoint can be an input port or clock pin of a register. An Endpoint can be  an output port or D pin of D flipflop/Latch.
The timing paths can start at one of these startpoints and end at one of these endpoints.
- clock to D (reg2reg timing paths) : constrained by clock
- (IO timing paths)
   - clock to output (reg2out timing paths) : constrained by output external delay and clock period
   - input to D (in2reg timing paths) : constrained by input external delay and clock period
- input to output (IO paths are not present ideally)
This constraining of input and output delays is known as IO delay modelling. IO delay modelling is done mostly based on standard interface specifications.
 The IO Budgeting is done based on the interactions with other modules (how much external and internal delays to be specified). The IO paths need to be constrained for both setup and hold constraints.

The clock period decides the permissible delay of combinational logic but not combinational delay deciding the clock period. 
For example, Consider the frequency of design to be 500MHz(So, delay will be 2ns). If the setup is specified as 0.5ns and clk-to-q as 0.5ns. Then the combinational delay must be limited to 1ns.

The clock definition limits the delay in all the reg-to-reg timing paths.
Once the clock period is defined, the tool picks cells from .lib (which contains the registers and information of clk-to-q delay, setup time). 
So, It picks the cells for combinational delay in such a way that the limited condition on period is satisfied.
#### Input and Output external delay
The input ports are also an output of another external register, which may be clocked by same or different clock as register. The output ports may be D input of another external register. 
These external registers also must satisfy the timing conditions. As there is a boundary around the design, these external registers may be assumed as ports. Inorder to meet this timing, the input logic and output logic must be optimized such that no timing violations occur.
![fig](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e75b4aa4-1e46-4f44-913b-c7a5484620fa)

The input external delay and output external delay are the two constraints, that limit the combinational design delay. 
The external delays are usually defined inorder to constrain the combinational logic before the external world from using the clock period. They are usually constrained by 30-70 rule i.e., internal delay constrained to 30% of clock period (combinational and setup)and external delay constrained to 70% of clock period.
#### Input transition and output capacitance
As the external delays are specified, the clock period gets budgeted as external delay, combinational logic delay and setup time.
This budgeting is when signal are ideal i.e., with zero transition at input and no load at output. We know that cell delay is a function of input transition and output capacitance. 
So, when there is either transition time of signal at input or load capacitance at the output port, the delays increase and the combinational delay infringes into setup time budget. This causes a violation. 
So, The input transition and output load needs to be constrained such that tool optimize the combiational delay more specifically.
</details>
<details>
<summary> Timing .lib </summary>
<br>
	
The .lib contains the information such as units of R,L,C, power, current, output capacitance, max transition, delay model used etc ...
![lib (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5552eb55-3e45-4193-85eb-c551b3bcca0f)

#### Output Capacitance	
The output capacitance needs to be constrained. If the fanout of a cell is high, the input capacitance of each cell(load) and net capacitance of net connecting the consecutive cells (if net is long, capacitance will be more) and output pin capacitance of the cell sum up to the output capacitance of that cell.
As capacitance is high, the charging time is slow, so more input transition which may jeopardize the circuit. The worst can be logic '0' being seen instead of logic '1', which is undesired. Inorder to avoid this, the tool needs to be constrained on output capacitance.
When the output capacitance is higher than constrained, the tool breaks the net and buffers the net so that the fanout gets divided among buffers, not the cell and the cell drives the buffers.
#### Lookup Table
The lookup table is a table that contains cell delay values as a function of input transition and output capacitance. the input transition values are take as row and load capacitance values are taken as columns. 
![lib5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b69c46a4-c82b-486f-ab3c-cef2bb6efa08)

The cell having a certain input transition time and output capacitance are mapped to a delay value.
If these transition and capacitance values are not present in the table, the range/interval (between which two values the cap and tran exist) of values are considered and interpolated to obtain a new delay value corresponding to that input transition and output capacitance.   
The power consumed by the cell is also specified interms of lookup table (LUT).
#### Different flavors of cells
The cells are available in different flavors. For example, an AND gate is available with different area(wider and narrower transistors).
![lib2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9bf19f17-f912-4bc8-9cb1-2aa1ed19b3bc)

The .lib also gives information regarding the power pins such as n-well connection, p-well connection etc.. 
The .lib also gives the input pin capacitance and the max transition allowed for each pin, whether pin is clocked or not and for output pin, it specifies the direction, logic function etc..
![lib3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7a08a8f5-b02b-4b4c-9e15-1e49c84229e8)

The following image shows whether a specified pin is clock pin or not. The right side image is the clock pin of flop and left side shows signal pin of combinational gate.
![lib4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/67b3ecc3-1fa3-4149-a63c-b8828169bc1e)

All of these are known as attributes which can be obtained in the dc_shell by using commands with attributes.
#### Timing Unateness
Unateness helps the tool in understanding how to propagate the transition.
Positive unateness: For a rise in input, the output may rise or no change but it never falls. AND gate, OR gate follows positive unateness.
![lib6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6f8ca62e-ea7a-4e58-84ce-adb483d7b347)

Negative unateness: For a rise in input, the output may fall or no change but it never rises. NOT gate, NAND gate, NOR gate follows negative unateness.
![lib7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/78b60bff-f928-4eb2-b52f-1ae0e8bad927)

Non-Unateness: For a rise in input, the output may rise or fall. It depends on other input. EX-OR gate, EX-NOR gate follows Non-Unateness.In combinational design, the unateness is defined as both positive and negative as shown below:
![lib8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0414e39c-60ed-44fa-b879-81ea0898ff2d)

Let us consider the unateness of a sequential design.The sequential design clearly defines unateness and non-unateness. The CLK_N represents active low pin of clock.
The following image shows the clock attribute of clock pin is true and signal pin(D) is false for a D flip-flop.
![lib1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/631a3876-1afd-43c0-adcd-1e0e5aeead60)

The following image shows the direction of Q pin and the type of flop. So, it is a negative triggered flop.
![lib1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8e449d9d-056d-4325-9d40-d23f129d5d72)

This can clearly demonstrated in the below picture showing falling edge triggered and follows non-unateness.
![lib1_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ef69c986-4f4e-4d94-8214-ee0c94b2e508)

The below image shows the comparison of combinational gate and sequential flop defining unateness.
![lib1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e0695a4f-a6de-4212-8470-8ce896486233)

The following image shows the rising and falling edge triggered flop look up tables (timing information of rise and fall delays) as follows:
![lib1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9b4a4169-f139-4ffd-8bb4-23dc35392655)

The following image shows the setup and hold considerations with respect to edge as follows:
![lib1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/08352038-2e74-49f4-b94f-b028f5407104)

Now the attributes of these cells can be called using dc_shell. The following image shows the list of libraries linked to design (using **list_lib** command) and the various flavor of and cells present in design( using foreach loop).
![lib2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/af3440fc-765b-46e2-bec3-dd73c4181cce)

The following image shows the attributes such as function (that gives the function of design),  pin direction and usage of dc specific commands such as get_lib_attribute, get_lib_pins.
![lib2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4772425e-b773-4c8f-957f-9e8899bdb079)

The below image shows usage of attributes such as clock, area, capacitance.
![lib2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4dce63b3-1420-47b9-9e16-f7812517a233)

There are various attributes og library cells. These attributes can be viewed using command:
```bash
dc_shell> list_Attributes -app
```
![listatte](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/486dea21-9854-4ade-bb18-11acc33b5683)

The following image shows the output of the tcl script. 
![lib2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/62a8fdf0-b5e6-4e28-b40f-8c1fe16a07d1)

The script is as follows:
```tcl
set my_list [list sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and3b_2 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and3b_4 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4_1 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4_2 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4_4 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4b_1 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4b_2 \
sky130_fd_sc_hd_tt_025c_1v80/sky130_fd_sc_hd_and4b_4 ] 

#for each cell, find output name and its functionality

foreach my_cell $my_list {
foreach_in_collection my_lib_pin [get_lib_pins ${my_cell}/* ] {
set my_lib_pin_name [get_object_name $my_lib_pin];
set a [get_lib_attribute $my_lib_pin_name direction];
if {a ==2} {
set fn [get_lib_attribute $my_lib_pin_name function];
echo "$my_lib_pin_name $a $fn";
}
}
}
```
</details>

## Day8 : Advanced SDC Constraints

<details>
<summary> clock</summary>
<br>
	
Every timing path needs to be constrained by clock. Constraining the clock means defining the period, its waveform etc ... 
The clock period limits the combinational delay as the other values in max/min delay constraint equations are specified in .lib.
The clock is considered to be ideal until CTS (Clock Tree Synthesis) stage in ASIC flow.The clock is usually generated using an oscillator or PLL or any external clock source.
### Clock Modelling
So, the clock needs to modelled for Synthesis stage such that no violations occur. The factors to be modelled are:
- Period :The frequency at which it needs to operate.
- Source Latency : Time taken by the clock source to generate clock.
- Clock Network Latency : Time taken by the clock distribution network.
- Clock Skew : Clock path delay mismatches which causes difference in the arrival of the clock.
- Jitter : Stochastic variations in the arrival of clock edge.
The clock network is practical post CST stage. So, the modelled network latency and skew must be removed as the actual clock network is present now. This removes the extra pessimism defined.
#### Skew
In ideal case, the clock is assumed to arrive at launch and capture flops at the same time. In the practical design, the clock is at fixed position and the flipflops are placed such that place is optimized. 
But there will be a delay (∆) to reach the distant (capture) flop than the nearer (launch) flop when routed.If the nets are long, there will be buffers placed causing delay, so clock may take more time to reach. So, this would cause a violation reducing the arrival time.

*Skew is the difference in clock arrival time across the chip*.
Let us consider a clock arriving to two flops launch with two clock buffers and capture with one buffer. This would reduce available window by one buffer delay period.So, the timing may be clean post synthesis, but it fails after CTS.
 - Local Skew : The difference in clock arrival between two consecutive/related pins of flops.
 -  Global Skew : The difference in clock arrival between the longest path and shortest path.
 - Positive skew: if the capture clock comes late than the launch clock.
 - Negative skew: if the capture clock comes early than the launch clock.
 - Useful skew: if the clock is skewed intentionally to resolve setup violation
Skew can be either positive or negative. A positive skew helps setup by increasing violation but improves hold constraint. A negative skew makes the arrival time more stringent helps setup and might violate hold.
    - Thold +Tskew < Tckq + Tcomb

CTS will balance the clocks, but the skew still cannot be reduced to zero.
![skew](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7cd6bd01-d0ff-4c06-8494-8478672477e8)


#### Jitter
The clock sources have inherent variations in the period due to stochastic effects. This is known as jitter
The edges do not occur with zero transition. So, there will be a window in which these edges arrive. The arrival of edge varies from cycle to cycle.
![clock](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fa13fdfc-a401-438a-bc95-5d7c9e5a4212)

*Jitter is the fluctuation in the timing of clock edges*.Jitter is due to the clock generator.
Let us consider a clock of 100MHz (of period 10ns) having a jitter of 100ps.If the launch flop is assumed to start second cycle at 10ns, the capture flop might have second cycle at 9.9ns. This causes the reduce in clock available clock window to 9.9ns which would cause a violation. 

There are two types of Jitter:
 - Duty cycle Jitter - This causes a variation in ON period thus changing the duty cycle ( as duty cycle = Ton/Tperiod)
 - Period Jitter - This occurs within a clock cycle, The consecutive cycles occuring before or after the specified period.

The clock skew and clock jitter are collectively known as clock uncertainty. During synthesis, the clock uncertainty contains both skew and jitter but post CTS stage, it contains only jitter.
</details>
<details>
<summary> SDC constraints</summary>
<br>
	
All the constraints must be written as commands in the SDC (follows tcl format)for the tool to understand.
Ports are nothing but primary IOs in the design. A net is a connection of two or more pins or a pin and a port. The following design shows ports and nets in the design. Let us consider this design to understand the constraints.
![ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/55a085aa-376b-4517-9b23-b54aa04de08a)

 All the names (such as ports, pins, nets) are case sensitive.
 ### get_* 
 querying commands to get the specific details of design
#### get_ports
This command is used to query the ports in the design. So, the get_ports can be used:
```bash
 get_ports *    #to obtain all ports in design
get_ports clk  #to obtain port named clk
get_ports *clk* #to obtain all ports containing string 'clk' in their name
get_ports * -filter "direction == in" #to obtain all input ports in design
get_ports * -filter "direction == out" #to obtain all output ports in design
```
#### get_clocks
This command is used to query the clocks in the design. So, the get_clocks can be used:
```bash
 get_clocks *    #to obtain all clocks in design
get_clocks clk   #to obtain clock named clk
get_ports *clk*  #to obtain all clocks containing string 'clk' in their name
get_clocks * -filter "period > 10"  #to obtain all clocks in design with period more than 10
get_attribute [get_clocks my_clk] period"  #to obtain attribute period of the clock my_clk
get_attribute [get_clocks my_clk] is_generated  #to determine whether clock is master ot generated
report_clocks my_clk  #gives detailed information about clocks
```
#### get_cells
This command is used to query the cells in the design. There are types of cells in a design such as hierarchical cells, physical cells.
- Physical cells (standard cells) are predefined building blocks that contain the logic gates and other components necessary to implement various digital functions.
Physical cells are used to create the layout of the digital logic in the chip.
```bash
get_cells * -hier #lists all the cells in the design (both physical and hierarchical cells)
```
- Hierarchical cells are a methodology used in VLSI design to manage the complexity of large circuits.
![cell](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7f38f6e4-4d35-4a28-aed2-1099228ed733)

In the above design, the *is_hierarchical* attribute can be used as follows. The is_hierarchical attribute is a boolean function that gives either true or false.
```bash
dc_shell> get_attribute [get_cells u_combo_logic] is_hierarchical
true
dc_shell> get_attribute [get_cells u_combo_logic/U1] is_hierarchical
false
```
Similarly y pin is physical pin and out_1 is hierarchical pin.
### Clock Distribution
 The command to create clock is *create_clock*.
```bash
dc_shell> create_clock -name <clock_name> -per <PERIOD> [clock_definition point]
```
The clock definition point would be output of generator (can be a cell or a port or a pin).
Clocks must be created only on valid generation points i.e., clock generators (PLL, oscillators) or primary IO pins(external clocks).
Clocks should not be generated on hierarchical pins which are not clock generators.
 #### Clock uncertainty and clock latency
 Clock latency : The total time it takes from the clock source to an end point. There are two types of latency as follows:
- Source latency: Source latency is also called insertion delay. The delay from the clock source/origin to the clock definition points.
- Network latency: The delay from the clock definition points (create_clock) to the flip-flop clock pins.
   ![latency](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b4383dc6-badb-427f-8cc6-de685b4ba6bf)
  
  Network latency gets ignored once the clock tree is built as it is the estimate delay of the clock tree prior to synthesis.
The clock uncertainty is the skew,jitter and other pessimism of a clock. Inter-clock uncertainties for clock domain boundaries will also take into account the skew between the clocks for setup and hold checks
The uncertainty and latency are also defined as follows:
```bash
create_clock -name MY_CLK -period 10 [get_ports clk]
set_clock_latency 3 MY_CLK  #This is the latency, modelling clock delay in network
set_clock_uncertainty 0.5 MY_CLK #This is for setting clock network (jitter & skew)
```
#### Waveform
The clock defintion command defines 50% duty cycle and for a period of 10ns, the rise edge wil be a 0,10 and fall edge will be at 5ns by default.
The waveform is usually defined as 
```bash
 -wave { <starting rise edge> <first fall edge>}
```
The ON period is usually defined with -wave and the period is adjusted such that remaining cycle is OFF period. This can be illustrated with following definitons and waveform
![waveform](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/37a5aa4f-351d-475e-9840-0e6d2bd3c5aa)
#### Half-Cycle Paths
 The Half Cycle paths occur when two flops are triggered by different clock edge (such as lauch by positive and capture by negative and vice-versa). This would make setup more stringent as the available period would be from rise edge to fall edge i.e., ON period.It relaxes the hold by half path with huge slack.
![hcp](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/750393ce-4754-4eb9-989b-a36f1d4e2f0e)

#### Multi-Cycle paths
A multiple cycle path occurs when the data takes more than one clock cycle to reach the capture flop. So, These paths are set as multi-cycle paths inorder to avoid violation. This is done by:
```bash
set_multicycle_path 3 –setup –from [get_pins UFF0/Q] –to [get_pins UFF1/D]
set_multicycle_path 2 -hold -from [get_pins UFF0/Q] -to [get_pins UFF1/D]
```
Here, both setup and hold are constrained because hold check always happens at n-1 position of setup by default. So, inorder to avoid this, the hold moves back the check to 0th cycle (by 2 cycles back).This can be illustrated as follows:
![mcp](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1c601e2e-f7eb-479e-a0c9-259f3cada0e0)

#### False Paths
A false path is a path whose functional operation need not be constrained in design. These paths are set as false paths as follows:
```bash
set_false_path -from [get_clocks clockA] -to [get_clocks clockB]
```
#### Asynchronous timing Checks
The asynchronous checks can be either recovery or removal checks.

**Removal Checks**

Removal check ensures there is adequate time between an active edge of clock and release of the asynchronous signals such as set, reset. This is done in order to ensure the clock edge has no effect and does not cause any change in the values It is a min path check like hold check. All asynchronous timing checks are assigned to default path groups and the endpoint signifies it is removal timing check

**Recovery Checks**
Recovery check ensures that there is minimum amount of time between asynchronous signal becoming inactive and arrival of next active edge of clockIt ensures the design has enough time to recover and respond back to the clocks that once the asynchronous signal inactivates.It is a max path check like the setup check. The Endpoint in the report indicates the check is a recovery check against the clock

![removerecover](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aea8e8c3-c69b-427c-89ca-4fe351f28fc5)

### Constraining IO paths
The input ports and output ports are constrained with respectto MY_CLK genrated on port clk. These constraint require a window of the period during which it can vary. This is done using *-min* and *-max* switches
#### Input ports
The input ports are constrained with clock period, input transition and input delay.
The following commands are used to constraint the input ports of a design:
```bash
set_input_delay -max 3 -clock[get_clocks MY_CLK] [get_ports IN_*]
set_input_delay -min 0.5 -clock[get_clocks MY_CLK] [get_ports IN_*]
set_input_transition -max 1.5 [get_ports IN_*]
set_input_transition -min 0.75 [get_ports IN_*]
```
-rise and –fall options to specify slew for rising and falling edges
-min and –max options to specify constraints in various operating conditions
#### Output ports
The output ports are constrained with clock period,output delay and output load.
The following commands are used to constraint the output ports of a design:
```bash
set_output_delay -max 3 -clock[get_clocks MY_CLK] [get_ports OUT_Y]
set_output_delay -min 0.5 -clock[get_clocks MY_CLK] [get_ports OUT_Y]
set_output_load -max 80 [get_ports OUT_Y]
set_output_load -min 20 [get_ports OUT_Y]
```
</details>
<details>
<summary> Lab on SDC commands</summary>
<br>
	
Let us synthesize a design as follows:
The synthesize is linked with libraries as shown. So, by giving behavioral code as input, we link and compile and synthesize logic level netlist. The design infereed all the 3 registers as shown.
![step1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/691542ad-6798-4178-8aed-50c849ee04cf)

The expected behavior of the circuit is:
![expected](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6f797872-1d02-4efe-b91e-61691d1d6b51)
Let us look few query commands as follows:
The *get_ports* gives a collection of ports present in the design. Inorder to print all the names, we use *get_object_name* else it prints the pointer such as_sel3. The ports can be input or output,so, to know the direction of a port, the tcl script is as follows. The following *get_cells* command shows that all cells are physical cells and there are no hierarchical cells present in the design.The REGC_reg is the instance name in the design. Reference name is the name of the3 physical cell in .lib.Here, the ref_name dfrtp signifies d flipflop with asynchronouus reset positive edge triggered true output(Q).
![steps2 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/351e0cca-8c48-4163-b1f4-f28f16244817)
After writing the netlist, let us look at ddc file using design_vision.The ddc file contains all the information in the cell. The ddc file is given to tool using *read_ddc* command.
![steps3 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e2433af8-cd90-4b11-92b2-6b14fd5cd9e5)
The schematic would look as follows. The reset is an active low pin so an inverter is connected before it.
![steps4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2092f16e-6192-4ebd-99eb-fd6fb521ef29)
The following circuit is the optimized implementation of the expected circuit.
![change](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/55d4aea4-6baa-482f-bfe7-ae08a3ba19cc)
The following image shows all nets present in design usign *get_nets* command. All the pins connected to a particular net are obtained by *all_connected* command.
![steps6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b616abfe-98fc-403b-aa02-458450ce78c4)
In a digital design, a net can only have one driver. Multi-driven nets corrupts the logic level of design.In a latch, where gates are connected badk forth, it is multi-driven within a standard cell, so sizing of transistor would be taken care of. 
But, when using different standard cells, multi-driven nets would corrupt logic level in the design. The above script also shows that there is only driver on net  n8
and no of nets being driven can be many.

#### get_pins 
The following image shows that get_pins gives a collection of all pins in design.So, the various attributes such as direction, whether pin is clock or not can be illustrated.
![2steps1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dc4bdd74-7650-4102-822f-c3d5904b20ec)
The following image shows that output ports do not have an attribute clock so we first print all pins with direction. The *regexp* command is used to compare two strings. It is same as strcmp in C. It returns boolean value whether same or not.So, The script for printing only clock pin is as follows:
![3+4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e41aac42-e641-4c62-b666-c61a4734b865)
#### get_clocks
The following image shows defining a clock on a port, attributes such as period, is_generated, clocks(attribute used to find the clock being propagated on port) and information returned by report_clocks.
The report_clocks shows that whther it is master/generated, period,waveform. The *current_design* gives you the name of the design being worked on.
![5+6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/76829269-3e5c-4ed7-8a6f-e98e7256f098)

The clock should be properly defined on a port, not on any input pins (where clock should not propagate). Let us consider a clock at REGC_reg as follows. The input pin on REGC is NAND gate. So, clock defined on Y pin of NAND gate as shown. 
A clock gets created but the clock cannot propagate as it is on input pin. This corrupts the entire design. The *remove_clock* can be used to remove unnecessary clocks in the design.
![2steps7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6678b0c6-bb4b-408b-a7b9-f24bc74a1fbb)

The following image shows the different waveforms defined for a clock. The clock creation switches need not follow any order. This is illustrated in right side of image.
![8+9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/281ea60a-a612-419f-9a6c-eee3508615e6)

#### clock modelling
The following image shows defining clock latency and uncertainty. FOr clock latency, when *source* switch is used, it defines source latency, else defines network latency default.
The clock uncertainty is specified with *-setup* (max) and *-hold*(min) switches.
*report_timing* command is used to check every cell delay, transition and fanout etc.. The report_timing by default gives setup constraint of violation.
Slack is the difference between required time and arrival time of a timing path. Arrival time is the sum of clk-to-q delay and combinational delay. Required time is the clock period minus setup time and uncertainty (if any).
Let us consider the reg2reg timing path that ends at REGC_reg. As the clock is not defined in the design, it is showing as unconstrained. 
![4steps4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7c9d72c0-3348-4f52-b6c0-923fadd07672)

When a clock is defined, the timing path is showing that timng is met with a positive slack of 9.55ns which is very huge.
![4steps3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/62b27169-7a85-4404-b43e-fe3ef9871c2a)

Let us define the clock constraints such as uncertainty and latency as follows:
![4steps1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cacc6f10-40f2-4896-bf79-da4a9e1262cf)

The following timing report shows that slack was reduced to 9.05ns, due to addtion of uncertainty and latency.
![4steps5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d5422c62-261a-49a3-ae46-324d30e4022a)

The corresponding timing report shows the hold report (minimum constraint) for the same reg2reg timing path. Here, the uncertainty is added for a hold path.
![4steps6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6e6043e2-ef22-4571-b39a-1529548f892a)

The *report_port* gives the information about all the constraints on the port.The following image shows all the consraints on the port. Nothing is constrained so it is viewed as follows:
![report_port](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a6a1acec-72bb-49a8-b0a4-0170d6b30ecd)

The following image shows that in2reg and reg2out paths are unconstrained as IO constraints are not defined yet.
![uncon io path](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9a577ff5-9ec1-4bb2-b101-66f5cb3de9ae)

#### IO constraints

The following image shows that the input delay is constrained to 5ns so the timing report is as follows:
![123](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fed2afce-c712-4f97-9763-6b3f661f0d7a)

The following image shows that hold timing path is unconstrained as input delay -min is not specified. So, after constraining min delay the timing report is as follows:
![56](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ebd2f25a-0e75-4465-861e-f12b11bbea51)

The following image shows the timing report after defining input transition. The cells delay got increased after defining transitio so arrival time increased and thus reduced slack.
![89](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8826ef41-d86e-4d31-8104-b6706c02786d)

Now Let us define the output constraints, after defining output delay, the timing report is as follows:
![1112](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a20354f0-da7c-4d49-8d1c-feadcdf4b53e)

After defining the load or capacitance, the timing report is as follows:
![1314](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/791e129b-b61e-432a-8f3e-2a74064745c4)

Now, after defining the min load capacitance the hold report is as follows:
![5steps15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f6e5ad43-ec9b-4250-a183-d6561742ef8d)

### Generated clock
The clock for external world and input module can't be physically same due to long routing length. These long nets include buffers thus increasing the clock network delay. So, To avoid this, the generated clock is defined at another point so logically and physcially clocks would be same.
Creation of a new master clock instead of generated clocks has below disadvantages:
• More clock domains to deal with
• Requires additional constraints to be specified
• Source latency specifications need to be defined all over again for the new master clocks
The generated clocks are always defined with respect to master. Master clock is the main clock source or Primary IO pins. The command is as follows:
```bash
create_generated_clock -name MYGEN_CLK -master [get_clocks MY_CLK] -source [get_ports clk] -div 1 [get_ports out_clk]
```
The command shows that the generated clock MYGEN_CLK is derived from master clock MY_CLK defined at clk port with a divide factor of 1. The generated clock is defined at output port out_clk.
All implementation tools propagate the clock downstream based on timing arcs. All timing arcs from definition point will see clock propagation by default.
The creation of gnerated clock can be illustrated as follows:
![lab3_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3adfdcd3-66fe-485d-83cf-1c56c49cbc58)

Let us model the out2 reg path with generated clock as follows:
![lab3_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3cfbac30-374f-4152-94bf-026e297a7804)

 Now let us modify our design by adding another output register as follows:
 ![lab3_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fe1a7ac8-9c7a-44cd-9c25-86607ca22c6b)
 
So, After resetting the design and linking it, there are 4 registers in design as follows:
![lab3_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/24da76e9-7dd4-428f-a8dd-2896f1a5988c)

Let us define all the constraints in a file and source it as follows:
![lab3_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/edc86c2b-ed40-4360-b965-641b85a221d5)

Now, the report_clocks reports all the clocks in design as follows:
![lab3_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d9d7d6ff-0c62-40a6-b01d-cb844320eec3)

</details>
<details>
<summary> IO delays</summary>
<br>

 The constraint on IO delays are input delay, output delay. Let us discuss them in detail. 
 #### set_input_delay
 The following command says that data comes to the input port IN_A 3ns after the arrival of clock edge. So, the 3ns of the total period (10ns) is constrained for input delay. So the available time for combinational delay reduces for setup constraint.
 ```bash
create_clock -name myclk -per 10 [get_ports clk]
set_input_delay -max 3 - clock myclk [get_ports IN_A]
set_input_delay -min 1 - clock myclk [get_ports IN_A]
```
If this input delay defined is negative, the combinational gets an additional time. This can be explained as, When the clock and data were routed, the clock got delayed, but data arrives on time.
Usually, positive delay implies data arrival after clock edge. Negative delay implies data arrival before clock edge.In other words, Negative delay means clock relatively getting pushed out with respect to data.
In the hold constraint, When input delay is positive, the data arrives after 1ns of clock period.This helps meetimg hold time as the data arrives after the hold window. 
When it is negative, the data arrives prior to the hold window, which causes failure. So, additional changes must be made to delay the data arrival.

For an input port, if multiple external registers are being connected (i.e., more timing paths exist to one endpoint with different startpoints), then the input delay can be constrained more than once using -add switch. 
If one of these paths is a negative edge triggered and capture is positive edge_triggered, this can be specified using -clock_fall switch.
This can be illustrated as follows:
```bash
set_input_delay -max 2 -clock MY_CLK [get_ports IN_A]
set_input_delay -max 3 -clock MY_CLK -clock_fall -add [get_ports IN_A]
```

**The positive delay tightens the path for maximum constraint and relaxes the path for minimum constraint.The negative delay relaxes the path for maximum constraint and tightens the path for minimum constraint.**
 #### set_output_delay
 The following command says that data needs 3ns to reach the external flop. So, the 3ns of the total period (10ns) is constrained for output delay. So the available time for combinational delay reduces.
 ```bash
create_clock -name myclk -per 10 [get_ports clk]
set_output_delay -max 3 - clock myclk [get_ports OUT_Y]
set_output_delay -min 1 - clock myclk [get_ports OUT_Y]
```
Similarly, The positive delay tightens the path for maximum constraint and relaxes the path for minimum constraint.The negative delay relaxes the path for maximum constraint and tightens the path for minimum constraint.The hold is independent of the clock period because launch and cature flops are checked at same instant.
Also, the add switch and clock switch is also same for output delay that can be given as follows:
```bash
set_output_delay -max 2 -clock MY_CLK [get_ports OUT_Y]
set_output_delay -max 3 -clock MY_CLK -clock_fall -add [get_ports OUT_Y]
```
The clock_fall switch is to specify that annotated delay is with respect to negative edge. The add switch is to append the constraint to pre-exisiting constraints but not to overwrite.

#### How to constraint IO path?
Inorder to constrain a pure combinational logic (without any flops), the command set_max_latency is used or a virtual clock can be defined. 
The command is defined as folows:
```bash
set_max_latency 1.0 -from [get_ports IN_C] -to [get_ports OUT_Z] 
```
This means the data from port IN_C to OUT_Z should arrive within 1ns.
**A virtual clock do not have latency and no definition point**.
A virtual clock is an imaginary clock for budgeting the time. The virtual clock can be defined as follows:
```bash
create_clock -name my_vclk -period 5
set_input_delay -max 1.5 -clock my_vclk [get_ports IN_C]
set_output_delay -max 2.5 -clock my_vclk [get_ports OUT_Z]
```
#### set_driving_cell
The set_driving_cell command is used for module level IOs (such as where same technology can be used). 
The set_input_transition command can be used for top level primary IOs where two different chips may be connected and the transition is specified by the interface. Both these commands ca nbe used alternatively. The set_driving cell command is more accurate and recommended for all internal timing paths.

The driving cell is defined so that the input transition can be modelled depending upon the load/fanout on the input port/pin. The driving cell command can be illustrated as follows:
 set_driving_cell -lib_cell <lib_cell_name> [ports]
```bash
set_driving_cell -lib_cell sky130_fd_sc_hd _buf_1 [all inputs]
```
### Lab
Now let us consider the same design with an in2out path added (lab14_circuit.v). The Behavioral code is as follows:

```verilog
module lab8_circuit (input rst, input clk , input IN_A , input IN_B , output OUT_Y , output out_clk , output reg out_div_clk , input IN_C , input IN_D , output OUT_Z );
reg REGA , REGB , REGC ; 

always @ (posedge clk , posedge rst)
begin
	if(rst)
	begin
		REGA <= 1'b0;
		REGB <= 1'b0;
		REGC <= 1'b0;
		out_div_clk <= 1'b0;
	end
	else
	begin
		REGA <= IN_A | IN_B;
		REGB <= IN_A ^ IN_B;
		REGC <= !(REGA & REGB);
		out_div_clk <= ~out_div_clk; 
	end
end

assign OUT_Y = ~REGC;

assign out_clk = clk;
assign OUT_Z = IN_C ^ IN_D ;

endmodule
```
The following image shows the expected behaviour of the design.
![expected des](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/847eac50-206c-441a-9343-6494b8c5e73a)

The below shows that there are 4 flipflops after modifying the design.So, all the constraints are sourced using lab8_cons.tcl file. When clocks are reported, all clocks in the design are inferred as follows:
![12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/627bc493-34ea-4e90-aaf8-fe2ac64310d5)

The left image shows that before compilation timing report infers SEQGEN cells and after compile the lib_cells are read as shown on right image.
![35](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f24b556a-f9fd-4f78-8932-92598b561858)

The left image shows that the path with pure combinational logic is unconstrained. The right image shows the usage of commands such as 
- all_inputs : returns all the inputs in design
- all_outputs : returns all the outputs in design
- all_registers : returns all the registers in design
- all_clocks : returns all clock in design
- all_fanout : returns all pins connected as load to given port/pin
- all registers -clock \<clock_name\> : returns the registers clocked with the given clock
  The image also shows there is no timing path between any input port to output port directly.
![78](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c0c680d9-badd-4501-a3ba-e40c7bfd60ff)

- all_fanin : returns all the driving cells to a port/pin
- all_fanin -flat -startpoints_only : returns only startpoints of a timing path connected as driver
- all_fanout -flat -endpoints only : returns only  endpoints of a timing path connected as load
The following image shows all cells that are fanout of reg A and their ref_name
![last10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/90ca8841-1bee-49f1-8c44-069d0c5c8588)

The following image shows that when max delay is constrained, it violates the path. When it is compiled again, the path is met as the tool optimizes the logic by choosing appropriate cells.
```bash
set_max_delay 0.1 -from [all_inputs] -to [get_ports OUT_Z]
```
![1112](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d3e6b2d6-4e54-46a8-a9db-910668eb5c90)

The following image shows the schematic view of the design after writing out ddc file.
![last13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9b06f74a-c37c-44c6-af84-bc9911036b20)


The following image shows the clock report before and after defining the virtual clock. A there is no clock before, the path is pure combinational hence it is unconstrained.
A virtual clock do not have a definition point as follows:
![1718](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4e3642f2-5068-4dd1-9b33-2c84e3a46e7d)

The following image shows that constraining the design has violated a path. The last image shows the timing was met after compiling the design after constraining it.
![202122](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4d5e9434-fac3-459e-ac0a-fe48799ad6bd)

The following image shows the constraints on all ports of design. Here, the pure combinational logic has a period of 10ns, input delay constrained to 5ns and output delay constrained to 4.9ns, limiting the period of EX-OR gate to 0.1ns or 100ps.
![last22](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cd0f1f88-378f-48f9-ab01-1c152373810f)
</details>

## Day9 : Optimization in Synhesis
<details>
<summary> Combinational and Sequential Optimizations</summary>
<br>

The optimization goals are usually cost function based optimizations.
The goals of synthesis are to meet timing, area and power (also called PPA). The over optimization of one goal may worsen another goal. For example, When faster cells are used for timing, they occupy more area and consume more power. The timing goals are IO delay,clock period and max delay.
### Combinational Logic Optimizations
The combinational logic can be optimized by squeezing the logic design such that area and power are saved. The Combinational logic can be done by
- Constant Propagation
   - Direct Optimization
 In the constant propagation, when one input is made constant, the remaining circuit can be simplified. As discussed before, the (AB+C)' can be reduced to C'.
Thus optimizing the area and power.

- Boolean Logic Optimization
   - K-Map
   - Quine McKluskey
 Consider a nested ternary operator circuit that would ocntain 3 multiplexers. As discussed before, when it is optimized it can be reduced to an exnor gate.
![comb](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/141d7e56-63d4-4fc3-ab42-ab586aaf8af1)

#### Resource Sharing:
Consider a ternary operator y=sel?a*b:c*d. This multiplies two numbers when sel changes. A multiplier is a large circuit consuming more area. So, two multiplexers can be used such that y=(sel?a:c)*(sel?b:d). So, same sel can be used for both multiplexers and the same output is obtained with less area.
Thus area and power are optimized.
![comb2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e18629f7-623b-4ccc-b51a-6a34860f2da2)

#### Logic Sharing:
The logic can be shared when multiple gates can use the logic as intermediate one. For example, Consider a design having y=a&b&c, z=(a&b)|c.
This usually requires one 3 input AND gate(consumes more area &power), one 2-input AND gate and one 2-input OR gate. But, Both logic have an AND gate in common. 
So two 2-input AND gates and one OR gate will consume less power and area than the prior circuit.

#### Balanced Implementation and Preferential Implementation:
A Balanced implementation gives equal time to all the timing arcs (i.e., delay from input to output pin). A Preferential implementaion gives less delay time to late arriving signal and more time depending on their margins. 
Let us consider an example. Assuming no 5-input AND gate in the design. The design can be implemented in the following ways:
The left side image shows equal delay between a-->y and e-->y, whereas the right image shows more delay for a-->y and less delay for e-->y. If e is a very tight delay i.e.,late arriving signal (with huge external delay) that it cannot withstand 2 gate delay, the second one is preferred for its implementation to meet the timing.
![combi](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d9176cd2-25a4-488e-84d1-81994b57e982)

### Sequential Logic Optimizations
The Sequential Optimization can be done by
- Basic
   - Sequential Constant Propagation
   - Retiming
   - Unused Flop Removal
   - Clock Gating
- Advanced
   - State Optimization
   - Sequential logic Cloning

     An example for this can be a flop with asynchronous set and D pin connected to high (can be optimized as connected to Vss)or a flop with asynchronous reset and D pin connected to low(can be optimized as connected to Vdd)). But a flop with asynchronous set and D input connected to Vss or asynchronous reset and D input connected to Vdd, cannot be optimized, it retains in the circuit.
     Let us consider the following circuit which has a sequential propagation (flop) and logic. Now, these circuit gets reduced to an inverter as follows:
     ![seq](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e2591069-24af-47b2-8e60-8ae22ccf84d4)

#### Optimization of Unused Outputs:  
The unused outputs in a design need not be generated. As discussed before, let us consider a 4-bit up counter where q is assigned cnt\[0\]. As the remaining outputs(cnt\[1\] cnt\[2\] cnt\[3\]) are unused,the design can be reduced to a single flop that toggles when enabled. This is done with one flop and multiplexer with inverter, instead of 4 registers to count.
  But If we require the cnt\[1\] in future, The tool can make suboptimal changes while designing such that no violations occur.So,This can be done by tool using following boolean variables:
  - compile_seqmap_propagate_constants
     If this variable is not set to true, the sequential constant propagating circuits are retained in circuit and not optimized.
  - compile_delete_unloaded_sequential_cells
     If the variable is not set to true, it doesn't remove the counter cells as discussed, it retains all counters in the circuit.
  - compile_register_replication
     If the variable is set to true, this replicates the registers in cloning optimization so that timing is met.
#### Lab

**Combinational Optimization**:

 The following image shows the behavioral codes of different designs being synthesized as follows:
 ![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4f013901-2945-456c-bcc5-891fa92044ce)

The following image shows the steps of synthesis to synthesize opt_check.v The design shows there is a multiplexer(ternary operator) in the design.The unconstrained path uses lib cells after linking and compilation as follows:
![23](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2d98bfa0-b8bd-4ed4-b64b-6336cec7a6cb)

The following image the synthesized design of opt_check. Initially, it has a multiplexer in the design but after optimization, the design is reduced to and gate and an inverter.
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c056b68d-9720-4510-9a9b-8f6bdc527eea)

Similarly, the following image shows the ternary operator of opt_check2.v is reduced to an OR gate after synthesis as follows:
![lab1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f7e87238-c863-4658-8482-0a57acaf4c4e)

The opt_check3.v is reduced to a 3-input AND gate as follows:
![lab1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cd4b7055-2de8-4bca-add7-d0baddc71481)

The nested ternary operator which would have three multiplexers in opt_check4 is reduced to an EX_NOR gate as follows:
![lab1_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/efa3821f-d7a5-4c8a-bebc-41b2380ef164)

Let us consider the timing path of this circuit. When it is constrained to maximum delay of 60ps, the timing report is unconstrained. If a slower gate is used, after compilation, the tool picks a faster gate to meet the timing violation as follows:
![89](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/30e35a91-7a12-402c-a15a-3699eb2568e2)

**Sequential Optimization**:

The following image shows the behavioral code of the designs as follows:
![lab2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dc089b09-1bb5-4b9b-ac84-9a9e9d3246f6)

The following image shows that the design consists of one flipflop with asynchronous reset. This shows the steps of synthesis of dff_const1.v
![lab2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c501e414-2a65-4f4e-b21b-15288b6ad110)

The following image shows the design synthesized of dff_const1.v It shows a flipflop input connected to logic high through a tie cell and an asynchronous reset condition as defined in the code.
![lab2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/57247827-b5a0-47fd-a0f8-ac548b081f88)

#### Tie cell

We know that, the source terminal is connected to PMOS and gate terminal is connected to input pin in a CMOS design. The gate terminal of CMOS is very sensitive because of gate oxide.So, the gate terminal should not be allowed to see any surges thus the VDD (or logic high) is not directly connected to input pin.The **TIE cells** are used for driving 1'b1 or 1'b0.

The following image shows the synthesized circuit of dff_const2.v The circuit is fully optimized as the variable compile_seqmap_propagate_constants is set to true. 
![lab2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7df131f1-9667-4f21-8bfc-b57eb6487754)

If the boolean variable is set to false, the design is as follows:
![lab2_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/473fcc87-24f7-4c7a-9a01-f3fc768ad30c)

The following image shows the output of the dff_const3.v This design is retained as it exhibits a set-reset relation between flipflops.
![lab2_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bc3b7819-6bb1-498e-9161-6aeb382a6534)

The following image shows the output of dff_const4.v  The design is sub-optimized as the variable is set to false.
![lab2_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2526840f-69d6-4d04-97b9-0164d8466f87)

When it is optimized(variable set to true), the following output is obtained as follows: 
![lab2_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c0f81b29-9398-407f-ac60-b7c965ea691d)

The following image shows the output of dff_const5.v The two flipflops are retained as the design has set and reset behaviour.
![lab2_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/51abe4f1-31dd-418b-a4e2-03ebc02f5b29)
</details>
<details>
<summary> Special Optimizations</summary>
<br>

### Register Retiming
Regiater Retiming is also known as Pipelining.Pipelining is a technique that breaks combinational paths by inserting registers.
This can be explained through an example. Let us consider the following design with a huge combinational delay of 48ns and the setup of flops can be 1ns each. This is the critical path of the design, hence limiting the circuit to operate at a frequency of 20MHz. 
This can be avoided by adding more flops to the design. As these new reg2reg paths have huge positive slack upto 48ns. The combinational logic can be sliced and shared among this flipflops. Thus improving the performance of the design. 
![vid1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c5a1fb2b-336f-46dd-bd8d-81acffe27c66)

The tool do not share the logic equally, it optimizes the design to the extent. So, If it is shared as shown, the delay of the design now will be 20ns in the critical path. This, Improving the performance of the design to 50 MHz. 
If the design is optimized, the intermediate values cannot be defined. So, The optimization of tool is hard to calculate. SO, Any bug in subsequent design makes debugging more complex. The repercussion of not using it is sub-optimal design and using is complex behaviour at intermediate stages.
#### Lab
The following code is a 4-bit multiplier multiplying two 4-bit numbers and three 8-bit registers through which data is propagated to output.
![lab3_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9550579c-514a-4f9e-ad67-abdc3938bbea)

The following image shows that there are three 8-bit registerswith asynchronous reset.
![lab3_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/28e6c425-bd46-483a-85ae-80d7ccbd437e)

The following images show the synthesized design withGUI of multiplier(sub_module) and complete design.
![lab3_8_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/703818b3-6d72-4266-83cc-295b6b29e1c8)

![lab3_8_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cd3308de-e7f9-4915-abeb-24d3733fcc39)

The following image shows the timing path which violates worst delay in the design at input port.
![lab3_10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3958f6eb-5f3a-4996-8aee-b221ee44fbb7)

The following image is obtained after using the command as follows:
```bash
dc_shell> compile_ultra -retime
```
![lab3_11](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/804efb6c-bb46-4ea2-933f-1a4a048de809)

Now the violated slack has reduced and violation is at output delay.
![lab3_12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8da0471d-c99f-4c54-859d-ff4da31d67ba)


### Boundary Optimization
The Boundary Optimization can be explained through an example. Consider a top module having internal sub module, the combinational logic at output port of sub module and external logic can be optimized such that area or power consumation reduces.It dissolves the boundary of the submodule, merges the logic to obtain the opyimal logic and implements the design. So, The optimization os done without any regard to boundary such that design is remodelled. The optimization do not preserve the hierarchy so the intermediate signals in the netlist were removed by the tool in optization. So, Debugging becomes complex as some hierarchical modules and intermediate signals are absent.
The Boundary optimizations are done using the switch as follows:
- set_boundary_optimization <design> true|false
```bash
set_boundary_optimization u_im false
```
#### Lab
The folowing image shows the behavioral code of boundary_check.v.
![lab3_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/34f8271b-4873-4dc1-80f1-31f1672f8df3)

In the following code, im is the internal module which is a 3-bit counter. Upon reaching, 111 it gives cnt_roll as enable to 4-bit register.
The following image shows that the design consists of 3-bit counter and 4-bit register with asynchronous reset
![lab3_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5242d41b-97f3-4d46-995d-c1189bd49e0a)

The following image shows the design with hierarchical module u_im in the design. The Boundary Optimization is not done in this design
![lab3_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fe0722c0-7d4b-4951-9e70-53b8103d0318)

In the dc_shell, the boundary optimization is done so it cannot find any hierarchies but design vision can show the hierachical pins of sub_module as above.
![lab3_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1eaf7f31-df42-46ff-8f64-2441df12161e)

The Boundary optimized design is as follows:
![lab3_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d07ea9c1-cb1a-400b-9f16-d099e1297195)


During functional ECOs, If any bugs occur, it can be directly changed in netlist only if hierarchies are preserved, otherwise the synthesis run of complete design may take huge time.
There is no thumb rule to set the set_boundary_optimization to either true or false. It completely depends on the need of design.

### Multi-Cycle Paths
Let us consider the following design. Assume all the flops work at some clock frequency of 100MHz. The multiplier may have a delay of 15ns, and the total delay might account to 16ns. 
![vidi-1-2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7017a5c0-28da-490c-8255-72afe79fa869)

But the design implies the output requires two clock cycles to get data. The enable to select requires one clock cycle and select to output requires another clock cycle. 
Such timing paths are defined as multi-cycle paths so that tool do not over optimize the design. The over optimization may cause violations at other paths which is unnecessary.
#### How paths are timed MCP?
For a single cycle path, the setup check is done at the consecutive edge of the flop and hold is done at the same edge of the flop.
*Hold is always checked edge before setup.*
For a half cycle path, the setup check is done at the subsequent fall edge of the flop and hold is done at the previous falling edge of the flop. In a half cycle path, setup is very stringent and hold is relaxed.
Fir a multicycle path, the -setup switch specifies the number of cycles after the launch edge, it needs to check setup and the -hold switch specifies the number of cycles the launch edge moves to check with capture.

This definition of multi-cycle path is done as follows:
```tcl
set_multicycle_path -setup 2 -to prod_reg[*]/D -through [all_inputs]
set_multicycle_path -hold 1 -to prod_reg[*]/D -through [all_inputs]
```
The above commands for a clock period of 5ns check setup from 0ns to 10ns at capture and hold at 0ns for both the flops.
This can be done after careful understanding of design else single cycle paths shiuld not be defined that may corrupts the whole design.
#### Lab
The following image shows the behavioral code of mcp_check.v
![lab4_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/adb8e888-d622-4cb3-b762-8af12b49a616)

The following image shows that the design constains a 16-bit register for multiplier output and a flop for enable.
![lab4_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/feb5bf34-4599-46b7-a2b6-e26659bae51c)

The following image shows the constraints defined in a tcl file for mcp_check
![lab4_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ba8ba68f-09cb-4522-82cb-1baa77811b69)

The following image shows the initial violation before compilation and the violation after compilation
![37](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0339220d-9448-4891-b748-3b6793e10a5b)

Now, the multi-cycle path is set and the violated slack is reduced as follows:
![lab4_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/930b4b55-73cd-4360-b184-175358a05251)

The command should infer about the startpoint also because the single cycle paths should never get affected(relaxed) because of multi cycle paths.
The following image shows that all timing paths met the setup violation.
![89](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/24259146-e5d2-4a77-a550-42b7f078bab5)

But the hold is violated as it is not constrained as follows:
![lab4_11](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/33f3aea8-4bdc-43a1-a0e3-d28224a72aa2)

So, After defining hold, the timing is met as follows:
![1213](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aa3559e3-c6ab-4280-bd53-e30e40bb046a)

Here the flop is overloaded with 0.4 fF, so by adding buffers to isolate output ports, all the timing violations are met as follows:
![1415](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c35dcd33-83bb-41aa-90e2-368747bee2e7)


#### False Paths
False paths are the paths that are invalid for STA.If the launch and capture flops have no temporal correlation between edges, then the path can be regarded as false path.
Different clocks are not always asyncronous, the clocks generated from same master and master will have a relation which can't make it a false path. 
The path from a constant selection line of multiplexer to register cannot be a timing path, so considered as false path.
The false path can be specified as
```tcl
set_false_path –through <>
```

### Isolating Outputs
When there are more number of outputs to be connected after implementation of design, this may cause a violation of internal delays as cell delay is a function of load capacitance. Inorder to avoid internal failure, we isolate by inserting a buffer at output port. So, the buffer drives the external load.Now, the internal paths are decoupled from output paths..This is illustrated in the following design.
![load](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ebe027ad-18f9-46aa-83ca-1fc2a0bbd3c7)
The command to isolate ports is:
```tcl
set_isolate_ports -type buffer [get_ports OUT_Y]
```
#### Lab
Let us consider the behavioral code of check_boundary as before. The following image shows the synthesized design before dissolving the boundary.
The highlighted net shows that the output of registers goes to output ports and also input of registers through AOI cells.
![lab3_15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cb617976-b2b5-444f-87cb-953ae2b26dbf)

After dissolving the boundary, there is no isolation implemented. So, By using set_isolate_ports command the design is isolated from external load.
![lab3_15_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9e3bf41b-33bd-4fe1-9516-fdb7d603dd18)

After insertion of buffers, the design is as follows:
![lab3_15_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/54b7584e-4dac-4148-8f62-794246a8c005)
</details>

## Day10 : QOR
<details>
<summary>Summary</summary>
<br>
	
The following constraints are defined for a synthesis.tcl to constrain a design
- clock : Master clock, generated clock and virtual clock (if any)
  
    create_clock, create_generated_clock
- Practicalities of clock :Latency and  Uncertainty (Skew + jitter for pre-cts and jitter for post-cts)
  
   set_clock_uncertainty, set_clock_uncertainty
- Input delay and output delay
  
set_input_delay, set_output_delay
- Input transition/Driving cell
  
   set_input_transition, set_driving_cell
- Output load
  
   set_load
- max capacitance, max transition and area
  
   set_max_capacitance, set_max_transition, set_max_area

The DC flow for synthesizing netlist is
- read_verilog
- read_db
- check_design
- source constraints
- check_timing
- compile_ultra
- report_constraints -all_violators
- report_area
- report_timing
- write

The various synthesis knobs for optimization are
- Boundary Optimization
- Retiming
- Constant Propagation
- Unused flop removal
- Isolate ports

 When all these constraints are met with good margin, the QOR is good. The DC flow can be illustrated as follows:
 ![flow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/798ecb6a-62e6-49ec-acf5-d3e678cb8dd8)

</details>
<details>
<summary>report_timing</summary>
<br>	

 #### Propagation delay
No two timing arcs will have same propagation delay. This can be explained using CMOS structure as follows:
![nand](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/86f54055-7667-4ab1-9f3d-44d795d4e8f2)

In the above image, the pull-up or PMOS act as the current sourcing path and pull-down or NMOS is the current-sinking path. In the truth table, when both inputs are zero, both PMOS transistors drive the output thus faster rise in output.
When one of the input changes to 1, only one transistor sources the output and the rise of output varies. So, the timing arc varies from each input to output and for each rise or fall.
### report_timing
The report_timing is used to analyse the report of a timing path that gives information such as cell delays, transition, capacitance, the slack etc..
The report_timing command gives the setup delay of a timing path with two significant digits by default. The following are the different ways to use report_timing command as follows:
- report_timing -from DFF_A/clk
- report_timing -from DFF_A/clk -to DFF_C/D
- report_timing -fall_from DFF_A/clk
- report_timing -rise_from DFF_B/clk
- report_timing -delay_type min -to DFF_C/D
- report_timing -delay_type min -through INV/a
- report_timing -delay_type max -through AND/b
- report_timing -rise_from DFF_B/clk -delay_type max -nets -cap -trans -sig 4 

Let us consider the following timing paths of design. The following design have 3 flops and 2 timing paths i.e., from A to C and B to C. The different arc delays are given to gates and flops. So, the delay of different timing paths are calculated as follows:
![eg1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/be2901bc-cdc5-4980-892f-189b43b58945)

The timing path from DFF_B to DFF_C gives the minimum delay of 1ns and path from DFF_A to DFF_C gives the maximum delay of 1.65ns. So, when startpoint is not specified, the delay_type max reports A to C path and delay_type min specifies B to C path.
For the circuit to work at the specified cycle time, the clock signal’s rising edge should always arrive later (or at the same time) than your data signal, which means that your slack should be non-negative.
- check_design checks for design consistency. E.g.: Will report a feedthrough, as we take out_clk in some of our examples directly from the defined clock.
- check_timing checks for the specification of constraints, and also let us know if the provided constraints are enough. It might not specify proper end-points to be constrained, that we need to justify.
- report_constraints provides us with a glimpse as to how our design is feasible in terms of electrical parameters such as power and capacitance.
The time or the sum of the delays in the timing path shown is called the arrival time of a timing path. 
Let us assume a clock of 5ns in the circuit. Assuming there are no latency and uncertainty, the data at DFF_C needs to be stable by 4.5ns(Tclk-Tsu). This is known as the required time of the flop.
- The report_timing -rise_to DFF_C/D reports the A to C path of 1.5ns for max delay and B to C path of 1.15ns for min delay. 
- The Setup Slack is the required time minus arrival time. So, The timing path A to C for setup  has a positive slack of 4.5-1.65=2.85ns. The positive slack implies that timing is MET and no violation present.
- The Hold Slack is the arrival time minus required time. The data should change after 0.1ns. So, The timing path B to C for hold has a positive slack of 1.0-0.1ns=0.9ns. The hold condiiton is also MET.

The following image shows 4 timing paths in the design. The -max_paths switch is used to obtain n maxpaths in the design. The report_timing -max_paths 2 gives the 2 timing reports of slack -1vand -1.2ns.
- The max_paths gives the worst violated path per endpoint, not the worst violated paths in the design. 
- The nworst switch gives n worst violated paths per endpoint.
- These switches when used combined, the max_paths states number of paths to be reported and nworst states number of paths per endpoint can be picked.
![eg2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/07024cd3-8cfe-456a-8992-b94055706493)

Let us consider the design. The right side of image shows the behavioral code of the design. The left side of image shows the constraints to be defined for the design.
![lab1_1 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/96ee33b4-4945-47f4-b60b-4387b7abf738)

The following image shows the setps of synthesizing netlist from benavioral code. The image shows that the design consists of 4 flops with asynchronous reset.
![lab1_2 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9c888288-f8de-48e8-8c77-d11bf606d56e)

The following image shows the timing report of setup. 
![lab1_3 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4bada9b9-8c7e-4bfe-a887-3f9ad2b5e57d)

It infers that
- The delay type defined is max.
- The launch edge and capture edge occur at different instants.
- The library setup time is defined.
- The slack is obtained by required time minus arrival time.
  
The following image shows the timing report considering fall_from IN_A and right image shows rise_from IN_A. The r indicates rise and f indicates fall delay being considered. The U14 cell has a less delay for rise to fall arc(113ps) than the fall to rise arc (248ps) as the gate is an inverter (negative unateness). The library setup time is different for a rise transition and fall transition. The delay varies between rise_from and fall_from of a timing path. The slack also shows a variation of 200ps as below:
![lab1_5 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1e189c4e-3d16-407d-93f3-a9b944b04c01)

The following shows the hold (min) condition of a timing path. It defines library hold time. The launch edge and capture edge are calculated at same instant. The slack is arrival time minus required time.
![lab1_6 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/645a0ea4-235d-4d44-8390-0fa51ec7afa3)

The following image shows that the timing report through a cell for setup and hold gives different cell delay. The U14 cell has 25 ps (for setup at rise transition) and 60ps (for hold at fall transition). 
The cell delay may be high or low, but the overall arrival time is considered by the path to be reported as worst violating timing path.
![8+9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d46bc08a-945e-4065-b17b-193f7f3cae57)

</details>
<details>
<summary>Labs</summary>
<br>	

The following image shows the steps of synthesizing the netlist from the behavioral design. The check_design implies a feedthrough path in the design and inport clock and output clock are connected directly.
![lab2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/609a2a80-1eeb-4a97-8513-61ce512ca8ed)

The following image shows the check_timing and report_constraints output. The check_timing shows whether the design is properly constrained or not. The constraints shows MET and unconstrained endpoints are listed as the constraints are not defined yet. The report_constraints shows the default constraints loaded in the tool memory.
![lab2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7d6468e8-9065-4120-a234-b685a123a1f2)

After defining the constraints, the check_timing shows some of endpoints are defined. So, only the clock ports are not defined. This is illustrated as follows: 
![lab2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d9bae563-7903-4684-9de2-9219bba816a9)

The following report shows that the timing paths met the violation.
![lab2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7186bf72-843b-40ab-b674-8980b7948ec0)

The following image shows the report_constraints that there is no negative slack. So, the constraints are MET.
![lab2_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f3cdfa6f-a7bb-4a92-9b07-6fb90177112c)

Let us consider another design of 128 bit multiplexer.The code below is a 4:1 mux and above is 128:1 mux. The Behavioral code is as follows:
![lab2_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8f1fd23e-608e-48ac-9866-ba12e0c4ad6d)

Now, let us read the design and synthesize the netlist as follows. The design infers a latch but after the synthesis, there will only be gates.
![lab2_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a2f67bc4-e229-4bd1-a870-ec5ac1d4c43a)

The following image shows the generated list is a pure combinational logic design.
![lab2_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9d433d7e-9d5d-4f8a-b855-2ab0d6cb2b1c)

The following image shows there are no sequential cells in the design. The latch is inferred because always statement is used and y is assigned in for loop. The reoirt_timing shows it has so many fanouts such as 16, 17. The fanout can increase the capacitance as it shows the net with fanout of 17 has a capacitance of 40fF.
![lab2_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c940ffd7-db98-4376-b194-174cadf35afd)

The following image shows the check_timing report. The report shows y is unconstrained so the set_max_delay constraints all feedthrough paths so it gets constrained. Now, the timing gets violated.
![1112](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2fa1e9c1-abe4-4324-8ade-6b71a3f380c0)

Now, The capacitance needs to be constrained to a less value such as 0.025pF. So, The following nets are being violated for capacitance. This can be illustrated with report_constraints command.
![lab2_13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d1e33f4d-acf0-4bd2-8110-0feb7b615277)

Now, after compile_ultra, there is no unconstrained endpoint due to set_max_delay command.
![lab2_14](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/26415e07-c5f5-4680-bb06-8855883c35e4)

The report_constraint shows that all constraints MET as the set_max_capacitance is defined. The set_max_capacitance is used for breaking/buffering the high fanout net. If net is loaded bad, it can cause timing issues.
![lab2_15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/609deffb-b8d3-4977-b516-552c19edb62c)

Now, the capacitance is defined below 25fF for each cell as shown below after constraining it. The fanout is optimized and split such that transition and capacitance is optimized so the cell delays are reduced.
![1618](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e3b3bac1-35f1-4fcc-9989-5ca0aee19991)

As the number of inputs increase, the fanout of selectline increases. When fanout is high, the net will be heavily loaded and this is called High Fanout Net (HFN).
The fan-out is the number of gate inputs driven by the output of another single logic gate. Generally clock nets, reset, scan, enable nets are High Fanout Nets.
- A high fan-out corresponds to a very high capacitance load, which in turn translates to timing violation, because of a high transition time which adds up in the delay calculation.
Let us consider the following design. The enable pin is ANDed with input. Thus the load on enable pin is very high. The Behavioral code is as follows:
```verilog
module en_128 (input [127:0] x , output y , input en);
  assign y[127:0] = en ?x[127:0] :128'b0;
endmodule
```
The following image shows the steps to synthesize the netlist as follows:
![lab2_19](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/88bb9d0e-01e0-42f7-99b8-5ac34175b3d4)

Now, the report_timing shows the unconstrained path as follows. It has a fanout of 128 which results a high capacitance of 0.2pF
![lab2_20](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1003e7ee-a93e-4e0e-a6cb-58334259c604)

Let us constraint the capacitance to 30fF on current design. So, the capacitance is violated by huge amount as follows:
![lab2_21](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/220f3c3b-095b-47dd-8292-d422539b8a8d)

By compiling the design, the capacitance is now limited to 0.03 pF and fanout is reduced to 17 as follows:
![lab2_22](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7d212cf4-52da-481d-ac6b-a6f898c05f08)

The design in ddc can be viewed as follows:
![lab2_23](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2b3a1a5c-33e0-489d-9a44-7cce60561758)

![lab2_24](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/98134c88-ec40-48d1-87b9-3dd104eb4fd0)

The enable is not driving all the cells now. It is driving a set of selective cells through a buffer as follows:
![lab2_25](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cb688063-f77c-476b-a123-29db5e1de1b2)

![lab2_26](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/89063c25-8b3e-470a-a8ac-4c4993472bcf)

The following image shows that the transition is not optimized yet. So, The set_max_transition is used to constrain it.The transition is high if it is 0.36 so it can be constrained to 0.15. The report_constraint shows that transition is violated. The cost implies the constraint that needs to be optimized by the tool. As capacitance has no cost, it will not be optiized further, only transition wil be optimized.
![lab2_27](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a5da2b96-dfc5-437d-bc6a-eb7f9723bdf9)

The report_constraint shows all the pins violating the transition as follows:
![lab2_30](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/01eba79e-db94-4b2d-b5bd-3fcc41791e8d)

Now, after compiling the design, there are no violated constraints as follows. The leakage power is ignored as the constraint to define it is obsolete.
![lab2_28](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d91a7a74-55b0-4e25-81c8-b33de6aa35d9)
 
So, the check_timing shows only the unconstrained endpoints as follows:
![lab2_29](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d4399e74-c735-4991-a7f7-bbd4c0f085a3)

Now, the transition is limited to 150ps in the timing report.
![lab2_31](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c8b6645b-9cd0-484b-93f1-ff53765769c7)

The following image shows the same path before compilation and after compilation such that transition and cell delays are improved. The tool upsized the buffer so the transition reduced thus AND gate delay reduced. The slack improved from 442 ps to 254 ps as input transition is a function of cell delay.
![33](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4d4e5869-5f74-4af4-a9ae-04218f59fca6)

The max_capacitance and max_transition should be constrained because the tool takes the values from lib if not defined. This are usually very high making the design sub-optimum.
check_design ensures the quality of design is proper or not. check_timing ensures all constraints are implemented. report_constraints shows constraints violated if any.
</details>

## Day11 : Introduction to BabySoC
<details>
<summary> Introduction </summary>
<br>
	
## SoC
SoC is a single-die chip that has some different IP cores on it. These IPs could vary from  microprocessors to 5G broadband modems.
An SoC consists of hardware functional units, including microprocessors that run software code,  as well as a communications subsystem to connect, control, direct and interface between these functional modules.
It refers to an integrated circuit (IC) or semiconductor device that integrates all or most of the components and functionality of a complete electronic system onto a single chip. 
The SoC is basically a combination of:
- Microprocessor or Microcontroller: The central processing unit (CPU) or microcontroller is the brain of the system and performs computation and control tasks.
- Memory: SOC chips often include various types of memory, such as RAM and ROM
- Input/Output Interfaces: SOC devices provide interfaces for connecting to various external devices, such as sensors, displays,interfaces like USB, Ethernet, or Wi-Fi.
- Peripheral Interfaces: SOC chips may integrate various peripheral interfaces like GPIO (General-Purpose Input/Output), UART (Universal Asynchronous Receiver-Transmitter)...
- Power Management: SOC devices often incorporate power management units to efficiently regulate power consumption, including voltage regulators, sleep modes, and power gating.
- Clock Management: They may include clock generators and management units to control and synchronize the timing of various components within the chip.
  There are different types of SoCs such as mobile SoC, IoT SoCs, Automotive SoCs, Networking SoCs, Industrial SoCs, FPGA SoCs...
 #### Why SoC?
- Integration: SoCs integrate multiple components and functions of an entire electronic system onto a single chip. This integration simplifies the design, reduces component count, and saves space on printed circuit boards (PCBs). It leads to more compact and power-efficient devices.
- Power Efficiency: SoCs are designed to be highly power-efficient. By integrating components on a single chip, the distance that signals need to travel is minimized, reducing power consumption.
- Size Reduction: SoCs enable the design of smaller and more portable devices. This is especially important for applications like smartphones, wearables, and IoT sensors where size constraints are significant.
- Performance Optimization: SoCs can be optimized for specific workloads or applications. For example, specialized accelerators for artificial intelligence or digital signal processing can be integrated for enhanced performance.

## Mobile Processor
The Processor used in Samsung F23 Ultra is Qualcomm SM7225 Snapdragon 750G 5G (8 nm technology). 

 1. Manufacturing Process (Node):
The Qualcomm Snapdragon 750G 5G is manufactured using an 8nm process technology. This process node provides a good balance between power efficiency and performance.

2. CPU Cores:The CPU architecture of this processor includes a combination of eight Kryo cores. These consist of two high-performance cores and six power-efficient cores.
The high-performance cores are typically based on ARM Cortex-A77 or custom Qualcomm Kryo cores, while the power-efficient cores are based on Cortex-A55 or similar designs.

3. GPU (Graphics Processing Unit):
The processor features an Adreno GPU, which provides excellent graphics performance for gaming and multimedia tasks.The GPU in the Snapdragon 750G is designed to handle graphics-intensive applications and supports APIs like OpenGL ES, Vulkan, and DirectX.

4. 5G Connectivity:
One of the key features of this processor is its integrated 5G modem, which supports both sub-6 GHz and mmWave 5G bands.It offers faster download and upload speeds, low latency, and improved network connectivity compared to 4G LTE.

5. AI and Machine Learning:The Snapdragon 750G includes AI processing capabilities, thanks to its Hexagon DSP and AI Engine. These components enable on-device AI tasks such as image recognition, voice commands, and other machine learning applications.

6. ISP (Image Signal Processor): The Image Signal Processor in this processor enhances camera capabilities, supporting features like multi-camera setups, advanced image processing, and HDR photography.

7. Connectivity: In addition to 5G, the Snapdragon 750G offers a range of connectivity options, including Wi-Fi, Bluetooth, and NFC, making it suitable for various IoT and mobile devices.

8. Security: Security features such as secure boot and a trusted execution environment (TEE) are integrated to protect user data and enhance device security.

9. Cache Hierarchy: Like other Qualcomm processors, it features a hierarchical cache system with L1, L2, and sometimes L3 caches for improved data access and latency reduction.

10. Power Management: The processor employs power-efficient technologies to optimize energy consumption and extend battery life, including dynamic voltage and frequency scaling (DVFS).

11. Customization: Manufacturers can customize the Snapdragon 750G for specific devices or applications, enabling optimization and differentiation in the market.



</details>

## Day12 : BabySoC Modelling
<details>
<summary>4-bit adder</summary>
<br>	
	
The 4-bit full-adder is a basic combinational design with output a sum and a carry. The full adder takes 3-inputs i.e., two numbers being added and carry input from the previous stage. 
The truth table of a full-adder is as follows:
	
 ![adder ckt](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6fe2214b-04cb-452a-9b68-fc77143bb59a)
	
The following image shows the behavioral code of a 4-bit adder as follows:
```verilog
module full_add_4 (input [3:0] a , input [3:0] b , input c , output reg c_out , output reg [3:0] sum);
 always @ (a or b or c)
  begin
   {c_out, sum} = a + b + c;
  end
endmodule
```

The code defines a module in which two 4 bit inputs were taken and a 1 bit input carry and generates a 1 bit output carry and a 4 bit sum. The code defines the inputs and outputs as arguments.
The always statement is used to change the output when there is change in any one of the input and begin-end statement is used here for assigning the output values.
The following image is the testbench written for the 4-bit adder as follows:
![lab4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/396e4de5-d3a4-46cc-a5be-f3232d58bdab)

The inputs are defined in the testbench and the unit under test (uut) is assigned values that should be used for output waveform. The $dumpfile and $dumpvars is used to dump the vcd format file that can be viewed with the gtkwave. The variables are assigned values using Non-Blocking statements. 
The $monitor command prints the output of the code in the format specifier with the variables used. The for loop is defined to assign different values to the variables in a random manner ($random is used). 
So, The 5 different values are assigned as follows:
![lab3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8e7ecdf8-6840-4c5c-ab24-4d951fe898e5)

I have used the hex format specifiers so inputs are viewed in hexadecimal numbers.
</details>
<details>
<summary>BabySoC</summary>
<br>	
	
### System on Chip

SoC is a single-die chip that has some different IP cores on it. These IPs could vary from microprocessors (completely digital) to 5G broadband modems (completely analog).
Modeling and simulation is the use of a physical or logical representation of a given system to generate data and help determine decisions or make predictions about the system.
Models are representations that can aid in defining, analyzing, and communicating a set of concepts.
Modelling can be 
- Behavioral Modelling
- Structural Modelling
- Gate level Modelling
- Layout level Modelling
  Simulation enables engineers to test, analyze, and validate integrated circuits before physical fabrication. It plays a crucial role in ensuring the functionality, performance, and reliability of complex VLSI designs. The Simulations hrlps in early evaluation, functional validation of the design.The simulation can be timing, functional or power simulation.
  The simulation involves modelling, test bench development, analysis, validation and Optimization.

  Let us model the BabySoC that contains a PLL, DAC and RISC V processor. So, the design has three IP cores and a wrapper and a testbench.
  The module is fed with input signals such that PLL generates the clock and processor executes the instructions and the output is converted to analog by DAC.
  #### RVMYTH
  RVMYTH stands for RISC V processor. The RISC processor is used as it has following advantages compared with CISC:


| RISC                                      | CISC                                      |
|-------------------------------------------|-------------------------------------------|
| Abbreviated as Reduced Instruction Set Computer. | Abbreviated as Complex Instruction Set Computer. |
| It is a microprocessor architecture that uses small instruction set of uniform length. | Complex and variable-length instructions with a wide range of addressing modes. |
| Small instruction set, typically 100-200 instructions. | Large instruction set, often exceeding 1000 instructions. |
| Generally faster execution of instructions due to simplicity and predictability. | May have slower instruction execution due to complexity but can complete tasks in fewer instructions. |
| Highly amenable to pipelining, allowing for efficient instruction processing. | May have more challenging pipelining due to variable-length and complex instructions. |
| Rely more on load/store architecture, minimizing memory access in instructions. | May include memory access within complex instructions. |
| Code tends to be more compact and efficient. | Code can be larger due to complex instructions, potentially leading to larger memory requirements. |
| Typically more power-efficient due to simplified instruction set. | May consume more power due to complex instructions and decoding logic. |
|Registers are used for procedure arguments and return addresses. | The stack is used for procedure arguments and return addresses. |
| Examples are ARM, MIPS, PowerPC.| Examples are x86, x86-64 (Intel and AMD processors).|
|It doesn't support arrays.| It has a large number of instructions. It supports arrays.
##### Why RISC V is preferred?
- Open Source and Open Standards: RISC-V is an open standard ISA, which means anyone can freely use, modify, and implement it without licensing fees or legal restrictions. 
- Scalability: RISC-V is designed to be scalable, accommodating a wide range of implementations from small, power-efficient embedded systems to high-performance servers and supercomputers.
- Security: The open-source nature of RISC-V allows for greater scrutiny of the ISA, which can lead to improved security.
- Vendor Neutrality: RISC-V's openness reduces vendor lock-in and encourages competition among chip manufacturers.

The "I" in RISC-V stands for the integer base ISA, and it defines the core set of integer instructions that are common to all RISC-V processors. The "32I" and "64I" variants specify the integer base ISAs for 32-bit and 64-bit RISC-V processors, respectively.
The instruction set of 32 bit and 64 bit are mostly same, but extensions such as the "M" extension for integer multiplication and division are used.
The 64I RISC processor means that data registers are 64 bits wide, and arithmetic, logical, and immediate operations work with 64-bit operands. This modularity and extensibility are some of the key strengths of the RISC-V ISA.
![single cycle](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ed40aadf-8183-46a1-aa94-06616105d5b0)

Pipelining is a technique for breaking down a sequential process into various sub-operations and executing each sub-operation in its own dedicated segment that runs in parallel with all other segments.
- Fetch: Fetches the instruction from memory or instruction cache.
- Decode: Decodes the instruction to determine the operation to be performed and the operands.
- Execute: Executes the operation, which may involve arithmetic, logic, or memory operations.
- Memory: Accesses memory for data read or write operations.
- Write-back: Writes the result back to the register file or memory.

  The steps for the simulation are as follows:
  ```bash
  $iverilog mythcore_test.v tb_mythcore_test.v
  $./a.out
  $gtkwave tb_mythcore_test.vcd
  ```

  The following image shows the output simulated wave of RVMYTH processor. Upon reset, all values are ignored.
  ![lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7669efb5-31f6-460e-b85a-cf42d9ce365f)

#### Phase Locked Loop (PLL)
A phase-locked loop (PLL) is an electronic circuit with a voltage or voltage-driven oscillator that constantly adjusts to match the frequency of an input signal.
The off-chip clock causes delay due to long nets as they supply more blocks(resulting jitter). Clock Accuracy is not attained due to ppm error.
The ppm error is parts per million error. For example, 20 ppm error will cause 51 sec error in a month. Processor cannot take such huge error is operation is done in the order of micro and nano seconds.
The following image shows the block diagram as follows:
![PLL](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fc7a959a-50f1-4733-8896-212cd9251772)


- A Phase detector is a multiplier and it produces two frequency components at its output − sum of the frequencies fref and fosc and difference of frequencies fref & fosc.
- An active low pass filter produces a DC voltage at its output, after eliminating high frequency component present in the output of the phase detector. It also amplifies the signal.
- A VCO produces a signal having a certain frequency, when there is no input applied to it. This frequency can be shifted to either side by applying a DC voltage to it. Therefore, the frequency deviation is directly proportional to the DC voltage present at the output of a low pass filter.
PLL operates in free running mode when no input is applied to it. WHen there is input, the output signal frequency changes (called capture mode). The signal frequency changes until it equals the input signal frequency (called lock mode).
 The steps for the simulation are as follows:
  ```bash
  $iverilog avsd_pll_1v8.v pll_tb.v
  $./a.out
  $gtkwave test.vcd
  ```
The simulated output of PLL is as follows:
![lab5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6d60ca7d-64dc-4cff-9256-4442e4539d28)

The following image shows the enable of VCO is always high.  The reference input and VCO input are shown. 

#### Digital to Analog Converter (DAC)
The  Digital to Analog Converter (DAC) converts a digital input signal into an analog output signal. The digital signal is represented with a binary code, which is a combination of bits 0 and 1. A Digital to Analog Converter (DAC) consists of a number of binary inputs and a single output.
 The number of binary inputs of a DAC will be a power of two.
There are two types of DACs :
![DAC](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/75069b32-f517-45aa-8b72-ec3474816b90)

- Weighted Resistor DAC
  
    A weighted resistor DAC produces an analog output, which is almost equal to the digital (binary) input by using binary weighted resistors in the inverting adder circuit.
- R-2R Ladder DAC
  
  The R-2R Ladder DAC solves the disadvantages of binary weighted resistor DAC. R-2R Ladder DAC produces an analog output, which is almost equal to the digital (binary) input by using a R-2R ladder network in the inverting adder circuit.
  
 The steps for the simulation are as follows:
  ```bash
  $iverilog avsddac.v avsddac_tb_test.v
  $./a.out
  $gtkwave avsddac_tb_test.vcd
  ```
The following image shows the output waveform of the DAC. The voltage Vref is 3.3V as shown.
![lab8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7efe0299-6d67-48dd-bc8a-58642a8f0903)

The steps for the simulation are as follows:
  ```bash
  $iverilog rvmyth_pll.v rvmyth_pll_tb.v
  $./a.out
  $gtkwave test1.vcd
```
The interfacing of PLL and RVMYTH gave a simulated output as follows:
![lab7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fe83fd0f-d998-435e-b3ab-5da1d7149ab5)

 The steps for the simulation are as follows:
  ```bash
  $iverilog rvmyth_avsddac.v rvmyth_avsddac_TB.v
  $./a.out
  $gtkwave rvmyth_avsddac.vcd
  ```
The interfacing of DAC and RVMYTH gave the folowing simulated output:
![lab6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a2c69cc1-b72d-44dd-b496-a5f0cd89a6dc)

### Modelling Baby SOC
The Baby SoC consists of 3 IP cores and a wrapper as follows:
![babysoc](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cb51bcd5-114a-48fe-87c7-367be355173c)

Now, the top module SoC simulated output wave is as follows:
![lab9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/926934b4-6066-49a4-b10c-4debac9bc39a)

</details>

## Day13 : Post-Synthesis Simulation
<details>
<summary>Post-Synthesis of Full-Adder</summary>
<br>	

- Pre-synthesis simulation is done according to the logic designed for(functionality).
- Post synthesis simulation / ‘gate level simulation’ is done after synthesis considering each and every gate delays into account. It reports the violations in both functionality and timing.
- This verifies any mismatches in the design. There are different RTL coding styles that may cause synthesis mismatch such as casex, casez and synopsys directives such as full_case, parallel_case etc..
  These directives infer the tool about design such that it is optimized. But Their usage mostly causes a mismatch.
- Simply, RTL simulation is pre-synthesis, GLS is post-synthesis. RTL simulation is a zero delay environment and events generally occur on the active clock edge. GLS can be zero delay also, but is more often used in unit delay or full timing mode. 
The Full-Adder output as discussed for the pre-synthesis simulation matches with the post-simulation output.The following are the sequnece of steps for simulating the output.
```bash
iverilog full_add_net.v tb_add4.v primitives.v sky130_fd_sc_hd.v
./a.out
gtkwave tb_full_add_4.vcd
```
The iverilog command uses the simulated gatelevel netlist and the same testbench for post-synthesis simulation. The ./a.out dumps the vcd format file with respect to netlist. The gtkwave is used to view the waveform.
The post-simulation output is as follows:
![lab3 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cc9a920e-1905-4351-ae9e-c29c3a2f2c97)

 So, The output of post-synthesis and pre-synthesis exactly matches so the logical corectness of the design is verified.

The inputs a and b are given to each full adder and the carry from previous stage is given as input to the next stage. The following sequence of commands writes the netlist and ddc format as follows:
```bash
set target_library /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd__tt_025C_1v80.db
set link_library {* /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd__tt_025C_1v80.db}
read_verilog add4.v
link
compile_ultra
write -f verilog -out full_add_net.v
write -f ddc -out full_add.ddc
```
The read_db command is not used as the target_library and link_library are previously set to sky130 technology .db. 
The schematic of the full-adder can be viewed as follows:
![lab4 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c15dd490-b42c-417f-bb22-fa2bf74ab497)

</details>
<details>
<summary>Post-Synthesis of BabySoC</summary>
<br>	

The post-synthesis of the RISC-V processor RVMYTH is as follows:
![lab1 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d3e6c836-6f60-4749-bda9-a36f5d3e3590)

The .lib file, also known as a library file, is a critical component of the design flow. It contains information about standard cell libraries, which are pre-designed and pre-characterized digital logic cells used in the creation of digital integrated circuits.
The .db file, often called a "technology database," stores essential information about the semiconductor process, including cell libraries, transistor models, and process parameters, used by electronic design automation (EDA) tools for chip design and analysis.
A file is converted from .lib to .db using lc shell. The lc shell converts the human readable .lib file into machine readable .db file.
The steps for converting .lib to .db are
```bash
read_lib avsddac.lib
write_lib library -format db -output write_lib library -format db -output avsddac.db
```

The commands used for generating the out netlist are as follows:
```bash
read_verilog mythcore_test.v
set target_library /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd__tt_025C_1v80.db
set link_library {* /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd__tt_025C_1v80.db}
link
compile_ultra
write -f verilog -out rvmyth_net.v
```
The netlist being written here as out is the output of the clk_gate as it is default in code. So, the current_design is changed to core and the netlist is written out as follows:
```bash
current_design core
write -f verilog -out rvmyth_net.v
```
The schematic view of RVMYTH processor is as follows:
![lab5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6cd3b0ef-25c9-4011-9a6a-db007f5aefc8)

The processor output increments in the same way as at the pre-synthesis stage, So, the logic is properly defined.
The iverilog uses flags such as -D to define preprocessor macros, which can be used to conditionally include or exclude portions of your Verilog code during compilation. These macros can be very helpful for creating flexible and configurable designs.
- -DFUNCTIONAL : This flag defines a preprocessor macro named FUNCTIONAL. When compiled, the code inside the ifdef block will be included, and the code inside the else block will be excluded.
  
- -DUNIT_DELAY=#\<value\> : The -DUNIT_DELAY=#1 command you provided is used to define a preprocessor macro named UNIT_DELAY with a value of 1 when invoking the iverilog compiler. This macro definition can be useful when you want to parameterize or configure your Verilog code based on the value of UNIT_DELAY.
  
  It defines UNIT_DELAY with a value of 1, and the Verilog code inside the ifdef block will be included in the compilation, resulting in a wire with a range of \[0:0\]. If you compile without that flag, the code inside the else block will be included instead, resulting in a wire with a range of \[1:0\].
  
  The sky130_fd_sc_hd.v file is changed, especially the end if statement is changed from ```endif SKY130_FD_SC_HD__LPFLOW_BLEEDER_FUNCTIONAL_V``` to ```endif //SKY130_FD_SC_HD__LPFLOW_BLEEDER_FUNCTIONAL_V``` when iverilog command prompted errors.
  
The following commands are used to simulate the output waveform.
```bash
iverilog -DFUNCTIONAL -DUNIT_DELAY=#1 rvmyth_net.v tb_mythcore_test.v primitives.v sky130_fd_sc_hd.v
./a.out
gtkwave tb_mythcore_test.vcd
```
#### BabySoC
The post-synthesis of the BabySoC is as follows:
The Behavioral code of the BabySoC top module is as follows:
```verilog
module vsdbabysoc (
   output wire OUT,
   //
   input  wire reset,
   //
   input  wire VCO_IN,
   input  wire ENb_CP,
   input  wire ENb_VCO,
   input  wire REF,
   //
   // input  wire VREFL,
   input  wire VREFH
);

   wire CLK;
   wire [9:0] RV_TO_DAC;

   core test (
      .out(RV_TO_DAC),
      .clk(CLK),
      .reset(reset)
   );

   avsdpll pll (
      .CLK(CLK),
      .VCO_IN(VCO_IN),
      .ENb_CP(ENb_CP),
      .ENb_VCO(ENb_VCO),
      .REF(REF)
   );

   avsddac dac (
      .OUT(OUT),
      .D(RV_TO_DAC),
      // .VREFL(VREFL),
      .VREFH(VREFH)
   );
   
endmodule
```
The following commands are used to simulate the output waveform.
```bash
iverilog -DFUNCTIONAL -DUNIT_DELAY=#1 rvmyth_net.v testbench.v primitives.v sky130_fd_sc_hd.v avsddac.v avsdpll.v vsdbabysoc.v
./a.out
gtkwave dump.vcd
```
The schematic view of the BabySoC simulated is as follows. Here, the PLL,DAC are assumed as blackboxes and the libs provide lef and timing information of the IPs.
![lab6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f3b63d72-40ac-4f1f-84c3-c5702f727b2b)

The multiple modules defined in the top module are given as arguments to iverilog command so that all files included in design can be read and the output is simulated.

![lab2 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e4cfc812-5e14-4e04-bbf1-b471ecc0fb7c)

So, The output of Pre-Synthesis simulation and Post-synthesis simulation are obtained same. So, the logical correctness of the design is verified.

</details>

## Day14 : Synopsys DC and Timing Analysis
<details>
<summary>Introduction</summary>
<br>	

The PVT corners refer to specific combinations of Process, Voltage, and Temperature conditions that integrated circuits (ICs) or electronic devices operate under. These corners are crucial for designing and testing semiconductor devices and ensuring their functionality across different operating conditions.
- Process Corner: The process corner represents variations in the manufacturing process, including factors like doping levels, gate oxide thickness, and lithography variations. Process variation is the deviation in parameters of the transistor during the fabrication.Process corners are typically categorized as slow (SS), nominal (TT), and fast (FF), referring to the worst-case, typical, and best-case process conditions, respectively.
- Voltage Corner: Voltage corners refer to variations in the supply voltage (Vdd) of the electronic device. Common voltage corners include high voltage (HV) and low voltage (LV) corners. Different voltage levels can affect the speed and power consumption of the device.
- Temperature Corner: Temperature corners account for the temperature range in which the device operates. Corners typically include low-temperature (LT) and high-temperature (HT) scenarios. Temperature variations can influence the device's performance, power consumption, and reliability.
  The following graph illustrates the Delay with respect to change in PVT conditions assumin the other two to be ideal.
![graph](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/da097aa2-24d3-446c-9882-97c62305715b)

In order to make our chip to work after fabrication in all the possible conditions, we simulate it at different corners of process, voltage, and temperature. These conditions are called corners. All these three parameters directly affect the delay of the cell.
</details>
<details>
<summary>Timing Analysis</summary>
<br>

 The libs of the corners are provided in the git cloned. After cloning this repository, the libs are converted into db files using lc_shell by using following commands:
 ```bash
 read_lib <path to .lib file>
write_lib <library file name> -format db -output <nameof db file>
```
It generates errors showing some pins were defined to cells. So, All these unwanted attributes to pins are removed (deleting the error line).
Now The human readable library files are read and written into machine readable db files. Now, these files are synthesized using dc_shell with the following sequence of commands:
```bash
set target_library { sky130_PVT_corner.db , avsddac.db , avsdpll.db}
set link_library {* sky130_PVT_corner.db , avsddac.db , avsdpll.db}
read_verilog vsdbabysoc.v
link
source constraints.tcl
compile_ultra
report_timing
report_qor
```

The constraints.tcl file is as follows:
```tcl
 set_units -time ns
create_clock -name MYCLK -per 2 [get_pins pll/CLK];


set_clock_latency -source 1 [get_clocks MYCLK]
set_clock_uncertainty -setup 0.5 [get_clocks MYCLK]; 
set_clock_uncertainty -hold 0.4 [get_clocks MYCLK]; 


set_input_delay -max 1 -clock [get_clocks MYCLK] [all_inputs];
set_input_delay -min 0.5 -clock [get_clocks MYCLK] [all_inputs];

set_output_delay -max 1 -clock [get_clocks MYCLK] [all_outputs];
set_output_delay -min 0.5 -clock [get_clocks MYCLK] [all_outputs];

set_input_transition -max 0.2 [all_inputs];
set_input_transition -min 0.1 [all_inputs];

set_max_area  800;

set_load -max 0.2 \[all_outputs];
set_load -min 0.1 \[all_outputs];
```

The Timing delay of a path varies for each PVT corner being used.

|Corner  	|WNS	|WHS	|THS	|TNS    |
|---|---|---|---|---|
|ff_100C_1v65   |   0   | 0.15  | 50.22 |   0   |
|ff_100C_1v95   |   0   |  0.2  | 125.64|   0   |
|ff_n40C_1v56   |0.19	|0.11	|7.19	|141.44 |
|ff_n40C_1v76   |0	|0.18   |86.34	|0      |
|ff_n40C_1v65	|0.02	|0.14	|42.33	|4.13   |
|ss_100C_1v40	|3.38	|0	|0	|3488.63|
|ss_100C_1v60	|1.83	|0	|0	|1884.76|
| ss_n40C_1v28	|8.95	|0	|0	|9629.38|
|ss_n40C_1v35	|6.03	|0	|0	|6433.23|
| ss_n40C_1v40	|4.81	|0	|0	|5083.92|
|ss_n40C_1v76	|1.21	|0	|0	|1221.33|
|ss_n40C_1v44	|4.13	|0	|0	|4290.31|
|tt_025C_1v80	|0.23	|0.09	|5.12	|187.25 |

Let us consider the following corners and their delays as follows:
The following image shows the setup delay and qor when there are noconstraints defined.
![lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f72ad3e9-7c87-4114-92c3-356d23911c7e)

![lab3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e6b9a88e-7fb5-4012-8a6e-96247cdd76a0)

The following reports show the timing and QoR for each corner as follows:
- ff_100C_1v65
![lab4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bbda4675-0530-41f9-8729-d63776f37753)

![lab4_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5d766fa4-d762-4adb-868e-b12c909aa22a)

- ff_100C_1v95
![lab5 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aba2dd7f-101c-4d38-9c07-2cc720b7dcb9)

![lab5_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a0ba7780-7da8-44dc-886b-84a2f8caf163)

- ff_n40C_1v56
![lab6 (1)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1abc536e-6e5a-4ca8-ba6c-81467b738f39)

![lab6_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2ac1c9ab-9d99-4aec-8c05-3dba869395f4)

- ff_n40C_1v65
![lab7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4ebc94fc-76f2-4098-8532-0e6d898e75e3)

![lab7_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f640e6f4-2d56-4650-afea-a853c17607e5)

- ff_n40C_1v76
![lab8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7ad5b645-9eb3-4667-aadd-076b8b447032)
  
![lab8_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/97eb933a-abdb-4f5c-aedd-12e5b6c6c305)

- ss_100C_1v40
![lab9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1116a797-9042-487e-86f7-ca7b20287b8b)

![lab9_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ae01d4c8-746c-4bda-abcf-f13f730b2aa7)

- ss_100C_1v60
![lab10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e137971c-44bc-4116-b7a9-7dff1bc6396b)

![lab10_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0e9893b2-71de-452f-8129-fcbbdae3fc79)

- ss_n40C_1v28
![lab11](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/03af12fc-6c00-4e51-8c72-17aa9ba52b08)

![lab11_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bb26e863-a7e2-4d08-b82f-567979a6a647)

- ss_n40C_1v35
![lab12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/882674cd-03fe-476d-9506-449c8ece8b83)

![lab12_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e36080fd-db74-43b4-8d61-4b8abd25029f)

- ss_n40C_1v40
![lab13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/54aabbdf-0036-4674-8232-04cfd63729a0)

![lab13_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/da277e49-b479-4480-9f46-081423bb0582)
  
- ss_n40C_1v44
![lab14(1v44)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9c6bac77-fdfa-4279-8a89-59a333ab0d7c)

![lab14_2(1v46)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e27064c6-728b-469b-a8f1-7563d57d3567)

- ss_n40C_1v76
![lab15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7f382d0b-4c73-4809-b2a7-fbf26de4d073)

![lab15_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b25761f8-8416-41cb-a36c-ddb869a5b835)

- tt_025C_1v80
![lab16_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6c2a8c22-e355-4a05-abb6-133dbe93f7e7)

Now The following graphs illustrate the change in slack from slow process to fast process, change in voltage and change in temperature as follows:

This graph shows that the WNS is mostly 0.00 for fast corners and the setup violates for slow corners. WNS stands for Worst Negative Slack, the setup violated slack of the most critical path in the design.
![WNS](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9a9cf657-ebdc-4677-8448-403e06108eb3)


This graph shows the TNS of the design. TNS stands for Total Negative Slack, which is the sum of all the violated setup slack in the design.
![TNS](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d3d16394-057c-4b25-812d-960210bea127)


This graph shows that the WHS is mostly 0.00 for slow corners and the hold violates for fast corners. WHS stands for Worst Hold Slack, the hold violated slack of the most critical path in the design.

![WHS](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/923ea37f-193e-474e-b6a2-861c66864e9f)


This graph shows the THS of the design. THS stands for Total Hold Slack, which is the sum of all the violated hold slack in the design.
![THS](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ae3f65ea-ff5c-42b6-940c-086a1515f0ee)

</details>

## Day15 : Inception of EDA and PDK
<details>
<summary>Introduction</summary>
<br>	

Anykind of electronic circuitry is fabricated on a board. The board typically consists of a process along with many interfaces such as JTAG and DAC etc..
A particular chip would look as follows:
![img](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/69cc5fe2-2e06-4772-87da-a41623bba8f6)

This is a package of QFN-48( Quad Flat No Leads with 48 pins). All these pins work interfaced with other packages on the design board.
The size of this package is 7mmx7mm. There are various kinds of packages available in different sizes.
A chip usually sits at the centre of the package. The outbounds are used to communicate data from external world to the chip.
A chip contains various components such as Pads, core and die.
- Pads are used to send signals inside the chip to external pins and vice-versa.
- Core is place where the digital logic is present.
- Die is the size of chip, being manufactured on the silicon wafer.

The RISCV SoC looks as follows:
![img2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d527d090-57df-4e92-9d5e-67f51b5fe67e)

In this design, PLL,DAC, SRAM are Foundry IPs and SPI, RISCV are macros. The macros contain pure digital logic whereas the IPs are Intellectual Properties that are desgined externally and placed in the design.

The RISC V Instruction Set Architecture defines the way of interacting with the computer. When a task is to be performed on the layout, the task needs to converted to assembly code and then to machine understandable binary format and the output is processed. A HDL is used to interact between the layout and the instruction set architecture.

The following image shows the overview of the architecture to layout design. The task to be perfomred in the application software is governed through the Operation system, that handles IO functions and low level system functions. The application software compiles, and the .exe file is converted to assembly language and the nbinary fomat. This binary format links with the HDL code and gnerates a synthesized netlist.
![img3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a8b7ab2e-8336-4c1c-9970-602e081500ad)
</details>

<details>
<summary>OpenLANE</summary>
<br>	
	
The Digital ASIC design requires the Register Transfer lanfer language(RTL) models including models of all IPs used, the EDA tools and the PDK.
There are various Open source inputs for Digital ASIC design like RTL models at opencores.org, github, EDA tools such as Qflow, OpenLane, PDK such as skywater for 130nm technology.
The interface between the Fab and the designer is a set of files referred as Process Design Kit (PDK). The PDK is a collection of files used to model a fabrication process for the EDA tools used to design an IC such as device models, design rules, technology information etc..
The 130nm technology executes single cycle at frequency greater than 300MHz, so pipelining can achieve a frequency of 1GHz. So, The frequency of operation is good.
The  basic ASIC flow includes various stages such as Floorplan, Powerplan, placement, CTS and so on. The RTL to GDSII flow is as follows:
![img4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f5b67b34-be4b-4a7d-a94e-8a375bb1fcc8)

- Synthesis : Converts the RTL into a circuit of components of Standard Cell Library (SCL). This generated circuit is read through HDL and referred as netlist. The RTL and netlist have equivalent functionality.
  The Standard cells have a regular layout. The standard cell height is always fixed, the width is varied as discrete multiples of site width. Each design has dillferent views/models such as  HDL view, SPICE view, ELectrical view, Layout view.
- Floorplan and powerplan : Plans silicon area and robust power distribution.
   - In chip Floor-Planning, The chip die is partitioned between different building blocks and places IO pads.
   - In Macro Floor-Planning, The dimensions, pin locations, rows and routing tracks are defined.
   - In Power-Planning, the power mesh is constructed.The power pads are connected to all cells through power rings, vertical and horizontal metal straps.
   - The EMIR problem is avoided by using higher metal layers thus reducing the resistance.
- Placement : Places the macros and cells in gate-level netlist on the wafer rows, aligned with sites. The connected cells are placed close such that reduces interconnet delay and to enable successful routing.
    Placement is done in 2 ways.
   - GLobal placement tries to find optimal position for all cells, which maynot be legal causing cells to overlap.
   - In Detailed placement, the positions in global placement are minimally altered to make the design legal.
- Clock Tree Synthesis : Clock must be routed before routing signals. The clock distribution network is created to deliver clock to all sequential cells with minimum skew, minimum latency. The clock network is a tree where clock source are roots and clocked elements are roots. The clock tree shapes can be H tree, Fish bone etc.
- Routing : Signals are routed after the clock is routed. It implements the interconnect using the available metal layers as defined by PDK.
   - PDK defines metal pitch, thickness, tracks, minimum width.
   - It also defines vias to connect different metal segments together. Most routers are grid routers, constructed out of metal layer tracks.
   - It uses divide and conquer approach. First, Global routing is done by coarse-grained grid to generate routing guides. Next the detailed routing used fine-grained grid to implement the actual wiring.
- Sign Off: After routing, the final layout can be constructed after verification. This includes:
   - Physical Verification: Design Rule Checking (DRC) and Layout vs Schematic (LVS)
   - Static Timing Analysis : Ensures all timing constraints are defined and met.
     
The reference methodology created for the Opensource ASIC flow to avoid missing tools and their calibration is referred as Openlane. Openlane is started as an opensource flow for a true opensource tapeout experiment.
Strive is a family of Open everything SoCs that has open PDKs, open EDAs and open RTL. The strive family has several members as follows:

|SoC |Features|
|---|---|
|striVe|Sky130 SCL + Synthesized 1KBytes SRAM|
|striVe 2 |Sky130 SCL + 1 KBytes OpenRAM block|
|striVe 2a|striVe 2 with a single chip core module |
|striVe 3|OSU SCL + Synthesized 1KBytes SRAM |
|striVe 5|Sky130 SCL + 8x 1 KBytes OpenRAM banks|
|striVe 6|striVe 2 with DFT|

The main goal of OpenLane ASIC flow is to produce clean GDSII with no human intervention in the loop. Clean means with no timing violations, DRC violations, LVS violations.
OpenLane can be used to harden Macros and chips. It has 2 modes of operation i.e., Autonomous or Interactive.
 The Autonomous is an automated flow that waits for output after some time, the Interactive flow can check intermediate outputs, used to experimenting the design.
The OpenLANE provides design space exploration to find best set of flow configurations. The following image shows the complete OpenLANE ASIC flow.
![img4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c499ce7a-54c9-4eed-9003-27bddc232cd6)

- The flow starts with RTL. The RTL is fed to ```Yosys``` with design constraitnts. This circuit can be optimized and mapped into cells from synthesis library using ```abc```. abc has to be guided using the optimization through scripts. OpenLANE has different ```abc``` scripts referred as synthesis strategies that target best timing. 
- The ```synthesis exploration utility``` is used to generate a report of the delay, area affected by synthesis strategy.OpenLANE has ```Design exploration utility```which can be used to sweep design configurations and generate the best design to be chosen. It also uses regression for testing.The best design  configuration is recommended to go forth for the design for a clean layout.
- After testing, Structure insertion is done. This step is enabled for testing after fabrication. The DFT stage uses ```Fault``` for scan insertion, automatic test pattern generation and compaction,  fault coverage and simulation. This step adds extra logic such as scanchain for testing. It can also add JTAG controller, that allows access of internal scan chains to external devices. 
- The Physical implementation has various steps and OpenROAD does all the implementation such as End decoupling capacitors and tap cells insertion, placement, optimization, CTS and routing. 
- After optimization, there may be some changes in gate-level netlist, so logical equivalence checking is performed.  This can be done using ```yosys```. Everytime netlist is changed, verification must be performed. The CTS modifies the netlist, placement optimization also modifies the netlist.
- When a metal wire is fabricated, it can act as an antenna.Reactive ion etching causes charge to accumulate on the wire, this damaging gates during fabrication. This has two solutions:
  - Bridging attaches a higher layer intermediary, it requires router awareness.
  - To add antenna diode cell to leak away charges, these diodes are provided in libs.
The preventive approach is to add fake antenna diode cell after placement and run the antenna checker. If any violations, replace the fake diode cdell with real one.
The OpenLANE signoff checks DRC,LVS and STA. LVS and DRC uses ```magic``` and STA uses ```OpenSTA``` with parasitic extraction.
</details>
<details>
<summary>Lab on OpenLANE</summary>
<br>	
The OpenLANE is a flow, that comprises of many open-source EDA tools such as yosys for synthesis, OpenSTA for Static Timing Analysis. The OpenLANE completely cuts off the human intervention such that the inputs RTL, foundry PDKS being provided, the GDSII file is generated.
	
Let us explore the contents of our openlane working directory. This directory consists of openlane and pdks. In pdks, they contain timing libraries, lef files, tech lef, cell lef etc.. The open_pdks contain scripts that make the sky-water pdks, which are designed for commercial EDA tools, compatible with open-source EDA tools.

The sky130A is the variant that is made compatible. This contains libs.ref and libs.tech. The libs.ref contains the process specific and libs.tech contains tool specific. As shown, the netgen,openlane are the tools and sky130_fd are process variants.

![lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f554a452-8679-49d6-8335-146bccb41a9f)

The sky130_fd_sc_hd is the process used for our design. The sky130 is the 130nm technology being used and fd is abbreviated as foundry, the sc stands for standard cell and hd stands for high density. 

This sky130_fd_sc_hd contains the following files such as lef, tech lef, libs. The libs contain the information to various PVT corners and the lef and tech lef are as follows.
![lab2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3b15f851-a5c8-4cd0-bc1b-74d44f9672d3)

Now, inorder to run the openlane, we initialize the docker using the following command:

```docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) openlane:rc2```

But it is aliased as ```docker```

![lab3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dd7d7ac9-c6c3-42ea-b123-1ef7ca9816e7)

Now Let us look at the design. There are various designs in the designs directory. Let us use picorv32a. In this, the src directory contains the RTL information such as the behavioral code (.v file), constraints file (.sdc file). The config.tcl bypasses any configuration already done to the lane. The design takes some default values to the attributes that are not defined.

 The order of precedence is
- the attributes defined by PVT corner config.tcl
- attributes defined in config.tcl
- attributes default values of OpenLANE

  The design has config.tcl and sky130 variant config.tcl for each and every PVT corner in every design as follows:
  ![lab5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/92a60c4e-a535-4b3e-b730-1bb6b785425b)

  The contents of config.tcl are as follows:
  ![lab4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/75cfb31e-a19c-411d-8089-4bcadf3ba6ca)

 The contents of sky130_fd_sc_hd vonfig.tcl are as follows:
![lab6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/098873f4-6454-46d7-b670-e50e3981d953)

Now, the design is prepared with the command as follows. It links all the lef files, lib files, macros, diodes etc..
```tcl
prep -design picorv32a
```
This can be viewed as follows:
![lab7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ee2eca54-fcb8-4532-8da7-d26b5c0cd2fc)

After the completion of this run, the runs directory is created and the reports, logs, results are all dumped to different direcotries as follows:
![lab8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5a7eb18b-2919-4281-ab54-b8582b6c5439)

The merged.lef contains the layer information, via information, macro information in the design as follows:
![lab9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/35883d97-916e-4523-8b4a-fff7b7ff6f0b)

![lab10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aa46d080-c6e3-445a-9283-77dd71976012)

The results files are empty as the design is not run.
![lab11](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6be6a779-2d73-470c-a3b1-69ddc020c7c6)

In the runs directory, a file is created to show all the defined values of attributes called config.tcl as follows:
![lab12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cde39ca3-76c3-4e4e-a8d0-94b81b0345c4)

Now, the synthesis is fired using the command ```run_synthesis```. So, the synthesis was successfully done.
![lab13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d4faadb2-0834-44fd-bf38-6a75049a179f)

The flop ratio is the number of flops to the number of cells in the design. As shown, there are 1613 flipflops in the design (dfxtp-D flipflop with positive trigger) and 14876 cells in the design. So,

  Flopratio = No. of flops/No. of cells in design = 1613/14876 = 0.108.
  
  So, The flop count is 10.8% of cells in the design.
  
![lab14](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f60f4503-7bf9-4fc1-8348-ec49a0f75de2)

The following image shows the synthesized netlist such that all cells are mapped to skywater 130nm technology.
![lab15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/05010d3e-9468-4b31-b9cd-8dd93f47a284)

The following image shows that the design is violated. One of the report is violated with huge negative slack as follows:
![lab16](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ec94cf32-f69f-443f-a6f3-df73c57ed617)

</details>

## Day16 : Good Floorplan vs Bad Floorplan

<details>
<summary>Chip Floorplan Considerations</summary>
<br>	

Floorplan considerations:
- Height and Width of core and die
  
  Let us consider a simple netlist that has a reg-reg timing path with 2 flops and 2 combinational gates as follows:
  
  ![12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/69b90b30-ef43-495a-8ddc-fd9700b7bdb8)

The dimensions of core and die are the summation of the area of standard cells present in the design. 
Let us assume that the area of the standard cell as 1sq. unit and the area of flipflop as 1 sq. unit.
So, the minimum area occupied by the netlist is 4 sq. units, however may be placed.

A core is the section of a chip where the fundamental logic of a design is placed.
A die, which consists of core, is a small semiconductor material specimen on which the fundamental circuit is fabricated. The core is encapsulated with the die.
When our design is placed on the core, the logic cells completely occupy the area of the core i.e., the utilization of area is 100%. So,

   Utilization factor =   Area occupied by netlist/Total area of the core
   
When the utilization factor is 1, there is no space left on die for any other optimization. So, ideally the utilization factor used is 50-60%.

Aspect Ratio = Height/Width

Whenever the aspect ratio is 1, it signifies a square chip. Otherwise, it is a rectangle.

Let us now consider the following example that has a utilization factor of 0.5 and aspect ratio of 0.5. 
The length of the die is 2 units and height is 4 units. So, aspect ratio=2/4=0.5. The area required by the logic is 4 units so the utilization factor = 4/2x4=1/2=0.5. 
![34](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/93f030ae-cddb-4306-b91a-d3b8f2a1c317)

  Let us consider another core with area of 4x4 sq.units with the same netlist. So, The utilization factor now would be (2x2)/(4x4)= 0.25. So, Only 25% of area is utilized, the reamining area can be used for optimization.The aspect ratio here is 1, so it is a square chip. 
  ![123](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1832eb88-5287-44ea-a55d-f47a64f223ea)

- **Location of Preplaced Cells**
  
 Preplaced cells are the piece of combinational logic such as macros, IPs that is being reused multiple times. The preplaced cells are placed based on the design scenario.The location of the preplaced cells need to be very well-defined.
 The preplaced cells can be understood with an example. Let us consider a combinational logic with 100k gates that can be granularised. Let us divide the circuit into two parts that can be seperated as two blocks.
![34](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b873a560-8336-4b82-a3fe-76d7ce5e72ed)

The IO pins of these blocks are extended and are seperated as two different IP modules, where the logic in the block is a black box. These blocks can be used multiple times on the netlist and designed only once. In other words, the block is designed as an IP and defined as blackbox in the main netlist and can be reused.

These models functionality defined once and reused on the chip. This is done before actual placement and routing. The location of these cells is usually fixed. 
The arrangement of these IPs is referrred as floorplanning. These IPs have user-defined locations, hence are placed in chip before automated place and route, and are called as pre-placed cells.
The tool places the remaining logical cells in the design onto chip. The tool do not touch the location of these pre-placed cells.

These pre-placed cells needs to be surrounded with decoupling capacitors. When the output of a logic gate changes from 0 to 1, an amount of current is demanded by the output capacitance of the gate. It is the responsibility of Vdd to supply the necessary voltage for switching the logic in the design.Similary, From logic 1 to 0, the Vss should be able to handle the discharged currents by logic in the design. The physical wires that connect the design will have a drop as they have resistance, inductance and capacitance.
![capacitance model](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/07f30b08-f84d-48a4-ba93-41858a8522ce)

During switching operation, the circuit demands switching current. There will be a voltage drop across them and voltage will be Vdd-IRdrop. If this value goes below noise margin, due to IR drop, the logic 1 at output won't be detected as 1 at the input of circuit. As shown, any voltage between Vol and Vil is considered logic '0' and voltage between Voh and Vih is considered as logic '1' and the voltage between Vil and Vih is undefined region as the voltage may rise to Vih or degrade to Vil.
![noise](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ffb2006a-7b5d-4486-b26f-a30da19d379a)

The decoupling capacitors helps to overcome the noise due to long distance from the supply voltage. So, Addition of decoupling capacitor in parallel with circuit is done. So, Every time the circuit switches, it draws current from decoupling capacitor (Cd) as the RL network is used to replenish the charge into Cd.
![decap](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8bcfa01e-5d14-4227-b1d0-558d26f2b894)

*Addition of decoupling capacitor will avoid the problems of crosstalk and degradation of logic.*

#### Power Planning
The macros requires the current for each cell in the design when reused.Let us assume a design where it ocntains various macros surrounded with decoupling capacitors. The Power Supply Vdd and Vss are connected as shown to each macro.Now, let the two macros connected as shown be the driver and load. 
The signal should propagate from the driver to load without any degradation. Assume that the driver is sending logic 0 to logic 1 to the load. It is not feasible to add decoupling capacitor to each cell in the logic. The critical blocks are added with decoupling capacitor.
Consider the connect is a 16-bit bus, that has 16-bit logic, that is it charges and discharges as shown. The logic at output is connected to an inverter.
This means all the capacitors which were charged to 'V' volts will have to discharge to '0' volts through single ground tap point. This will cause a bump in Ground tap point. If this bump exceeds the noise margin level, the output will be in a undefined region. (In undefined region, the output becomes unpredictable).
![powerplan](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2c0c62a7-aeda-4fea-886e-c00cf8a5caac)

Also, all capacitors which were 0 volts will charge to V volts through single Vdd tap point. This causes a voltage droop. If it goes beyond noise margin, it again becomes unpredictable. 
All this occur due to a single Vdd point, if there are multiples power supply points then each capacitor can charge and discharge from its nearest points as shown.
So, Powermesh is the exact solution to mitigate voltage droops and ground bounces.
#### Pin placement
The connectivity information between the gates is coded using VHDL/verilog language and is called the netlist. Let us consider an example. There are two timing paths driven by different clocks, two timing paths driven by two (interclocks)clocks (alternate flops)  and preplaced cells are connected in the design as shown.
![placepin](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/831dfec7-b607-43b3-88a6-c866e6d3a2cf)

The pins are usually placed in the region between die and the core. This area is reserved for pin location. The logical cell placement blockage is used to avoid tool from inserting cells in this region.
Let us consider that the input ports are connected on the left hand side and the output ports are connected on the right hand side. The ordering of the ports is random, it depends on where the cells are planned to place. 
The flipflops should not be placed on the preplaced cells, because their location is fixed. The clock port drives the cells continuously, so the least resistance path is required for the clock.

### Lab
The README file in the opelane/configuration contains all the switches that are defined for the design flow. The cotents of README are as follows:

The switches for synthesis step are:
![lab1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/22e0ed87-6590-4524-b84b-2fc9ed8c7ac8)

The switches for Floorplan step are:
![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/09402c2e-a6d7-4e96-8d52-e2c5ed3ef452)

- The FP_CORE_UTIL is to define the utilization of the core.
- The FP_ASPECT_RATIO defines the aspect ratio i.e., height/width of the core.
- The FP_CORE_MARGIN is the offset between the core and die area.
All the switches need not be set. The switches that are required vary from design to design.

The switches for placement as follows:
![lab1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0a20de94-6b2b-47c0-ade0-40ae8d400e7d)

The contents pf floorplan.tcl in this folder shows the variables set to values as follows:
![lab1_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9b887336-ed9e-4b87-93b7-a7d37cccc76e)

The config.tcl contents inside the design are as follows:
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/294d3ce2-9d6b-4dae-b920-1c001abcef4d)

The contents of sky130_fd_sc_hd_config.tcl are aas follows:
![lab1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/31bc21a7-9a9e-4589-b920-0a58091bc460)

Now, 
```run_floorplan``` command is given and the floorplan run is fired. The PDN was created successfully.
![lab1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b42b4469-2a2f-4c80-888d-90afcbbccce8)

The following image shows that the design after run, 
![lab1_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/04e6788c-7896-4fcb-83cc-928c054acbdc)

The config.tcl after the run shows the variables set in the design as follows:
![log before 2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/658e8a41-cf4c-4c85-9100-3d1678b4a17d)

The metal layers are set to one more than defined value. Here VMETAL is 3 and HMETAL is 4 after the run. The core utilization is 35% in the log after run and before run is as follows:
![log before 3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dbfd684b-0042-4822-a3f7-1a8293000bca)

The contents of io-placer log is as follows:
![log before](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e49b80d0-9e8e-460d-bc15-abd53b879d1a)

The contents of def file after floorplan are as follows:
![def](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d74555be-40cd-45e8-8fdf-6854170a9a6e)

Inorder to view the floorplan the magic command is used as follows:

This command is executed in the results/floorplan directory after runs.
```
magic -T /Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```
Now, The floorplan is opened. Press **S** for selecting the whole design nd **V** to align the design to center.
![design1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a8bad38f-df7e-4889-84e6-6ace9aa36fa7)

By zooming,
![design2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/85f38403-d089-43dd-b4bc-33ecf33328ac)

By selecting a particular object and giving ```what``` command in tkcon.tcl gives the description of the shape as follows:
![design3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/70be3b8a-2c60-479b-8887-f8240cf530f5)

![design4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/08deabd0-0f6d-4940-8006-1db75f5bbb1f)

The physical cells can be viewed when more zoomed in,
![design5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9ca96966-4d98-4b65-a190-453d2744bfc7)

All the cells are not placed in the design as placement is done. All these cells are present as cluster at the origin point as follows. When a particular cell is selected, it shows a standard cell as OAI cell.
![design6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8ab79e3c-eee5-4f6a-a7c3-090d2dc3d04c)

</details>
<details>
<summary>Library Binding and Placement</summary>
<br>	
	
#### Binding netlist with physical cells
Each cell represented in synthesis as per functionality, has certain width and height. So, These cells information placed according to their size and shape in a file called library. The library contains the timing information and shape,size information of cells and condition on cells such as when condition.
The library contains various flavours of cells that can be picked based on timing and area available on the floorplan.
#### Placement on floorplan
The floorplan has well-defined ports and pins in the design. The netlist has the physical view of logic gates as follows:

The placement stage ensures that the pre-placed cells are unaffected i.e., no cells are placed on the pre-placed cell locations. The cells are placed in a way that it is relatively less distant from the ports connected to it.
The Signal Intergrity is the faithful transmission of signal from one point to another point. The signal intergrity is maintained by repeaters which are basically buffers that recondition the original signal and make new signal that replicates original signal and send it to next stage.
In the placement optimization stage, the wire length and capacitance are estimated such that the transition of signal is in permissible range.
The Slew is dependent on the value of capacitance. For high value of capacitance, the amount required to charge is more, the slew will be bad.
When the cells are placed farther, then the transition and capacitance will be more, so the length is cut down by inserting buffers so that the signal is not deteriorated.
When the signal frequency is high, the delay cannot be wasted on nets, so they are placed close to each other to avoid any significant delay.
The Buffers are inserted in the design assuming that clock is ideal as clock is not built yet. The data path is considered and when the length is greater than permissible values, depending upon the transition and slew, buffers are inserted.
 The timing must be met in the placement stage because it is bound to go worst in the next stages especially routing stage.
 #### Need for  characterization
 IC flow:
 - The process of converting functionality (Behavioral code) into legal hardware is referred to as Logic Synthesis. It is arrangement of gates for reproducing the original functinality described with RTL.
 - Importing the netlist of logic synthesis and defining height and width of core and die in the floorplanning.
 - The logic cells are placed in such a way that the timing is met in the placement stage.
 - The CTS generates clock in such a way that skew is minimal i.e., all flops in design would get clock at almost same time. The clock buffers take care of equal fall and rise time of the signal.
 -  The Routing follows some constraints inorder to connect one cell to another cell in design.
 -  Static TIming Analysis is the last sign-off stage to check timing vilations in the flow.

The cells are common in each stage.The cells are modelled such that the tool understands which cell to pick at each stage for better optimization.

### Lab
The placement being done is congestion aware, not for timing optimization.
 - Global placement is a coarse placement where no legalization is happening.
   Legalisation is nothing but the cells must be placed in the rows and must be abutted to each other and there should be no overlaps. The global placement reduces wire length. The openLANE uses HPW (Half parameter wirelength).
The placement run is fired with ```run_placement``` command.

   The following figures show the HPW variatin during placement stage
   ![day2_2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b17032c4-c11c-4bbd-90fa-afff1a6bd239)

   ![day2_2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7ce9d9ac-76ce-4ce1-97bd-3c82476c8e85)
The placement run is successfully completed as follows:
![day2_2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/30efce03-50a3-40c0-bfd9-11bade6fb133)

The following images show that cells are placed in their rows as follows:
![day2_2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5d1504d6-039c-4e05-8840-c20a2258ddf9)

![day2_2_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8522cef8-68b1-49bc-82ec-0ffa0ae2acf0)

All the cells in the lower left corner are now placed along the core of the design. There are no DRCs and all standard cells are placed in their rows.
Flooplan ensured that decap cells are at boundary of standard cells, tap cells are properly placed, IO cells are correctly placed. The Power distribution Network(PDN) is created during the floorplan.
</details>
<details>
<summary>Cell Design and Characterization</summary>
<br>	

The flipflop, buffer, combiantional gates are called Standard cells. The library contains various information such as Standard cells, Decap cells, macros, IPs etc..
The cells in library have different size and different functionality and different threshold voltage.The bigger buffers have higher drive strength.

#### Cell Design flow
The cell design can be explained as inputs, design steps and outputs. 
#### Inputs
   - Process Design Kits (PDKs)
   - LVS & DRC rules
     The tech file gives some rules such as extension over active, polywidth etc.. The active area is place where you place transistors. 
   - SPICE models
      The SPICE model parameters are the values provided by foundry.
   - Library and User-defined Specifications
 	- The seperation of Power rail and ground rail defines the cell height. The cell width depends on the timing information.
	- The typical cell has to work on the supply voltage provided by TOP level. The library cell is designed  and noise margin is defined based on this specification by TOP level
        - Certain cells need to be designed with specified Metal layers, Pin locations are defined by TOP level, the drawn gate length may vary above or below specified value.
#### Design Steps
 The library cell is chosen that adheres with all the design specifications specified in the inputs.
 - Circuit Design
   The circuit design implements the function and models NMOS and PMOS in such a fashion that meeets the library requirements.The output of circuit design is circuit description language (cdl).
 - Layout Design
   - The design is implemented thorugh NMOS and PMOS transistors and obtain network graph for nmos and pmos.
   - The art of layout is a combiantion of Euler's path and stick diagram. The Euler's path is the path being traced only once. The stick diagram is obtained from the Euler's path.
   - The stick diagram is converted into typical layout adhering to the rules from inputs.
 - Characterization
   It helps to get timing, noise and power information.In an extracted SPICE netlist, the resistance and capacitance of various cells will be defined.
    - NMOS, PMOs models are read
    - Extraced SPICE netlist is read
    - Recognizing the behaviour of the cell(buffer)
    - Reading sub-circuits of inverter
    - Read in necessary power supplies
    - Applying stimulus (Characterization setup)
    - Applying necessary output capacitance
    - Necessary simulation commands are given
   These are carried out by GUNA simulator generationg outputs files that characterize timing, power and noise.
#### Outputs
- CDL file : It is obtained as output of the cirucuit design step after modelling the circuit with NMOS and PMOS transistors.
- GDSII file : The output of the layout design modelled with stick diagrams.
- LEF basically defines height and width of cell
- CIR file is the extracted parasitics of each cell called extracted spice netlist used to do characterization.

### General Timing Characterization Parameters
GUNA software is a characterization software that works on variables available as inputs with us.Let us understand the syntax and symnatics of timing.lib, power.lib, noise.lib.
The different threshold points of a waveform are called timing threshold definitions.
- slew_low_rise_thr
  This is determined by taking points near to lower side of power supply which is 0 volts for rising signal. The typical value is 20%.
- slew_high_rise_thr
  This is determined by taking points near to rising side of the supply for rising signal. This is usually 80%. 
- slew_low_fall_thr
  This is determined by taking points near to lower side of power supply which is 0 volts for falling signal. The typical value is 20%.
- slew_high_fall_thr
   This is determined by taking points near to rising side of the supply for falling signal. This is usually 80%. 
- in_rise_thr
  The slew in the input transition of the applied stimulus for rising input. This is usually 50%.
- in_fall_thr
  The slew in the input transition of the applied stimulus for falling input. This is usually 50%.
- out_rise_thr
   The slew in the output waveform obtained as the output of cell for rise in output. This is usually 50%
- out_fall_thr
  The slew in the output waveform obtained as the output of cell for rise in output. This is usually 50%
These are used to calculate slew, propagation delay, currents etc..
The threshold points must be chosen carefully. When chosen wrong, the cell delay may be negative, as output point comes becomes the input. While writing out libs, this issue is seen.
 - The propagation delay is defined as difference between output and input thresholds points.
 - The transition time is the difference between high threshold to low threshold points. 
If a circuit is not designed properly i.e., input has more transition then the slew (50% point) at input comes much later than the slew of output (50% point).
</details>

## Day17 : Std Cell Characterize Experiment

<details>
<summary>CMOS Inverter Simulations</summary>
<br>	

 #### IO placer
The OpenLANE provides chance to change the variable options on the fly. Inorder to change the congestion of IO pins alignment, the magic command is used to view the floorplan def as follows:
```
magic -T /Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
The floorplan can be viewed as follows. The pins are placed in equidistant.
![lab0_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/29bab887-e1f4-4451-88d4-bd7730644433)

The IO placer is the tool used to place IO pins based on the requirement specified. So, let us increase the congestion by changing the variable to 2 as follows:
![lab0_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6bcd33b3-04f8-4690-895f-bfc12215c45c)

Now the floorplan run is fired again, the pins are placed closely as follows:
![lab0_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f872f99b-7405-416d-b615-515ab58adf85)

![lab0_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/450fea42-ca8f-4a12-ab05-c803aa1ee0c0)

#### SPICE simulations
- The SPICE deck needs to be created before simulation. The SPICE deck is the connectivity information about the netlist, inputs provided, tap points to view outputs.
The SPICE is created by defining component connectivity, component values, identifying the nodes and naming them.
- A substrate is a potential component/pin that needs the connectvity information. The substrate tunes the threshold of NMOS and PMOS.The substrate pin direction varies between NMOS and PMOS symbol.
The value of output load capacitance is obtained with huge computational analysis.
- The component value needs to be defined for PMOS and NMOS i.e., W/L values(0.375u/0.25u). Let us assume same value although PMOS should be twice in size to NMOS. The output capacitance say 10fF.The applied gate voltage is usually considered multiple of channel length, say 2.5V. A node is defined when a component is placed between two nodes.

The netlist is defined in a fashion of drain, gate, source and substrate.
The definition of a component is as follows:
```cdl
M1 out in vdd vdd pmos W=0.375u L=0.25u
M2 out in 0 0 nmos W=0.375u W=0.25u
cload out 0 10f
Vdd vdd 0 2.5
Vin in 0 2.5
```
- Here, M1 is the component name and PMOS is the type of component and W/L values are defined. Here, the out is connected to drain and in is connected to gate.
- The substrate and source of PMOS are connected to supply and that of NMOS are connected to ground.
- The load capacitance is connected between out port and ground and the value is 10fF. Similarly, the supply voltages are connected between groud and respective nodes and the voltage is 2.5V.

The simulation commands are 
```cdl
.op
.dc Vin 0 2.5 0.05
```
This command implies that gate voltage is varied from 0 to 2.5V in steps of 0.05V. This is done to note the output characteristics with respect to input voltage.
The model file must be described as follows that contains the complete model description of NMOS and PMOS of the length.
```cdl
.LIB "tsmc_025um_model.mod" CMOS_MODELS
.end
```

The SPICE simulation is done as follows:

The above netlist is written out in cmos_inv.cir and fired run. After setting plot, it gives options as op1, dc1. As the dc transfer characteristics are to be plotted, dc1 is given. The display command displays the voltages present in design. After plot command, we get the graph.
```
source cmos_inv.cir
run
setplot
dc1
display
plot out vs in
```
Now Let us simulate another inverter with PMOS width varied to 2.5 times of NMOS i.e., 0.9375um.
The output of these both simulations are as follows:
![graph](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e330da7c-3773-419b-b15d-cec92bc3ab66)

The CMOS inverter is a robust device, though size is varied, the switching waveform is same. The robustness is evaluated with some characteristicis such as switching threshold, noise margin.
#### Switching Threshold
The switching threshold is the point where Vin is equal to Vout. When a tan 45 line is drawm from origin, the point that intersects the output is the threshold value. It is the point where both PMOS and NMOS turn ON. If both turned ON, high leakage will be present.
![graph2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1b5e8f90-5d26-41cd-945d-e7f499e28350)

The operation of PMOS and NMOS in an inverter is as follows:
![new](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/743208da-b9c0-4563-8410-7bab60d055f5)

Here, the gate voltage and output voltage are same. The current flowing from PMOS to output capacitor and capacitor to NMOS are almost same. So, ```VGS=VDS``` and ```Idsp=-Idsn```.

Let us now do the dynamic simulation of the CMOS inverter. The netlist written is as follows:
```
M1 out in vdd vdd pmos W=0.375u L=0.25u
M2 out in 0 0 nmos W=0.375u W=0.25u

cload out 0 10f

Vdd vdd 0 2.5
Vin in 0 0 pulse 0 2.5 0 10p 10p 1n 2n

**SIMULATION Commands**
.op
.tran 10p 4n
*** .include mosis_1um_model.mod ***
.LIB "tsmc_025um_model.mod" CMOS_MODELS
.end
```
The input signal defined is it starts from 0V and ends at 2.5V and shift is 0 and rise time and fall time of 10ps and ON pulse width is 1ns and period is 2ns. So, The duty cycle is 50%.
The simulated transient waveform is as follows:
![graph3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/69cdb634-6243-4074-ae4b-cecf65860fca)

Clone the vsdstdcelldesign as follows:
![lab0_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5ac76c59-0472-496a-9c10-8266b2c7e567)

The magic command gives the following inverter as shown:
![lab0_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/924db0c5-4a7b-44d5-b9a2-8f0cc8a231fb)

</details>
<details>
<summary> CMOS Fabrication Process</summary>
<br>
	
The 16-mask process is

1. Selecting a Substrate
 A substrate is on which the whole design is fabricated. The GDSII is fabricated on to a substrate. There are various kinds of substrates available.
The most commonly used substrate is P-type silicon substrate. It has the folowing properties:
- High resistivity (5-50 ohm)
- Doping level (10^15/cm3)
- orientation (100)
 A substrate doping should be less than well doping. A well is used to fabricate NMOS and PMOS seperately.
2. Creating an active region for transistors
  Active region is wher PMOS and NMOS cells are there on a substrate. These are like pockets created on p-substrate. An isolation must be created between these pockets.
- A Silicon dioxide layer is grown, that acts as an insulator(of ~40nm thickness).
- Next, deposit a layer of silicon nitrite (~80nm of Si3N4)
- To create the wells, the silicon nitrite layer is covered with a photoresist (negative or positive film seen in camera) layer of ~1um. A layout is a mask in fabrication terms.
![step1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a844f749-0838-4703-9ce0-92fa8d53c734)
  
- These masks act as protecting shields for the photoresist below them and the UV light is passed through the substrate. So, the area below mask is left and the remaining photoresist is gone. Now, The extra resist exposed to UV light is washed away with a developing solution. Now, the masks are removed
- The silicon nitrite is etched. The photoresist is now removed, as silicon nitrite acts as protection, to grow other layers. The photoresist is removed chemically.
- The substrate is placed in an oxidation furnace, that grows second level of oxidation lyer. The area under silicon nitrite is protected and oxide is grown on exposed area.
- Now, the area at which the transistor is formed is isolated from one another. The field oxide is grown. This process is called LOCOS.(Local Oxidation of silicon)
![step2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e84b56f2-2afe-4791-9537-cc7819c20910)

- The Silicon nitrite is stripped off using hot phosphoric acid. A strict electrical isolation is created between NOS and PMOS.
3. N-well and P-well formation
The P-well is used for NMOS fabrication and N-well is used for PMOS fabrication.
- A photoresist layer is deposited and define the pattern of layers to be protected.
- A part  of the substrate is masked and exposed to UV lightand washed away with solution.
- A p-well is created using boron. The boron is diffused into p-type substrate using ion-implantation. The energy needed to diffuse boron through the oxide layer is ~200keV.
- Similarly, the other part is masked now and covered with photoresist and masked, etched. Now, phosphorous is diffused through oxide layer with an energy of ~400keV using ion-implantation.
- The wells are created but they need o be diffused such that they occupy half of the substrate area.
- Now, the substrate is taken into a high temperature furnace (driving furnace) of ~1100c forming clear wells. This is known as twin-tub process.
![setep3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0ab536ac-9f48-485f-8617-56bad3985c7c)

4. Formation of Gate terminal
 Gate is an important terminal of PMOS and NMOS that controls the threshold voltage. The threshold voltage is the turning ON voltage of transistor.
Threshold voltage is dependent on body effect co-efficient, inturn doping concentration and oxide capacitance.
So, these variables are controlled while fabrication such that required threshold voltage is obtained.
- Again the new mask is placed, etched and the boron is diffused with less energy of ~60keV such that this diffuses to the edge of surface.
- The Mask is used for N-well, and etched and the n-type material is diffused with less energy such that it lies beneath the top of surface.
- The oxide is damaged due to implantation and penetration of p-type and n-type dopants through it. The original oxide is etched using hydroflouric acid solution.
- The oxide is regrown again to give high-quality oxide (~10nm thin). This thickness is controlled to obtain desired threshold voltage.
 ![step4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/63bd4f82-9feb-4e0a-8621-e7020dd1d462)

  The gate formation is done by
- Deposit a polysilicon layer of 0.4um. The gate area needs to be of low resistance. The layer is doped with impurities such as phosphorous or arsenic.
- Again, deposit a photoresist and gate mask is used and etch away extra exposed layer and photoresist is removed forming the gate terminal.
5. Lightly Doped Drain (LDD) Formation 
The doping profile for PMOS in n-well are P+, P-, N. The doping profie for NMOS in p-well are N+, N-, P. We need the variation (of +,-) in the doping profile due to
- Hot electron effect
  When device size reduces, the electric field increases as power supply is not changed.
  - The high energy charge carriers break Si-Si bonds leading to more elctron flow which is undesirable as the doping profile is maintained.
  - The energy might be high that it crosses the 3.2eV barrier between Si conduction band and SiO2 conduction band. If it crosses, it might enter into oxide layer, which is just above the surface creating liability issues.
- Short Channel effect
 For short channels, the drain field penetrates tthe channel. In other words, As the channel length reduces, the gate voltage applied is directly injected into the device loosing control over the current flow in it.
![step5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/567d6912-eed3-403a-9303-770e6a8e76b0)

The process to generate LDD structure is
The mask7 is used on the photoresist. It is exposed to UV light and etched, washed. The phosphorous is diffused with energy such that it is implanted just beneath  the surface. N+ means heavily doped concentration and N- means lightly doped concentration. The gate avoids phosphorous entering beneath it.
Similarly, the mask8 is used on photoresist and then the boron is diffused with energy such that it is implanted just beneath  the surface. 
The whole layer is covered with SiO2 or Si3N4.
The Plasma anistropic etching is a directed etching that removes the oxide except that on the side walls of gate. The side-wall spacers help us to keep the lightly doped areas more intact.
![step6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/56f43e45-0638-4abc-8cba-25fde9952009)

6. Source and Drain formation
A thin layer of screen oxide is added to avoid the effect of chanelling. It is added to randomize the  direction of ions.
Channeling effect occurs when the vector velocity of ions matches with the crystalline structure of p-type substrate, the ions mightgo deeper into the substrate without hitting any silicon atoms.
Now, tha mask 9 is used with the photolithographic process forcovering n-well and mask 10 for p-well. The P+ areas are formed below the surface in the N well region and N+ areas are formed beneath the P well region.
![step7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4553573b-f85d-4381-b892-7bd2bd3ff311)

The lightly doped drain areas are still intact and the boron(~50keV) and arsenic (~75keV) are diffused into n-well and p-well respectively.
8. Contacts and local interconnects
First, remove the thin screen oxide using HF solution. The oxide layer is etched to form the interconnects
- Deposit titanium on wafer surface using sputtering. When titanium metal reacts with argom gas, the titanium ions moves from the metal surface to the surface of substrate.
-  Then, Wafer is heated at about 650-700c in nitrogen ambience.The lowresistant TiSi2 gets deposited all over the surface that can be used for local interconnects.
-  The mask 11 is used to create the gaps to draw interconnects to top.The extra TiN is etched by RCA cleaning. The RCA solution consists of deionized water, hydropgen peroxide, ammmonium hydroxide.
![step8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ff3c1371-06db-490b-a84e-9b3e7d8932c7)

8. Higher level metal formation
   The surface topography is not planar. Inorder to planarise it, we deposit a thick SiO2 layer doped with phosphorous or boron. The chemical mechanical polishing is used for planarizing the wafer surface.
   The contact holes are drilled using the photolithographic process with mask 12. The holes are drilled and mask is removed.
   A thin layer of TiN is grown, as it acts a good adhesion layer for SiO2 and as goold barrier between bottom and top interconnects. A blanket tungsten layer is deposited and on which an aluminium layer is deposited. The mask13 is used on the aluminium layer to form metal contacts with photolithographic process.
![step9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/59ec4a44-72e2-4b38-aec9-a8f16d41cbd4)

   The SiO2 is deposited again and holes are created with mask14 with photolithographic process and TiN layer is deposited.
   The mask15 is used to define the pattern again above this second tungsten layer. The thickness of metal layer is increased from bottom to top.
   The mask 16 is used to drill open contact holes in this layer.
![last](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/63b145c1-8b0d-4e08-8a0f-e9de47c21ac5)


#### Lab
   When a poly crosses n-diffusion, it is NMOS. When a polysilicon crosses p-diffusion, it is PMOS.

The magic command gives the following inverter as shown:
![lab0_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/924db0c5-4a7b-44d5-b9a2-8f0cc8a231fb)

The layer can be selected by clicking S and giving what command tells you about the shape selected as follows:
![lab0_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/19ba801b-ef31-4dab-8bb8-bf2a23188e6c)

![lab0_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a7f6a4b0-6444-48d5-9cb6-f118b7de013d)

Clicking S thrice by placing cursor on any shape, will highlight the connected objects to that shape as follows:

The output port is connected to NMOS and PMOS as follows:
![lab0_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3719a64e-0dab-48f4-9e1e-f8a3bebfe17f)

The source of PMOS is connected to powersupply.
![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9444ef9e-73eb-40a8-ace5-49d1cae7893a)

The drain of NMOS is connected to Ground.
![lab1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1095bfe1-7b02-4577-8ab3-9b9c401ca86c)

When a box of the mask is deleted, it shows a drc error due to discontinuity.
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a8d34297-1a87-4bad-b8a9-3f0123edab79)

The color palette on right shows the different metal layers available. 
</details>

<details>
<summary> Labs with magic</summary>
<br>

Inorder to extract the spice deck file, open tkcon window and execute the following commands:
```
extract all
ext2spice cthresh 0 rthresh 0
ext2spice
```
![lab1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9155086a-1f4c-45e8-bfdd-f428288048ec)

![lab1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/99efa887-e046-421c-a80e-5ba394f35dea)

The contents of pshort.lib are as follows:
![lab2_1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a9aa6f2f-72a3-427a-95ce-f67380683ca7)

This creates a spice file with .spice extension and .ext extension file. The SPICE file is now edited and a netlist is written in it as follows:
![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b23277bf-4cf1-413e-82dc-d79a5d0f574c)

 Now, the ngspice is installed and the ngspice is simulated as:
 ```
sudo apt install ngspice
ngspice sky130_inv.spice
```
![lab1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/75b79ccf-6845-4cb2-8f3d-1907821a4f2c)

The circuit is simulated and output is plotted as follows ny command:
```
plot y vs time a
```
![lab1_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/33d12c00-2128-48fe-9c18-e9880738059a)

The load capacitance is high forming spikes at the peaks so let us increase cload to 2fF. The output simulsted is as follows:
```
C3 Y 0 2fF 
```
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2f4c098f-f6b6-4fe6-900f-2199178c8a47)

The rise time and propagation delay can be calculated by obtainig the points as below:
![lab2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5079c24c-e01e-4238-b1e2-4ae103c4cdab)

```
Risetime = 2.182ns - 2.067ns = 0.115 ns or 115ps
Rise delay = 2.207ns - 2.151ns  = 0.056 ns or 56ps
```
#### Labs on magic DRC

First we copy ```drc_tests.tgz``` file from open_pdks in ```opencircuitdesign.com```. This zip file is unzipped using tar command. It contains various .mag files of layers such as met2, met3.
![lab3_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/58cc939a-5cee-4ea4-a26f-791baabf14da)

The contents of .magicrc are as follows:
![lab3_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e49b31e7-94d1-4216-9a2a-f3a9a8e1367a)

Now, the met3.mag file is loaded after opening an empty magic window using command:
```
magic -d XR
```
![lab3_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cd48d775-0c9d-4b85-8141-6ef9d7ac68c9)

The various drc errors are present on each box. This can be viewed by selecting a box and ```drc why``` in tkcon window.
![lab3_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c88d4f9d-aa8a-4740-b59e-b7abe91bf57d)

The following image shows the drc error in metal 3.2
![lab3_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fe9384dd-d1e3-4ac2-9988-b91c4111edb5)

The following image shows the drc error in metal 3.6 
![lab3_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9c9e3628-1e27-4fe2-b186-b19165da172f)
As the 3.4 rule is not visible, it is visualised by selecting the location and filling it with metal3 layer
![lab3_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c5a269e6-74ac-429f-8c91-b5de547219c5)

Now, using the command the vias are viewed in the rule.
```
cif see VIA2
```
![lab3_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/27aabacc-7992-4f6f-802e-df968cb4a3b6)

Now let us load poly.mag
![lab3_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b44acf88-b035-44e0-b1f3-0658cdc62b21)

The poly.9 has an error as shown. The vertical layer and horizontal layer are npolyres and npoly respectively. The spacing between these resistors is as follows:
![lab3_10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/27bcf00f-dc11-4f9f-af58-cc453ce9413f)

Inorder to remove the error, let us check poly.9 in sky130A as follows:
![lab4_1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/528b01d6-ea91-4c6c-844a-11ea3b0bc2d9)

Let us check for aliases used
![lab4_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fab2e5a5-0803-4698-bf47-dd5b91298c9d)

The diffusion layers are changed from ```alldiff``` to ```nonpolyres```
![lab4_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ab7da8a9-01f4-4496-a1d3-a947f5dea23b)

![lab4_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f234a766-6975-4a69-b4e7-a0a2dbb9a815)

Now, the sky130A.tech is loaded and there is no drc error as shown.
![lab4_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5cb2ef0f-1430-4c83-93bd-22b9b8c7a9c1)

The other violations are
- Copy the 3 poly metal and paste it into 2 different places and add pmos and nmos substrate and contact. This is to fix the issue with poly resistor spacing to diff and tap
![lab2_1_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/04d21bed-5365-46fb-ad3b-15e0a6bba450)

Now you change it back to alldiff in the poly.9 as follows:
![lab2_1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cf4f4220-f3de-4d1a-a01a-6e96958d3662)

The other drc error is as follows:

![lab2_1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/679edf4f-f3b7-4947-ab34-236b4d96a0fd)

![lab2_1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c8cd88d7-761c-4669-9944-8413bbd547f1)

All n-wells contain metal contacted tap. This is viewed as error in nwell.4
![lab7_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ca95020e-3f18-45ac-924f-65091be82106)

![lab7_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7003e912-1204-48b8-98cc-8925a51fe4e8)

![lab7_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e0e0c302-4ec3-4f62-8e83-68a50608842f)

![lab7_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a61b2b09-f042-44d9-a380-121aa2f49dda)

![lab7_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1ff25643-c0a9-4e13-90b9-eefb602d19d6)

</details>

## Day 18 : Pre-layout STA aqnd importance of good clock tree
<details>
<summary>Timing Models using delay tables</summary>
<br>	

OpenLANE is a place n route tool. It does not require the mag information. It only requires, the pr boundary (inner box), power, ground, input and output ports information.
The lef file contains only this information required.

The guidelines for standard cell height are:
- The input and output ports must lie on the vertical and horizontal tracks.
- The width of the standard cell must be odd multiples of track pitch.
- The height should be multiple of vertical pitch.

The tracks are used during the routing stage. Routes are metal traces. The routing is specified through tracks.
The following image shows the tracks.info contents as follows:
![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f02f51ac-d4fc-4115-9693-af10fa71eea1)

The first line says the horizontal track has an offset of 0.23 and pitch of 0.46. Every metal layer has X(horizontal) and Y(vertical) direction.

The grid mode can be activated as follows.These are the reference for drawing a layout.
![lab1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5897e336-e11f-4678-90f2-aefba63619af)

The grid command needs an x spacing, y spacing, x origin, y origin. As the grid is being defined to check the alignment of input and output ports, the li1 is used as reference.
So, the grid view is as follows.
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/08b7709c-7063-4f1e-b25d-68f1b227359e)

The ports are at the intersection of horizontal and vertical tracks ensuring route can reach from one to another.
The PR boundary is the layer that the place and route tools will use for placing the cells next to each other. The standard cell PR boundary takes 3 boxes horizontally and 8 boxes vertically.
![lab1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5133a3fe-528a-4f9e-a4e1-fdb1bec31515)

The port information is not required by magic, but required for lef files. These ports, when extracted are defined as pins of macro. 

A port can be defined by selecting it, and giving the values as follows:
![lab2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6de35888-f19b-4a54-a912-454cfacfb0dd)

Port enable number defines the order in which the port is defined in lef.

The valid classes are default, input, output, tristate, bidirectional, inout, feedthrough, and feedthru. Valid uses are default, analog, signal, digital, power, ground, and clock. These attributes are set in tkcon window as follows:
![lab2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6caf551f-9a2c-4d31-a009-bee16bca1f67)

![lab2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/49690918-2422-438b-b3e0-7b7ad1a84f0c)

Now, save the mag file using the command:
```
save sky130_invusha.mag
```
![lab2_15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3f9126e4-95e3-46d3-a4cb-742978fb98e7)

The ```lef write``` creates the lef file with the name same as cell name.
![lab2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2fa19d7c-8baa-4193-8377-9ca47c565f68)

The contents of the lef file created are as follows.The ports are defined as the pins in the lef.
![lab2_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7b5dad88-3416-4897-b7b3-425be8d60600)


The lef, libs that contain cell information are copied to src directory in designs/picorv32a. The information present in libs are as follows:
![lab2_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f9c50c88-0a12-415d-b986-ba6385616b13)

![lab2_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/26920572-f829-403e-b010-22140d9fd5cf)

![lab2_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/905c8839-cd4f-4ad1-b136-acda593274de)

The cofig.tcl is edited as follows:
![lab2_10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6571d487-6848-4c7f-ade8-738c8c18a7d8)

Now, invoke the docker and open lane as follows:
![lab2_12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8f8292a7-9ac7-495f-8165-4664c577e749)

The following commands are added inorder to ensure the inverter lef is included to the flow.
```
% set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
% add_lefs -src $lefs
```
![lab2_13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5ab96ea8-1573-4ef6-ac77-7bb2c27f3511)

Now, the synthesis run is fired using the following command.
```
run_synthesis
```
![lab2_14](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f2da6490-8acc-4dfc-b595-1a3a39544451)

Clock gating is a technique that restricts the clock to propagate under specific conditions.

The AND gate acts as clock gate that is the other input decides whether it propagates the clock to the clock tree or not. The AND gate with input connected to 1 and OR gate with input connected to 0 can act as **clock gate**.
The advantage is that the short-circuit power is saved during the dynamic switching time.

The following clock tree is usually used for splitting load at the driver. The buffer can be swapped with a gate as follows.
- The clock tree has levels of buffering and identical buffers(of same size) are present at same level
- The load/fanout is same at each level.
![screen](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/27047de1-c798-4622-b548-b3c7f83f6ef6)

The delay tables act as timing models of the cell. The delay table is a two-dimensional table, function of input slew and output load.
A cell is characterized for range of input slew and range of output load values. The delay values vary with the size of cell also. This can be considered as a new cell with different specifications that is either slow or fast depending on requirement.
![screen2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2c8f9bce-9f2e-496f-bd85-35b7c8e329dd)

When the required delay is not present in table, but lies within the intervals of specified values, there are various techniques to deduce the equation and find out the delay value. This can be called interpolation.

The latency at endpoints will be the sum of the delays of each individual cell in that path.
The total skew value between two endpoints will be non-zero if the output load driven for a cell is varied, meaning different delay numbers are seen between endpoints, this is why it is preferred to have the nodes at each level driving the same load.
This non-zero skew might lead to setup and violations.
Inorder to retain the skew to be zero in the presence of variable load,it is done by using a different buffer size at the same level that can achieve the same level of delay as the other buffer in same level based on its delay table.
Power aware CTS needs to consider the active and inactive parts in the design. The clock need not be propagated in the parts where it is inactive for sometime and later propagated.

These are the various switches present in the configuration/README.md file.
- SYNTH_STRATEGY: control the area and timing
  The ```SYNTH_STRATEGY``` variable is set to DELAY 0 i.e., it optimizes the timing of the design with a trade-off of area.
- SYNTH_BUFFERING: control if we want to buffer high fanout net
  The ```SYNTH_BUFFERING``` set to 1 ensures usage of cell buffer on high fanout cells to reduce delay with high capacitance loads.
- SYNTH_SIZING: control in cell sizing instead of buffering
  The ```SYNTH_SIZING``` when set enables cell sizing where cell will be upsized or downsized as required to meet timing.
- SYNTH_DRIVING_CELL: ensure more drive strength cell to drive input
  It is the cell used to drive the input ports and is vital for cells with a lot of fan-outs since it needs higher drive strength.
![lab2_16](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f9b2850d-429f-4435-bc55-5028ebb6e047)

These variables are defined in the flow as follows:
![lab2_18](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/236c33c1-98eb-4084-bb8f-55ac30dddbe1)

The previously dumped netlist is removed, as it is popping a message that synthesis is skipped as the netlist exists. 
After the ```run_synthesis``` command, the design is much optimized such that the worst negative slack (WNS) and total negative slack (TNS) are zero as follows.
![lab2_19](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3bef1077-a1be-4c54-ac1a-12183d839ffc)

The cell created is in the list as follows:
![lab2_28](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3f6e3c65-4eb3-426c-b322-019b0dbe5a41)

The contents of merged.lef in the runs are as follows:
![lab2_21](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9bd8e3eb-3fde-4125-9720-129772d6f099)

The following command is used to run the floorplan.
```
run_floorplan
```
![lab2_20](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/40132430-7bb5-4d45-9d0c-1f584e9bb26e)

This error implies that run is exited while executing ```or_basic_map.tcl```. This happened after the macros being called.  The path of these files to be commented are as follows:
![lab2_26](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b0dc85a1-52dd-4a34-981a-c0d8e9d30012)

So The command that calls macro_placement is commented as follows.
![lab2_23](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d75c791f-5af0-4d69-b792-084cd5e215f8)

Again, In the floorplan.tcl, it calls for global_placement or macro_placement. So, this is also commented as follows:
![lab2_22](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aec04cbe-0701-40f6-9f86-b81ce7a8e4bd)

Now, the floorplan run is successfully done as follows:
![lab2_24](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/81767515-b3ab-4e0f-8cc7-fc523160727b)

The following command is used to run the placement.
```
run_placement
```
The placement run is completed as follows:
![lab2_25](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5cae3bfc-276c-4eef-8e70-7f0f17105b78)

The def created after the placement is as follows:
![lab2_27](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7d0af394-d9b6-40bd-a728-070377ff498a)

After giving ```expand``` command in the tkcon window, the metal layers railed are as follows:
![lab2_30](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8eeea7f7-2954-462a-b46f-6995751f35d5)


</details>
<details>
<summary>Timing Analysis with ideal clocks using OpenSTA</summary>
<br>	

Ideal clock means the clock is not built (pre-cts stage). Let us consider the setup analyis with a single clock specifying theclock to be 1GHz (period=1ns).
Inorder to avoid setup violation, the sum of internal delay of launch flop and combinational delay should be less than the time period of clock.

Let us say that the clock at launch arrives at 0ns then the data takes a time of clock period to arrive at the capture flop. When the internal delay of a flop is considered, the capture flop also takes some time to produce output for propagated input. So, this internal delay is called setup time.
![dsk2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2820f176-9a5e-4ce2-b05d-f6944e750071)

The setup uncertainty is usually caused by the clock jitter, this makes the delay available for the path more stringent. The clock jitter is the uncertainty that causes delay in the clock that needs to reach at 0ns (to 0.1ns). This is usually caused due to the variations of the clock source. 
![dsk2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9cd020de-1a01-425e-99d0-97a155bc2e7a)

The combinational delay of a path involves the cell delays and net delays in the path aws follows:
![dsk2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ef645dd0-f260-4cc0-8ae7-55c077deb869)

The STA is usually done with PrimeTime (SYnopsys)tool. The timing analysis here is done using OpenSTA. Let us go to the openlane flow directory and create a file as follows:
```
cd ~/Desktop/work/tools/openlane_working_dir/openlane
gvim pre_sta.conf                               \\for pre-layout STA i.e., with ideal clock conditions
```
The contents of the pre_sta.conf are as follows:
```
set_cmd_units -time ns -capacitance pF -current mA -voltage V -resistance kOhm -distance um \\units are defined
read_liberty -max /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib \\liberty file for max(setup) delays

read_liberty -min /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib \\liberty file for min(hold) delays

read_verilog /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-10_12-49/results/synthesis/picorv32a.synthesis.v

link_design picorv32a

read_sdc /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/my_base.sdc
report_checks -path_delay min_max -fields {slew trans net cap input_pin}
report_tns
report_wns
```
![lab2_31](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/398b82c6-2ea6-4217-aaa6-9f84bbe2d433)

The netlist file is written at synthesis stage and then at CTS stage, but not at floorplan and placement stage. As the clock buffers are inserted at the CTS stage, the netlist is being changed, thus new netlist written out.

The contents of my_base.sdc is as follows:
```
set ::env(CLOCK_PORT) clk 
set ::env(CLOCK_PERIOD) 12.00
set ::env(SYNTH_DRIVING_CELL) sky130_inv_usha 
set ::env(SYNTH_DRIVING_CELL_PIN) Y 
set ::env(SYNTH_CAP_LOAD) 17.65 
create_clock [get_ports $::env(CLOCK_PORT)] -name $::env(CLOCK_PORT) -period $::env(CLOCK_PERIOD)
set ::env(IO_PCT) 0.2
set input_delay_value [expr $::env(CLOCK_PERIOD) * $::env(IO_PCT)]
set output_delay_value [expr $::env(CLOCK_PERIOD) * $::env(IO_PCT)]
puts "\[INFO\]: Setting output delay to: $output_delay_value" 
puts "\[INFO\]: Setting input delay to: $input_delay_value"
 
## set max fanout S::env(SYNTH MAX FANOUT) (current design)
set clk_indx [lsearch [all_inputs] [get_port $::env(CLOCK_PORT)]]

#set rst indx [isearch (all inputs) Iget port resetn]]
set all_inputs_wo_clk [lreplace [all_inputs] $clk_indx $clk_indx]

#set all inputs wo clk rst (treplace sall inputs wo clk srst indx Srst indx] 
set all_inputs_wo_clk_rst $all_inputs_wo_clk

# correct resetn
set_input_delay $input_delay_value -clock [get_clocks $::env(CLOCK_PORT)] $all_inputs_wo_clk_rst

# set_input_delay 0.0 -clock [get clocks S::env(CLOCK PORT)] (resetn)
set_output_delay $output_delay_value -clock [get_clocks $::env(CLOCK_PORT)] [all_outputs]

# TODO set this as parameter
set_driving_cell -lib_cell $::env(SYNTH_DRIVING_CELL) -pin $::env(SYNTH_DRIVING_CELL_PIN) [all_inputs]
set cap_load [expr $::env(SYNTH_CAP_LOAD) / 1000.0] 
puts "\[INFO\]: Setting load to: $cap_load" 
set_load $cap_load [all_outputs]
```
The pre-sta is run by using the following command:
```
cd ~/Desktop/work/tools/openlane_working_dir/openlane
sta pre_sta.conf
```
The following reports are generated showing the least positive slack as follows:
![lab2_33](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c0f05a5a-c956-4adf-9863-4e801df6e62f)

![lab2_35](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4daa1fcd-d21e-4ef1-b4dc-9be3767e38a0)

The hold is insignificant because the clock tree synthesis is not done yet. As skew is assumed zero, the hold is optimistic.
Let us reduce the fanout, so the delays of the design are more optimized. The variables to be set are in README file as follows:
![lab2_34](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/cfde8d9b-5f2a-4e10-875b-36690b6e6b75)

Now, we set the fanout to 4 using the following command. 
```
echo $::env(SYNTH_MAX_FANOUT)
set ::env(SYNTH_MAX_FANOUT) 4
```
Now, remove the synthesis netlist again and fire the synthesis run and subsequent stages as follows:
```
run_synthesis
run_floorplan
run_placement
```
Now the sta is again checked for as follows:
```
sta pre_sta.conf
report_net -connections _16837_
```
The report_net command is used to check all the connected inputs, outputs and nets as follows.
![lab2_36](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c3d330eb-d94d-4f22-8741-a0722c6d5980)

The buffers can be upsized using the ```replace_cell``` command. Upsizing the  cell improves transition, thus reducing cell delay.

The following command is used to check the report of timing path as follows:
```
report_checks -fields {net cap slew input pins} -digits 4
```
![lab2_37](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/613cf3a8-bee6-41b9-bf95-70f0ffa68c66)

![lab2_38](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1cf55293-3ffc-412c-abe0-40806e3216ba)

A timing ECO is generated and fed to the PnR tools once the timming is met.

</details>
<details>
<summary>Clock Tree Synthesis and Signal Integrity</summary>
<br>	

The time difference required by clock to reach the launch and capture flops is referred as skew. Skew should be as minimal as possible.
![dsk3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/96a72ca1-8015-4eda-b071-0ad039e210f6)

#### H-tree algorithm
The tool calculates the distance from the clock port to all the clock points that needs to be connected to that port. The clock is routed to the midpoint of distance and then, to the midpoint of the nearby flops and so on. This midpoint procedure makes the skew almost zero, or as minimal as possible.
![dsk3_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0bc660c8-deb9-4603-9dbb-8ec65e312deb)

#### Clock Tree Buffering
The clock repeaters have equal rise and fall delay and the datapath buffers do not have equal rise and fall delay. The cells are connected with wires that have some resistance and capacitance. The long length wires causing more transition and more net delays. So The buffers are added inorder to break these long length nets.
![dsk3_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e3513cd4-0719-4fc8-bf99-cd9ad9d6188d)

#### Clock Net Shielding
The clock nets are encapsulated from the external world to avoid any coupling between other wires and clock net causing glitch or crosstalk.
The shield can be connected to ground or to Vdd, as long as there is no switching activity occurring. Critical data nets are also necessary to be shielded.
The unshielded nets can interact with other and act as capacitor causing ground bounds or voltage droop (glitch). This may impact the logical performance of the design.
![dsk3_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c0bd3d22-e9b1-4dd0-9b5f-78fd6538486e)

When both agressor and victim are switching as follows, the agressor impacts the victim such that it charges instead of discharging for certain time, increasing the cell delay.
![dsk3_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5993b389-8474-4b78-bba8-c6d93fab7180)

#### Lab
The netlist is written out, after the STA using OpenSTA using the following command:
```
write_verilog ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-10_12-49/results/synthesis/picorv32a.synthesis.v
```
So, The pre-existing netlist of the synthesis stage is usually overwritten with additional buffers to meet the timing. As there are no aditional buffers required, same netlist is being used.
Now, thwe synthesis netlist is generated and timing is met. Let us continue with the consecutive steps as follows:
```
run_floorplan
run_placement
run_cts
```
![lab2_39](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2a25af30-bba0-4061-92a1-7c4963846c32)

This completes the successful clock tree synthesis as follows:
![lab2_40](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a9002b79-cd89-40ef-aadd-aa2d00778b42)

Each stage in PnR has the relative .tcl files in openroad. The files for CTS are or_cts.tcl and cts.tcl.
The contents of cts.tcl are as follows:
![lab_41](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c7c002e2-87e3-4436-abd2-fbcd72e89b1b)

The contents of or_cts.tcl are as follows:
![lab2_42](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a6d0d83b-a0d0-4cc6-a6af-8cab3d62109c)

Let us check the following variables defined in openlane.
```
echo $::env(LIB_TYPICAL)
echo $::env(CURRENT_DEF)
echo $::env(CTS_MAX_CAP)
echo $::env(CTS_CLK_BUFFER_LIST)
echo $::env(CTS_ROOT_BUFFER)
```
![lab2_43](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d0f2d595-0922-4e18-96cc-faae93b90bc7)

The value of capacitance can be checked in typical.lib as follows:
![lab2_44](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d7980c53-fd04-4740-abcd-95bf733d927b)

</details>
<details>
<summary>Timing Analysis with real clocks using OpenSTA</summary>
<br>	

Due to addition of clock buffers, clock network delay has been introduced and it will combine all the delays.With real clocks, we will need to have buffers inserted into the clock path to ensure the clock signal integrity.Because of the buffer insertion, the clock edge will reach the clock pin with consideration to the delays of the buffers inserted.

The clock network delay will also need to take into consideration the delays from the buffers inserted.The window will become shifted as a result of the delays from the buffers inserted.
The skew for this design will now be the difference between the deltas, and the equation for setup timing analysis will also changed based on the image shown.If the data arrival time is higher than the data required time, then we will have negative slack on the path, meaning we have violations.
![dsk4_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3086186c-8b59-4513-bd99-cd4a52b5eb27)

For hold timing analysis, where the capture edge is on the 0 clock rise edge, the combinational delay should be greater than the hold time of the flop.
Hold time refers to the second mux delay, which is the time required for the data to be sent after the clock edge within the flop.
So the data needs to be arrived after the hold time, so the new data can be captured into the flop, after existing data is launched out.
![dsk4_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d612f1f8-32a5-40b4-aaaa-69d8486731c7)

Jitter for the launch clock and capture flop will not need to be taken into consideration as the design is on the 0 clock edge, and the arrival difference for the capture and launch flop will be the same.
So, the uncertainty should be kept low for the hold analysis.

 slack = data arrival time – data required time
 
If data required time is higher, we will have negative slack, meaning the timing path for hold will be violated.The equations for setup time and hold time are as follows:
![dsk4_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/17825368-38b6-4195-a990-656cf90fc4b2)
#### Lab
The following steps are executed after CTS stage.

In openroad, the timing analysis is done by creating db using the lef and def files. The lef and def are read and the db is written out as follows. Now, the db is read and the steps are same as in conf.
```
openroad                                                                          \\Invoking openroad
read_lef /openLANE_flow/designs/picorv32a/runs/13-01_14-09/tmp/merged.lef
read_def /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/cts/picorv32a.cts.def
write_db pico_cts.db
read_db pico_cts.db
read_verilog /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/synthesis/picorv32a.synthesis_cts.v
read_liberty -max $::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd_slow.lib
read_liberty -min $::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd_fast.lib
set_propagated_clock [all_clocks]
read_sdc designs/picorv32a/src/my_base.sdc   \\calculates actual cell delay in clockpath
report_checks -path_delay min_max -format full_clock_expanded -digits 4
```
![lab2_45](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6645dacf-fb99-478e-9c9f-2eabf9a8f25d)

![lab2_47](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ad849cea-8c25-4f00-841a-83880f52c0e7)

![lab2_46](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3cca809c-1e88-406b-a39a-282fb10e96b0)

The above analysis stands incorrect because the design is defined for typical corner and the libs for analysis are min and max. So, the correct way of analysis is as follows. Now, the same steps are follwed but the liberty file used is typical corner.
```
exit        \\Exit openroad...Do it twice if read_sdc command doesn't work
openroad
read_db pico_cts.db
read_verilog /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/synthesis/picorv32a.synthesis_cts.v
read_liberty $::env(LIB_SYNTH_COMPLETE)
link_design picorv32a
read_sdc designs/picorv32a/src/my_base.sdc
set_propagated_clock [all_clocks]
report_checks -path_delay min_max -fields {slew trans net cap input pin} -format full_clock_expanded
echo $::env(CTS_CLK_BUFFER_LIST)                              (To see the list of buffers)
```

![lab2_48](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/360475aa-78b5-441d-9b11-cee5dcf97842)

![lab2_49](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b5561ad9-6f85-4a59-860c-ed7646c52295)

![lab2_50](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/689cc6cc-00b2-496d-9753-8fa0357579b0)

```
exit 
echo $::env(CTS_CLK_BUFFER_LIST)
set ::env(CTS_CLK_BUFFER_LIST) [lreplace $::env(CTS_CLK_BUFFER_LIST) 0 0]
echo $::env(CURRENT_DEF)
set ::env(CURRENT_DEF) /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/placement/picorv32a.placement.def
run_cts
```

![lab2_51](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6532eeec-1507-4c82-a8d6-cd29d6400853)

```
openroad
read_lef /openLANE_flow/designs/picorv32a/runs/13-01_14-09/tmp/merged.lef
read_def /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/cts/picorv32a.cts.def
write_db pico_cts1.db
read_db pico_cts1.db
read_verilog /openLANE_flow/designs/picorv32a/runs/13-01_14-09/results/synthesis/picorv32a.synthesis_cts.v
read_liberty $::env(LIB_SYNTH_COMPLETE)
link_design picorv32a
read_sdc designs/picorv32a/src/my_base.sdc
set_propagated_clock [all_clocks]
report_checks -path_delay min_max -fields {slew trans net cap input pin} -format full_clock_expanded
```
After changing clock buffers, the new timing reports are as follows:
![lab2_52](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/65c77bbb-4464-489b-a874-ad0c17818afb)

![lab2_53](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/211a4374-697d-48b0-8e4a-d91e50e60cbe)

Let us check the clock skew of the design as follows:
```
report_clock_skew -hold
report_clock_skew -setup
set ::env(CTS_CLK_BUFFER_LIST) [linsert $::env(CTS_CLK_BUFFER_LIST) 0 sky130_fd_sc_hd__clkbuf_1]      (Adding back clkbuf1)
```

![lab2_54](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6fe1aa14-71d8-49da-b6da-a98da4036a5c)

</details>

## Day19 : Final steps for RTL2GDS
<details>
<summary>Routing and Design Rule Check</summary>
<br>

#### Maze routing - Lee algorithm
Routing: the process of creating the physical wire connections within the design in which it helps in determining the best way of routing that can be done between two endpoints.
The best possible shortest path is routed between two cells with less twists and turns. No route can go on the pre-placed cells. The algorithm creates routing on the backside of floorplan.
The adjacent grids to the point that is to be connected are labelled as 1, then their adjacent layers as 2 and so on as shown.
![dsk5_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/89033e27-f6f5-4c2d-bd2a-51a18e680cfb)

The grids under the bockage are not labelled as route cannot be done through it. 
It is preferable to choose the LHS instead of RHS of the figure below because the chosen route in the LHS figure got the best route which is less bending (L-shaped) rather than the RHS figure.
Performing the routing for 1 route will be fairly simple, but when we have millions of start and endpoints to route between, this method will consume a lot of time and memory when design is huge.
There are some algorithms that can help to reduce the time and memory consumption such as line-search algorithm, stanner-tree algorithm.
![dsk5_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/58c67100-2327-4cb6-af76-4c8bb1c91748)

#### Design Rule Check
Design Rule Check (DRC) are the rules that should be followed whenever the routing of the design is performed such as 
- the minimal wire width (width of the wire should not be less than a specified amount based on the limitations of the fabrication process)
- the wire pitch (the centre-to-centre distance between 2 wires should be no smaller than a certain distance)
- wire spacing rule (distance between 2 wires should be no smaller than a certain distance)
These wires are made with photolithographic process for desired width and pitch.
![dsk5_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f9f16641-75cb-4ec7-9c17-72b19d4c66e7)

The parasitic information is extracted for each cell and net as shown.
![dsk5_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e8bd5536-79ae-4121-9743-daefbc64f041)

One type of DRC violation is a signal short, where two wires that are not intended to be connected becomes in contact on the same layer causing functional failure.
To fix this, we need to simply moving one of the wires onto a different metal layer. The new drc rules after fixing are
- Via width where the width of the via should be no less than a certain value.
- Via spacing where the distance between 2 vias cannot be less than a specific distance.
  Upper metal layers are usually wider than lower metal layers.
![dsk5_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6a37f3c4-4b9f-45dc-ae7d-c373eb2d2ab6)

</details>
</details>
<details>
<summary>PDN and routing</summary>
<br>	
	
If we want to retain the configurations from the last openlane job, we need to use ```prep -design -tag```. If we want to create a fresh run with new configurations but without changing the tag name, we need to use ```prep -design -tag -overwrite```.
	
```
cd work/tools/openlane_working_dir/openlane
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a -tag 13-01_14-09
```
	
![next](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2776963d-9e78-4989-97e3-694f835a291a)

The power and ground rails need to be a part of floorplan, this is done using gen_pdn command to build the power distribution network.
The standard cell height should be multiple of pitch of layers(metal1), so that cell gets power and ground rails alog its edges for proper connectivity.

Inorder to generate the pdn network, the following commands are used.

```
echo $::env(CURRENT_DEF)    \\Ensure current_def is on the CTS stage
gen_pdn                     \\To generate power distribution network
```
This is giving an error as follows:
![lab1_2 (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0ec73ac0-c8d7-4210-90d6-29929c08053c)

Due to this error, the pdn def is not generated so CTS def is used for routing.

The design is covered with IO pads around them. These pads contain the power and ground pads as shown.

```power and ground flows from power/ground pads --> power/ground ring --> power/ground straps --> power/ground rails```

![design](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3f37cfd1-54ed-4341-9b64-345abce0dd35)

The current def is set to the CTS def and the routing run is fired.
```
echo $::env(CURRENT_DEF)            
echo $::env(ROUTING_STRATEGY)
run_routing
```
The ROUTING_STRATEGY variable implies the optimized routing in the design. The value 0 specifies the routing is not much optimized.
![lab1_3 (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c84f4078-b7ee-466b-93b7-abcf01078f20)

</details>
<details>
<summary>TritonRoute Features</summary>
<br>

The routing stage consists of two stages:
- Global Routing: Form routing guides that can route all the nets. The tool used is FastRoute.
- Detailed Routing: Uses the global routing's guide to connect the pins with the least amount of wire and bends. The tool used is TritonRoute.
![route](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/468f3aaf-3012-42ec-8f8c-9c26247a2020)

### Triton Route
- Fast routing is the engine which is used for global routing, that creates a rough routing draft.
- During global routing, the region is divided into grid cells, which acts as a route guide for the TritonRoute to be used for the detail routing, where an algorithm is used to find the best connectivity between the points.
- It honours the preprocessed route guides (obtained after fast routes), wherein the tool attempts as much as possible to route within route guides, assuming each net satisfies inter-guide connectivity.
- Triton route works on proposed MILP (Mixed integer liner programming) based panel routing scheme with intra-layer parallel and inter-layer sequential routing framework, to finds the best way to perform the routing.
- Intra-layer refers to the routing within a layer, while inter-layer routing refers to routing between layers, through the uses of vias.
- Preprocessed guides should have unit width and must be in the preferred direction of the layer.Global route is done by fast route, and the output would be the routing guide.
- The initial route guides are transformed into the preprocessed guides through splitting, merging, and bridging.
- Whenever the tool detected the route guide with non-preferred direction, it divides the route guide into unit widths, and then the route with preferred direction is merged, while the non-preferred direction route is bridged to be a route on another layer, which is the preferred direction for routing.
This way, parallel routing with higher layers are avoided thus avoiding parallel plate capacitance.

Each layer or panel will have its own preferred routing direction assigned to it, in which the routes should be formed.
Routing in higher layers will begin only once the routing the bottom layers have been completed.
Two guides are connected if they are on the same metal layer with touching edges, or if they are on neighbouring metal layers with a non-zero vertically overlapped area.
Each unconnected terminal i.e. pin of a standard cell instance, should have its pin shape overlapped by a route guide.

Inputs file needed for TritonRoute are the LEF file, DEF file, and the Preprocessed route guides.Outputs from the TritonRoute would be a detailed routing solution with optimized wire-length and via count.
Constraints needed in TritonRoute are the route guide honouring, connectivity constraints and design rules.

#### TritonRoute method
TritonRoute handles connectivity through 2 ways
- Access Point (AP)
- Access Point Cluster (APC)
  
**Access point**: on-grid point on the metal layer of the route guide, and is used to connect to lower-layer segments, upper-layer segments, pins or IO ports.Access point refers to the point where the via can be placed to allow connectivity between layers.

**Access Point Cluster**: a union of all Access Points derived from the same lower-layer segment, upper-layer guide, a pin or an IO port.

The objective of the Mixed Integer Liner Programming (MILP) is to connect one access point to another optimally.
- Choose one of the access points where the via should be dropped
- Determining how the first access point will be connected to the next access point.

</details>

## Day20 : Floorplanning and Powerplanning Labs
<details>
<summary>Theory</summary>
<br>

Physical design refers to the process of transforming a high-level logical description of a circuit into a detailed physical representation that can be manufactured. It involves the creation of a layout that defines the exact positions, sizes, and interconnections of individual components, such as transistors, gates, and wires, on the silicon wafer. Physical design is a critical step in the chip design flow, as it directly impacts factors like performance, power consumption, and manufacturability.

The steps in Physical Design flow are as follows:
1. Technology Selection: Choose the semiconductor process technology, which defines the manufacturing parameters, transistor sizes, and available components.
   
2. Floorplanning: Define the chip's overall layout, specifying the positions of major components and areas for routing.

3. Placement:Place standard cells and macro blocks within the floorplan to optimize for area, power, and performance.

4. Global Routing: Create a high-level interconnection structure, connecting the blocks and ensuring that power and clock signals can reach all parts of the chip.

5. Detailed Placement: Refine the placement of standard cells to meet performance and area goals, considering factors like signal propagation delay and wirelength.

6. Clock Tree Synthesis: Create a clock distribution network to ensure synchronous operation of the circuit elements.
Routing:
7. Route wires to connect all components while adhering to design rules and optimizing for minimal wirelength and congestion.

8. Design Rule Checking (DRC): Verify that the layout adheres to the manufacturing constraints and design rules.

9. Layout vs. Schematic (LVS) Verification: Ensure that the physical layout matches the intended logical design.

10. Extraction: Extract parasitic information from the layout, which is essential for accurate timing analysis.

11. Static Timing Analysis (STA): Analyze the circuit's timing behavior to ensure that it meets performance specifications.

12. Power Analysis: Evaluate power consumption and optimize for low power, if required.

13. Physical Verification: Perform additional checks like Antenna Checks, Metal Fill, and Design for Manufacturability (DFM).

14. Tapeout: Prepare the final design data for manufacturing.
![designflow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3dbd97fe-4741-40aa-8594-341801e4a7b7)

#### Inputs of Physical Design:
- Technology file (.tf or .db)
- Physical Libraries (In general Lef of GDS file for all design elements like macro, std Cell, IO pads etc)
- Timing, Logical and Power Libraries
- TDF file (.tdf or .io) 
- Constraints (.sdc) 
- Physical Design Exchange Format – PDEF (optional)
- Design Exchange Format –DEF (optional)
#### Outputs obtained:
- Standard delay format (.sdf)
- Parasitic format (.spef, .dspf)
- Post routed Netlist (.v) 
- Physical Layout (.gds)
- Design Excahnge format (.def)
  
![flow steps](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3c9e82f0-b653-4c29-88a8-28cb46088d51)

#### Floorplan:
Objectives:
 - Minimize Area
 - Reducing the wire length
 -  Making routing easy
 -  Minimizing delay
 -   Less IR Drop
   
Issues with Bad Floor plan: Congestion, IR Drop, Reduced lifespan of IC, Noise, Increased Area, Routing, etc

Types:
 - Abutted
 - Non-Abutted
 - Mixed

 Steps in Floor Planning::
 - Links Netlist with physical library
 - Creates initial core
 -  Creates I/O pin placement and pad rings
 -  Place macros and standard cells
 -  Creates placement blockages
 - Specifies power nets and ground nets
 - Creates power rings and macro rings
 - Creates power and ground nets
 -  Routes power and ground nets
 -  Checks for violations
   
#### Powerplan
It is done to connect the power to chip by considering issues like EMand IR Drop. Power routing includes creation of Power ring, Stripes, Rails
Power Planning involves 
- Calculating number of power pins required
- Number of Rings, Stripes
- Width of Rings and Stripes
- IR Drop
</details>
<details>
<summary>Lab</summary>
<br>

Clone the following repositories for the physical design flow setup
```
git clone https://github.com/manili/VSDBabySoC.git
git clone https://github.com/Devipriya1921/VSDBabySoC_ICC2.git
git clone https://github.com/bharath19-gs/synopsys_ICC2flow_130nm.git
git clone https://github.com/kunalg123/icc2_workshop_collaterals.git
git clone https://github.com/google/skywater-pdk-libs-sky130_fd_sc_hd.git
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
```
The contents to my path are changed to the locations where files are cloned.
The changes in vsdbabysoc.tcl are as follows:
- remove -lib in read_lib commands
- replace MYCLK to clk since the clock used in the design is {clk}

All the commands for synthesis are included in the tcl file such as read_lib, read_verilog as follows:
![lab2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/32c0a33e-b01e-4ec7-b83b-fe1e43e99230)

The unwanted pins in avsdpll.lib are already commented out.
The vsdbabysoc.tcl file is sourced to generate the area, power, timing and sdc as follows:
```
cd ~/Physical_Design/VSDBabySoC_ICC2
csh
dc_shell
source vsdbabysoc.tcl
```
![lab2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f54bba06-727b-469a-b6ae-cd477c1fd1b5)

![lab2_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/18cba87e-07c4-4085-b37d-389aa8c21260)

This generates the following gui based circuit of the design as follows:
![lab2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f00af62e-d37f-41f8-9315-bfec95bae039)

The RYMTH core schematic is as follows:
![lab2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2f39d752-e20c-4a54-ba82-6cdc81aad363)

The reports are dumped in the seperate directory ```report```. The reports are viewed as follows:
#### Reports

Area report:
![lab2_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/42c595a8-45de-4cb0-a715-82c792788f59)

power report:
![lab2_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ed629c18-1bc6-47ea-9523-1520cd5582f2)

timing report:

The timing is met with a positive slack of 30ps. The worst slack is considered as the critical slack.
![lab2_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/97ae1557-3035-4276-9549-7ddc4fde4d1c)

Constraints report:
![lab2_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/aef2baea-8b09-4043-83dd-fa8dde6900e5)

The schematic of the BabySoC is as follows:
![lab2_10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1d5874b0-f3e0-473b-a2fd-4e45f031db35)

The RVMYTH processor has wide number of gates as shown.
![lab2_11](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d4713518-8940-47b5-9a2b-7a3e326e12cc)

#### Physical design

Inorder to setup the flow, the following files are edited with present working constraints of design and location of files.
The following files are edited:

**top.tcl**

The floorplan switch is added for create_placement command and all linking paths are updated.
![lab2_16](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/baf67a8e-9a0c-4a08-a8e0-65ff84c619a9)

**icc2_common_setup.tcl**

All the paths are updated and the metal routing layers are defined.
![lab2_17](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1debbe04-c581-4a0b-adab-0b5a39c5da9d)

All paths are updated in the **icc2_dp_setup.tcl** file also.

**init_design.read_parasitic_tech_example.tcl**

Inorder to generate tluplus file from itf file, the following command is used.
```
grdgenxo -itf2TLUPlus -i skywater130.nominal.itf -o skywater130.nominal.tluplus 
```
The file is generated as follows:
![lab2_12](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8070b9d5-1fd9-4826-bec5-25a11a8c151b)

This generated file path is passed as an argument in the file as shown.
![lab2_14](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/67eee0fa-8351-443f-9075-1912425a4abd)

**init_design.mcmm_example.auto_expanded.tcl**

The SDC path in the file is updated to the generated SDC after the synthesis.
![lab2_15](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0aeadd9c-e7c7-4dd0-9dd4-ad472523749d)

**pns_example.tcl**

The power grid pattern for supply and ground rails requires the definition of the layers to be used. The vertical and horizontal layers are changed as shown.
![lab2_13](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a863ade2-8a50-41fa-a469-906d7262cdde)

Invoking the icc2_shell, inorder to run the design using following commands.
```
cd ~/Physical_Design/icc2_workshop_collaterals/standaloneflow
csh
icc2_shell
source top.tcl
```
![lab2_18](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b9b9701f-47e6-41cc-a12b-bfe0e1b20470)

The gui based design is as follows:
![lab2_19](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e0fb8d1f-7eaf-41f9-9a04-f27d5f2ad51e)

The cells are placed as a cluster as the floorplan is not done yet. The following image shows the cells in the design.
![lab2_20](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b9a4f065-5c9b-4d1a-9758-db2129268753)

The DAC and PLL are the analog IPs (macros in the SoC) such that the blockage for the circuits in the design are as shown.
![lab2_21](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/979f3605-9cda-4480-802f-7c32bda1c404)

The filler cells along the design with power rails are as follows:
![lab2_22](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/59c377de-e799-4194-92a4-bc6789fa38aa)

Let us check for the timing violations.
```
icc2_shell> set_propagated_clock [all_clocks]             //Converting clock object from ideal clock to propagated clock
icc2_shell> report_timing
```
The slack is violated with 2.25ns.
![2322](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e8b5b499-c402-4d2b-b52d-699cd5fa36e9)

```
icc2_shell> estimate_timing
```
estimate_timing report could not be generated since there is no estimate timing rules detected on nets
![lab2_25](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/befa89b6-24d3-450d-89ef-28165144903d)

![lab2_26](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/64bda72e-65dd-4910-b116-e194c29cb113)

```
icc2_shell> report_constraints -all_violators -nosplit -verbose -significant_digits 4 > violators.rpt
icc2_shell> sh gvim violators.rpt &
```
![lab2_27](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2fec742e-6d69-4ec0-b02b-56e32d4f34f3)

### Observing the same design with core utilization 45%
Let us comment the clock latency also and creating new directory as report_changed. Now, the following comments are executed as follows:
```
gvim ~/Physical_Design/VSDBabySoC_ICC2/vsdbabysoc.tcl
csh
dc_shell
source ~/Physical_Design/VSDBabySoC_ICC2/vsdbabysoc.tcl
```

The SDC before and after the changes is as follows:
![lab2_28](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9ed1b0fc-ddb8-4ded-aca0-c707f8f88e12)

Edit the top.tcl with the core utilization to 0.45
![lab2_29](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bcc12a0f-f171-47d9-b5af-212f075ad093)

After sourcing top.tcl, the GUI based design is as follows:
![lab2_30](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b42ec200-c784-404e-93f2-76b85b8a791a)

The macros PLL and DAC in the design are as shown.
![lab2_31](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0128de93-899e-4362-947b-ea9a81b24f5b)

The slack is increased to 2.37ps after increasing the core utilization from 7% to 45%
![lab2_33](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5b03297d-4e45-48f2-af06-e8fc200c0922)

![lab2_32](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fa0c49a6-12e5-47cd-8adc-2b24d79e72f2)

The violators report for the 45% utilization of core is as shown:
![lab2_34 (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/edf11304-d59f-4283-92ac-e4a3c22edcdd)

</details>

## Day21 : Placement and CTS Lab
<details>
<summary>Theory</summary>
<br>	

#### Pre-Placement
- Physical Cells: These library cell doesn’t have signal connectivity and connect only to the power and ground rails. Physical cells, often referred to as standard cells, are used to implement various logical functions and are crucial for the layout and manufacturing of these circuits.

  Functions:
   - Functionality
   - Cell libraries
   - Fixed cell height and variable width
-  Well Taps :Well taps ensure that the substrate (n or p) is properly connected to the supply or ground, breaking the parasitic thyristor structure and preventing latch-up.

   Types:
    - N-Well Taps: N-well taps are used in the CMOS process to connect the n-well regions of PMOS transistors to the ground (Vss). This is necessary to maintain the correct biasing of PMOS devices.
    - P-Well Taps: P-well taps serve a similar purpose but are used for NMOS transistors, connecting the p-well regions to the supply voltage (Vdd).

 Functions:
   - Preventing Latch-Up
   - Substrate Bias control
   - Maintains isolation
- End Cap Cells :Endcap cells, also known as filler cells, are specialized cells placed at the periphery of a chip to fulfill several important functions.

   Functions:
  - Planarity and Uniformity
  - Densification
  - Isolation and Protection
  - Enhanced Manufacturing Yield
    
Types of Endcap cells:

- Standard Fillers: These are basic endcap cells used to fill empty spaces and maintain uniformity in the design. They are often rectangular or square in shape and come in various sizes to accommodate different gaps.
- Corner Fillers: Corner fillers are designed to fill L-shaped or T-shaped gaps at the corners of the chip, ensuring that these irregularities do not affect the chip's structural integrity.
- Edge Cells: Edge cells are tailored to fit gaps along the long edges of the chip. They are elongated and can be optimized to suit specific design requirements.
- Special Cells: Special cells, also known as custom cells or macros,that serve specific functions and cannot be represented by standard or generic cells. These are mostly Memory Cells, Analog blocks, arithmetic units, I/O cells
- Spare Cells: Spare cells, also known as redundant cells are integrated into the chip design to replace defective or malfunctioning standard cells.
- Decap Cells :
  
  Functions:
   - Power Supply Noise Reduction
   - Stabilizing the Power Distribution Network
   - Improving Signal Integrity
   - Mitigating Electromagnetic Interference (EMI)
  
  Types of Decap Cells:
   - Standard Decap Cells: These are general-purpose decap cells with fixed capacitance values that are commonly used across the chip.
   - Switchable or Programmable Decap Cells: These cells offer flexibility by allowing designers to configure the capacitance based on the specific requirements of different regions or functional blocks within the chip.
- Cell Padding is done to reserve space for avoiding routing congestion

Placement doesn’t place the standard cells in synthesized netlist, it optimizes the design and placement also determines the routability of design

 Goals and Objectives:
- Timing, Power and Area optimization
-  Minimum Congestion
-   Minimum cell density, Pin density
-    Inputs for Placement: .tf, netlist, .sdc, .lib & .lef, Floor Planning and Power planning DEF File

  Placement Methods:
- Timing Driven
- Congestion Driven

Steps:
- Defining Design Constraints
- Reading Gate Level netlist from Synthesis
- Global Placement
- Detailed Placement
- Placement Optimization
   - Cell sizing
   - Cloning
   - Buffering
 Outputs of Placement:
- Physical layout Information
- Cell placement location
- Physical layout, timing and technology information of reference libraries
#### Clock Tree Synthesis

There are number of algorithms to build the clock tree:
- H Tree
- Clock Mesh
- Spine
- Fish bone

  Clocks are used to synchronize data communication. Before clock tree synthesis, clock path behaves as ideal, where there is equal delay from clock source to sink.CTS is the automatic insertion of buffers/inverters along the clock paths of the ASIC design to balance the clock delay to all clock inputs
  
Key Objectives of Clock Tree Synthesis:

- Clock Signal Distribution: CTS aims to efficiently distribute clock signals from a single source (the clock buffer) to all flip-flops, latches, and other sequential elements throughout the chip.
- Minimizing Skew: Skew refers to the variation in arrival times of the clock signal at different destinations. Minimizing skew is crucial to ensuring that all sequential elements sample data at the same time, maintaining synchronous operation.
- Balanced Load: The CTS process seeks to balance the capacitive load on each branch of the clock tree to avoid uneven voltage drop and maintain signal integrity.
- Reducing Power Consumption: Efficient CTS can reduce power consumption by minimizing the number of clock buffers and optimizing their placement to minimize power dissipation.

Key Steps in Clock Tree Synthesis:

- Clock Tree Construction: The clock tree network is created by generating a tree-like structure of clock buffers and wires. These buffers amplify the clock signal and ensure it reaches all destination points.
- Buffer Sizing and Insertion: Buffer sizing involves selecting the type and size of clock buffers to balance the drive strength with the capacitive load. Buffers are inserted strategically to ensure signal quality and minimize skew.
- Clock Tree Balancing: This step aims to distribute the clock signal uniformly to all parts of the chip, reducing skew. Balancing can involve adjusting the buffer placements, buffer sizes, or wire widths.
- Skew Minimization: Advanced techniques, such as clock skew optimization, are employed to further reduce clock skew to an acceptable level.
</details>

<details>
<summary>Lab</summary>
<br>	

The following image shows the reports directed and the place_opt and clock_opt stage.
![lab1_1](https://github.com/Usha-Mounika/Samsung_PD/day21/lab1_1.png)

The SDC does not contain the latency as it is calculated by the tool in real time as the CTS is build. 
The ```create_placement``` is used to create placement for the design. floorplan option is selected to make the design planning styled as placement.
Pin Placement is done by sourcing pns.tcl to sync with the current technology file regarding power grid creation.
![lab1_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6bbe8fdc-3518-4efc-a6e8-162b64b95672)

Reports are generated after the run in a directory ```rpts_icc2``` as defined in the SDC. The reports are:

**check_design.pre_pin_placement**

There are no errors and warnings before pin placement checked with ```check_design``` command.
![lab1_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/093c28bc-e191-4776-9ac6-2eefa51c7a05)

**report_port_placement.rpt**

This report contains the ports of the top level design with the metals used for routing and their offset values
![lab1_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/233f2e48-6cba-4e80-9795-6cf94c7ac3b6)

**report_placement.rpt**

The following report shows 
- the total net length in design is 65790 microns.
- No hard macros being overlapped
- No cells hae placement violations
- All cells are placed within respective voltage areas.

![lab1_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f99ced33-d327-42cd-806c-60a1d8094781)

**vsdbabysoc.post_estimated_timing.rpt**

The estimated timing report shows that slack is MET with 860 ps margin as follows:
![lab1_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6d977c60-d6d1-46e8-9579-552986aae60b)

**vsdbabysoc.post_estimated_timing.qor**

The QOR shows the cell count, criticsl path, critical slack, macros used, area used. It gives the detailed report of cells placed in design.
![lab1_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/135e2a1a-8883-4cc4-82b5-b976dff023e6)

**vsdbabysoc.post_estimated_timing.qor.sum**

This reports shows the DRC violations and timing violations of estimated corners timing.
![lab1_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/4af242a0-09b2-4015-834f-4512d2146e5d)

#### Clock Tree
Here when gui opens we need to go to window sections and in that we need to select clock tree synthesis analysis window.

The following image shows the PLL source to connection to various cells.
![lab1_10 (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fb3a92c6-fc34-416a-a00a-0a634c3794bb)

The following image shows the fanout view of clock in the design. The nets of all cells from clock source to clock pins.
![lab1_9 (2)](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/23f47dbc-6c19-46d4-8b71-75af98931a1d)

</details>

## Day22 : CTS analysis Labs

<details>
<summary>Theory</summary>
<br>
	

The primary purpose of Clock Tree Synthesis is to distribute the clock signal uniformly and with minimum skew to all sequential elements (flip-flops, registers, etc.) of the VLSI chip. This is essential to ensure synchronous operation and proper timing in the digital circuit.
*The goal of clock tree synthesis (CTS) is to minimize skew and insertion delay.*

Algorithms used for CTS:
![algo used](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/028ffc89-4f70-43a6-a1d4-5418c3e5cbb3)

The H-tree algorithm is
1. Find out all the flops present
2. Find out the center of all the flops
3. Trace clock port ot the center point
4. Now divide the core into two parts, trace both the parts and reach to each center.
5. Then form this center again divide the area into two and again trace till center at both the end
6. Repeat this algo till the time we reach the flop clock pin.
![H-tree](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5a4081a0-e390-4e3e-a845-3b26477b9f90)

Clock Tree Synthesis involves several key steps:
- Clock Tree Generation: A hierarchical structure is created, branching from a primary clock source to various regions of the chip. This tree structure minimizes skew and optimizes signal distribution.
- Buffer Insertion: Buffers are inserted along the clock tree to maintain signal integrity and minimize clock skew. Buffers help to drive long clock lines and reduce their delay.
- Clock Skew Optimization: CTS algorithms aim to minimize clock skew, ensuring that all flip-flops across the chip experience the clock signal simultaneously. This is vital to prevent setup and hold time violations.
- Clock Gating: In some cases, clock gating elements are inserted into the clock tree to disable the clock signal for specific sections of the design when they are not in use. This reduces dynamic power consumption.
- Verification: After CTS, the design is rigorously verified to ensure that the clock signal is distributed correctly and meets timing requirements.

#### Significance of CTS in VLSI:

- Timing Closure: CTS is critical for achieving timing closure, ensuring that the digital design operates within specified clock frequencies without setup and hold time violations.
- Reducing Clock Skew: CTS minimizes clock skew, ensuring synchronous operation and preventing metastability issues in sequential elements.
- Power Optimization: Clock gating techniques employed in CTS help reduce dynamic power consumption by disabling clock signals in inactive areas of the chip.
- Enhancing Chip Performance: Properly synthesized clock trees lead to better chip performance by reducing clock distribution delays and enhancing synchronization.

**Challenges in CTS:**

- Skew Minimization: Achieving minimum clock skew can be challenging, especially in complex designs with a high number of clock domains.
- Trade-offs: There's often a trade-off between power consumption and clock distribution delay, and optimizing both aspects requires careful consideration.
- Hierarchical Design: Hierarchical VLSI designs can make CTS more complex as it involves synthesizing clock trees at various levels.

Let us look at some commands at CTS:
```
check_clock_tree
```
This command checks and reports issues that can lead to bad QoR
- Clock tree structure
- constraints
- Clock tree exceptions
```
check_legality
```
If it is legal — well and good, else use legalize_placement. The default constraints can be 0.5ns for transition time, 0.6pF for maximum capacitance, 2000 of maximum fanout.

IC Compiler uses the clock tree synthesis design rule constraints for all optimization phases, as well as for clock tree synthesis. For information about setting the clock tree synthesis design rule constraint
```
compile_clock_tree
optimize_clock_tree
```
The clock_opt command does the following:
1. Performs clock tree power optimization 
2. Synthesizes(Re-Synthesizes) the clock trees
3. Optimizes the clock trees
4. Adjusts the I/O timing 
5. Performs RC extraction of the clock nets and computes accurate clock arrival times
6. Performs placement and timing optimization
The ```remove_clock_tree``` command is used for unrouted clock trees (if any).

</details>
<details>
<summary>Labs</summary>
<br>

Let us explore the clock tree behaviour using the following commands

```
check_clock_tree
```
The report shows the QoR of the tree built. It shows
- Any multi-voltage violations caused
- Skew Balancing
- capacitance & transition in clock network
- reference cells defined as don't use/don't touch cells

The output of this command shows *None* to all the violations that might arise. 
![lab2_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/44ae9799-ddce-4746-b303-2532d369f6a2)

![lab2_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f88229df-29b0-4a94-97da-f365de7d6393)

- CTS-013 : Cells  in  the  clock  network  have  been  marked  with  a  dont_touch attribute. *dont_touch*  on  a  cell prevents sizing, optimization, and replacement during CTS.  dont_touch can limit CTS  optimization,  which can cause worse latency, skew, or area in the clock network.
- CTS-904 : CTS cannot resize a cell in the clock network unless  there  are  logically equivalent lib_cells specified in the clock reference list.  This message indicates that there are cells instantiated in the  clock  network that have no logically equivalent lib_cells in the reference list, so no sizing can be done.
- CTS-913 : set_clock_ignore_points is used to define pins in the clock  tree  that should  be ignored for skew balancing.  create_clock_skew_group is used to add clock pins into a separate skew  group  from  the  default  skew group for that clock.  This message reports clock pins that are defined as explicit ignore points but also have been added to a skew group. 
```
check_legality
```

This command shows the design rules checking such as any overlaps in the design, improper routes on metal layers as shown. All are shown as 0 and the legality is successfully checked.
The various app_options are set to true. One of them is,

place.legalize.enable_prerouted_net_check :
              This  app_option enables checking of cell placement against pre-routed nets, including Power and Ground nets,  during  legalization  and  legality checking.
![lab2_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/fb2c0fc3-30e5-44d2-bbb4-59fe94f417b1)

![lab2_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/79736090-211e-457e-902a-27680666bb0f)

![lab2_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0e0bd843-5d92-4466-9936-5710f95a0a04)

As all the violations reported were zero, the legality is successful.
```

report_clock_timing -type summary
```
![lab2_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/adc14342-d7cf-4709-8843-a4b5f370310f)

- The summary gives the report of launch latency and capture latency of flop i.e., the clock network delay of flop.
- The rp-+ implies the rise transition propagated clock from launching flop to capture flop.
- The defined corner is func1 in init.design_mcmm.auto_expanded.tcl file.
The various symbols used are as follows:
    r     -->    Rising transition

    f    -->     Falling transition

    p    -->     Propagated clock to this pin

    i    -->     Clock inversion to this pin

    -    -->     Launching transition

    +    -->     Capturing transition

    e    -->     Exception on this pin
```

report_clock_timing -type skew
```
![lab2_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b3a0e9dc-2a1c-4d0c-bbea-c8824cbf3e9a)

- The skew reports the local skew. Each report entry is a pair of sink pins and their relative skew.
- For skew reports, the from-to skew sense is defined by the pins in the from_list and to_list options respectively. If the to_list option is not specified, by default all sink pins in the given clock networks are used. Thus, specifying the to_list option reduces the topological scope of the report. For transition time and latency reports, the from_list and to_list options are concatenated and treated as a single list. If neither is specified, the to_list option is assumed to be populated with all sink pins in the given clock networks.
- Local skew exists from one sink pin to another only if their associated sequential devices are connected via a data path in the appropriate from-to sense.
```
report_clock_timing -type transition
report_clock_timing -type latency
```
![lab2_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e88c9109-63d5-48f9-9f22-fe353dd0930e)

- The transition report gives the source latency and network latency and transition of the design clock.The source latency is 0 as the PLL in the design is blackbox yet.
- The transition report gives maximum transition and the latency to that clock pin. The latency report gives the maximum latency of the clock pin along with transition at that pin.

```
report_clock_tree_options
```
This command is used to look at the values defined for skew, latency, fanout as shown. 
![lab3_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0064691f-1670-4ad6-935c-a5bf582a4e03)

These are defined using the command ``set_clock_tree_options`` as shown.

```
set_clock_tree_options -target_skew 0.3 -target_latency 0.6
report_clock_tree_options
```
![lab3_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bca31b69-4a5d-402c-a2be-b88c36fa419e)

This  command  reports  all  existing  settings   like   clock   targetskew/latency  constraints, fanout-based ndr, etc, previously defined by set_clock_tree_options commands.
</details>

## Day23 : Clock Gating Technique
<details>
<summary>Theory</summary>
<br>


#### Advanced H-Tree for million flop clock end-points randomly placed

- When CTS is performed, power consumption also needs to be taken care of, especially when designing a large number of clocks where the design might induce a larger power, as well as a larger power usage. A digital circuit with a lot of clocks would be so huge with many buffers etc when designing its clock tree
- In order to fix that, the whole chip is sectioned into smaller versions where each section will have its own clock tree, and managed to get a complete routed tree.Therefore, Clock Gating (CG) technique is introduced.
![23](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a9a55137-9a6a-40e1-ae52-80fb65d60531)

### Clock Gating
- Clock gating involves the use of a gating logic, often in the form of an AND gate, to control the clock signal. When the gating logic's control input is inactive, the clock signal is effectively blocked, preventing it from reaching the clocked elements.
- Clock signals in digital circuits toggle at a high frequency, consuming a significant portion of the power budget.
-  Clock gating helps in mitigating this power consumption by turning off the clock signal when the circuit elements do not need to perform any computation.
![cg](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5ef93f98-6c32-4458-b28f-b3840128201d)

#### Types of Clock Gating:
- Latch-Based Clock Gating: In latch-based clock gating, latches are used to store data between clock cycles. The gating logic controls whether the latches accept or ignore data based on the control input.
- Flip-Flop-Based Clock Gating: Flip-flop-based clock gating is similar to latch-based gating, but it uses flip-flops instead of latches to store data. Flip-flops are edge-triggered, providing better synchronization.

Advantages:

-  Clock gating significantly reduces the dynamic power consumption of a digital circuit by preventing unnecessary switching activity.
-  Clock gating can help reduce clock skew, leading to better timing closure in designs.
-  Clock gating can make it easier to achieve timing closure in complex VLSI designs by allowing more control over clock distribution.

Types of routing

- P/G routing
- Clock routing
- Signal routing: Global & Detailed routing

Clock Tree Synthesis:

- In designs with synchronous circuits, a dedicated clock tree is synthesized to distribute the clock signal with minimal skew.
- Clock tree synthesis ensures that all clocked elements in the design receive clock signals at the same time.


#### Routing
Routing is a critical step in VLSI design, where the logical connections between various components are physically established.
Power Grid Routing:

- Power grid routing focuses on routing power and ground signals to ensure even distribution of power throughout the chip.
- Proper power grid routing is essential to avoid voltage drop issues and ensure that all components receive adequate power.

Global Routing:

- In the initial stage, global routing is performed to establish approximate routes for nets across the chip.
- The objective is to find a path for each net between source and destination cells while considering the macro placement and available routing tracks.

Detail Routing:

- Detail routing, also known as track assignment, refines the global routes by determining the specific tracks and metal layers that will be used for each net.
- Detailed routing ensures that the physical implementation adheres to design rules and constraints, optimizing for area, timing, and manufacturability.

The ```route_auto``` command is used during routing stage in top.tcl.
![routing](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bd7d3618-6c85-4dc0-8e3a-14aa6f3e37b4)

</details>
<details>
<summary>Lab</summary>
<br>

Let us optimize the clock network. Inorder to do this, the nets to the flops from the pll block requires buffers to improve transition thus reducing delay. 
The following image shows the initial steps followed.
- ```place_opt``` is used to optimize the placement in the design.
- ```clock_opt``` is used to optimize the clock such thst latency improved and skew reduced.
- ```route_auto``` is used for global routing, track and via assignment, detailed routing done at once. 
![lab4_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/734c9c7a-850b-4d57-8f1c-c8086997851c)

For the power grid routing, the following file contains the pg_mesh, pg_ring for the design and the pg pattern for standard cells as follows:
![lab4_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/32145c3d-26d2-48e4-81ea-7fab098ab806)

But the design contains no clock buffer cells in design. So, The lib cells were added and the clock tree is synthesized and propagated using the following commands:
```
set_lib_cell_purpose -include cts {sky130_fd_sc_hd_tt_025C_1v80/sky130_fd_sc_hd_buf_*}
synthesize_clock_tree
set_propagated_clock [all_clocks]
```
- ```set_lib_cell_purpose -include cts {sky130_fd_sc_hd__tt_025C_1v80/sky130_fd_sc_hd__buf_}``` command specifies that the library cells in the PVT_lib library(sky130_fd_sc_hd__tt_025C_1v80) whose names start with "buf" should be used for clock tree synthesis i.e., buffer cells are used for synthesizing the clock tree.
- ```synthesize_clock_tree``` command synthesizes clock trees and updates the design database with the compiled clock trees. The compilation of the clock tree is skew driven. This command can optimize compiled clock tree for improving the slack.
- ```set_propagated_clock [all_clocks]``` command specifies that delays be propagated through the clock network to determine latency at register clock pins.Propagated clock latency is used for post-layout, after final clock tree generation. If the set_propagated_clock command is applied to pins or ports, it affects all register clock pins in the transitive fanout of the pins or ports. The above command specifies to use propagated clock latency for all clocks only in the current mode in the design .

These steps should be involved after placement stage i.e., at CTS stage. So, These commands are added after optimizing placement and before the clock optimization.
![lab4_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/bf9ecf64-d72d-4183-9bdd-bd7f0022ad5e)

We know, the PVT corner is defined for 1.8V  and 25C temperature, so the voltage set while defining constraints needs to be set to 1.8V.
![lab4_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/497f2a13-f87b-4e2d-8ae7-c1758e431af6)

So, sourcing top.tcl file now, created the buffers as follows:
![lab8_ctsbuf](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/551a8088-0e26-4ca0-ad85-76f87a41c440)

The clock buffers in the design are viewed with GUI as follows:
![lab7_clockbuffer](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c23f82d4-d061-4bdb-b6f9-c353c5dff64e)

![lab8_clocksink](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/011ae032-0291-422c-aa44-4f6b40f3675e)

The following image highlights the fanout of the clock tree in the design.
![lab4_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1cac02fb-8e88-4b5c-af03-6e720a234586)

The cells view based on level and type connected to clock i.e., clock buffers and clock sinks (usually sequential cells with clock pin) are highlighted as follows:
![lab9_clocktree](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5638e318-53e4-4469-9962-50c1aae1b976)

Even the setup slack now has reduced to 0.11ns or 110ps and the hold violations are met as shown.

The setup path is viewed as 
```
report_timing
```
- The setup path gives the arrival time minus required time. The required time is the summation of period and setup uncertainty, clock network delay of capture flop.
- The library setup time is 0.09ns (defined in libs), uncertainty is 0.5ns (user-defined in SDC) and network delay of 2.6ns.
- The required time is 12.02 ns. The timing is violated by 0.11ns as the arrival time in data path is 12.13ns (clock network delay + comb delay)
![lab4_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/92156791-8cdb-426d-9676-7b7584e31692)

The hold oath is viewed as
```
report_timing -delay_type min
```
- The hold path gives required time minus arrival time. The required time is due to network delay and uncertainties of clock, library hold time of capture flop.
- The library hold time is 40ps (defined in libs), uncertainty is 0.5ns and the network delay is 2.38ns.
- The hold is checked at the same edge of flop(at 0ns). The clock network delay is same for both flops as same clock is being propagated.
- The hold is MET with a very minimal margin as shown.
![lab4_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ecfd7fff-31d4-4668-bbc5-68122bcdbb8c)

</details>

## Day24 : Timing violations and ECO
<details>
<summary>Theory</summary>
<br>

- Engineering Change Order or ECO is how you incorporate last minute changes in your design. 
So typically we do ECO on the gate level netlist. Designer need to edit the gate-level netlist, make the same changes in RTL. 
Then pass all verifications before it is passed on to layout.
- Make sure the ECO pass formal and functional verification before you start editing your layout.In this stage all the violations are fixed and seal all the sign-off checks that weren’t done during the PD flow

It is all dependent on the PPA - Power(dynamic, short-circuit, leakage), Performance, Area.
- We need to see different options for tradeoff between the PPA.
- Implementation tool doesn’t fix all the violations => So here engineers come into pictures. 
- More sign-off corners than what is enabled in PnR.
- Verification catches bugs but can’t do a re-spin, hence we just directly change the netlist

ECO has has the following steps :
1. Investigate the problem using the recent database
2. ECO generation to address the problem
3. ECO implementation with the recent database
4. After implementing and fixing the problem, save it in the database for future
![eco](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/83118548-1880-4280-8592-b807b962f710)

</details>
<details>
<summary>Lab</summary>
<br>

The following image shows the run completed by placing the filler cells in the design.
The various filler cells of different size are as follws:
![lab5_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9e01df29-a5d6-43b7-a939-2fc4dc5df3f0)

The setup slack is as follows:
![lab5_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2fc64314-967b-4166-bd02-b492bc2e2869)

The critical path in the design i.e., the report that has highest worst slack is viewed in GUI as follows:
![lab5_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/69ea6dc9-c71c-4bec-b703-6c4f789340cf)

All the cells, ports,pins are highlighted so the view is not clear, the only cells and label highlighted view is as follows:
![lab5_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2148dddc-f2a0-4e94-8d14-8430c6ee5f7c)

The inserted fiiler cell in the cell-view is as follows:
![lab5_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/06dc929f-49eb-4b77-ac48-5fc15ba47e15)

After inserting the decap cells in top.tcl,
![lab5_9](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/44a26cf7-79b1-42e2-b2df-c0f42d879e0e)

The decap cells are inserted as follows:
![lab5_8](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/dc232c1c-268b-43a6-9a35-76ba20fe0bcb)

The setup slack was violated after inserting decap cells as shown.
![lab5_afterinsertdecap](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/e97b0834-dc1f-4eae-a7a8-703f0cebedd6)

The following report of global timing shows that there are 20 setup violations(NVE) with worst negative slack(WNS) of 0.08 ns and 0.76 of total negative slack(TNS).
![lab5_afterinsertdecap_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/c9a212aa-4b14-4f4f-8eca-931d7b613c31)

The setup violation can be fixed by upsizing the cells in the arrival path of the data path. So, using ```size_cell``` command, the following violations are made to zero.
```
size_cell core/U339 sky130_fd_sc_hd_fa_2
size_cell core/U3 sky130_fd_sc_hd_fa_2
size_cell core/U340 sky130_fd_sc_hd_fa_2
```
![lab5_afterinsertdecap_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5fc1cc0b-ee07-493f-af90-b511cac7d717)

![lab5_afterinsertdecap_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/36037d70-d694-460e-a738-e7169887f150)

![lab5_afterinsertdecap_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/35dbef28-6271-4308-bd69-56ba28a55a0e)

![lab5_afterinsertdecap_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0ec253e0-c413-4d17-95d1-feafb8219181)

The improvement in the slack can be seen after upsizing the each cell. FInally the setup is MET with a positive margin of 30ps.

Let us fix the tran violations. 
The tran violations can be checked using the following command 
```
report_constraints -all_violators -max_transition
```
There are 5 violations. The driving cell needs to be upsized to fix the transition violation.

The various methods to fix transition violation are:
- upsize the driving cell
- add_buffer_on_route (if netlength is high)
- split_load/split_fanout by adding buffer

The method to fix capacitance is to upsize the cell. So, Upsizing the driving cell at transition violating pins might fix the capacitance violations.

The following image shows the net reported as violating with high fanout.
![lab5_tran_1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/3a6f571b-539d-4172-874b-9f3ad1b21f0d)

![lab5_tran_2](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/5307ab1a-9472-401c-8cd5-fa1b07ad3c08)

The following commands are used:
```
change_selection [get_net <violating_net>]
// switch to schematic view and highlight the driving cell of net
get_selection
get_attribute [get_selection] ref_name
size_cell <instance_name> <new_ref_name>
```
Similarly,
![lab5_tran_3](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/24f2320c-755d-4f13-b8ee-ec4d0e617a9d)

![lab5_tran_4](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/d049c24a-7b93-4838-ad62-d7e5414afae5)

All the transition violations are MET as shown.
![lab5_tran_5](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/edab0720-2fa8-4a7a-9bda-3a50b0c6f45e)

Fixing the transition violations, also fixed the capacitance violations but setup was violated again 
![lab5_tran_6](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b2387700-ba9b-43ad-ad31-5e14ed365ca0)

Again resizing the cells, the setup got fixed and all the violations are fixed.
![lab5_tran_7](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/de5d6d4c-fe04-402f-9141-60e4a95d98f6)

**report_power**

The ```report_power``` shows the final leakage power, switching power when the timing is completely MET.
![lab6_power_after](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ad350b80-764d-424b-badc-56bddbe1b249)

The following report shows the power before ECO.
![lab6_power_before](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b49b289d-627a-4578-b231-ff1d347b2ef2)

- Internal power is any power dissipated within the boundary of a cell. A circuit dissipates internal power by charging or discharging any existing capacitances internal to the cell during switching.
The internal power is 2.86 mW before and after ECO.
- Switching power results from calculations based on the voltage, netlist capacitance, and switching of the nets. The switching power is 1.34mW before and after ECO.
- Leakage power is the power dissipated by a cell when it is not switching—that is, when it is inactive or static.  The Leakage power increased from 190nW to 194nW.
- The total power is at 4.2mW due to the negligible change of leakage power.  The cell internal power and the net switching power and cell leakage power are almost same. So, There is not much variation in power i.e., 4nW of increased power dissipiation.
  
  **report_qor**

![qor](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/2b40944d-5d20-49fa-8873-bf80630e6f5a)

- The above image shows the all violations fixed in design, including the capacitance and transition violations.
- The cell area has increased from 700465 to 700487 microns.
- There is no change in buffer area or non-combinational area, as the combinational cells only are upsized.
**So, This is an improved qor with no timing violations with little trade-off in area**.

</details>

## Day26: Introduction to mixed signal flow
<details>
<summary>Mixed Signal flow</summary>
<br>

Mixed signal flow refers to the concurrent utilization and integration of both analog and digital signals within a system or process. This combination allows for the advantages of both signal types to be harnessed in achieving specific functionalities.

**Analog Signals:**

Analog signals are continuous in nature, representing information through a smooth, continuous waveform. Examples include voltage, current, and temperature. They are characterized by their infinite range of values within a given range.

**Digital Signals:**

Digital signals, on the other hand, represent information in discrete, binary form—commonly as 0s and 1s. These signals are used in computing systems and have distinct levels, usually on/off or high/low. They allow for robust storage, processing, and transmission of data.

**Analog-to-Digital and Digital-to-Analog Converters (ADCs/DACs):**

These components are fundamental in mixed signal design. ADCs convert analog signals into digital format, while DACs perform the reverse operation converting digital signals back into analog form. These are crucial for facilitating communication between the analog and digital sections of a system. These chips have very different Design and Process Technology demands than normal digital circuits
  
![amsflow](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/0ed0dc37-f814-4e69-bb13-6a56d777dec3)

In our vsdbabysoc design, the PLL and DAC are analog blocks and RVMYTH processor is a digital block.
![lab2_10](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/1d5874b0-f3e0-473b-a2fd-4e45f031db35)

#### Various files required
- **LEF (Library Exchange Format)**: The LEF file contains the physical information such as height,width etc.. of standard cells. A LEF file has two parts:
   - Cell LEF
   - Tech LEF
  Technology LEF part contains the information regarding all the metal interconnects, via information and related design rules whereas cell LEF part contains information related to the geometry of each cell.
  Technology LEF part contains the following information
    - LEF Version ( like 5.7 or 5.8 )
    - Units (for database, time,  resistance, capacitance)
    - Manufacturing grids
    - Design rules and other details of BEOL (Back End Of Layers)
       - Layer name (like poly, contact, via1, metal1 etc)
       - Layer type ( like routing, masterslice, cut etc)
       - Prefered direction (like horizontal or vertical)
       - Pitch
       - Minimum width
       - Spacing
       - Sheet resistance
 Cell LEF basically contains the following information
   - Cell name (like AND2X2, CLKBUF1 etc)
   - Class ( like CORE or PAD)
   - Origin 0 0
   - Size (width x height)
   - Symmetry ( like XY, X, Y etc)
   - Pin Information
   - Pin name (like A, B, Y etc)
   - Direction (like input, output, inout etc )
   - Use (like Signal, clock, power etc)
   - Shape  (Abutment in case of power pin)
   - Layer (like Metal1, Metal2 etc )
   - rectangular coordinate of pin (llx lly urx ury)
- **LIB (Liberty File)** : LIB file is an ASCII representation of timing and power parameter associated with cells inside the standard cell library of a particular technology node. Lib file is basically a timing model file which contains cell delay, cell transition time, setup and hold time requirement of the cell. So Lib file basically contains the timing and electrical characteristics of a cell or macros. Lib file is generated and provided to ASIC designer by a standard cell library vendor or Foundry if the foundry provides a standard cell library. Timing and power parameter of a cell is obtained by simulating the cell in a variety of operating conditions and data are represented in the Lib file.
- **GDSII file** : GDSII (Graphic Data System II) is a file format commonly used in the semiconductor industry, particularly in the design and manufacturing of integrated circuits. It is the standard format for transferring and storing design data for electronic chips. The 
  1. Geometric Shapes and Layout Information: GDSII files encapsulate geometric shapes that define the layout of an integrated circuit. This includes polygons, paths, and other structures representing different elements of the chip design such as transistors, interconnects, vias, and metal layers.
  2. Layered Information: The design is segmented into various layers, each representing a distinct aspect of the chip. Layers are crucial in distinguishing different elements of the chip design, from the physical components to the interconnections.
  3. Hierarchical Data: GDSII files can contain hierarchical information, allowing designers to create and manage complex designs with different levels of detail, from macros to smaller components, making the representation of the layout more efficient and organized.
  4. Text Labels and Markings: GDSII files may include textual information that labels components, specifies measurements, or contains other crucial annotations to aid in the understanding and interpretation of the design.
  5. Design Data Compression: To manage the complexity and size of the file, GDSII uses data compression techniques, grouping geometric shapes into structures that facilitate efficient storage and retrieval of information.
  6. Technology Information and Design Parameters: GDSII files can include information about the technology used, design rules, and parameters that define the chip's characteristics and constraints.
- **OASIS file** : OASIS (Open Artwork System Interchange Standard) is another file format used in the semiconductor industry for representing and transferring layout data of integrated circuits. It was developed to address some limitations of the older GDSII format, aiming to handle the challenges posed by increasingly complex chip designs and to improve data handling efficiency.
   - OASIS was designed to handle the complexities of modern chip designs more efficiently compared to GDSII
   - They enable the representation of complex designs with various levels of detail, allowing for a more organized and manageable layout representation.
   - OASIS files incorporate advanced features such as reusability of cell libraries and the ability to represent larger data volumes with improved data access, addressing the limitations faced by GDSII.
   - OASIS employs variable-sized elements and serialization techniques, enhancing the handling of complex and detailed geometries.


The PnR tool takes the inputs and generates the GDSII file. The various tools for PnR are Innovus (Cadence Design System), IC Compiler II (Synopsys), Olympus SOC (Mentor Graphics).

The inputs required are the gate level netlist (.v or .vg format), the constraint files (.sdc format), the logical libraries (.lib or .db format), physical libraries (.lef), technology libraries(.tf or .techlef), the PVT conditions (scenarios defining file) and the RC parasitics file.

The additional input files can be block partition (.fp file), I/O pin locations file (as pad_placement_constraints.tcl in vsdbabysoc), power plan script or rule, the power intent file and saif file(switching activity file).

The following images shows the stages of physical design and brief need for stages.
![whatwhy](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7824bb9a-a4af-4eeb-8293-148e726d64cc)

#### IP cores
An IP core consists of a block of logic or data that is used in a semiconductor chip. It is usually the intellectual property of a particular person or company. IP cores are used when making a field
programmable gate array (FPGA) or application-specific integrated circuit (ASIC). IP cores are created throughout the design process and can be turned into components for reuse.

There are different categories for IP cores including hard IP cores and soft IP cores.
- The soft IP core , can be customized during the physical design phase and mapped to any process technology.
- A hard IP core is one that has the logic implementation and the physical implementation. In other words, the physical layout of a hard macro-IP is finished and fixed in a particular process technology.
  
</details>

## Day27 : Introduction to crosstalk - glitch and delta delay
<details>
<summary>Theory</summary>
<br>

#### Crosstalk

- Signal Integrity & Crosstalk are the Quality checks of the clock routes.
-  Signal integrity is the ability of an electrical signal to carry information reliably and resist the effects of high-frequency electromagnetic interference from nearby signals.
- Crosstalk is the undesirable electrical interaction between two or more physically adjacent nets due to capacitive cross-coupling. Crosstalk is a type of noise signal that corrupts the actual signal while transmission through the communication medium

As the geometry of cell reduces, the distance between the interconnects decrease, thus increasing crosscoupling capacitance between nets. So, the parasitic capacitance becomes less as interconnections become narrower.The cell delays are also reduced as the size of transistor is small.

The various reasons for Crosstalk are more number of metal layers in design, more congestion (interms of routing), low voltage design and Thin and long metal layers are routed.
These can be fixed by using guard rings, down-sizing the agressors or shielding, layer promotion of nets or breaking of long nets.

-  A net that receives undesirable cross-coupling effects from a nearby net is called a victim net.
-  A net that causes these effects in a victim net is called an aggressor net.
-  An agressor can also be a victim net and vice-versa.
  The timing effects of an agressor net on a victim net can be depending on various factors such as switching direction of rise and fall, relative times & slew rates of signal transition, amount of cross coupled capacitance and combinatinal effects of multiple agressor nets on single victim net.

#### Glitch
When one net is switching, and another net is constant then switching signal may cause spikes on other net because of which coupling capacitance (Cc) occurs between two nets, this is called as crosstalk noise.
A steady signal net can have a glitch due to the charge transferred by the switching aggressors through coupling capacitances. The glitch magnitude may be large enough to be seen as a different logic value by the fan-out cells of the victim nets.
The various types of glitches are rise, fall, overshoot and undershoot.
![glitch](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/deeedd52-dcaf-4631-8f24-4a71b9a98c68)

- Rise glitch: Raising aggressor net induces a rise glitch on a steady low
- Fall glitch: Falling aggressor net induces a fall glitch on a steady high
- Overshoot glitch: Raising aggressor net induces overshoot glitch on a steady high This takes the victim net voltage above its steady high value.
- Undershoot glitch: Falling aggressor net induces an undershoot glitch on a steady low This takes the victim net voltage below its steady low value.
</details>
<details>
<summary>Lab</summary>
<br>

Before generating the reports for the crosstalk and SI analysis using primetime, the inputs required to read the design by the primetime tool are generated using icc2_shell.

**Generating SPEF file**:

```
source top1.tcl
update_timing
write_parasitics -format spef -output vsdbabysoc_spef
```
The following image shows the generation of SPEF:
![update spef](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ec125087-5b94-41ba-9c12-1fc97172f4ed)

The generated zip file is unzipped using the command:
```
cd write_data_dir/vsdbabysoc
gzip -d vsdbabysoc.pt.v.gz
gzip -d func1.sdc.gz
cp vsdbabysoc.pt.v /home/usha.m/Physical_Design/icc2_workshop_collaterals/standaloneFlow
cp func1.sdc /home/usha.m/Physical_Design/icc2_workshop_collaterals/standaloneFlow
```
These files are copied to main directory standalone flow.
![unzip_sdc](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/54f8995d-c506-4bd2-8521-1f7b9cd64505)

![pt_shell1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/7efbeaae-e7e2-40d4-ba5a-047235b3b599)

The design is read into the pt_shell are as follows:
```
set target_library {list set target_library "avsddac.db avsdpll.db sky130_fd_sc_hd__tt_025C_1v80.db"
set link_library [list avsddac.db avsdpll.db sky130_fd_sc_hd__tt_025C_1v80.db]
read_verilog vsdbabysoc.pt.v
link_design vsdbabysoc_1
current_design
```

The sdc is read into the design and
```
read_sdc func1.sdc
set_app_var si_enable_analysis true
read_parasitics -keep_capacitive_coupling vsdbabysoc_spef.temp1_25.spef
```
The following image shows the parasitics read by the tool.
![sdc read](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/676ab596-6113-4173-a32f-b9ba3105fd98)

The following image shows the report of check_timing as follows:
![check_timing](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/6a7fe832-711d-41ae-894c-0e202893f2fe)

The design can be viewed using GUI is as follows:
![gui](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/81e1c3a1-ca8c-4b84-89ea-231225f43cc1)

The various checks done specific to crosstalk analysis are:
- no_driving_cell : reports input ports with no driving cell and doesn't have case analysis set on it. These nets are assigned as a stronger driver for modelling agressors.
- ideal_clocks : reports nets that do not have propagated clocks. The design must have propagating clock tree to calaculate crosstalk.
- partial_input_delay : reports the delays set with set_max_delay and set_min_delay commands in SDC.
- unexpandable_clocks : reports any clocks that are not expanded to common time base.

The various reports are as follows in pt_shell
```
report_si_bottleneck              
report_bottleneck                
report_si_delay_analysis
report_si_aggressor_exclusion
report_si_noise_analysis
```
![report_si_bn](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/89c1f27d-1a2b-4053-8cf4-cba816ff2f66)

![report_si_bn1](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/ce763d16-b52a-4e9c-8677-d19f467b4ccd)

</details>
