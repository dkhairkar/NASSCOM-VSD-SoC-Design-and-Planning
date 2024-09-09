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

* #### QFN-48 Package
  This is QFN-48 package where pin locations are driven by arduino board. The size of this package is 7mmx7mm.

* #### Chip
  Chip is at the center of the package and is connected with the pins using wire bonds. All the signal is being tranfered from the pins to the interior of the chip.

* #### Pads
  through which we can send signal inside the chip any signal which needs to go from inside the chip to ouside the chip can go through pads
* #### Core
  where all digital logic gates are present e.g. or gate, and gate ,f/f etc.
* #### Die
  Size of the entire chip
* #### Sample Chip(RISC-V SoC)
  A chip consists of SoC, SRAM, PLL, adc, dac and SPI, etc.

  PLL, SRAM, adc, dac are called as Foundry IP's. A Foundry is a big factory where chips get manufactured. Foundry is nothing but a set of machines and we communicate with the foundry with some interface.Intellectual properties(IPs) where some amount of intelligence needed to build

  Digital blocks are called as Macros
  

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



