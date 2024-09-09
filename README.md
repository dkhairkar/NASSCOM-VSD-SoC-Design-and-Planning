# Digital VLSI Soc Design and Planning

>2 Week Workshop on Digital VLSI SoC Design and Planning organised by VSD in collaboration with NASSSCOM

## DAY 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK

### THEORY

#### Introduction to QFN-48 Package, chip, pads, core, die and IPs

* Systems in the electronic industry comprise of processing, software, storage and external interface components. In a system all of these sub components would work together to form one central processing system. At the center of this system is a chip. For example, This is a typical electroc board, Arduino board (highlighted part is a chip).
![Arduino board](https://github.com/user-attachments/assets/9ab077bc-5821-4465-b371-93d523bd1df1)
* If we want to design a particular board, it can be described with the help of this block diagram. At the center is a processor along with the interfaces.
![Block_Diagram](https://github.com/user-attachments/assets/e19018ff-870e-447b-9e9f-121543013da8)
* #### Package
  Here, the part we considered as a chip is nothing but the PACKAGE. A Package is the protective layer over the actual chip.
![Package](https://github.com/user-attachments/assets/1b7915ce-080a-4079-850e-07add1d7fdb5)
* #### QFN-48 Package
  This is QFN-48 package where pin locations are driven by arduino board. The size of this package is 7mmx7mm.
![Package QFN-48](https://github.com/user-attachments/assets/b13c0209-6930-443c-95e7-f82eeee33529)
* #### Chip
  Chip is at the center of the package and is connected with the pins using wire bonds. 
![Chip](https://github.com/user-attachments/assets/ff7b6ad3-d06b-4d13-a290-3f74b1f556db)
All the signal is being tranfered from the pins to the interior of the chip.
![Chip with wire bonds](https://github.com/user-attachments/assets/6c8d65de-3ab0-4045-b474-52d5a301079e)
* #### Pads
  through which we can send signal inside the chip any signal which needs to go from inside the chip to ouside the chip can go through pads
 ![Padding](https://github.com/user-attachments/assets/9897d0d0-7e4b-49bc-837a-00b4929e19ed) 
* #### Core and Die
  Core is where all digital logic gates are present e.g. or gate, and gate ,f/f etc. Die is the size of the entire chip.
![Die and Core](https://github.com/user-attachments/assets/485697df-4c70-46bb-a9b2-c15d43a5789b)
* #### Sample Chip(RISC-V SoC)
  A chip consists of SoC, SRAM, PLL, adc, dac and SPI, etc.
![SoC Chip](https://github.com/user-attachments/assets/f02ec7da-c41a-4d7c-9af4-5adf1818d9d2)
  PLL, SRAM, adc, dac are called as Foundry IP's. A Foundry is a big factory where chips get manufactured. Foundry is nothing but a set of machines and we communicate with the foundry with some interface.Intellectual properties(IPs) where some amount of intelligence needed to build
![Foundry IPs](https://github.com/user-attachments/assets/e5d2fbf2-b98d-4550-9abd-0ebd0460fab1)
  Digital blocks are called as Macros
![Macros](https://github.com/user-attachments/assets/9a399dde-9665-4d86-97f9-f9897cf2d5b6)


### LAB

## Day 2 - Good floorplan VS Bad floorplan and Introduction to library cells

### THEORY


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



