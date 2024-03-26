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

  The output of the compiler are instructions and the output of the assembler is the binary pattern.
  Now, we need some RTL (a Hardware Description Language) which understands and implements the particular instructions.
  Then, this RTL is synthesised into a netlist in form of gates which is fabricated into the chip through a physical design implementation.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/fc440054-4494-493d-9358-f7dec7bdef20)

* There are mainly 3 different parts in this course.
* They are:
     *RISC-V ISA
    *RTL and synthesis of RISC-V based CPU core - picorv32
     *Physical design implementation of picorv32


  ![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/9ff7d5ee-346b-4d2d-89b0-0eb1fa4d8158)

  Open-source Implementation
	• For open-source ASIC design implemantation, we require the following enablers to be readily available as open-source versions. They are:-
	1. RTL Designs
	2. EDA Tools
	3. PDK Data
	• Initially in the early ages, the design and fabrication of IC's were tightly coupled and were only practiced by very few companies like TI, Intel, etc.
	• In 1979, Lynn Conway and Carver Mead came up with an idea to saperate the design from the fabrication and to do this they inroduced structured design methodologies based on the λ-based design rules and published the first VLSI book "Introduction to VLSI System" which started the VLSI education.
	• This methodology resulted in the emergence of the design only companies or "Fabless Companies" and fabrication only companies that we usually refer to as "Pure Play Fabs".
	• The inteface between the designers and the fab by now became a set of data files and documents, that are reffered to as the "Process Design Kits (PDKs)".
	• The PDK include but not limited to Device Models, Technology Information, Design Rules, Digital Standard Cell Libraries, I/O Libraries and many more.
	• Since, the PDK contained variety of informations, and so they were distributed only under NDAs (Non-Disclosure Agreements) which made it in-accessible to the public.
	• Recently, Google worked out an agreement with skywater to open-source the PDK for the 130nm process by skywater Technology, as a result on 30 June 2020 Google released the first ever open-source PDK.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/fbd486ec-eb8f-415d-a043-1bfbe8974a18)

*ASIC design is a complex step that involves tons of steps, various methodologies and respective EDA tools which are all required for successful ASIC implementation which is achieved though an ASIC flow which is nothing but a piece of software that pulls different tools togather to carry out the design process.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/9735541c-a5ed-4004-a6e1-5685024c2923)


OpenLANE Open-source ASIC Design Implementation Flow
The main objective of the ASIC Design Flow is to take the design from the RTL (Register Transfer Level) all the way to the GDSII, which is the format used for the final fabrication layout.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/503e7a7b-0ca1-481d-a5b8-ab5b1de8c694)



• Synthesis is the process of convertion or translation of design RTL into circuits made out of Standard Cell Libraries (SCL) the resultant circuit is described in HDL and is usually reffered to as the Gate-Level Netlist.
Gate-Level Netlist is functionally equivalent to the RTL.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/5ed4be48-e818-47dc-9bbb-334bdf753985)

• The fundemental building blocks which are the standard cells have regular layouts.
Each cell has different views/models which are utilised by different EDA tools like liberty view with electrical models of the cells, HDL behavioral models, SPICE or CDL views of the cells, Layout view which include GDSII view which is the detailed view and LEF view which is the abstract view.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ea7cfe59-fa71-4624-bf43-31366b3b0c8b)

->Chip Floor Planning


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/a4d38eab-59c5-43fb-a3c8-b5e1bc7cfba7)

-> Macro FP

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ce84fcbf-1f98-40c7-b862-d5bb9e97f779)

-> Power Planning typically uses upper metal layers for power distribution since thay are thicker than lower metal layers and so have lower resistance and PP is done to avoid electron migration and IR drops.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ae0fcc65-b1ea-4d56-a52c-4247403c1cde)

->Placement

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/99aac4cb-d22e-4157-a3ba-9d8d9b290c21)

-> Global placement provide approximate locations for all cells based on connectivity but in this stage the cells may be overlapped on each other and in detailed placement the positions obtained from global placements are minimally altered to make it legal (non-overlapping and in site-rows)


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/8a9fdfd4-7a2a-4c09-bbf0-700848ba37e5)



