# VSD_SOC_NASSCOM

Day 1 - Introduction and Invoking the openlane

In today’s era, everyone has heard the word chip. Somewhere in the news or on social media. The electronics world works on these small chips. To find a chip you need to find a PCB board, which can be found easily around you. For example, Tv, Computer, A.C., Smartphones, and the list goes on. Or simply you can refer to the following image which shows a PCB board Arduino

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/5339b5b5-bdf0-4f9a-a49b-8f7d36141aca)

The yellow circled mark is an Integrated circuit. The chip is inside that package.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/9a498be7-abbb-4438-9c6d-159fd23fa717)

The Size of the package is 7x7 mm. It consists of 48 pins. The package type is QFN (Quad Flat No-leads).
There are different packages available such as BGA, SOIC, LGA, QFP, etc. But for our project, we are going to discuss the QFN package.
The chip is inside the package. It is connected with the outside world with the help of pads. The pads are the 48pins which are seen in the above figure.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ef84c0bf-78e3-4a62-a7f5-cfccae34dcc9)

A chip consists of a Die, core area, Pads, IPs, Macros, and std cells.

So the question arises why do we need chips?
Chips do all the computation work and make our lives easy. Let's take an example of a stopwatch.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/a2376857-eade-4116-9c99-5d84dd1eeacd)

The Application or software is written in some language such as C, C++, or Java (human language/ coding language). The OS (System Software) with the help of a compiler converts those coding statements into Instruction sets which are again converted to Machine language (Binary numbers 0’s or 1’s) with the help of an assembler. The Hardware(chip) will understand the program and will produce the output.


ISA (Intruction Set Architecture)
A C program which has to be run on a specific hardware layout which is the interior of a chip in your laptop, there is certain flow to be followed.
Initially, this particular C program is compiled in it's assembly language program which is nothing but RISC-V ISA (Reduced Instruction Set Compting - V Intruction Set Architecture).
Following this, the assembly language program is then converted to machine language program which is the binary language logic 0 and 1 which is understood by the hardware of the computer.
Directly after this, we've to implement this RISC-V specification using some RTL (a Hardware Description Language). Finally, from the RTL to Layout it is a standard PnR or RTL to GDSII flow.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/4740cdf5-6d22-441e-a334-0d70d11aa609)

* For an application software to be run on a hardware there are several processes taking place. 
* To begin with, the apps enters into a block called system software and it converts the application program to binary language. There are various layers in system software in which the major layers or components are OS (Operating System), Compiler and Assembler.
* At first the OS outputs are small function in C, C++, VB or Java language which are taken by the respective compiler and converted into instructions and the syntax of these instructions varies with the hardware architecture on which the system is implemented.
* Then, the job of the assembler is to take these instructions and convert it into it's binary format which is basically called as a machine language program. 
* Finally, this binary language is fed to the hardware and it understands the specific functions it has to perform based on the binary code it receives.


* ![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/118372a3-4599-4d70-b379-2cabb8d224c8)

* For example, if we take a stopwatch app on RISC-V core, then the output of the OS could be a small C function which enters into the compiler and we get output RISC-V instructions following this, the output of the assembler will be the binary code which enters into your chip layout.


* ![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/d52611a8-4dba-46c8-a9d3-9fdb10634547)

  > For the above stopwatch the following are the input and output of the compiler and assembler.


  ![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/aaf66c01-567c-4ceb-ae37-abfa04c56ab9)








