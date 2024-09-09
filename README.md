# Digital VLSI Soc Design and Planning

>2 Week Workshop on Digital VLSI SoC Design and Planning organised by VSD in collaboration with NASSSCOM

## DAY 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK

### THEORY

#### Introduction to QFN-48 Package, chip, pads, core, die and IPs

* Systems in the electronic industry comprise of processing, software, storage and external interface components. In a system all of these sub components would work together to form one central processing system. At the center of this system is a chip. For example, This is a typical electroc board, Arduino board (highlighted part is a chip).
  
![Arduino board](https://github.com/user-attachments/assets/9ab077bc-5821-4465-b371-93d523bd1df1)

* If we want to design a particular board, it can be described with the help of this block diagram. At the center is a processor along with the interfaces.

![Block_Diagram](https://github.com/user-attachments/assets/e19018ff-870e-447b-9e9f-121543013da8)

* ##### Package
  Here, the part we considered as a chip is nothing but the PACKAGE. A Package is the protective layer over the actual chip.

![Package](https://github.com/user-attachments/assets/1b7915ce-080a-4079-850e-07add1d7fdb5)

* ##### QFN-48 Package
  This is QFN-48 package where pin locations are driven by arduino board. The size of this package is 7mmx7mm.

![Package QFN-48](https://github.com/user-attachments/assets/b13c0209-6930-443c-95e7-f82eeee33529)

* ##### Chip
  Chip is at the center of the package and is connected with the pins using wire bonds.
 
![Chip](https://github.com/user-attachments/assets/ff7b6ad3-d06b-4d13-a290-3f74b1f556db)

All the signal is being tranfered from the pins to the interior of the chip.

![Chip with wire bonds](https://github.com/user-attachments/assets/6c8d65de-3ab0-4045-b474-52d5a301079e)

* ##### Pads
  through which we can send signal inside the chip any signal which needs to go from inside the chip to ouside the chip can go through pads.

![Padding](https://github.com/user-attachments/assets/9897d0d0-7e4b-49bc-837a-00b4929e19ed) 

* ##### Core and Die
  Core is where all digital logic gates are present e.g. or gate, and gate ,f/f etc. Die is the size of the entire chip.

![Die and Core](https://github.com/user-attachments/assets/485697df-4c70-46bb-a9b2-c15d43a5789b)

* ##### Sample Chip(RISC-V SoC)
  A chip consists of SoC, SRAM, PLL, adc, dac and SPI, etc.

![SoC Chip](https://github.com/user-attachments/assets/f02ec7da-c41a-4d7c-9af4-5adf1818d9d2)

  PLL, SRAM, adc, dac are called as Foundry IP's. A Foundry is a big factory where chips get manufactured. Foundry is nothing but a set of machines and we communicate with the foundry with some interface.Intellectual properties(IPs) where some amount of intelligence needed to build.
  
![Foundry IPs](https://github.com/user-attachments/assets/e5d2fbf2-b98d-4550-9abd-0ebd0460fab1)

  Digital blocks are called as Macros
  
![Macros](https://github.com/user-attachments/assets/9a399dde-9665-4d86-97f9-f9897cf2d5b6)

#### Introduction to RISC-V

* ##### RISC-V Instruction Set Architecture(ISA)
When a C program needs to pass some information to the hardware with a layout i.e. interior of the chip of the computer or device.
C program is compiled to the Assembly language program which is then converted to machine level language (logic 1 or logic 0 or simply 0's and 1's bits). The machine level language is understood by the hardware which then executes logic 1 or logic 0 in the layout.
  
![C program to Layout](https://github.com/user-attachments/assets/536a2424-c1d9-40b8-a9e8-2625b965ba2d)

* The interface that needs to be present between RISC-V Architecture and Layout is Hardware Description language. So, we need to implement RISC-V specification using some RTL (e.g. picorv32 cpu core) to get a standard pnr i.e. RTL2GDS in the layout.

![RTL to GDS](https://github.com/user-attachments/assets/e48b8655-a63f-472a-8ff3-de4d1dc1c74e)

#### From Software Applications to Hardware

Applications run on hardware or a chip. Applications enters into block called System Software that converts the application program into machine level language.

##### Components of the system software:
* Operating System
The job of the OS is taking application and converting into binary 0's and 1's so it can be understood by the hardware.
The output of the Operating system is in the form of C, C++, Java, etc.

![Operating System](https://github.com/user-attachments/assets/2d576d75-a1c9-4125-a720-06917e208ca4)

* Compiler
This C, C++, etc language functions are taken by the compiler and converted into instructions set. The syntax of the core of these instructions are dependent on the hardware. These instruction set are saved as .exe file.

![Compiler](https://github.com/user-attachments/assets/2bd88921-ae69-4816-a733-2ca2799419d3) 

* Assembler
Once the Application is turned into instruction set, the job of the assembler is to take these instructions and convert it into its respective binary language.
Finally the binary language fed to the hardware and performs functions.

![Assembler](https://github.com/user-attachments/assets/4c6d91af-9254-471e-9f84-a727eb6b837c) 



![RTL2GDS flow](https://github.com/user-attachments/assets/43e87a95-5b9f-4f43-8039-aab5bc5af885)




#### Introduction to all components of open-source digital ASIC design


#### Simplified RTL2GDS flow


#### Introduction to OpenLANE and Strive chipsets


#### Introduction to OpenLane detailed ASIC design flow

### LAB



```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
```
```math
Percentage\ of\ DFF's = Flop\ Ratio * 100
```




```math
Flop\ Ratio = \frac{1613}{14876} = 0.108429685
```
```math
Percentage\ of\ DFF's = 0.108429685 * 100 = 10.84296854\ \%
```

## Day 2 - Good floorplan VS Bad floorplan and Introduction to library cells

### THEORY

#### Chip Floor Planning considerations

##### Utilization factor and aspect ratio


##### Concept of pre-placed cells


##### De-coupling capacitors


##### Power Planning


##### Pin placement and logical cell placement blockage



#### Library Binding and Placement


##### Netlist binding and initial place design


##### Optimize placement using estimated wire-lenght and capacitance


##### Final placement optimization


##### Need for libraries and characterization


##### Congestion aware placement using RePIAce



#### Cell design and characterization flows


##### Inputs for cell design flow


##### Circuit design step


##### Layout design step


##### Typical characterization flow


#### General timing characterization parameters


##### Timing threshold definitions


##### Propogation delay and transition time



### LAB

## Day 3 - Design library cell using Magic Layout and Ngspice characterization

### THEORY



### LAB

## Day 4 - Pre-layout Timing Analysis and Importance of Good Clock Tree

### THEORY


### LAB


## Day 5 - Final Steps for RTL2GDS using triton Route and openSta

### THEORY



#### LAB



