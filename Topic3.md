# Topic Three, CANBUS Sniffing, and Control

## Proposal 3

> **CANBUS Sniffing, and Control: **
> Sniff and decode GM's custom CANBUS communication protocol found in their "GM Epsilon" Platform. These cars use a Gm style canbus system, with three canbus networks: The I, P, and C Bus. Here we will be focusing on the "I" bus wich is reffered to as the Instrimentation Bus.
> The Goal is to sniff the network via the OBD II port, and this will allow us to collect data from the bus, using a simple canbus decoder aht for either an aurduino, or a Raspberry pi, and from that reverse engineer the protocol, and be able to provide requests, and replied on the network, aswell as collect data for display.

### Milestones:

Phase 1:
This Phase would conatin the Settup and OCnfiguration of our tools, as well as a basic understanding of the system

* Research the data type, and the how the requests are formatted
* Build and configure the device, to be used for collecting the data
* Start sniffing the canbus traffic
* Generate repeatable requests/results that can be either decoded or correlated
* Generate a Chart or Resource for the layout of the requests

Phase 2:
This phase is where we start making use of the data that we are gathering

* Design a system to display data that could be usefull for the driver
* Try and make commands/requests to the system
* Output data to the User

Phase 3:
This phase is the DF/Hunting phase where we will see how far we can go, and potental problems or damage that can be done

* See if there is any message request filtering, or packet checking
* See if any device can make requests or if you need to spoof a module
* Can we make tasks/commands to th emodules, for alteretor uses
* Where ar elogs or data stored, and is it protected
