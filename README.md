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
**Objective :** To run Opnelane flow using 'picorv32a' design and calculate the flop ratio.

**Invoking the Openlane flow using picorv32a :**

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Alias docker**
```bash
alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
```
Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command.
```bash
docker
```

**Invoke the OpenLane flow in the interactive mode**
```bash
./flow.tcl -interactive
```

**Now that we have invoked the OpenLANE flow, we require the package**
```tcl
package require openlane 0.9
```

**Now we need to prep the the design, in this case we are using 'picorv32a' design**
```tcl
prep -design picorv32a
```

**Running Synthesis**
```tcl
run_synthesis
```

Screenshots of the OpenLane flow:
![VirtualBox_vsdworkshop_25_09_2024_20_09_49](https://github.com/user-attachments/assets/968adc6c-0d4f-4d73-be14-b30e82aca511)

![VirtualBox_vsdworkshop_25_09_2024_20_10_17](https://github.com/user-attachments/assets/b8c44f2b-6fc5-400e-af01-eb850594124f)

**Calculating the flop ratio:**

```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
```
```math
Percentage\ of\ DFF's = Flop\ Ratio * 100
```
**Screenshot of both Number of D flip flop and Total number of Cells**
![VirtualBox_vsdworkshop_25_09_2024_20_24_14](https://github.com/user-attachments/assets/aac53075-b63e-4761-b818-a5b41194311b)

![VirtualBox_vsdworkshop_25_09_2024_20_24_33](https://github.com/user-attachments/assets/dbd813d5-e03a-4272-9f2b-bc0eee79e567)
*Here, Total number of Cells =14876 and* 
*Number of D flop flops = 1613* 

```math
Flop\ Ratio = \frac{1613}{14876} = 0.108429685
```
```math
Percentage\ of\ DFF's = 0.108429685 * 100 = 10.84296854\ \%
```

**Exiting the OpenLANE flow**
```tcl
exit
```

**Exiting the docker**
```bash
exit
```

![VirtualBox_vsdworkshop_25_09_2024_20_24_51](https://github.com/user-attachments/assets/1e8c2f8e-41a6-4d4e-b4ab-fc3b4b57c3de)



## 2. Good floorplan VS Bad floorplan and Introduction to library cells

### Lab Implementation

**Objective :** To run the OpenLANE flow using 'picorv32a' design, calculate the die area and generate floorplan def and placement def in magic tool.

**Invoking the Openlane flow using picorv32a :**

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Alias docker**
```bash
alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
```
Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command.
```bash
docker
```

**Invoke the OpenLane flow in the interactive mode**
```bash
./flow.tcl -interactive
```

**Now that we have invoked the OpenLANE flow, we require the package**
```tcl
package require openlane 0.9
```

**Now we need to prep the the design, in this case we are using 'picorv32a' design**
```tcl
prep -design picorv32a
```

**Running synthesis**
```tcl
run_synthesis
```

**Running floorplan**
```tcl
run_floorplan
```

Screenshots of OpenLANE flow:
![VirtualBox_vsdworkshop_26_09_2024_18_25_41](https://github.com/user-attachments/assets/b62583f0-59bd-4be8-ab81-faf08f69180a)

![VirtualBox_vsdworkshop_26_09_2024_18_26_11](https://github.com/user-attachments/assets/9a9de95a-87d0-4b62-a388-bae075dd6e16)

![VirtualBox_vsdworkshop_26_09_2024_18_28_45](https://github.com/user-attachments/assets/d3edd32a-09db-4767-9828-0d976ff25dcd)

**Change to the directory containing floorplan def path**
```bash
 cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-09_12-55/results/floorplan/
```

**Command for loading the floorplan def in Magic tool**
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

![VirtualBox_vsdworkshop_26_09_2024_23_36_12](https://github.com/user-attachments/assets/4534b0b4-3387-44e9-953a-52a5cb4c60b2)

![VirtualBox_vsdworkshop_26_09_2024_23_36_28](https://github.com/user-attachments/assets/ddb24e45-cefc-42d1-95db-1c329baf8224)

Screenshots of the floorplan def in Magic tool:
![VirtualBox_vsdworkshop_26_09_2024_23_39_14](https://github.com/user-attachments/assets/a6d8f3ed-cc42-4ab2-8fe8-13202ff9fb3b)

![VirtualBox_vsdworkshop_26_09_2024_23_39_58](https://github.com/user-attachments/assets/5abca351-9d75-4178-ab63-1fad4e052f77)

![VirtualBox_vsdworkshop_26_09_2024_23_43_14](https://github.com/user-attachments/assets/ab76cba8-28e1-4db3-8907-07645d0c3409)

![VirtualBox_vsdworkshop_26_09_2024_23_43_30](https://github.com/user-attachments/assets/e9eebf43-7cb0-410c-b363-12951993cd96)

![VirtualBox_vsdworkshop_26_09_2024_23_44_12](https://github.com/user-attachments/assets/353b3986-4779-4419-b229-469bf3bfe313)

**Running Placement**
```tcl
run_placement
```
![VirtualBox_vsdworkshop_26_09_2024_23_46_11](https://github.com/user-attachments/assets/ac9489e2-485d-4e1e-9f50-37011f8dca44)

![VirtualBox_vsdworkshop_26_09_2024_23_48_23](https://github.com/user-attachments/assets/33901a59-4b6f-40ac-90a7-1d3df2a8a7b6)

Screenshot of the floorplan def:
![VirtualBox_vsdworkshop_04_10_2024_20_46_59](https://github.com/user-attachments/assets/f2671ee2-d1c8-4c33-a77c-643a7ea614a5)

According to floorplan def
```math
1000\ Unit\ Distance = 1\ Micron
```
```math
Die\ width\ in\ unit\ distance = 660685 - 0 = 660685
```
```math
Die\ height\ in\ unit\ distance = 671405 - 0 = 671405
```
```math
Distance\ in\ microns = \frac{Value\ in\ Unit\ Distance}{1000}
```
```math
Die\ width\ in\ microns = \frac{660685}{1000} = 660.685\ Microns
```
```math
Die\ height\ in\ microns = \frac{671405}{1000} = 671.405\ Microns
```
```math
Area\ of\ die\ in\ microns = 660.685 * 671.405 = 443587.212425\ Square\ Microns
```
**Change the directory to placement def path**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-09_12-55/results/placement/
```

**Command for loading the placement def in Magic tool**
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```
![VirtualBox_vsdworkshop_26_09_2024_23_51_12](https://github.com/user-attachments/assets/1ec2db04-c9b4-41ef-9b13-e6ab7f17803e)

Screenshots of the placement def in Magic tool:
![VirtualBox_vsdworkshop_26_09_2024_23_51_26](https://github.com/user-attachments/assets/10583d58-d45a-4c08-86cc-a3900121a8d8)

![VirtualBox_vsdworkshop_26_09_2024_23_52_40](https://github.com/user-attachments/assets/0ea4def2-0dd1-4811-aeb9-265625d5398f)

![VirtualBox_vsdworkshop_26_09_2024_23_54_32](https://github.com/user-attachments/assets/90ed44f7-5851-471f-98f9-23ff3a3de3fd)

**Exiting the OpenLANE flow**
```tcl
exit
```

**Exiting the docker**
```bash
exit
```

## 3. Design library cell using Magic Layout and Ngspice characterization

### Lab Implementation

**Objective :** To run the following task:
1. Clone and Open the custom inverter layout in magic tool.
2. Spice Extraction on the inverter.
3. Post layout simulation in ngspice.
4. Fixing the incorrect magic tech files.

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Clone the repository which contains the custom inverter**
```bash
https://github.com/nickson-jose/vsdstdcelldesign.git
```
![VirtualBox_vsdworkshop_27_09_2024_00_01_11](https://github.com/user-attachments/assets/60472270-2ace-463d-8158-e5e68ec39d3a)

![VirtualBox_vsdworkshop_29_09_2024_00_13_10](https://github.com/user-attachments/assets/7c7cf9cf-3506-4fb7-9e0e-e610de991dea)

**Change the directory**
```bash
cd vsdstdcelldesign
```
**Copy magic tech file to vsdstdcelldesign directory**
```bash
cp sky130A.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```

![VirtualBox_vsdworkshop_29_09_2024_00_19_42](https://github.com/user-attachments/assets/08681fb0-6140-4f1e-9ad8-ee17ec3746b9)

**Command to Open inverter in Magic tool**
```bash
magic -T sky130A.tech sky130_inv.mag &
```

![VirtualBox_vsdworkshop_29_09_2024_00_24_09](https://github.com/user-attachments/assets/366578ea-a599-48f5-bb2c-5fd072e51591)

Screenshots of inverter layout in Magic tool:

![VirtualBox_vsdworkshop_29_09_2024_00_28_15](https://github.com/user-attachments/assets/dfe6f989-97de-4a8e-805a-dc78726709e0)
NMOS and PMOS:

![VirtualBox_vsdworkshop_29_09_2024_00_28_45](https://github.com/user-attachments/assets/46781375-b1a9-4ad5-aab1-a0b42db21f14)

![VirtualBox_vsdworkshop_29_09_2024_00_29_34](https://github.com/user-attachments/assets/c8280f95-c6ea-4711-9a83-2aad01ae41a5)

![VirtualBox_vsdworkshop_29_09_2024_00_29_44](https://github.com/user-attachments/assets/35a1bc6a-ceea-4e5a-a989-dd12c9b91dc6)

Y connected to PMOS and NMOS drain:
![VirtualBox_vsdworkshop_29_09_2024_00_30_50](https://github.com/user-attachments/assets/8650761a-984e-479a-9e77-ed110b825ca7)

PMOS connected to VPWR:
![VirtualBox_vsdworkshop_29_09_2024_00_32_11](https://github.com/user-attachments/assets/ceed3995-b4ec-41fd-9f05-54f4669556e1)

NMOS connected to VGND:
![VirtualBox_vsdworkshop_29_09_2024_00_32_29](https://github.com/user-attachments/assets/c83d6b80-9081-4678-aef4-439910f4bd0c)

**Commands to Spice extraction of the inverter in tcl window**

Extracting spice to .ext 
```tcl
extract all
```

parasitic extraction
```tcl
ext2spice cthresh 0 rthresh 0
```

Convert ext to spice:
```tcl
ext2spice
```

![VirtualBox_vsdworkshop_29_09_2024_20_37_38](https://github.com/user-attachments/assets/eb826f23-9fe5-4acf-95c5-35b88285708e)

Checking for .ext and .spice in the directory:
![VirtualBox_vsdworkshop_29_09_2024_20_37_53](https://github.com/user-attachments/assets/e50bbbbc-0f5c-48d5-a974-7e1daa7aa190)

Measure unit distance in grid:

![VirtualBox_vsdworkshop_29_09_2024_21_06_09](https://github.com/user-attachments/assets/24136f4d-10a5-4488-a2ce-98ff9909a882)

Edit the .spice file for ngspice simulation:

![VirtualBox_vsdworkshop_29_09_2024_20_38_19](https://github.com/user-attachments/assets/a3e5076a-53ab-4249-b539-05bb129b7b5f)

Edited .spice file:
![VirtualBox_vsdworkshop_29_09_2024_23_21_56](https://github.com/user-attachments/assets/ee1f5f9e-0f92-4e4f-8b6a-bb3b0285a2bf)

**loading spice file for ngspice simulation**
```bash
ngspice sky130_inv.spice
```

**Once the ngspice has been loaded, we need to plot**
```
plot y vs a
```
![VirtualBox_vsdworkshop_29_09_2024_23_22_18](https://github.com/user-attachments/assets/a3815033-be2b-482d-9a2d-c7a3a32ddda3)

![VirtualBox_vsdworkshop_29_09_2024_23_27_09](https://github.com/user-attachments/assets/3e07b672-1f18-4dbe-926e-1377507f27fe)

![VirtualBox_vsdworkshop_29_09_2024_23_26_58](https://github.com/user-attachments/assets/c2bcef7e-5a6c-4246-ab52-987df586fc85)

![VirtualBox_vsdworkshop_29_09_2024_23_30_24](https://github.com/user-attachments/assets/5869d269-8c97-47bb-8a7a-cb85f1a99251)

![VirtualBox_vsdworkshop_29_09_2024_23_31_50](https://github.com/user-attachments/assets/b933d86f-3638-48f4-9581-a81ea055deae)

![VirtualBox_vsdworkshop_29_09_2024_23_32_30](https://github.com/user-attachments/assets/701829c7-6ffa-47b2-9e0d-f9c869127ba6)

**Change to home directory**
```bash
cd
```

**Command to download the files**
```bash
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
```

**Extract the files**
```bash
tar xfz drc_tests.tgz
```

**Change into the lab directory**
```bash
cd drc_tests
```

![VirtualBox_vsdworkshop_30_09_2024_00_56_57](https://github.com/user-attachments/assets/1a361264-b23a-4429-85eb-6d2055201205)

**List all files and directories present in the current directory**
```bash
ls -al
```

**To view .magicrc file**
```bash
gvim .magicrc
```
![VirtualBox_vsdworkshop_30_09_2024_00_57_45](https://github.com/user-attachments/assets/c81a23bd-0dfe-451a-acd3-9342388a71ed)

Screenshot of .magicrc file:
![VirtualBox_vsdworkshop_30_09_2024_00_58_01](https://github.com/user-attachments/assets/7e8c8234-500b-49ad-a90f-8fec9c707929)

**Command to open magic tool**
```bash
magic -d XR &
```

![VirtualBox_vsdworkshop_30_09_2024_01_04_55](https://github.com/user-attachments/assets/af05e829-181b-43e1-823a-ffb33465e2fa)

Screenshot of the magic tool:
![VirtualBox_vsdworkshop_30_09_2024_01_09_15](https://github.com/user-attachments/assets/c3165142-35c0-4908-93cf-3715b24b25de)

Opening the file in magic (from the directory):
![VirtualBox_vsdworkshop_30_09_2024_01_10_05](https://github.com/user-attachments/assets/7b3a5734-04d3-4bc0-988e-8e5e4c142d85)

**check the met3.mag file in magic tool**
![VirtualBox_vsdworkshop_30_09_2024_01_10_14](https://github.com/user-attachments/assets/95df352f-0755-4532-99f9-49d541d4ce1f)

![VirtualBox_vsdworkshop_30_09_2024_01_21_05](https://github.com/user-attachments/assets/c7f92b73-d902-45f1-91b0-337df8b8856a)

**Incorrectly implemented poly.9 simple rule correction**
![VirtualBox_vsdworkshop_30_09_2024_01_21_31](https://github.com/user-attachments/assets/ca890495-44bc-4409-aaa7-5988d960c2c1)

![VirtualBox_vsdworkshop_30_09_2024_01_21_40](https://github.com/user-attachments/assets/b2b1d67e-f71d-4c0a-92f6-e2a0f9202d59)

Incorrectly implemented poly.9 rule with no drc violation:
![VirtualBox_vsdworkshop_30_09_2024_01_22_18](https://github.com/user-attachments/assets/c2b999bb-65ba-4388-83d5-89cdbb33b168)

![VirtualBox_vsdworkshop_30_09_2024_01_24_50](https://github.com/user-attachments/assets/336cdf03-836f-46ad-8327-4d0ebe1a93f6)

![VirtualBox_vsdworkshop_30_09_2024_01_26_15](https://github.com/user-attachments/assets/10012b8c-fee9-4e01-9902-ef09f6f3c03c)

**Insert new commands in sky130A.tech to update drc**

![VirtualBox_vsdworkshop_30_09_2024_01_28_48](https://github.com/user-attachments/assets/00e53f5a-26fc-4681-9a81-8bd3d7fdf129)

![VirtualBox_vsdworkshop_30_09_2024_01_54_03](https://github.com/user-attachments/assets/f6143250-fc2d-4742-8e7d-aff2f0a22456)

![VirtualBox_vsdworkshop_30_09_2024_01_57_20](https://github.com/user-attachments/assets/423602f4-79b5-4275-bb47-809d9e16ebf4)

**Loading updated tech file**
```tcl
tech load sky130A.tech
```

![VirtualBox_vsdworkshop_30_09_2024_01_58_11](https://github.com/user-attachments/assets/63dcd3a9-f540-4e10-ab01-03bd982d5afd)

**re-run drc check to see updated drc errors**
```tcl
drc check
```

**Selecting region displaying the new errors and getting the error messages**
```tcl
drc why
```

![VirtualBox_vsdworkshop_30_09_2024_01_58_42](https://github.com/user-attachments/assets/90d3dde2-91ea-4f26-9726-0bfd70565d10)

![VirtualBox_vsdworkshop_30_09_2024_02_36_33](https://github.com/user-attachments/assets/0bc59b3f-6538-4371-b393-54abbcfa9ba5)

**Incorrectly implemented difftap.2 simple rule correction**

**Insert new commands in sky130A.tech to update drc**

![VirtualBox_vsdworkshop_30_09_2024_02_47_47](https://github.com/user-attachments/assets/5925f375-54ed-47a6-b82b-8a29ba0f3274)

**Commands to run in tkcon window**

**Loading updated tech file**
```tcl
tech load sky130A.tech
```

**re-run drc check to see updated drc errors**
```tcl
drc check
```

**Selecting region displaying the new errors and getting the error messages**
```tcl
drc why
```

![VirtualBox_vsdworkshop_30_09_2024_02_48_47](https://github.com/user-attachments/assets/d28498e6-be28-4899-9bee-4c364ca8aedc)

![VirtualBox_vsdworkshop_30_09_2024_02_49_16](https://github.com/user-attachments/assets/f4b026b4-dcdf-45a3-abde-9c38dd8f0212)

**Incorrectly implemented nwell.4 complex rule correction**


**Insert new commands in sky130A.tech to update drc**

![VirtualBox_vsdworkshop_30_09_2024_02_50_12](https://github.com/user-attachments/assets/32ec10bb-c196-4ce3-bad8-97a973663edb)

![VirtualBox_vsdworkshop_30_09_2024_02_57_11](https://github.com/user-attachments/assets/f68eafed-db6c-4fe2-9c83-528052137ba6)

![VirtualBox_vsdworkshop_30_09_2024_03_01_37](https://github.com/user-attachments/assets/f7f97215-5553-4930-bed8-366007cc16dc)

**Commands to run in tkcon window**

**Loading updated tech file**
```tcl
tech load sky130A.tech
```

**re-run drc check to see updated drc errors**
```tcl
drc check
```

**Selecting region displaying the new errors and getting the error messages**
```tcl
drc why
```
![VirtualBox_vsdworkshop_30_09_2024_03_03_27](https://github.com/user-attachments/assets/d9a9372e-28f5-4cd4-aae7-2cc78b1984fd)

![VirtualBox_vsdworkshop_30_09_2024_03_05_18](https://github.com/user-attachments/assets/4433b434-b6e9-4993-b148-da9ffb05240f)
## 4. Pre-layout Timing Analysis and Importance of Good Clock Tree

### Lab Implementation

**Objective :** To run the following task:
1. Explore timing modeling using delay tables.
2. process of converting grid information to track information.

**Change the directory to vsdstdcelldesign**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```

**Open the inverter layout in magic tool**
```bash
magic -T sky130A.tech sky130_inv.mag &
```

**Change the directory to tracks.info path**
```bash
cd Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd
```

![VirtualBox_vsdworkshop_30_09_2024_12_15_15](https://github.com/user-attachments/assets/7577856d-e622-4dc4-bd71-ddee3d79f987)

![VirtualBox_vsdworkshop_30_09_2024_12_15_22](https://github.com/user-attachments/assets/25f2388e-3907-4fc6-b1f8-756bd7f03a35)

**syntax for grid command**
```tcl
help grid
```

![VirtualBox_vsdworkshop_30_09_2024_12_17_08](https://github.com/user-attachments/assets/b36e36f0-29da-48f2-bba2-8f1ca89b32a6)

![VirtualBox_vsdworkshop_30_09_2024_12_17_59](https://github.com/user-attachments/assets/59a6d784-a039-4339-8c3a-d29b6fa155fd)

**Set grid values according to track.info**
```tcl
grid 0.46um 0.34um 0.23um 0.17um
```

![VirtualBox_vsdworkshop_30_09_2024_12_18_54](https://github.com/user-attachments/assets/d3f5822f-e43b-4ca6-84b5-22126a909a35)

**Command to save .mag file**
```tcl
save sky130_vsdinv.mag
```

![VirtualBox_vsdworkshop_30_09_2024_13_02_14](https://github.com/user-attachments/assets/3e4de42c-8e72-4c33-938c-22d116458f77)

![VirtualBox_vsdworkshop_30_09_2024_13_12_09](https://github.com/user-attachments/assets/0b9679d9-242a-4aef-9f4e-a0d9968bbc2a)

**Command to open inverter layout in magic tool**
```bash
magic -T sky130A.tech sky130_vsdinv.mag &
```

![VirtualBox_vsdworkshop_30_09_2024_13_13_05](https://github.com/user-attachments/assets/5d08b581-0a15-46a3-8f3c-e3c8e09be2b0)

**lef command**
```tcl
lef write
```

![VirtualBox_vsdworkshop_30_09_2024_13_13_45](https://github.com/user-attachments/assets/cd3f7592-946f-491e-a7ce-71e38b2a777b)

![VirtualBox_vsdworkshop_30_09_2024_13_13_55](https://github.com/user-attachments/assets/a429dbd1-dcd9-413a-a0cc-3fcf1eb25f37)

![VirtualBox_vsdworkshop_30_09_2024_13_15_00](https://github.com/user-attachments/assets/757f4e73-47b0-4656-9856-1fc3fbdc8e9c)

Screenshot of new created .lef file
![VirtualBox_vsdworkshop_30_09_2024_13_14_47](https://github.com/user-attachments/assets/fe1b9372-f24e-4646-97f4-f0fab4a9b70e)

**Copy the lef file**
```bash
cp sky130_vsdinv.lef ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/
```

![VirtualBox_vsdworkshop_30_09_2024_13_29_20](https://github.com/user-attachments/assets/e59b14c4-db24-43ff-b141-4fdaa3149815)

![VirtualBox_vsdworkshop_30_09_2024_13_30_25](https://github.com/user-attachments/assets/e3d25640-dd84-4b0a-9f89-cad1ca0bb957)

**List and check whether it's copied**
```bash
ls ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/
```

**Copy the .lib files**
```bash
cp sky130_fd_sc_hd__*  /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/
```

**List and check whether it's copied**
```bash
~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src$ ls -ltr
```

![VirtualBox_vsdworkshop_30_09_2024_13_30_44](https://github.com/user-attachments/assets/3ee6cd4a-5afe-479f-8b87-e5afcb54422a)

![VirtualBox_vsdworkshop_30_09_2024_13_33_19](https://github.com/user-attachments/assets/25b68c75-0eab-430c-a0c8-98b79f88600f)






**Commands to be added to config.tcl to include our custom cell in the openlane flow**
```
set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib"
set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib"
set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"

set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]
Edited config.tcl to include the added lef and change library to ones we added in src directory
```
![VirtualBox_vsdworkshop_30_09_2024_13_38_59](https://github.com/user-attachments/assets/46267822-7340-41e2-aaa1-614df0523ce1)

![VirtualBox_vsdworkshop_30_09_2024_13_34_02](https://github.com/user-attachments/assets/8377fff3-6f32-4e56-ba1c-bcfe3a55cf30)

![VirtualBox_vsdworkshop_30_09_2024_13_31_30](https://github.com/user-attachments/assets/19dbbd6b-d5aa-40b9-bc8e-a4d8ae5bd4a3)

![VirtualBox_vsdworkshop_30_09_2024_13_31_49](https://github.com/user-attachments/assets/47ba21f1-bc04-4e4e-a5d1-72983390c9a0)

![VirtualBox_vsdworkshop_30_09_2024_13_32_30](https://github.com/user-attachments/assets/da1bed77-5c39-46f9-bab6-afd40b5ec850)

**Invoking the Openlane flow using picorv32a :**

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Alias docker**
```bash
alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
```
Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command.
```bash
docker
```

**Invoke the OpenLane flow in the interactive mode**
```bash
./flow.tcl -interactive
```

**Now that we have invoked the OpenLANE flow, we require the package**
```tcl
package require openlane 0.9
```

**Now we need to prep the the design, in this case we are using 'picorv32a' design**
```tcl
prep -design picorv32a
```
![VirtualBox_vsdworkshop_30_09_2024_14_40_57](https://github.com/user-attachments/assets/4b4e8d84-3a9d-4aee-8cd4-25f0531e39ce)

**Additional commands to include new added .lef to OpenLANE flow**
```tcl
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
```

**Running synthesis**
```tcl
run_synthesis
```
![VirtualBox_vsdworkshop_30_09_2024_14_44_03](https://github.com/user-attachments/assets/4ab41e94-a38a-4a56-b678-ee498cfe08da)


**Note down current design values generated before modifying parameters to improve timing and chip area**
![VirtualBox_vsdworkshop_30_09_2024_14_51_17](https://github.com/user-attachments/assets/884dbab3-465f-4a17-bd13-7cc99cb34f12)

![VirtualBox_vsdworkshop_30_09_2024_14_53_22](https://github.com/user-attachments/assets/fd6b19a1-0318-4ce6-a593-eb180679a92e)

**Change the directory path to README.md**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/configuration
```
![VirtualBox_vsdworkshop_30_09_2024_15_00_08](https://github.com/user-attachments/assets/9acc5dd2-059d-4759-92a1-2db9bcd46e1d)

Screenshot of the README.md:
![VirtualBox_vsdworkshop_30_09_2024_15_00_17](https://github.com/user-attachments/assets/bb86141e-b2c7-4df3-8851-f4e2d1a699b2)


**prep design so as to update variables**
```tcl
prep -design picorv32a -tag 24-03_10-03 -overwrite
```
![VirtualBox_vsdworkshop_30_09_2024_15_17_46](https://github.com/user-attachments/assets/253ea57a-723d-4cad-a141-9cc1eea6549d)

**Addiitional commands to include in new added .lef to OpenLANE flow merged.lef**
```tcl
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
```
![VirtualBox_vsdworkshop_30_09_2024_18_39_28](https://github.com/user-attachments/assets/90afd8ca-d8d1-45bf-97c8-49c1b61140b8)

**Display current value of variable SYNTH_STRATEGY**
```tcl
echo $::env(SYNTH_STRATEGY)
```

**Set new value for SYNTH_STRATEGY**
```tcl
set ::env(SYNTH_STRATEGY) "DELAY 3"
```

**Display current value of variable SYNTH_BUFFERING to check whether it's enabled**
```tcl
echo $::env(SYNTH_BUFFERING)
```

**Display current value of variable SYNTH_SIZING**
```tcl
echo $::env(SYNTH_SIZING)
```

**Set new value for SYNTH_SIZING**
```tcl
set ::env(SYNTH_SIZING) 1
```

**Display current value of variable SYNTH_DRIVING_CELL to check whether it's the proper cell or not**
```tcl
echo $::env(SYNTH_DRIVING_CELL)
```

**Running synthesis**
```tcl
run_synthesis
```

![VirtualBox_vsdworkshop_30_09_2024_18_55_10](https://github.com/user-attachments/assets/1b38f34c-adaa-40e1-8f06-9b37dbd3e359)

![VirtualBox_vsdworkshop_30_09_2024_18_58_56](https://github.com/user-attachments/assets/40d00457-f554-4ed5-9314-7a297410ad4a)

![VirtualBox_vsdworkshop_30_09_2024_18_59_07](https://github.com/user-attachments/assets/36ec588b-0143-4771-b359-3a586326f0e7)

**Running Floorplan**
```tcl
run_floorplan
```

![VirtualBox_vsdworkshop_30_09_2024_19_04_21](https://github.com/user-attachments/assets/897f6f8d-a6e3-4b1b-8854-9ac47a9ea2fe)

Since we are facing unexpected un-explainable error while using run_floorplan command, we can instead use the following set of commands available based on information from Desktop/work/tools/openlane_working_dir/openlane/scripts/tcl_commands/floorplan.tcl and also based on Floorplan Commands section in Desktop/work/tools/openlane_working_dir/openlane/docs/source/OpenLANE_commands.md
**Following commands are alltogather sourced in "run_floorplan" command**
```tcl
init_floorplan
place_io
tap_decap_or
```

![VirtualBox_vsdworkshop_30_09_2024_19_10_48](https://github.com/user-attachments/assets/08291439-90e5-4d85-90e7-386baa79d111)

![VirtualBox_vsdworkshop_30_09_2024_19_11_08](https://github.com/user-attachments/assets/c7f5175c-e3c4-4905-8ffe-7aa21d272062)

![VirtualBox_vsdworkshop_30_09_2024_19_11_31](https://github.com/user-attachments/assets/27e6beae-7b50-45ff-8488-8c79d42e8906)

**Running placement**
```tcl
run_placement
```

![VirtualBox_vsdworkshop_30_09_2024_19_12_46](https://github.com/user-attachments/assets/6d842d23-3cc9-4d9d-949c-284ed5b33288)

![VirtualBox_vsdworkshop_30_09_2024_19_15_02](https://github.com/user-attachments/assets/be57b2b2-6a36-4c84-83cd-0722df2f8d67)

**Change directory path to generated placement def file**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/30-09_13-07/results/placement/
```

**Load the placement def in magic tool**
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```
![VirtualBox_vsdworkshop_30_09_2024_19_27_00](https://github.com/user-attachments/assets/44de225c-5b72-4a5d-9849-745839bb72ba)

Placement def in magic tool:

![VirtualBox_vsdworkshop_30_09_2024_19_29_36](https://github.com/user-attachments/assets/cb7910cf-69ca-4eaa-be9b-51e4e2087640)

![VirtualBox_vsdworkshop_30_09_2024_19_29_47](https://github.com/user-attachments/assets/1c0e288c-4064-4101-aac9-c2092bd4d658)

**Command to view internal connectivity layers in tkcon window**
```tcl
expand
```
![VirtualBox_vsdworkshop_30_09_2024_19_34_32](https://github.com/user-attachments/assets/68a34a53-4a35-4908-8a47-e588f68a9f16)

![VirtualBox_vsdworkshop_30_09_2024_19_34_48](https://github.com/user-attachments/assets/28193031-b6e0-489c-8278-572dd2ebb6be)

![VirtualBox_vsdworkshop_30_09_2024_19_35_02](https://github.com/user-attachments/assets/d88fe494-8249-45b8-aa0d-4e32d38bc360)

![VirtualBox_vsdworkshop_30_09_2024_19_35_43](https://github.com/user-attachments/assets/3c7acec5-484d-42c4-8405-604e64a51b84)

**Invoking the Openlane flow using picorv32a :**

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Alias docker**
```bash
alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
```
Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command.
```bash
docker
```

**Invoke the OpenLane flow in the interactive mode**
```bash
./flow.tcl -interactive
```

**Now that we have invoked the OpenLANE flow, we require the package**
```tcl
package require openlane 0.9
```

**Now we need to prep the the design, in this case we are using 'picorv32a' design**
```tcl
prep -design picorv32a
```
![VirtualBox_vsdworkshop_30_09_2024_20_38_02](https://github.com/user-attachments/assets/dab5b215-2daf-471d-aef3-d6defe496d0c)

**Addiitional commands to include in new added .lef to OpenLANE flow merged.lef**
```tcl
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
```

**Set new value for SYNTH_SIZING**
```tcl
set ::env(SYNTH_SIZING) 1
```

**Create New pre_sta.conf for STA analysis in openlane directory**
![VirtualBox_vsdworkshop_30_09_2024_23_45_22](https://github.com/user-attachments/assets/89a40732-cb35-4c03-9499-67a8c2e46904)

**Create New my_base.sdc for STA analysis in openlane/designs/picorv32a/src directory based on the file openlane/scripts/base.sdc**

![VirtualBox_vsdworkshop_30_09_2024_21_50_05](https://github.com/user-attachments/assets/b04462f8-d80d-4896-a52e-69b1bb8083b8)

![VirtualBox_vsdworkshop_30_09_2024_23_59_25](https://github.com/user-attachments/assets/295085a3-ca98-4ebb-87f7-2f97e0dbeb8e)

**Running Synthesis**
```tcl
run_synthesis
```
![VirtualBox_vsdworkshop_30_09_2024_20_40_32](https://github.com/user-attachments/assets/1318cc86-9812-4caf-af80-e7e2252a3b79)

To fix this slack we use:
**prep design so as to update variables**
```tcl
prep -design picorv32a -tag 24-03_10-03 -overwrite
```

**Addiitional commands to include in new added .lef to OpenLANE flow merged.lef**
```tcl
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
```

**Display current value of variable SYNTH_STRATEGY**
```tcl
echo $::env(SYNTH_STRATEGY)
```

**Set new value for SYNTH_STRATEGY**
```tcl
set ::env(SYNTH_STRATEGY) "DELAY 3"
```

**Display current value of variable SYNTH_BUFFERING to check whether it's enabled**
```tcl
echo $::env(SYNTH_BUFFERING)
```

**Display current value of variable SYNTH_SIZING**
```tcl
echo $::env(SYNTH_SIZING)
```

**Set new value for SYNTH_SIZING**
```tcl
set ::env(SYNTH_SIZING) 1
```

**Display current value of variable SYNTH_DRIVING_CELL to check whether it's the proper cell or not**
```tcl
echo $::env(SYNTH_DRIVING_CELL)
```

**Running synthesis**
run_synthesis

**When the slack has met**

**Running Placement**
```tcl
run_placement
```
![VirtualBox_vsdworkshop_30_09_2024_19_27_29](https://github.com/user-attachments/assets/79ff607f-18ca-41b3-8adb-b517f72375d0)

## 5. Final Steps for RTL2GDS using triton Route and openSta

### Lab Implementation:

**Objective :** TO run the following tasks:
1. Generate Power Distribution Network (PDN) and load the layout.
2. Perform detailed routing using TritonRoute


**Invoking the Openlane flow using picorv32a :**

**Changing directory to Openlane**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane
```

**Alias docker**
```bash
alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
```
Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command.
```bash
docker
```

**Invoke the OpenLane flow in the interactive mode**
```bash
./flow.tcl -interactive
```

**Now that we have invoked the OpenLANE flow, we require the package**
```tcl
package require openlane 0.9
```

**Now we need to prep the the design, in this case we are using 'picorv32a' design**
```tcl
prep -design picorv32a
```
![VirtualBox_vsdworkshop_01_10_2024_09_34_25](https://github.com/user-attachments/assets/69b9c477-721a-4429-8708-ae8b42eca3f1)

**Addiitional commands to include newly added lef to openlane flow merged.lef**
```tcl
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
```

**Set new value for SYNTH_STRATEGY**
```tcl
set ::env(SYNTH_STRATEGY) "DELAY 3"
```

**Command to set new value for SYNTH_SIZING**
```tcl
set ::env(SYNTH_SIZING) 1
```

**Running synthesis**
```tcl
run_synthesis
```
![VirtualBox_vsdworkshop_01_10_2024_09_38_45](https://github.com/user-attachments/assets/6270cf48-2f67-48f3-b3ee-19f6a68bda68)

**Following commands are alltogather sourced in "run_floorplan" command**
```tcl
init_floorplan
place_io
tap_decap_or
```

![VirtualBox_vsdworkshop_01_10_2024_09_41_44](https://github.com/user-attachments/assets/88fe5e37-2560-49fb-a768-51c31cb2ae79)

![VirtualBox_vsdworkshop_01_10_2024_09_42_38](https://github.com/user-attachments/assets/92e3d2c6-21ca-41dc-9925-e08b5be41c62)

**Run placement**
```tcl
run_placement

![VirtualBox_vsdworkshop_01_10_2024_09_44_07](https://github.com/user-attachments/assets/9c1f26aa-aec2-4724-99b9-1a5570d0a562)

**Incase getting error**
```tcl
unset ::env(LIB_CTS)
```

**Run Clock Tree Synthesis**
```tcl
run_cts
```

![VirtualBox_vsdworkshop_01_10_2024_09_51_10](https://github.com/user-attachments/assets/46be6f9c-3d56-4463-ad10-92731dcf969b)

**Power distribution network**
```tcl
gen_pdn
```

![VirtualBox_vsdworkshop_01_10_2024_09_51_33](https://github.com/user-attachments/assets/4c5767d8-8c53-4948-bf42-f899cea9dae7)

![VirtualBox_vsdworkshop_01_10_2024_09_52_00](https://github.com/user-attachments/assets/a2468075-93e0-4c27-82fc-38d834f0df0e)

**Change the directory to generated PDN def path**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/01-10_04-04/tmp/floorplan/
```

**Load PDN def in magic tool**
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read 14-pdn.def &
```

![VirtualBox_vsdworkshop_01_10_2024_09_57_13](https://github.com/user-attachments/assets/b7cccfd1-572f-47ed-a079-04d05e2eb33f)

Screenshots of PDN def in magic tool:
![VirtualBox_vsdworkshop_01_10_2024_09_57_31](https://github.com/user-attachments/assets/f127df83-88fd-479f-904f-0720a64a9f8c)

![VirtualBox_vsdworkshop_01_10_2024_09_57_59](https://github.com/user-attachments/assets/f4e33d65-db4e-4396-b28f-342ec22322ec)

![VirtualBox_vsdworkshop_01_10_2024_10_00_54](https://github.com/user-attachments/assets/f5a3574e-1d1a-4acd-8a3c-7e18b9f3d435)

![VirtualBox_vsdworkshop_01_10_2024_10_02_00](https://github.com/user-attachments/assets/32f3c93b-e533-44da-83b5-097a2c987657)

**Check value of 'CURRENT_DEF**
```tcl
echo $::env(CURRENT_DEF)
```

**Check value of 'ROUTING_STRATEGY**
```tcl
echo $::env(ROUTING_STRATEGY)
```

**Run Routing**
```tcl
run_routing
```

![VirtualBox_vsdworkshop_01_10_2024_10_04_35](https://github.com/user-attachments/assets/487acf6f-5c10-4dd8-b8fe-6a25f488fbfc)

![VirtualBox_vsdworkshop_01_10_2024_11_10_24](https://github.com/user-attachments/assets/965ea1ad-90be-4bad-a9a0-9fff1e6c8735)

![VirtualBox_vsdworkshop_01_10_2024_11_11_00](https://github.com/user-attachments/assets/9564b2ca-b996-421b-9e33-8e75c4e34e05)

**Change the directory to routed def path**
```bash
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/01-10_04-04/results/routing/
```
**Load the routed def in magic tool**
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.def &
```
Screenshots of routed def in magic tool:
![VirtualBox_vsdworkshop_01_10_2024_11_13_54](https://github.com/user-attachments/assets/12bbe8ec-a937-4073-bdcb-754dcacdee83)

![VirtualBox_vsdworkshop_01_10_2024_11_14_41](https://github.com/user-attachments/assets/2beacc03-6ff6-4c70-8f77-db4da0c1babd)

![VirtualBox_vsdworkshop_01_10_2024_11_15_43](https://github.com/user-attachments/assets/40f0a6b2-4ad4-4e0f-81d3-a8dbc6c37b3d)

![VirtualBox_vsdworkshop_01_10_2024_11_18_15](https://github.com/user-attachments/assets/eb26b785-7abb-48f3-b9ff-0d1497151205)
**Fast Route guide :**
![VirtualBox_vsdworkshop_01_10_2024_11_34_02](https://github.com/user-attachments/assets/6dc00975-7cb1-4f84-afd7-cb9ab3e2cd4b)

![VirtualBox_vsdworkshop_01_10_2024_11_34_09](https://github.com/user-attachments/assets/e672a6f6-fa9f-4f85-a0f4-d4d2dad7ca61)
