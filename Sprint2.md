# Sprint 2 

## Statement

Sprint 2 Will start once connections are estabished, and basic collection fo data, and logging is achieved, and data formatting is gathered. Here I will beggin logging data, and creating test events to corrolate, and cross reference to internet resources, to gain and understanfing of the hearers and identities of differen modules in the car. With this data I can parse outputs from logs, and provide live output data logging, in a easy to read human form to the CLI, and if sucessful, create a simpel User Interface for the system. Once That is achived I will have an udnerstanding of the unique headers used in the cars can network, and I can attempt to spoof modules in the car, activley querying data instead of passivly collecting it, allowing changes to be made to the system.

## Breakdown

* Log data and create chart of known headers, sucspected headers, and unknown headers
* Use passive data collection for readouts, and controls to systems not part of the cars origonal systems
* Use the collected data, and communications, to provide live chanegs to systems like infotainment and others.

## Reflections

Week 1 - 
I picked up the wire i needed, as well as went and got my soldering equipment out of storage. I soldered up the connector, but havent had the time to go out and give the settup a test with the accual car. I need to verify the speed of the CAN connection being used on the cars bus, soo that I have it for when the dogle is cnnected or else I will recive nothing but garbled gibberish from the output.

Week 2 - 
I was very sick last week, on Thursday, Friday, Saturday, Sunday, and didnt make it to work, nor did I have my normal block tok work on capstone. Going to try and delegate more time on week 3 to make up for this. 

Week 3 - 
This week I have spent getting my connection established with the car. After resolving some compatiblility issues with the python dependencies for scripting, i moved on to using canutils for my connections for probing around and diagnostic. Right now the issue i am currnetly working on is the car belived that the CAN device I am connecting is the ABS module, or an aditional component of it, as when I attemp to establish a connection, the car throws an error that remains untill I restart the car. Once i restart I can attemot again but I am greeted with the same error. I am working now to try and figure out how to change the unique Idntifier of the module, or in this case its header id, soo that this conflict is resolved. Right now becuase of the error correcting nature of CAN the car will stop attempting to contact what it thinks is the ABS module when the can module connects, and in turn it denied both the legitimate ABS component on the CAN network and also the hat, leading to no response, and therefor no dump. 
