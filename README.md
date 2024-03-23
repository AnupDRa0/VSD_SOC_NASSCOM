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

The figure shows the RTL to GDSII Flow,

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/d79b3365-ae72-4016-bd24-ac0264c03bdf)




