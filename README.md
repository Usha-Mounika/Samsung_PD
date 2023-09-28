# Physical Design Training

A brief description of what this training summarizes : 

- [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)
- [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)
- [Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles](https://www.github.com/Usha-Mounika/Samsung_PD#Day2)
-  [Day3 : Combinational and Sequential Optimizations](https://www.github.com/Usha-Mounika/Samsung_PD#Day3)
-  [Day4 : GLS,blocking vs non-blocking and Synthesis Simulation mismatch](https://www.github.com/Usha-Mounika/Samsung_PD#Day4)
-  [Day5 : DFT](https://www.github.com/Usha-Mounika/Samsung_PD#Day5)
-  [Day6 : Introduction to Logic Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day6)
-  [Day7 : Basic SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD#Day7)
-  [Day8 : Advanced SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD#Day8)
-  [Day9 : Optimization in Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day9)
-  [Day10 : QOR](https://www.github.com/Usha-Mounika/Samsung_PD#Day10)
-  [Day11 : Introduction to BabySoC](https://www.github.com/Usha-Mounika/Samsung_PD#Day11)
-  [Day12 : BabySoC Modelling](https://www.github.com/Usha-Mounika/Samsung_PD#Day12)
-  [Day13 : Post-Synthesis Simulation](https://www.github.com/Usha-Mounika/Samsung_PD#Day13)
-  [Day14 : Synopsys DC and timing analysis](https://www.github.com/Usha-Mounika/Samsung_PD#Day14)


## [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)

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

 ## [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)
 
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

## [Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles](https://www.github.com/Usha-Mounika/Samsung_PD#Day2)
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

## [Day3 : Combinational and Sequential Optimizations](https://www.github.com/Usha-Mounika/Samsung_PD#Day3)

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

## [Day4 : GLS,blocking vs non-blocking and Synthesis Simulation mismatch](https://www.github.com/Usha-Mounika/Samsung_PD#Day4)
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

## [Day5 : DFT](https://www.github.com/Usha-Mounika/Samsung_PD#Day5)
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

## [Day6 : Introduction to Logic Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day6)
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

## [Day7 : Basic SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD#Day7)
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

## [Day8 : Advanced SDC Constraints](https://www.github.com/Usha-Mounika/Samsung_PD#Day8)

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

## [Day9 : Optimization in Synhesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day9)
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

## [Day10 : QOR](https://www.github.com/Usha-Mounika/Samsung_PD#Day10)
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

## [Day11 : Introduction to BabySoC](https://www.github.com/Usha-Mounika/Samsung_PD#Day11)
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

## [Day12 : BabySoC Modelling](https://www.github.com/Usha-Mounika/Samsung_PD#Day12)
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

## [Day13 : Post-Synthesis Simulation](https://www.github.com/Usha-Mounika/Samsung_PD#Day13)
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

## [Day14 : Synopsys DC and Timing Analysis](https://www.github.com/Usha-Mounika/Samsung_PD#Day14)
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
	
The Timing delay of a path varies for each PVT corner being used. Let us consider the following corners and their delays as follows:
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

</details>
