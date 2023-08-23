# Physical Design Training

A brief description of what this training summarizes : 

- [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)
- [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)
- [Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles](https://www.github.com/Usha-Mounika/Samsung_PD#Day2)

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
-The following comparison shows that the same **AND gate** has three diferent flavors.
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
Step-1: Load the yosys tool by giving yosys command
```bash
$yosys
```
Step-2: Inorder to run yosys, we need two inputs verilog file and .lib file. So, These inputs were given using read_verilog and read_liberty thus successfully finishing frontend
```bash
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog multiple_modules.v
```
Step-3: Inorder to synthesize the netlist, we use **synth -top** command to synthesize the toplevel module. This gives the count of no. of bits, wires, inputs,cells etc...
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
The flattened nelist is the netlist where the hierarchies (or submodules) are are replaced by the actual gates logic present in those sub modules. Inorder to generate the flattened netlist the first 3 steps were same. In the step-4,
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
In a combinational logic design, the change in input is seen at the output after the propagation delay. During the propagation of data, if there are more cells of different delays, this might cause a glitch in the output. If this combinational logic has more cells, this would cause an unstable output.Inorder to avoid these glitches, the flops are used between the cmobinational design.
The flip-flop is a single bit storage device used between the combinational circuit to avoid glitches in the output.When a flop is used, the output of the previous stage is stored until there is a posedge or negedge triggered at the clock so the combinational circuit avoids glitches at the output as each stage is sort of shielded from input to output by the clock.
The signals such as set or reset are used to initialise the flops otherwise any (previous value) garbage value could be propagated to next stage. These signals can be asynchronous or synchronous.
### Lab on flop synthesis:
Inorder to generate the gtkwave using iverilog, the following sequence of steps are followed:
```bash
$iverilog dff_asyncres.v tb_asyncres.v
$./a.out
$gtkwave tb_dff_asyncres.vcd
```
The **./a/out** generates a vcd output file that can be viewed with gtkwave
Inorder to generate the synthesized circuit, the following sequence of steps are followed:
```bash
$yosys
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_asyncres.v
yosys> synth -top dff_asyncres
yosys> dff_libmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
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

**Synchronous reset**:
The synthesized circuit is as follows:
![dff_syncres show](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/f475f1b5-2d30-4f13-98b3-b1a1c662d7c8)

</details>
