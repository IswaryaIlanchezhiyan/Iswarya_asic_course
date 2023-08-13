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

**iverilog**

Icarus Verilog is a compiler that translates Verilog source code into executable programs for simulation.

**iverilog based simulation flow**

![Screenshot from 2023-08-13 22-36-54](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/a8b3e981-7319-49e5-8265-a0e93d06b646)

**Testbench**

A conventional Verilog testbench is a code module that describes the stimulus to a logic design and checks whether the design's outputs match its specification.

![Screenshot from 2023-08-13 22-34-39](https://github.com/IswaryaIlanchezhiyan/Iswarya_asic_course/assets/140998760/6d813524-1fd4-4c11-8877-aa934f363536)





    
</details>
