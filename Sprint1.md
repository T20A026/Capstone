# Sprint 1 

## Statement

Sprint 1 Will be the initail configuartion and settup for the canbus controller, and the hareware configuration. This will also involved weather I am proceeding with the Aurduino + Sparkfun Hat, or the Raspberry Pi 4 + RS485 Controler Board. I am curious to see how debian on the RPi treats the canbus interface, and if standard networking tools can be used with it, as research says that the canbus hat will work with debian much like a primative network interface, when configured with standard drivers. 

## Breakdown

* Build hardware, and nessisary semi permenant connection, and required adapters/power source for the device
* Acess the Can Network and collect packets from the netowkr, to see formatting, and compatible software
* Build system of collection, and logging, and provide a organization system

## Reflections

Week 02, Reflection

This week was spent reviewing the project, and checking some of the wiring components. I want to make sure that I dont damage any of the hardware, as I will be attempting to power the Rpi, and Hat from the OBD2 Port on the vehicle without external power. I did think about revising this as that would mean that the device would loose power when the car key is in the off position, may move to a 12V cigarette lighter plug adapter, and a battery bank to allow power even after the car is powered off. 


Week 03, Reflection

This week was light work, spent some time collecting tyhe cabling i would need, and the wiring and tools from storage for soldering the data wires from the OBD2 connector and to the power adapter. Has NECCDC this week so I didn't want to be too burned out for Saturday. 

Week 04, Reflection

This wee was pretty productive, and I have the hardware set up and working. I elected to use an Raspberry pi 3 Model B, as it offered a good tradeoff of minimal power consumptionl, and power. I an using RPI OS Legacy, Lite, 32 Bit. I chose this as it is a small OS install, leaving a good amount of space on the 32Gb SD Card Im using, wich is a Samsung EVO Model for Reliability, and speed. I attached the hat, and sucessfully connected the RS484 Hat to the device, and I am accessing it via SSH over its wireless connection. Another reson I picked a RPI3 is it uses MicoB USB and Only requires around 1000 Ma of power or !5 Watts when sniffing can messages. After Connecting the hat, I was able to confirm functionality using the "Open CAN" Project, linked at the end of my settup documentation, I was able to send, and loopback dump a can message, showing the hat was working. I now just need to solder up the two wires from the CAN hat for high and low, to the OBDII COnnector I used. 
Documentation: https://github.com/T20A026/Capstone/wiki/RS485-Hat-Connection-Instructions 
