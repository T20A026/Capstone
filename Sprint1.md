# Sprint 1 

## Statement

Sprint 1 Will be the initail configuartion and settup for the canbus controller, and the hareware configuration. This will also involved weather I am proceeding with the Aurduino + Sparkfun Hat, or the Raspberry Pi 4 + RS485 Controler Board. I am curious to see how debian on the RPi treats the canbus interface, and if standard networking tools can be used with it, as research says that the canbus hat will work with debian much like a primative network interface, when configured with standard drivers. 

## Breakdown

* Build hardware, and nessisary semi permenant connection, and required adapters/power source for the device
* Acess the Can Network and collect packets from the netowkr, to see formatting, and compatible software
* Build system of collection, and logging, and provide a organization system

## Reflections

Week 02, Reflectiond

This week was spent reviewing the project, and checking some of the wiring components. I want to make sure that I dont damage any of the hardware, as I will be attempting to power the Rpi, and Hat from the OBD2 Port on the vehicle without external power. I did think about revising this as that would mean that the device would loose power when the car key is in the off position, may move to a 12V cigarette lighter plug adapter, and a battery bank to allow power even after the car is powered off. 

