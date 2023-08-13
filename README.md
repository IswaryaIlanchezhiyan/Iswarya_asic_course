# Iswarya_asic_course
#Day 0
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

sudo apt update
sudo apt install gtkwave

```

Below is the screenshot showing successful installation:


![Screenshot from 2023-07-31 21-40-40](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/10ebb750-f2e9-4682-b8b8-6d19de17dfae)

Below is the screenshot showing successful launch:

![Screenshot from 2023-07-31 21-41-31](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/52180ab8-a498-4974-8ab7-03ef29a9c3b4)

</details>

#Day 1
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

```
$ yosys
```

![Screenshot from 2023-08-14 01-28-49](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/1193e665-0f8d-4c5c-a134-c49a29104b11)

</details>
