# Physical Design Training

A brief description of what this training summarizes : 

- [Day0 : Setup Check](https://www.github.com/Usha-Mounika/Samsung_PD#Day0)
- [Day1 : Introduction to Verilog RTL Design and Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day1)
- [Day2 : Timing Libs, hierarchical vs flat synthesis and efficient flop coding styles](https://www.github.com/Usha-Mounika/Samsung_PD#Day2)
-  [Day3 : Combinational and Sequential Optimizations](https://www.github.com/Usha-Mounika/Samsung_PD#Day3)
-  [Day4 : GLS,blocking vs non-blocking and Synthesis Simulation mismatch](https://www.github.com/Usha-Mounika/Samsung_PD#Day4)
-  [Day5 : DFT](https://www.github.com/Usha-Mounika/Samsung_PD#Day5)
-  [Day6 : Introduction to Logic Synthesis](https://www.github.com/Usha-Mounika/Samsung_PD#Day6)

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
 - Logic Synthesis tries to achieve a working digital circuit which is logically and electrically correct by meeting the timing specifications. Let us consider an example to understand.
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

We know that the library name consists of the information such as PVT (Process, Voltage, temperature) conditions of design. Every electronic circuit operation is a function of voltage, temperature and process.
The .lib is specified for each PVT corner.This PVT corner is a typical, 25c temperature and 1.8V. This .lib file gives information such as units of R,L,C, time & type of technology used and the various flavors of each cell etc... 
The dc shell is invoked using following commands:
```bash
$ csh
$ dc_shell
dc_shell> 
```
We need to enable cshell and then invoke DC shell. The DC shell checks the license of various compilers like VHDL compiler,HDL compiler(to understand the verilog or any other HDLs), DFT compiler(as DC enables scan stitich), Design vision(graphical version of DC), Power Compiler(as it is power aware synthesis) etc... This can be illustrated as follows:

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
dc_shell> write -f verilog -out lab1_net.v
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
dc_shell> sh gvim lab1_net.v &
```
Now the out netlist is as follows: 
The cells are in SEQGEN but not as sky130 cells format. This happens because target & link library not assigned any file.
**gtech** is the virtual library in DC's memory to understand the design.
```bash
dc_shell> set target_library /home/usha.m/DC_WORKSHOP/lib/sky130_fd_sc_hd_tt_025c_1v80.db
dc_shell> set link_library {* <path to standardcell library> }
dc_shell> link
dc_shell> compile
dc_shell> write -f verilog -out lab1_net_with_sky130.v
```
Now by assigning the files to the libraries, the design is linked and compiled as follows. Here, the link_library is assigned such inorder to append to the pre-existing list data without overwriting it.
Now the outnetlist obtained is as follows.

#### Lab on ddc gui with design_vision
Inorder to launch the design vision, we again load cshell and **design_vision** command. This will launch the gui format of DC shell called design_vision.
The command to write out a ddc file as output of dc_shell after writing out netlist is:
```bash
dc_shell> write -f ddc -out lab1_flop.ddc
```
The following image shows the design_vision loaded with gui. If the gui is not opened, you can use *start_gui* command.

The ddc automatically loads the technology file and current design without specifying. ddc stores all the information in the tool memory in that particular session. But, ddc is a synopsys proprietary format, i.e., it can only be understood by Synopsys tools. The main advantage of ddc is all the information loaded in one tool can be saved and used in another tool with one command *read_ddc*.*read_verilog* reads only the verilog file. 
The following image shows the loaded read_ddc and read_verilog command. In the *read_ddc*, you can find the .db file loaded without specifying whereas, *read_verilog* command loads only the design data.
The final behavior of the circuit is as follows (displayed with ddc gui) is:
 
#### Lab on .synopsys dc setup
Invoking the dc shell using csh, dc_shell commands. When a session is loaded, the target_library and link_library variables must be set everytime. In the real-time scenario, we will have multiple .db files for a design and we cannot miss them.
So, Setting these both variables everytime would be cumbersome and error-prone. This can be overcome by **.synopsys_dc.setup**.
There are two versions of .synopsys_dc.setup in dc_shell. 

 -  When dc_shell is installed, there will be .synopsys_dc.setup in the folder
 -  When dc_shell is invoked,  the shell looks for it in user_home_directory
The order of priority is, if file exists in user_home_directory, will be picked and the installed (default) is ignored. If not found, then installed one is picked.
All repetitive tasks which are needed for tool setup can be pointed in this file (mainly target_library, link_library).When the tasks are defined in this file, the tool automatically picks these values and load it in tool memory.
So, This can be done by creating a file with this name and loading the shell as follows:
```bash
$ gvim .synopsys_dc.setup
$dc_shell
dc_shell> echo $target_library
```
The same can be illustrated as follows:


</details>

<details>
<summary>TCL Scripting</summary>
<br>	
Tool Command Language is used for writing SDCs.
	
### Basic commands in TCL

The tcl is typed language i.e., all gaps and paranthesis should be properly followed.

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
  
```tcl
foreach_in_collection var collection {
   statements
 }
```

![foreach ex](https://github.com/Usha-Mounika/Samsung_PD/assets/142480150/8095eadc-d52b-42ca-bd4a-f341afb2e06e)

In the above example, the nesting of commands can be seen. The output of one variable is used to obtain another variable output.
#### Lab on TCL scripting







</details>
