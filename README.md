# SIBOOR-Voron-2.4-AUG

## Assembly Guide

### 1. Assembly Manual 2.4r2
- [Link]
- Pay close attention to manual comments.
- Green-highlighted sections denote variances between SIBOOR V2.4 [AUG] and VORON's official BOM.
- Red-highlighted sections indicate differences in metal structural components between SIBOOR V2.4 [AUG] and VORON's official BOM.

### 2. TAP Assembly Tutorial
- [Link]

### 3. SB Head Assembly Tutorial
- [Link]
    - Install the heating rod and thermistor.
    - Set up the CAN board, illustrate wiring, and set jumpers.
    - Install the Y-axis limit switch.
    - Install CAN board cables and steel wires.

### 4. Display Installation

### 5. Nevermore Installation

### 6. Wiring and Inspection

### 7. Networking and Configuration
1. Before debugging, ensure MCU communication between the CAN board and the mainboard is established.
   [Link:]

## FAQ

- Where can I find the BOM list for SIBOOR V2.4 [AUG] to verify my package?  
  Access the BOM list for SIBOOR V2.4 [AUG] [here](link).

- Is it necessary to burn the system and firmware?
  The Pi's built-in system is pre-matched with the mainboard and CAN bus. Avoid version upgrades unless issues arise.  

- Why are some metal structural components unused?  
  Certain parts are designed for the Afterburner version and are not applicable here. Remove them before assembly.

- Why are some screws in different positions from the official instructions?  
  Due to metal processing and weight reduction, some screws differ. See red annotations in Assembly_Manual_2.4r2.

- What are the Klipper account credentials?  
  Username: biqu, Password: biqu (Note: Case-sensitive)

- Why can't my Dragon hotend be installed on the printed part?  
  Remove the cylindrical joint on top of the Dragon hotend before installation. See illustration below.

- Why is there only one drag chain in my kit?  
  SIBOOR V2.4 [AUG] uses a CAN board, eliminating the need for X and Y axis drag chains. Wires will hang inside the chamber, reducing wear and poor contacts.

- Why can't my Z-axis reach the top due to the length limit of the Z-axis drag chain?  
  Removing the X and Y axis drag chains increases visible space, but printing height is still limited. For example, the 300 model can print up to around 280mm, and the 350 model up to around 330mm.

- Why are there no honeycomb skirts and fixed box panels in the kit?  
  If you didn't purchase decorative parts separately, you need to 3D print them. Download [here](link).

- Why does the hotend lower to 150℃ before raising to the printing temperature during pre-print preparation?

- How can I get technical support or after-sales service?

- Where can I download the system if mine is damaged?

## Links
- VORON Official Website: https://vorondesign.com/
- Klipper Official:https://www.klipper3d.org/
- BTT Official: https://github.com/bigtreetech


### BTT links :[Octopus Pro(446)](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-Pro)+[BTT Pi](https://github.com/bigtreetech/BTT-Pi) + [CAN RP2040](https://github.com/bigtreetech/EBB/tree/master/EBB%20SB2209%20CAN%20(RP2040))  
##
* **The pi built-in system has been matched with the motherboard and canbus. If there are no abnormalities, please do not upgrade the version at will. [(System)](https://drive.google.com/file/d/1oGNcbJPUD5zyJWyPYAsPpvsBOQSKj1cR/view?usp=sharing)**

# Kit related information
* **SIBOOR-Voron-2.4-AUG:[Bom](https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/SIBOOR_V2.4_AUG_BOM.md)**  
* **If you purchased the CNC kit, please click on the blue installation document below to view the differences with the official one: [Installation documentation](https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/V2.4%20R2%20V1.5%20CNC%20Assembly%20discrepant%20Manual.pdf)**  
**(It should be noted that the hot end included in the CNC is the old version of the AB hot end, so if you purchase the CNC kit, you need to use the printed version of the SB hot end.)**  
* **[Click here](https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/connection.md) ,Connection steps between motherboard and canbus.**  

* **[Click here](https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/0928%20SIBOOR%20V2.4%20R2%20AUG%20Wiring%20Diagram.jpg) ,Octopus motherboard wiring diagram.**
<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/0928%20SIBOOR%20V2.4%20R2%20AUG%20Wiring%20Diagram.jpg width="380"/><br/>
* **[Voron 2.4r2 PG7 Cable Gland and Endstop](https://www.printables.com/model/325765-voron-24r2-pg7-cable-gland-and-endstop)**
<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/Y-canbus.png width="300"/><br/>

# Things to note
## [Download](https://github.com/VoronDesign/Voron-2/raw/Voron2.4/Manual/Assembly_Manual_2.4r2.pdf) official assembly instructions
## Initial calibration settings Docs : [Vorondesign](https://docs.vorondesign.com/build/startup/)
## The short circuit position required by canbus
* Red is the position where the jumper cap needs to be inserted, and green is the position of the PT1000 thermal DIP switch.
* <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/canbus1.jpg width="600"/><br/>
* <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/canbus2.jpg width="600"/><br/>
* <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/EBB%20SB2209%20CAN%20V1.0%EF%BC%88RP2040%EF%BC%89-Pin.png width="600"/><br/>