->CLOC Tree synth


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/8b1759dd-9c89-410d-83f7-97c3b7aa97bc)

-> Clock skew is the time difference in arrival of clock at different components.

-> Routing


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/0a6a32c5-e708-4260-8651-7e7516fab28f)


-> skywater PDK has 6 routing layers in which the lowest layer is called the local interconnect layer which is a Titanium Nitride layer the following 5 layers are all Aluminium layers.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/c75e0017-006d-42a2-aa28-3a9054bc2413)


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/21edd8f0-4019-40b3-9ced-8fa330d24ea8)

• Once done with the routing the final layout can be generated which undergoes various Sign-Off checks.
• Design Rules Checking (DRC) which verifies that the final layout honours all design fabrication rules.
• Layout Vs Schematic (LVS) which verifies that the final layout functionality matches the gate-level netlist that we started with.
Static Timing Analysis (STA) to verify that the design runs at the designated clock frequency.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/670e019d-161c-4f40-8e33-088536bd65fe)



![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/7cdff4b4-a2b3-4a7c-9ebf-fc9ff921f791)




#Change directory to openlane flow directorycdDesktop/work/tools/openlane_working_dir/openlane

#alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'#Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command
docker

#Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

#Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

#Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

#Now that the design is prepped and ready, we can run synthesis using following command 
run_synthesis

#Exit from OpenLANE flowexit#Exit from OpenLANE flow docker sub-system
exit



![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/530c32d0-27bc-48cb-b9d8-7d677e58dfe8)
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/47cda489-07b6-4712-925d-62fabe405e3a)

Once the openLane is opened we need to load all the package everytime. By using command package require openlane 0.9 After that we need to do design setup by providing all the input files. By using command prep -design picorv32a.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/1f6e4701-4d6b-4e98-86a4-a344b3a844d4)

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/1d9c3a6c-7b10-4264-ad13-4863fd79e13f)

--------------------------------------------------------------------------
Day 2 - Good floorplan vs bad floorplan and introduction to library cells .
--------------------------------------------------------------------------

For floorplannning utilization factor needs to be checked. The formula for utilization factor and aspect ratio is given in below image.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/9b82654a-a17c-4143-9fe7-7dc160576749) 

As seen the Netlist Area is 2x2= 4sq unit, and the total area of the core is 4x4 = 16sq unit. So the Utilization Factor becomes 4/16 = 0.25 which is not good. 1 means there is no space for routing and placing additional cells. The aspect ratio is 4/4 = 1

After running Synthesis, we got the Chip area as
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/67e38168-9d3d-490c-b7f0-96ac9630d37a)

All pre-configured files can be found at the following location:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/14f8b5b8-d247-43ba-81e9-d84c67a79615) 

Now we need to run_floorplan. The reports and results are generated in the location shown in the below image:
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/86e4c601-f8ed-45a9-8df9-8de5a28554c2)

The ioplacer log can be found at the following location:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/78ade9d6-6aad-4db7-9325-84ee9f7d8a66) 

The details of the ioplacer.log are as follows:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/6484544a-1ea4-4d07-89dd-461de91713ab)

Invoke Magic tool by attaching tech file with the generated floorplan.def

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/0f7df471-9339-45f5-bfcd-365d525d677c)

Magic tool and the detail of a pin.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/c1babbd9-fad3-4d7c-9221-5d4fa93aa573)

Standard cells before placement

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/c9ba6ddb-e87b-466e-a91a-8653799fd1d5)

After using command global_placement, we can see the following image through Magic

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/7ef2fed0-2b4f-484f-b98a-b6fac63d7300)

By zooming in we can see the cells as follows:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ec0848f6-2db9-4a2e-8b45-6dfd18ed9c52)

---------------------------------------------
DAY 3 Adding new inverter cell to the library
---------------------------------------------

Get the git files of the inverter from VSDstdcelldesign git
We can get a detail understanding of the inverter from the repository of Nickson Jose
Clone the Git from above links to the system.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/26f37939-fefd-4168-8413-2dfd50e00ce4)

