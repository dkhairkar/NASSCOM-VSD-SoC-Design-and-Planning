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

![VirtualBox_vsdworkshop_27_09_2024_00_01_11](https://github.com/user-attachments/assets/60472270-2ace-463d-8158-e5e68ec39d3a)

![VirtualBox_vsdworkshop_29_09_2024_00_13_10](https://github.com/user-attachments/assets/7c7cf9cf-3506-4fb7-9e0e-e610de991dea)

![VirtualBox_vsdworkshop_29_09_2024_00_19_42](https://github.com/user-attachments/assets/08681fb0-6140-4f1e-9ad8-ee17ec3746b9)

![VirtualBox_vsdworkshop_29_09_2024_00_24_09](https://github.com/user-attachments/assets/366578ea-a599-48f5-bb2c-5fd072e51591)

![VirtualBox_vsdworkshop_29_09_2024_00_28_15](https://github.com/user-attachments/assets/dfe6f989-97de-4a8e-805a-dc78726709e0)

![VirtualBox_vsdworkshop_29_09_2024_00_28_45](https://github.com/user-attachments/assets/46781375-b1a9-4ad5-aab1-a0b42db21f14)

![VirtualBox_vsdworkshop_29_09_2024_00_29_34](https://github.com/user-attachments/assets/c8280f95-c6ea-4711-9a83-2aad01ae41a5)

![VirtualBox_vsdworkshop_29_09_2024_00_29_44](https://github.com/user-attachments/assets/35a1bc6a-ceea-4e5a-a989-dd12c9b91dc6)

![VirtualBox_vsdworkshop_29_09_2024_00_30_50](https://github.com/user-attachments/assets/8650761a-984e-479a-9e77-ed110b825ca7)

![VirtualBox_vsdworkshop_29_09_2024_00_32_11](https://github.com/user-attachments/assets/ceed3995-b4ec-41fd-9f05-54f4669556e1)

![VirtualBox_vsdworkshop_29_09_2024_00_32_29](https://github.com/user-attachments/assets/c83d6b80-9081-4678-aef4-439910f4bd0c)

![VirtualBox_vsdworkshop_29_09_2024_20_37_38](https://github.com/user-attachments/assets/eb826f23-9fe5-4acf-95c5-35b88285708e)

![VirtualBox_vsdworkshop_29_09_2024_20_37_53](https://github.com/user-attachments/assets/e50bbbbc-0f5c-48d5-a974-7e1daa7aa190)

![VirtualBox_vsdworkshop_29_09_2024_21_06_09](https://github.com/user-attachments/assets/24136f4d-10a5-4488-a2ce-98ff9909a882)

![VirtualBox_vsdworkshop_29_09_2024_20_38_19](https://github.com/user-attachments/assets/a3e5076a-53ab-4249-b539-05bb129b7b5f)

![VirtualBox_vsdworkshop_29_09_2024_23_21_56](https://github.com/user-attachments/assets/ee1f5f9e-0f92-4e4f-8b6a-bb3b0285a2bf)

![VirtualBox_vsdworkshop_29_09_2024_23_22_18](https://github.com/user-attachments/assets/a3815033-be2b-482d-9a2d-c7a3a32ddda3)

![VirtualBox_vsdworkshop_29_09_2024_23_27_09](https://github.com/user-attachments/assets/3e07b672-1f18-4dbe-926e-1377507f27fe)

![VirtualBox_vsdworkshop_29_09_2024_23_26_58](https://github.com/user-attachments/assets/c2bcef7e-5a6c-4246-ab52-987df586fc85)

![VirtualBox_vsdworkshop_29_09_2024_23_30_24](https://github.com/user-attachments/assets/5869d269-8c97-47bb-8a7a-cb85f1a99251)

![VirtualBox_vsdworkshop_29_09_2024_23_31_50](https://github.com/user-attachments/assets/b933d86f-3638-48f4-9581-a81ea055deae)

![VirtualBox_vsdworkshop_29_09_2024_23_32_30](https://github.com/user-attachments/assets/701829c7-6ffa-47b2-9e0d-f9c869127ba6)

![VirtualBox_vsdworkshop_30_09_2024_00_56_57](https://github.com/user-attachments/assets/1a361264-b23a-4429-85eb-6d2055201205)

![VirtualBox_vsdworkshop_30_09_2024_00_57_45](https://github.com/user-attachments/assets/c81a23bd-0dfe-451a-acd3-9342388a71ed)

![VirtualBox_vsdworkshop_30_09_2024_00_58_01](https://github.com/user-attachments/assets/7e8c8234-500b-49ad-a90f-8fec9c707929)

![VirtualBox_vsdworkshop_30_09_2024_01_04_55](https://github.com/user-attachments/assets/af05e829-181b-43e1-823a-ffb33465e2fa)

![VirtualBox_vsdworkshop_30_09_2024_01_09_15](https://github.com/user-attachments/assets/c3165142-35c0-4908-93cf-3715b24b25de)

![VirtualBox_vsdworkshop_30_09_2024_01_10_05](https://github.com/user-attachments/assets/7b3a5734-04d3-4bc0-988e-8e5e4c142d85)

![VirtualBox_vsdworkshop_30_09_2024_01_10_14](https://github.com/user-attachments/assets/95df352f-0755-4532-99f9-49d541d4ce1f)

![VirtualBox_vsdworkshop_30_09_2024_01_21_05](https://github.com/user-attachments/assets/c7f92b73-d902-45f1-91b0-337df8b8856a)

![VirtualBox_vsdworkshop_30_09_2024_01_21_31](https://github.com/user-attachments/assets/ca890495-44bc-4409-aaa7-5988d960c2c1)

![VirtualBox_vsdworkshop_30_09_2024_01_21_40](https://github.com/user-attachments/assets/b2b1d67e-f71d-4c0a-92f6-e2a0f9202d59)

![VirtualBox_vsdworkshop_30_09_2024_01_22_18](https://github.com/user-attachments/assets/c2b999bb-65ba-4388-83d5-89cdbb33b168)

![VirtualBox_vsdworkshop_30_09_2024_01_24_50](https://github.com/user-attachments/assets/336cdf03-836f-46ad-8327-4d0ebe1a93f6)

![VirtualBox_vsdworkshop_30_09_2024_01_26_15](https://github.com/user-attachments/assets/10012b8c-fee9-4e01-9902-ef09f6f3c03c)

![VirtualBox_vsdworkshop_30_09_2024_01_28_48](https://github.com/user-attachments/assets/00e53f5a-26fc-4681-9a81-8bd3d7fdf129)

![VirtualBox_vsdworkshop_30_09_2024_01_54_03](https://github.com/user-attachments/assets/f6143250-fc2d-4742-8e7d-aff2f0a22456)

![VirtualBox_vsdworkshop_30_09_2024_01_57_20](https://github.com/user-attachments/assets/423602f4-79b5-4275-bb47-809d9e16ebf4)

![VirtualBox_vsdworkshop_30_09_2024_01_58_11](https://github.com/user-attachments/assets/63dcd3a9-f540-4e10-ab01-03bd982d5afd)

![VirtualBox_vsdworkshop_30_09_2024_01_58_42](https://github.com/user-attachments/assets/90d3dde2-91ea-4f26-9726-0bfd70565d10)

![VirtualBox_vsdworkshop_30_09_2024_02_36_33](https://github.com/user-attachments/assets/0bc59b3f-6538-4371-b393-54abbcfa9ba5)

![VirtualBox_vsdworkshop_30_09_2024_02_47_47](https://github.com/user-attachments/assets/5925f375-54ed-47a6-b82b-8a29ba0f3274)

![VirtualBox_vsdworkshop_30_09_2024_02_48_47](https://github.com/user-attachments/assets/d28498e6-be28-4899-9bee-4c364ca8aedc)

![VirtualBox_vsdworkshop_30_09_2024_02_49_16](https://github.com/user-attachments/assets/f4b026b4-dcdf-45a3-abde-9c38dd8f0212)

![VirtualBox_vsdworkshop_30_09_2024_02_50_12](https://github.com/user-attachments/assets/32ec10bb-c196-4ce3-bad8-97a973663edb)

![VirtualBox_vsdworkshop_30_09_2024_02_57_11](https://github.com/user-attachments/assets/f68eafed-db6c-4fe2-9c83-528052137ba6)

![VirtualBox_vsdworkshop_30_09_2024_03_01_37](https://github.com/user-attachments/assets/f7f97215-5553-4930-bed8-366007cc16dc)
![VirtualBox_vsdworkshop_30_09_2024_03_03_27](https://github.com/user-attachments/assets/d9a9372e-28f5-4cd4-aae7-2cc78b1984fd)

![VirtualBox_vsdworkshop_30_09_2024_03_05_18](https://github.com/user-attachments/assets/4433b434-b6e9-4993-b148-da9ffb05240f)

## 4. Pre-layout Timing Analysis and Importance of Good Clock Tree

### Lab Implementation

![VirtualBox_vsdworkshop_30_09_2024_12_15_15](https://github.com/user-attachments/assets/7577856d-e622-4dc4-bd71-ddee3d79f987)

![VirtualBox_vsdworkshop_30_09_2024_12_15_22](https://github.com/user-attachments/assets/25f2388e-3907-4fc6-b1f8-756bd7f03a35)

![VirtualBox_vsdworkshop_30_09_2024_12_17_08](https://github.com/user-attachments/assets/b36e36f0-29da-48f2-bba2-8f1ca89b32a6)

![VirtualBox_vsdworkshop_30_09_2024_12_17_59](https://github.com/user-attachments/assets/59a6d784-a039-4339-8c3a-d29b6fa155fd)

![VirtualBox_vsdworkshop_30_09_2024_12_18_54](https://github.com/user-attachments/assets/d3f5822f-e43b-4ca6-84b5-22126a909a35)

![VirtualBox_vsdworkshop_30_09_2024_13_02_14](https://github.com/user-attachments/assets/3e4de42c-8e72-4c33-938c-22d116458f77)

![VirtualBox_vsdworkshop_30_09_2024_13_12_09](https://github.com/user-attachments/assets/0b9679d9-242a-4aef-9f4e-a0d9968bbc2a)

![VirtualBox_vsdworkshop_30_09_2024_13_13_05](https://github.com/user-attachments/assets/5d08b581-0a15-46a3-8f3c-e3c8e09be2b0)

![VirtualBox_vsdworkshop_30_09_2024_13_13_45](https://github.com/user-attachments/assets/cd3f7592-946f-491e-a7ce-71e38b2a777b)

![VirtualBox_vsdworkshop_30_09_2024_13_13_55](https://github.com/user-attachments/assets/a429dbd1-dcd9-413a-a0cc-3fcf1eb25f37)

![VirtualBox_vsdworkshop_30_09_2024_13_15_00](https://github.com/user-attachments/assets/757f4e73-47b0-4656-9856-1fc3fbdc8e9c)

![VirtualBox_vsdworkshop_30_09_2024_13_14_47](https://github.com/user-attachments/assets/fe1b9372-f24e-4646-97f4-f0fab4a9b70e)

![VirtualBox_vsdworkshop_30_09_2024_13_29_20](https://github.com/user-attachments/assets/e59b14c4-db24-43ff-b141-4fdaa3149815)

![VirtualBox_vsdworkshop_30_09_2024_13_30_25](https://github.com/user-attachments/assets/e3d25640-dd84-4b0a-9f89-cad1ca0bb957)

![VirtualBox_vsdworkshop_30_09_2024_13_30_44](https://github.com/user-attachments/assets/3ee6cd4a-5afe-479f-8b87-e5afcb54422a)

![VirtualBox_vsdworkshop_30_09_2024_13_33_19](https://github.com/user-attachments/assets/25b68c75-0eab-430c-a0c8-98b79f88600f)

![VirtualBox_vsdworkshop_30_09_2024_13_31_30](https://github.com/user-attachments/assets/19dbbd6b-d5aa-40b9-bc8e-a4d8ae5bd4a3)

![VirtualBox_vsdworkshop_30_09_2024_13_31_49](https://github.com/user-attachments/assets/47ba21f1-bc04-4e4e-a5d1-72983390c9a0)

![VirtualBox_vsdworkshop_30_09_2024_13_32_30](https://github.com/user-attachments/assets/da1bed77-5c39-46f9-bab6-afd40b5ec850)

![VirtualBox_vsdworkshop_30_09_2024_13_34_02](https://github.com/user-attachments/assets/8377fff3-6f32-4e56-ba1c-bcfe3a55cf30)

![VirtualBox_vsdworkshop_30_09_2024_13_38_59](https://github.com/user-attachments/assets/46267822-7340-41e2-aaa1-614df0523ce1)

![VirtualBox_vsdworkshop_30_09_2024_14_40_57](https://github.com/user-attachments/assets/4b4e8d84-3a9d-4aee-8cd4-25f0531e39ce)

![VirtualBox_vsdworkshop_30_09_2024_14_44_03](https://github.com/user-attachments/assets/4ab41e94-a38a-4a56-b678-ee498cfe08da)

![VirtualBox_vsdworkshop_30_09_2024_14_51_17](https://github.com/user-attachments/assets/884dbab3-465f-4a17-bd13-7cc99cb34f12)

![VirtualBox_vsdworkshop_30_09_2024_14_53_22](https://github.com/user-attachments/assets/fd6b19a1-0318-4ce6-a593-eb180679a92e)


## 5. Final Steps for RTL2GDS using triton Route and openSta

### Lab Implementation:



