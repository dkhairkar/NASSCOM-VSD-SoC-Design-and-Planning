# Digital VLSI Soc Design and Planning

>2 Week Workshop on Digital VLSI SoC Design and Planning organised by VSD in collaboration with NASSSCOM

## THEORY
<details>
<summary>CLick to expand</summary>

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


</details>

## 1. Inception of open-source EDA, OpenLANE and Sky130 PDK

### Lab Implemention

![VirtualBox_vsdworkshop_25_09_2024_20_09_49](https://github.com/user-attachments/assets/968adc6c-0d4f-4d73-be14-b30e82aca511)

![VirtualBox_vsdworkshop_25_09_2024_20_10_17](https://github.com/user-attachments/assets/b8c44f2b-6fc5-400e-af01-eb850594124f)


```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
```
```math
Percentage\ of\ DFF's = Flop\ Ratio * 100
```

![VirtualBox_vsdworkshop_25_09_2024_20_24_14](https://github.com/user-attachments/assets/aac53075-b63e-4761-b818-a5b41194311b)

![VirtualBox_vsdworkshop_25_09_2024_20_24_33](https://github.com/user-attachments/assets/dbd813d5-e03a-4272-9f2b-bc0eee79e567)


```math
Flop\ Ratio = \frac{1613}{14876} = 0.108429685
```
```math
Percentage\ of\ DFF's = 0.108429685 * 100 = 10.84296854\ \%
```
![VirtualBox_vsdworkshop_25_09_2024_20_24_51](https://github.com/user-attachments/assets/1e8c2f8e-41a6-4d4e-b4ab-fc3b4b57c3de)


## 2. Good floorplan VS Bad floorplan and Introduction to library cells

### Lab Implementation

![VirtualBox_vsdworkshop_26_09_2024_18_25_41](https://github.com/user-attachments/assets/b62583f0-59bd-4be8-ab81-faf08f69180a)

![VirtualBox_vsdworkshop_26_09_2024_18_26_11](https://github.com/user-attachments/assets/9a9de95a-87d0-4b62-a388-bae075dd6e16)

![VirtualBox_vsdworkshop_26_09_2024_18_28_45](https://github.com/user-attachments/assets/d3edd32a-09db-4767-9828-0d976ff25dcd)

![VirtualBox_vsdworkshop_26_09_2024_23_36_12](https://github.com/user-attachments/assets/4534b0b4-3387-44e9-953a-52a5cb4c60b2)

![VirtualBox_vsdworkshop_26_09_2024_23_36_28](https://github.com/user-attachments/assets/ddb24e45-cefc-42d1-95db-1c329baf8224)

![VirtualBox_vsdworkshop_26_09_2024_23_39_14](https://github.com/user-attachments/assets/a6d8f3ed-cc42-4ab2-8fe8-13202ff9fb3b)

![VirtualBox_vsdworkshop_26_09_2024_23_39_58](https://github.com/user-attachments/assets/5abca351-9d75-4178-ab63-1fad4e052f77)

![VirtualBox_vsdworkshop_26_09_2024_23_43_14](https://github.com/user-attachments/assets/ab76cba8-28e1-4db3-8907-07645d0c3409)

![VirtualBox_vsdworkshop_26_09_2024_23_43_30](https://github.com/user-attachments/assets/e9eebf43-7cb0-410c-b363-12951993cd96)

![VirtualBox_vsdworkshop_26_09_2024_23_44_12](https://github.com/user-attachments/assets/353b3986-4779-4419-b229-469bf3bfe313)

![VirtualBox_vsdworkshop_26_09_2024_23_46_11](https://github.com/user-attachments/assets/ac9489e2-485d-4e1e-9f50-37011f8dca44)

![VirtualBox_vsdworkshop_26_09_2024_23_48_23](https://github.com/user-attachments/assets/33901a59-4b6f-40ac-90a7-1d3df2a8a7b6)

![VirtualBox_vsdworkshop_26_09_2024_23_51_12](https://github.com/user-attachments/assets/1ec2db04-c9b4-41ef-9b13-e6ab7f17803e)

![VirtualBox_vsdworkshop_26_09_2024_23_51_26](https://github.com/user-attachments/assets/10583d58-d45a-4c08-86cc-a3900121a8d8)

![VirtualBox_vsdworkshop_26_09_2024_23_52_40](https://github.com/user-attachments/assets/0ea4def2-0dd1-4811-aeb9-265625d5398f)

![VirtualBox_vsdworkshop_26_09_2024_23_54_32](https://github.com/user-attachments/assets/90ed44f7-5851-471f-98f9-23ff3a3de3fd)


## 3. Design library cell using Magic Layout and Ngspice characterization

### Lab Implementation

## 4. Pre-layout Timing Analysis and Importance of Good Clock Tree

### Lab Implementation


## 5. Final Steps for RTL2GDS using triton Route and openSta

### Lab Implementation:



