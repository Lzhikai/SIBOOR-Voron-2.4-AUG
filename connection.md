# SIBOOR-Voron-2.4-AUG
## [Octopus Pro(446)](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-Pro)+[BTT Pi](https://github.com/bigtreetech/BTT-Pi) + [CAN RP2040](https://github.com/bigtreetech/EBB/tree/master/EBB%20SB2209%20CAN%20(RP2040))  

## SSH
    login as: biqu
    password: biqu  
## OS image
* The latest system image is [here](https://drive.google.com/file/d/1VgO3OKcQAX13cF3s93GIxDW8_OjxlwhL/view?usp=drive_link). （The TF card included in the kit has already burned the system, and there is no need to burn it again. This is to prevent system damage from being used in the future.）
## WIFI Settings
* After the OS writes to the SD card, there is a FAT32 partition named `BOOT`, open `system.cfg` file with `Notpad`, `Notpad++` or `VSCode`.
<br/><img src=https://github.com/bigtreetech/CB1/blob/master/Images/system.png width="800"/><br/>
* Set `WIFI_SSID` as your actual wifi name and `WIFI_PASSWD` as your actual wifi password, The space character can be parsed normally without additional escape character.<br/>
<br/><img src=https://github.com/bigtreetech/CB1/blob/master/Images/wifi.png width="800"/><br/>  

* Then power on the btt pi, go to the backend of your router, look for a device named `BTT-CB1`, remember this IP address,  
and use tools such as `putty` or `MobaXterm`.  

* Make ssh connection

## Connect the motherboard and EBB    
* Connect the motherboard to the Pi using a USB cable
    * Connect via ssh and enter the following command    
```cd ~/CanBoot/scripts```    
```python3 flash_can.py -i can0 -q```

    
<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect1.png width="800"/><br/>    

* The UUID displayed at this time is the UUID of the motherboard canbus.     
    * Copy it and paste it into our cfg document.
  
<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect2.png width="800"/><br/>    

* Then connect to EBB canbus and enter this command again
    * Use RJ11 adapter to connect, pay attention to the position of green and yellow.
    * <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/toRJ11.jpg width="600"/><br/>
    * <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/RJ11.jpg width="600"/><br/>
    * It should be noted that the EBB canbus needs to be shorted to 120R, otherwise it cannot be connected.
    * <br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/120R.png width="600"/><br/>   
    * ```python3 flash_can.py -i can0 -q```

<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect3.png width="800"/><br/>  

* This is the UUID of EBB canbus, Copy it and paste it here.


<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect4.png width="800"/><br/>    

* Then press this button, save and restart, and the device connection is completed.

<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect5.png width="800"/><br/>  
<br/><img src=https://github.com/Lzhikai/SIBOOR-Voron-2.4-AUG/blob/main/Images/connect6.png width="800"/><br/>  
