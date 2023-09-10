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
  ![latency](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/b4383dc6-badb-427f-8cc6-de685b4ba6bf)

- Clock Skew : Clock path delay mismatches which causes difference in the arrival of the clock.
- Jitter : Stochastic variations in the arrival of clock edge.
The clock network is practical post CST stage. So, the modelled network latency and skew must be removed as the actual clock network is present now. This removes the extra pessimism defined.
#### Skew
In ideal case, the clock is assumed to arrive at launch and capture flops at the same time. In the practical design, the clock is at fixed position and the flipflops are placed such that place is optimized. 
But there will be a delay (∆) to reach the distant (capture) flop than the nearer (launch) flop when routed.If the nets are long, there will be buffers placed causing delay, so clock may take more time to reach. So, this would cause a violation reducing the arrival time.

*Skew is the difference in clock arrival time across the chip*.
Let us consider a clock arriving to two flops launch with two clock buffers and capture with one buffer. This would reduce available window by one buffer delay period.So, the timing may be clean post synthesis, but it fails after CTS.
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
 #### Clock uncertainty and latency
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

The *report_port* gives the information about all the constraints on the port.The following image shows all the consraints on the port.
![report_port](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/a6a1acec-72bb-49a8-b0a4-0170d6b30ecd)

The following image shows that in2reg and reg2out paths are unconstrained as IO constraints are not defined yet.
![uncon io path](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/9a577ff5-9ec1-4bb2-b101-66f5cb3de9ae)

#### IO constraints


 
</details>
