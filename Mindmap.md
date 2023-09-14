# Mind Map:

![Mind Map](https://github.com/T20A026/Capstone/assets/70958837/1c901e02-cead-40de-bd4b-d32dd8d1a263)

## Topic: Secure IoT Network

I have broken down my topic into for major sections, and in tern 4 sprints of configuration and design. I am Calling them sprints but they do have some internal connections where some sections will need to be completed before others, and or refined by the outcome. 

### Environment
This is the actual environment where all the development, testing, and production networking happens.

* Proxmox Virtual Networking
	* Routing Configuration
		* After setting up the proxmox Environment i will be using I will need to configure some internal settings, and learn a bit more about making non flat networks within a proxmox environment. Additionally I will need to pick a routing product to use for the networks gateway
	* Network Isolation
		* Once routing is configured as a VM on the network, i will need to make sure I have to configure network isolation to prevent internal connections from other IoT devices, that don't need to contact each other. 
* IoT Devices
	* Real Devices Passed Through
		* Here I will use a spare wireless access point, and a separate network switch to connect physical to the virtual network on the proxmox system, and use these to connect real IoT devices for testing and use without affecting personal devices.
	* Replicated or Virtualized
		* Here i will configure some services and devices, that do not require physical hardware to work (3D printer controllers, smart home hubs, small media storage devices, etc.)
	* Vendors and Protocols
		* I will also need to see if there are differences in function, security, and capability based on the devices networking protocols used. 
* Snapshots
	* Additionally I will need to configure a reliable way for automatic and manual backups and snapshots of these virtual devices be taken, so they can revert them if there is an issue with the environment, or a configuration mistake is made.


### Policy
This is where I will design, implement, and refine a policy system for use with IoT devices. This will include a yes, circumstantial, and no "fly" list for devices on the network.  This will be determined on the following info:
* Device Brand
	* Is the device known for its security issues, has it been leveraged before?
* Protocol used
	* Is the protocol used by the device, outdated, or inherently flawed?
* Legitimate Use case
	* Does the device every have a use case in an enterprise or business environment
* Location
	* Will this device be in a location, where it would be capable of collecting sensitive data?
* Data Collection Capabilities
	* Is it capable of collecting data based on its use and construction?
* Preparation 
	* The process that must be followed for approved use of devices. 

### Monitoring and Logging
This section is the collection, monitoring, and logging side of the project, where network traffic will be collected and logged on its destination and source, and will be used for finding, and alerting of suspicious activity.
* Security Onion 
	*  Log Retention
		* How long and what logs will be retained
	* Custom Alerts and Monitoring
		* What alerts will be set, what are common malicious domains, and what traffic are these devices generating that is not necessary? 

### Networking and Access Control
Here I will be configuring the networks rules, IP ranges, settings, and authentication methods. 
* Connection Method
	* WPA2 vs Open with MAC Whitelisting vs both
* Device isolation and network parameters
	* What internal isolation will be used, can be used, and cant be used.
* Scope and size Requirements 
	* How many devices, users, and what network hardware?
