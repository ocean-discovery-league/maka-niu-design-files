The GNSS chip on the Maka Niu endcap needs to have different firmware flashed to use i2c. 
Without doing this, the Maka Niu cannont communicate with the GPS chip.

Whats is needed or recommened:
-a windows pc
-a serial USB cable that outpus 3.3v. TTL-232RG-VSW3V3-WE is known to work. 
-an endcap PCB
-a soldering station


Proceduce:

-Install gnsstool and the CP210x drivers (provided in this folder) and open the origram SW GNSS tool

-Solder the red, black, yellow and orange wires of the Serial USB cable to the endcap PCB, as shown in GNSS_Flashing_Example.jpg 

-In SW GNSS tools, look at the ports shown at the bottom left of the window. Connect the USB serial RS232 cable 
(which shoudl already be connected to the endcap PCB), and note which new port was added when you connected the USB cable
Select that port, set the baudrate, at bottom of the window of SW GNSS tool to 115200.
(if unit has been flashed before and you are reflashing some other newer firmware, set the baudrate to 9600)


-Connect to the GNSS chip on the endcap by clicking on the icon on the upper left of SW GNSS tool that looks like a cable
If the connection succees, the devices firmware should get printed in the command window of SW GNSS tool. You can also get firmware by clicking on the icon FW Ver.

-If you have a connection, you are ready to flash the device. Click on the icon with the red downward arrow. 
You need to select a "Download Agent" and a "ROM" file. Choose the download agent that is in the same directory as this read me.
The ROM is also in this directory: AXN5.1.6_8549_3333_96.1151100.1
Click Download to begin the flash. Hopefully SW GNSS completes and says "Pass"

-You can now disconnect the cable from your computer and unsolder the wires from the endcap PCB. the PCB is now ready to use


