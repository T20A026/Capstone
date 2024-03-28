# Sprint 2 

## Statement

Sprint 2 Will start once connections are estabished, and basic collection fo data, and logging is achieved, and data formatting is gathered. Here I will beggin logging data, and creating test events to corrolate, and cross reference to internet resources, to gain and understanfing of the hearers and identities of differen modules in the car. With this data I can parse outputs from logs, and provide live output data logging, in a easy to read human form to the CLI, and if sucessful, create a simpel User Interface for the system. Once That is achived I will have an udnerstanding of the unique headers used in the cars can network, and I can attempt to spoof modules in the car, activley querying data instead of passivly collecting it, allowing changes to be made to the system.

## Breakdown

* Log data and create chart of known headers, sucspected headers, and unknown headers
* Use passive data collection for readouts, and controls to systems not part of the cars origonal systems
* Use the collected data, and communications, to provide live chanegs to systems like infotainment and others.

## Reflections

Week 05 - 
I picked up the wire i needed, as well as went and got my soldering equipment out of storage. I soldered up the connector, but havent had the time to go out and give the settup a test with the accual car. I need to verify the speed of the CAN connection being used on the cars bus, soo that I have it for when the dogle is cnnected or else I will recive nothing but garbled gibberish from the output.

Week 06 - 
I was very sick last week, on Thursday, Friday, Saturday, Sunday, and didnt make it to work, nor did I have my normal block tok work on capstone. Going to try and delegate more time on week 3 to make up for this. 

Week 07 - 
This week I have spent getting my connection established with the car. After resolving some compatiblility issues with the python dependencies for scripting, i moved on to using canutils for my connections for probing around and diagnostic. Right now the issue i am currnetly working on is the car belived that the CAN device I am connecting is the ABS module, or an aditional component of it, as when I attemp to establish a connection, the car throws an error that remains untill I restart the car. Once i restart I can attemot again but I am greeted with the same error. I am working now to try and figure out how to change the unique Idntifier of the module, or in this case its header id, soo that this conflict is resolved. Right now becuase of the error correcting nature of CAN the car will stop attempting to contact what it thinks is the ABS module when the can module connects, and in turn it denied both the legitimate ABS component on the CAN network and also the hat, leading to no response, and therefor no dump. 

Week 08 - 
Sucessfully connected to the CAN network of the car. It took some diagnostics, and some bitrate calucations, but I was able to extablish connections, without panicking the CAN network, by setting the reciver to listen only mode, as well as I was able to then capture the communications of the vehicle from the OBD Diag CAN network, using tshark. This allowed me to export the data from the PI, and Open it in wireshark for easy interpritation. I do have to now further pursue the CAN headers, as they seem to be different from the OG Saab CAN networking. Im going to see if I can find resources from other 'GMLAN' cars in hopes that there is some overlap. The I-BUS network does have alot of components and modules connected to it that are reused in other GM Producst so this should be a helpfull resource. 

Week 09 - 
Still working on getting the can signals decoded. I have found some useful stuff related to simaler vehicals, as awell as some references to some fo the generic/standardized GM communication headers. I also found out that I was connected to the "P" Bus wich is the engine bus for this capture, and not the I BUS wich is also accessable from the OBD2 port. I am going to try and establish comms and a capture from the I bus on the car, but it is possible according to some resources that it is a single wire CAN network and this might not be readable from my controller. I am going to continue to dig into the CAN headers of the P bus as these will be helpful for some of my goals, and hopefully I can find a good resource, or at least a starting point to infeer the module headers. 

Week 10 - 
This week I was working on getting additonal sources of data, for knowing what each fo the messsgaes in the entwork capture I made where. I am going to ask on some forums, and alsoa ttempt to see if I can use a software, designed for accessing the system, and remove values, or check for data in that system. Currently this is the roadblock, and I have been banging my head on it, but I am going to see if there are any other ways for me to get this data, and try and readjust my scope. 