By using magic we can open the mag file

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/f0e1f384-f10c-48da-b549-1c0b4fb0c14a)

Now by zooming in and enabling grid (Press g on keyboard) we can see the grid dimensions (by using command- box). The value we get here is 0.01u which we will use in spice file.


![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/22b1dc2a-3e2c-4ecb-9ee9-076b4ed6220f) 


There are no DRC’s in the mag file

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/fce55181-0d0d-428d-a9ef-a7e2173330f1)

Now extract the spice file,

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/cfe52f8e-c5b1-449c-b7b0-ffcaa9d344f2)

Now edit the spice file, change the scale to the size of grid of inverter. Include the lib files, provide pulse and do the transient analysis.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/30703a6f-cdc3-44d6-bb95-5c3f47ea90be)

-> Run the ngspice solution and plot the graph using command -plot y vs time a

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/59fbed94-0c09-42e2-a2b3-1fe5d646621b)

The plot is shown below

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/b988850b-2989-4989-8a04-17938fe37354)


Now open tracks.info, to know the pitch and set the grid of inverter as per the track pitch
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/b921961d-8d77-412c-81ff-932f369804ba)

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/e1651ae5-13d8-45d6-a128-1edf65ac8b65) 

Setting the grid of track size to check whether the input and output port of the inverter are on the grid or not. The figure also ensures the width is multiple of the pitch as well as the height.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/0acecd63-570c-4d73-a7ca-e16558cadcbe)

From the above figure we can say that the stdcell layout is as per the requirement

Write lef to include the cell in our design file

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/03c892ce-10f3-47b3-9122-84c98b6ac9cf)

Contents of the lef file

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/c0243245-fc36-4d46-bf5c-40f1d795e203)

Change the config file, add the libs and our new cell lef.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/61d9f02e-ebea-42c1-87ab-4f5964819077)

Add the following commands to include lef in the design after changing the config file.
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/8b8b591c-888e-453e-be88-f5bd524d8b0b)

As we can in the following image the new inverters are added to the design

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/30290d5e-f773-43f8-9814-17df26cf5878)


-----------------------
Day 4 - Timing Analysis
-----------------------

Setting the commands to solve the negative slack

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/08ef671d-32d9-4a48-8f6a-a699c720eda6)

As we can see from the results the negative slack is gone and the area of chip is increased.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/1a225c57-0ba9-4783-8095-000a7976e968) 

-> After placement we can see our new inverter is placed in the design.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/d88af3b2-1bc7-4b52-853b-818ca8071320)

-> run_cts command if there are any violations, solve in openroad until the slack is met. Openroad can be invoked in openlane by simply typing openroad. The inputs to openroad are as follows:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/c376e5d2-7f2a-4926-aad5-780dcceba75f)

From the report, we can see that the timing slack is met

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/56b2e846-c278-4805-b5b3-5078f149ec15)

----------------------------
Day 5 - Final step - Routing
----------------------------

To check the current def or what was the last def file that we generated. Use the command echo $::env(CURRENT_DEF) 

Location for setting parameters for various stages.
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/4accc350-3035-4cc8-80fa-26c834033a7a) 

The following image shows the parameters set for routing stage.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/827def55-b1f3-44fe-bae0-64875ec3507a)

To run routing script, we just need to write the command run_routing in OpenLane tool. After the routing is done. we can get the report from the location as shown in the below image.

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/09a89d92-68f1-447e-9a50-abbcadbfb781)

If there are any errors in routing, we can check those error in the DRC report:

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/d378d07c-78e7-4317-91b4-78e437885079)

Routing def file can be find at the location shown in the below image
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/aee334c2-94c3-4850-8600-20d2b096dbc7)

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/ddba1667-c164-475a-bb88-b7337ff9da42)

A zoom in portion of the image, to see the routed tracks.
![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/5d156c56-110b-46bf-aacb-d903c1c0a883)


The inverter that we added is also routed, perfectly without any DRC's

![image](https://github.com/AnupDRa0/VSD_SOC_NASSCOM/assets/52745867/f5f46573-16cc-419a-9b38-b4d0a05ebc1b)





















































