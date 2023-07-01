# UniRetroROM
C64 and Vic20 replacement ROM 3 in one
With this adapter using a 27C256 you can replace a Commodore Vic20 or 64 breadbin rom (2332 or 2364)
by simply moving a jumper to emulate the Basic, Kernal or character ROM.

![alt text](https://github.com/zeus074/uniretrorom/blob/main/IMG/uniromv1.jpg)

:coffee: if you want the PCB, please support me and follow this link : <a href="https://www.pcbway.com/project/shareproject/UniRetroRom_26f4ca96.html" target="_NEW">PCBWAY!</a>

**Components:**

R1,R2: 10K Ω

R3,R4: 100K Ω

C1: 100nF 16/25v

U1: AT28HC256E

** Configuration **

J1 is used to select the rom

open: Rom Characters

1-2: Rom Kernal

2-3: rom Basic


JP2 is used to bring CS2 into the 2332 ROMs.

It is needed only in the vic20 character rom because this computer uses both CS1,CS2 signals.

In the C64 character rom it is optional, while it should not be jumpered if a 2364 is used. 


open: 2364 (or even 2332 C64)

closed: 2332 Vic20 only (also works on 2332 C64)

** Build a ROM **

To create the rom to be inserted into 28C256 you need to start from the character ROM and insert it 2 times (to get around the CS2 problem that might keep the A12 pin high).

Then the Basic ROM must be inserted and finally the Kernal ROM must be inserted.
 
Check the image to remove any doubt.

![alt text](https://github.com/zeus074/uniretrorom/blob/main/IMG/maprom.png)

To write the eeprom I used the Xgecu T48 programmer 

http://www.xgecu.com/en/ 

and a clamp with wires soldered to a socket.

You can also use a SOIC28 adapter, but you will only be able to program it before soldering it to the PCB.

Watch the video of the making and testing on the Retrofixer channel and subscribe thanks!!!

https://youtu.be/x2bJ3eeLD8s