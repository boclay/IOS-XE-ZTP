# IOS-XE-ZTP

Code for ZTP with IOS XE 16.9


## Business/Technical Challenge

Business Problem - Legacy devices in the customer network are approaching end of life milestones and need to be replaced. However, the customer does not always have enough staff resources to deploy the required quantity of new Cisco networking equipment. Additionally, new customer deployments are prone to error due to manual provisioning.

Technical Challenge - Develop a solution which enables the customer to auto-provision devices thus reducing deployment errors and saving staff resource time.

## Proposed Solution

Proposed Solution - Create a Python script with supporting services to auto-provision devices for Day 0 deployment.


### Cisco Products Technologies/ Services

The solution includes the following technologies:

- Catalyst 9000 and 3650 series switches
- Cisco ENCS 5400 Branch NFV Platform
- Cisco ISRv virtual router
- IOS XE 16.9 with IOx guestshell support
- IBNS 2.0
- Ubuntu Linux server (open source)
- Apache2 WebServer (open source)
- ISC DHCP Server (open source)
- Node.js json-server (open source)
- Python 2.7 (open source)

Our solution will leverage the following Cisco technologies

* [Catalyst 9300] (http://www.cisco.com/go/catalyst9000)
* [Catalyst 3650] (http://www.cisco.com/go/3650)
* [IOS XE] (https://www.cisco.com/c/en/us/products/ios-nx-os-software/ios-xe/index.html)
* [IBNS 2.0] (http://www.cisco.com/go/ibns)
* [ZTP] (https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/prog/configuration/169/b_169_programmability_cg/zero_touch_provisioning.html)
* [IOx] (https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/prog/configuration/169/b_169_programmability_cg/guest_shell.html)

## Team Members


* Bob Clay <boclay@cisco.com> - Global Enterprise
* Ameron Sheikh <imsheikh@cisco.com> - Commercial
* Jason Whiteaker <jawhitea@cisco.com> - Customer Experience


## Solution Components


<!-- This does not need to be completed during the initial submission phase  

Provide a brief overview of the components involved with this project. e.g Python /  -->

Solution components include:

* Files
* Open Source Tools
* Catalyst 9k, 3850, or 3650 switches running IOS XE 16.9

### Files

The files posted for this project include two Python scripts, a CSV file, and an IOS template.

The ZTP.py script contains the main Python program that runs in Guest Shell on the device. This script is automatically downloaded from a web server as identified in the DHCP reply when the network device boots onto the network for the first time.

The csv2json.py script is a server-side script which retrieves a list of devices and associated attributes from a CSV file and creates a JSON file. The Node.js service uses the JSON file to return device attributes based on the device serial number.

The serial-ip.csv file is a comma separated variable (CSV) file which contains a list of devices based on serial number. Each serial number corresponds to a list of device attributes such as hostname, IP address, etc. related to the devices' location in the network. 

The IBNS2.cfg file is an IOS template that contains commands for configuring an IOS XE 16 switch for use with ISE in a high security enviornment. The IOS configuraiton includes commands for AAA, Device Profiling, and an Interface Template for dot1x for the access ports. 


## Usage

<!-- This does not need to be completed during the initial submission phase  

Provide a brief overview of how to use the solution  -->



## Installation

How to install or setup the project for use.


## Documentation

Pointer to reference documentation for this project.


## License

Provided under Cisco Sample Code License, for details see [LICENSE](./LICENSE.md)

## Code of Conduct

Our code of conduct is available [here](./CODE_OF_CONDUCT.md)

## Contributing

See our contributing guidelines [here](./CONTRIBUTING.md)
