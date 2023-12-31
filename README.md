# Iswarya_asic_course  
# Table of Contents
 - [Day0 - Tools Installation](#Tools-Installation)<br>
 - [Day1 - Introduction to Verilog RTL design and synthesis](#Introduction-to-Verilog-RTL-design-and-synthesis)<br>
 - [Day2 - Timing labs,hierarchial vs flat synthesis and efficient flop coding styles](#Timing-labs,hierarchial-vs-flat-synthesis-and-efficient-flop-coding-styles)<br>
 - [Day3 - Combinational and Sequential Optimizations](#Combinational-and-Sequential-Optimizations)<br>
 - [Day4 - GLS,Blocking vs Non-Blocking and synthesis-simulation mismatch](#GLS,Blocking-vs-Non-Blocking-and-synthesis-simulation-mismatch)<br>
 - [Day5 - If,case,for loop and for generate](#If,case,for-loop-and-for-generate)<br>
  
# Day 0

# Tools Installation
<details>
<summary>
    Yosys
  </summary> 

    
  I installed Yosys using the following commands: 
  
    
```
    
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys-master 
$ sudo apt install make (If make is not installed please install it) 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make 
$ sudo make install

```

Below is the screenshot showing successful installation: 


![Screenshot from 2023-07-31 10-15-12](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/67cfade5-3e17-4374-89ff-93c64bce279f)



Below is the screenshot showing successful launch:

![Screenshot from 2023-07-31 10-21-57](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/8a6b68b0-d58c-403c-92a3-2a820a273b24)


</details>
<details>
<summary>
        iverilog
</summary>
I installed iverilog using the following command:

```

$ sudo apt-get install iverilog

```

Below is the screenshot showing successful installation:


![Screenshot from 2023-07-31 21-32-19](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/cdd3a329-79a3-490f-b3c9-b5463d1a9f1c)

Below is the screenshot showing successful launch:



![Screenshot from 2023-07-31 21-32-34](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/5e531280-719f-4b3c-ba58-dbd69cd72061)


    
</details>
<details>
    <summary>
        gtkwave
    </summary>
    I installed gtkwave using the following command:

```

$ sudo apt update
$ sudo apt install gtkwave

```

Below is the screenshot showing successful installation:


![Screenshot from 2023-07-31 21-40-40](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/10ebb750-f2e9-4682-b8b8-6d19de17dfae)

Below is the screenshot showing successful launch: 

![Screenshot from 2023-07-31 21-41-31](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/52180ab8-a498-4974-8ab7-03ef29a9c3b4)

</details>

<details>
 <summary>
   Ngspice
 </summary>
 
 **Source File** - https://sourceforge.net/projects/ngspice/files/

 Installation Commands:

 ```

$ sudo apt-get install build-essential
$ sudo apt-get install libxaw7-dev

$ tar -zxvf ngspice-41.tar.gz
$ cd ngspice-41
$ mkdir release
$ cd release
$ ../configure  --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install

```

Below is the screenshot showing successful launch: 

![ngspice](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/567096d8-8469-47c8-8a27-1761424ecb0e)

</details>

<details>
 <summary>
   OpenSTA
 </summary>

 Installation commands:

 ```

$ sudo apt-get install cmake clang gcc tcl swig bison flex

$ git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
$ cd OpenSTA
$ mkdir build
$ cd build
$ cmake ..
$ make
$ sudo make install

```

Below is the screenshot showing successful launch: 

![OpenSTA](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/2f4e41da-513c-47fa-bc34-d1b919020936)


</details>

<details>
 <summary>
   Magic
 </summary>

 Installation Commands:

 ```

$ sudo apt-get install m4
$ sudo apt-get install tcsh
$ sudo apt-get install csh
$ sudo apt-get install libx11-dev
$ sudo apt-get install tcl-dev tk-dev
$ sudo apt-get install libcairo2-dev
$ sudo apt-get install mesa-common-dev libglu1-mesa-dev
$ sudo apt-get install libncurses-dev
$ git clone https://github.com/RTimothyEdwards/magic
$ cd magic
$ ./configure
$ make
$ sudo make install

```

Below is the screenshot showing successful launch: 

![magic](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/4de90634-e24c-45b9-9c1e-0918c4e7d9a3)

</details>

<details>
 <summary>
   OpenLANE
 </summary>

 Docker Installation:

 ```
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt install -y build-essential python3 python3-venv python3-pip make git

$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
$ sudo docker run hello-world

$ sudo groupadd docker
$ sudo usermod -aG docker $iswarya
$ sudo reboot 

# Check for installation
$ sudo docker run hello-world

```

Below is the screenshot showing successful launch:

![docker](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/710d02e2-0ac9-4ff4-8cf0-f56d05b32eb5)

Install OpenLANE,PDKs and Tools

```

git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test

```
</details>

# Day 1

# Introduction to Verilog RTL design and synthesis
<details>
    <summary>
        Introduction to iverilog design testbench
    </summary>

    

**Simulator:**

It is a a device that enables the operator to reproduce or represent under test conditions phenomena likely to occur in actual performance.
iverilog is the simulator used for this course.

**How Simulator works**

- Simulator looks for the change in the values of input.
* Upon change to the input,output is evaluated.

**iverilog:**

Icarus Verilog is a compiler that translates Verilog source code into executable programs for simulation.

**iverilog based simulation flow**

![Screenshot from 2023-08-13 22-36-54](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a8b3e981-7319-49e5-8265-a0e93d06b646)

**Testbench:**

A conventional Verilog testbench is a code module that describes the stimulus to a logic design and checks whether the design's outputs match its specification.

![Screenshot from 2023-08-13 22-34-39](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/6d813524-1fd4-4c11-8877-aa934f363536)
</details>

<details>
    <summary>
        Labs using iverilog and gtkwave
    </summary>

**1.Introduction to Labs**

Lab setup is made using the following link:

```
https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git

```


![Screenshot from 2023-08-13 23-35-59](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/64edcb4b-85fb-48a6-939a-d833b750d707)

**2.Introduction to iverilog gtkwave**

A 2×1 multiplexer is used as an example for explaining how iverilog and gtkwave works.It initially creates a a.out file which eventually opened a dumpfile(tb_good_mux.vcd) for producing output.

The following commands are used for producing output:

```
$ iverilog  good_mux.v  tb_good_mux.v
$ ./a.out
$ gtkwave tb_good_mux.vcd

```

![Screenshot from 2023-08-13 23-52-48](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/55419881-5dd1-482f-bac5-f0b9e6701245)

**Output Waveform**

![Screenshot from 2023-08-13 23-54-09](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/34fc7a17-2c4b-4aca-b529-370bfa6dad81)
</details>
<details>
    <summary>
        Introduction to Yosys and Logic Synthesis
    </summary>
    
**Introduction to Yosys**

**Logic Synthesis**

RTL to gate level translation is called as synthesis.The design is converted into gates and connections are made between gates.This is given as a file called netlist.


**Synthesizer:**

Synthesizer is the tool used for synthesis.
Synthesis in VLSI is the process of converting your code (program) into a circuit. In terms of logic gates, synthesis is the process of translating an abstract design into a properly implemented chip. Hardware Description Languages (HDLs) are specific programming languages that are used to explain the hardware of a circuit.
Yosys is used as synthesizer in this course.


**Netlist:**

Netlist is also a description of a design written using a HDL code when it is written in an RTL style.The netlist is then supposed to perform the same function as the corresponding HDL code. The netlist out of the synthesis tool is fed into layout tools to produce the layout of the chip.

**RTL Design**
RTL (register-transfer level) design is a hardware design methodology that describes the behavior of digital circuits in terms of the flow of data between registers, and the operations that are performed on that data as it moves through the circuit.

**.lib**

A standard cell library is a collection of well defined and appropriately characterized logic gates that can be used to implement a digital design.The library files contain different flavours of standard gate which maybe like 2 input or 3 input gate with slower or medium or faster version of it.


**Yosys Setup**

![Screenshot from 2023-08-14 00-16-36](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/0bb3b3fa-6654-40da-b7d3-41c37ca9cc34)

**Verify the synthesis**

![Screenshot from 2023-08-14 00-18-11](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/b8e8725b-8ffe-4ae2-a8ee-e4374e2e5856)
</details>

<details>
    <summary>
        Labs using Yosys and Sky130 PDKs
    </summary>
    
Invoke and Synthesis using following commands:

**Invoke**

```
$ yosys
```

![Screenshot from 2023-08-14 01-28-49](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/1193e665-0f8d-4c5c-a134-c49a29104b11)

**Read the library**

```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
**Read the design**

```
read_verilog good_mux.v
```
**Model Synthesis**

```
synth -top good_mux
```

**Generate Netfile**

```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

**abc** is used to convert RTL file into gate design.

![Screenshot from 2023-08-14 01-46-57](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/867864e3-11fb-48c6-bde6-65160a41fa62)

**Graphical Version of Logic realized**

```
show
```

![Screenshot from 2023-08-14 01-51-43](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a65a2f5c-e48c-4989-9edb-7ffeafc84a07)

**How to write Netlist**

```
write_verilog good_mux_netlist.v
write_verilog -noattr good_mux_netlist.v


```
</details>

# Day 2
# Timing labs,hierarchial vs flat synthesis and efficient flop coding styles
<details>
    <summary>
        Introduction to Timing Labs
    </summary>

The following command is used to open .lib file in gvim:


```
$ gvim ../lib/sky130_fd_sc_hd__tt_025C_1v80
```

![Screenshot from 2023-08-14 10-59-50](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/7e7cddf1-817c-46fd-b82a-045bb4a68248)

The .lib files contains main element called **PVT**

**PVT:**

PVT in VLSI stands for Process, Voltage, and Temperature. Integrated circuits are designed in such a way so that they can function in a wide variety of temperatures and voltages, rather than a single temperature and voltage.

-PVT determines how my silicon is going to work under different conditions.

The .lib files also contains the details of standard cells which has the information of what are the gates used and its power values and its area.If the area of the gate is larger it means wider transistor is used which refers to more power consumption.

</details>
<details>
    <summary>
        Hierarchial vs Flat Synthesis
    </summary>

**Hierarchial Synthesis**

A hierarchical design approach divides the ASIC into smaller and simpler modules or blocks, each with its own functionality and interface, and then connects them by a top-level structure that defines the overall behavior and performance of the ASIC.

**Advantages:**

+ This approach has several advantages, such as better modularity, reusability, and scalability of the design
+ reduced complexity and size of the design
+ facilitation of parallelism and teamwork
+ improved quality and reliability of the design

**Disadvantages:**

+ requiring more planning and coordination
+ introducing more overhead and latency
+ potentially limiting optimization and performance

Commands used for Hierarchial Synthesis:

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog multiple_modules.v
synth -top multiple_modules
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show multiple_modules
write_verilog -noattr multiple_modules_hier.v
!gvim multiple_modules_hier.v
```

**Flat Synthesis**

A flat design approach treats the ASIC as a single, monolithic entity, without any submodules or levels of hierarchy, and uses basic components like gates, transistors, and wires. 

**Advantages:**

+ more flexibility and creativity for the designer to explore solutions and alternatives without restrictions
+ more optimization and performance
+ reducing overhead and latency


**Disadvantages:**

+ increases complexity and size of the design,
+ hinders parallelism and teamwork
+ can compromise quality and reliability
+ the design is harder to verify and test as a whole

Commands used for Flat Synthesis:

```
$ yosys
flatten
write_verilog -noattr multiple_modules_flat.v
!gvim multiple_modules_flat.v
show multiple_modules_flat
```
</details>
<details>
    <summary>
        Flop coding styles and optimization
    </summary>

Flop is a circuit that maintains a state until directed by input to change the state.

**Why flops**
Combinational circuits have glitches due to propagation delay.If there are multiple combinational circuits in a design ,the output of the design have more glitches in it.To avoid glitches,we are introducing flops inbetween combinational circuits .Flops have clock cycles to work which helps in restricting glitches from the input for providing satble output.

If the initial state of the flop is unknown ,the combinational circuit will evaluate into garbage value.So initializing the flop is an important thing.

The control pins in the flop known as Reset/Set is used to initialize the flop.Reset/Set can be synchronous or asynchronous.

**Lab flop synthesis simulations**

1.Using Asynchronous Reset

Commands used:

```
$ iverilog dff_asyncres.v tb_dff_asyncres.v
$ ./a.out
$ gtkwave tb_dff_asyncres.vcd 
```

![Screenshot from 2023-08-14 14-56-09](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/8f1b3c5b-90e5-4d76-8394-f30e3ac50c35)

**Synthesis**

![Screenshot from 2023-08-14 15-15-53](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/ed3ac152-5d28-4490-9613-78d94be44d0d)

2.Using Asynchronous set

Commands used:

```
$ iverilog  dff_async_set.v tb_dff_async_set.v
$ ./a.out
$ gtkwave tb_dff_async_set.vcd
```

![Screenshot from 2023-08-14 15-01-42](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a02ef81f-8a62-4e3b-a470-67a6360eecb4)

**Synthesis**

![Screenshot from 2023-08-14 22-45-39](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/abb5f936-cdc4-486f-8b15-e88efadabdf5)

3.Using Synchronous Reset

Commands used:

```
$ iverilog dff_syncres.v tb_dff_syncres.v
$ ./a.out
$ gtkwave tb_dff_syncres.vcd
```

![Screenshot from 2023-08-14 15-08-22](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/bb581545-b984-4c5f-a606-9f9cf12a12a3)

**Synthesis**

![Screenshot from 2023-08-14 23-12-46](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/38830b5f-4ba4-4741-b375-6059a299655d)

</details>

# Day 3
# Combinational and Sequential Optimizations
<details>
    <summary>
        Introduction to Optimizations
    </summary>

**Logic optimization** 

It is a process of finding an equivalent representation of the specified logic circuit under one or more specified constraints. This process is a part of a logic synthesis.

There are two types of logic optimization

1.Combinational logic optimization

2.Sequential logic optimization

**Combinational Logic Optimization**

- It is mainly for squeezing the logic into most optimized design in terms of area and power savings.
 
- It uses two techniques for optimization.

    1.Constant Propagation(Direct Optimization)
  
    2.Boolean Logic Optimization

**Constant Propagation**

Boolean minimization may lead to dissolution of certain section of code into constants. Such constants should be propagated at this stage in order to reduce gate count and area.

**Boolean Logic Optimization**

The optimization of a complex boolean expression is a process of finding a simpler one, which would upon evaluation ultimately produce the same results as the original one.

**Sequential Logic Optimization**

Precomputation is a recently proposed logic optimization technique which selectively disables
the inputs of a sequential logic circuit, thereby reducing switching activity and power dissipation,
without changing logic functionality.

There are two techniques used for optimisation.

1.Basic 

- Sequential Constant Propagation

2.Advanced

- State Optimisation
- Retiming 
- Sequential Logic Cloning
</details>

<details>
    <summary>
        Combinational Logic Optimizations
    </summary>
    
Commands used for opt_check2.v

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog opt_check2.v
synth -top opt_check2
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show 
```

**Synthesis**

![Screenshot from 2023-08-15 01-07-03](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/dc42f2e9-7caa-491b-935a-0fcfb0f3517b)

Commands used for multiple_module_opt2.v

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog multiple_module_opt2.v
synth -top multiple_module_opt2
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show multiple_module_opt2
```

**Synthesis**

![Screenshot from 2023-08-15 01-19-15](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/dc19e3bb-02c5-4460-8cfb-8806d7b3c3cb)
</details>

<details>
    <summary>
        Sequential Logic Optimization
    </summary>

**dff_const1**

![Screenshot from 2023-08-15 01-29-12](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/4ca2441b-b972-484c-97b4-7abbb7d32fc8)

**Output Waveform**

![Screenshot from 2023-08-15 01-30-36](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/2bcd75d2-ca76-4087-ad09-75df97225d92)

**Invoke Yosys**

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog dff_const1.v
synth -top dff_const1
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show 
```

**Synthesis**

![Screenshot from 2023-08-15 01-35-56](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/c931c718-b9fc-48b6-9c77-9ee3165975a0)

**dff_const3**

```
$ iverilog dff_const3.v tb_dff_const3.v
$ ./a.out
$ gtkwave tb_dff_const3.vcd
```

**Output Waveform**

![Screenshot from 2023-08-15 01-48-03](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a62efb51-e8ff-4090-b420-f8621e9b66be)

**Invoke Yosys**

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog dff_const3.v
synth -top dff_const3
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show 
```

**Synthesis**

![Screenshot from 2023-08-15 01-49-25](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/4eb16daa-5819-4425-9ffb-e7397f3827f3)
</details>
<details>
    <summary>
        Sequential optimizations for unused outputs
    </summary>

**Verilog code for counter**

![Screenshot from 2023-08-15 02-02-04](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/7a752588-3ba3-4a39-aa3d-3bb7567f4d2c)

**Invoke Yosys**

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog counter_opt.v
synth -top counter_opt
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show 
```

**Synthesis**

![Screenshot from 2023-08-15 02-02-52](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/cdb60b7d-945a-4055-a837-09e2a5d6ad57)

**Modified verilog code for counter**

![Screenshot from 2023-08-15 02-29-29](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a60614b2-f197-4e6d-88f2-c600f84aa066)

**Invoke Yosys**

```
$ yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog counter_opt2.v
synth -top counter_opt
opt_clean -purge
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show 
```

**Synthesis**

![Screenshot from 2023-08-15 02-27-37](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/35f06226-8440-4ec5-941b-04381f689123)
</details>

# Day 4
# GLS,Blocking vs Non-Blocking and synthesis-simulation mismatch
<details>
    <summary>
        GLS,Synthesis-Simulation mismatch and Blocking/Non-Blocking statements
    </summary>

**Gate Level Simulation**

The term "gate level" refers to the netlist view of a circuit, usually produced by logic synthesis. So while RTL simulation is pre-synthesis, GLS is post-synthesis. The netlist view is a complete connection list consisting of gates and IP models with full functional and timing behavior.

**Why GLS**

- Verify the logic correctness of design after synthesis.
- Ensuring the timing of the design is met(For this GLS needs to be run with delay annotation)

**GLS using Verilog**

![Screenshot from 2023-08-15 08-04-57](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/d158213c-dc0b-4e4a-ba89-ad0c8e5048cc)

If Gate level models are delay annotated, then we can use GLS for timing validation.

**Synthesis Simulation Mismatch**

Verilog coding styles that will cause a mismatch between prea nd post-synthesis simulations.

Synthesis Simulation Mismatch happens due to certains reasons like,

- Missing Sensitivity List
- Blocking vs Non-Blocking Assignments
- Non standard Verilog coding

**Blocking and Non-Blocking Statements**

**Blocking assignment** statements are assigned using (=) operator and are executed one after the other in a procedural block. But, it will not prevent the execution of statements that run in a parallel block.

**Non-blocking assignment** statements are allowed to be scheduled without blocking the execution of the following statements and is specified by a (<=) symbol.

**Note:**

Always use non-blocking statements for writing sequential circuits.
</details>
<details>
    <summary>
        Labs on GLS using sythesis-simulation mismatch
    </summary>

**Code**

![Screenshot from 2023-08-15 15-19-19](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/817feb67-dfba-4447-8916-f0a3ae87c74c)

**Screenshot of commands used:**

![Screenshot from 2023-08-15 14-19-05](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/aa2705e9-e94d-4501-9683-6f84e7aa9597)

**Output Waveform**

![Screenshot from 2023-08-15 14-18-08](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/ca8d5107-aae3-45bf-85a0-4a74165ac392)

**Synthesis**

![Screenshot from 2023-08-15 14-21-53](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/b895ab69-d85f-4add-93ed-4fe880058110)

Commands used to produce gtkwave using GLS

```
$ iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v ternary_operator_mux_net.v tb_ternary_operator_mux.v
$ ./a.out
$ gtkwave tb_ternary_operator_mux.vcd
```

**Output Waveform using GLS**

![Screenshot from 2023-08-15 15-04-08](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/6f772d94-8405-430e-8e8a-73bea2233951)
</details>
<details>
    <summary>
        Labs on synthesis-simulation mismatch using blocking statement
    </summary>
    
**Code**

![Screenshot from 2023-08-15 15-28-38](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/c6f9c5c9-b387-406f-991f-98455d8886b1)

Commands:

```
$ iverilog blocking_caveat.v tb_blocking_caveat.v
$ ./a.out
$ gtkwave tb_blocking_caveat.vcd
```

**Output Waveform**

![Screenshot from 2023-08-15 15-31-54](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/4f165739-46b8-4ab0-845d-3b14bee67b59)

**Synthesis**

![Screenshot from 2023-08-15 15-39-39](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/7df58edf-09c8-4814-be7a-c475b6fd97b8)


Commands used to produce gtkwave using GLS

```
$ iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v blocking_caveat.v tb_blocking_caveat.v
$ ./a.out
$ gtkwave tb_blocking_caveat.vcd
```

**Output Waveform using GLS**

![Screenshot from 2023-08-15 15-42-42](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/21477b62-f2ee-4490-ad7e-b320a3038e8b)
</details>

# Day 5
# If,case,for loop and for generate
<details>
    <summary>
        IF CASE Constructs
    </summary>

**IF Statements**

The 'If' statement is a conditional statement based on which decision is made whether to execute lines inside if block or not. The begin and end are required in case of multiple lines present in if block. For single-line inside if statement may not require 'begin.. end'.

Danger/Caution with IF statements are Inferred Latches.
Latches are inferred in VHDL by using the IF statement without its matching ELSE. This causes the synthesis to make the logical decision to “hold” the value of a signal when not told to do anything else with it. The inferred latch is a transparent latch.


**CASE Statements**

The case statement checks if the given expression matches one among the other expressions inside the list and branches.In Verilog, a case statement includes all of the code between the Verilog keywords, case ("casez", "casex"), and endcase.
</details>
<details>
    <summary>
        Labs on "Incomplete IF Case"
    </summary>

**Code**

![Screenshot from 2023-08-15 22-19-56](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/76ceca07-4488-4ab5-9342-0e1499c26802)

**Output Waveform**

![Screenshot from 2023-08-15 22-20-53](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/aad72fce-0862-4ff3-9e83-24f530e436b7)

**Synthesis**

![Screenshot from 2023-08-15 22-22-13](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/2f642e6a-8b97-437e-aa56-e3ef3f22a9af)
</details>
<details>
    <summary>
        Incomplete Overlapping Case
    </summary>

**Code for incomp_case**

![Screenshot from 2023-08-15 22-43-19](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/e8ef9814-54f6-4348-8ff2-57d538cc0aa1)

**Output Waveform**

![Screenshot from 2023-08-15 22-45-09](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/4edd256a-5a3f-4caa-8a32-4d62ae49d8d1)

**Synthesis**

![Screenshot from 2023-08-15 22-46-13](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/1a1c80ca-942d-490e-97f1-d06e5848b110)

**Code for comp_case**

![Screenshot from 2023-08-15 22-50-31](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/75adf9c0-767b-40fa-a79f-cfc38a037837)

**Output Waveform**

![Screenshot from 2023-08-15 22-52-23](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a5318bb6-32da-4ef4-873e-69f82bf421be)

**Synthesis**

![Screenshot from 2023-08-15 22-53-22](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/e922e77a-3c54-4973-85a6-5602fc70aef9)

**Code for bad_case**

![Screenshot from 2023-08-15 22-57-22](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/2b24cd14-b7fd-4953-a973-d7e626f14ef6)

**Output Waveform**

![Screenshot from 2023-08-15 22-58-09](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a4c42a67-6489-4e8f-b77d-19454961683b)

**Synthesis**

![Screenshot from 2023-08-15 22-58-46](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/1357244e-5187-4e11-8b38-afaf1f4030e2)
</details>
<details>
    <summary>
        For Loop and For Geneerate
    </summary>

**For Loop**

A for loop is the most widely used loop in software, but it is primarily used to replicate hardware logic in Verilog. The idea behind a for loop is to iterate a set of statements given within the loop as long as the given condition is true.

**For Generate**

A generate block allows to multiply module instances or perform conditional instantiation of any module. It provides the ability for the design to be built based on Verilog parameters.

</details>
<details>
    <summary>
        Labs for "For Loop" and "For Generate"
    </summary>

**Code for mux_generate**

![Screenshot from 2023-08-15 23-08-49](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/51c9ab12-5a28-4549-8fa9-2f5275deca5b)

**Output Waveform**

![Screenshot from 2023-08-15 23-09-58](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/98383599-9587-4566-b36c-be4f2f123198)

**Synthesis**

![Screenshot from 2023-08-15 23-10-48](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/fe8640b8-358f-4ca7-aecf-7a8549affbfd)

**Code for demux_case**

![Screenshot from 2023-08-15 23-14-40](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/dd08b864-6d8d-44e9-b312-b08803bbf4f3)

**Output Waveform**

![Screenshot from 2023-08-15 23-15-35](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/63fe486d-87ea-4e71-8a50-73437cc6987c)

**Synthesis**

![Screenshot from 2023-08-15 23-16-34](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/cd4f7382-82da-4c05-afd4-b552022bac07)

**Code for fa rca**

![Screenshot from 2023-08-15 23-19-35](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/7426c3f6-2fcb-4998-a189-df7462ef4b11)

**Output Waveform**

![Screenshot from 2023-08-15 23-22-58](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/eab9abc4-137b-45e9-b9fe-c65498917da0)

</details>


