# Router configuration

## Router modes

| Terminal | Function |
| -------- | -------- |
| Router> | User mode |
| Router# | Privileged mode(also known as EXEC-level mode) |
| Router(config)# | Global configuration mode |
| Router(config-if)# | Interface mode |
| Router(config-subif)# | Subinterface mode |
| Router(config-line)# | Line mode |
| Router(config-router)# | Router configuration mode |

## General commands

| Command | Function |
| ------- | -------- |
| enable | enter in the privileged mode |
| configure terminal | enables the terminal configuration mode |
| hostname | Configure the name of the device |
| enable password cisco | Sets enable password (this is plain text in the running-config file) |
| enable secret cisco | Sets enable secret password (this is encrypted text in the running-config file) |
| no enable (password or secret) | It removes the password or secret password setted |
| include something | When outputs a file, you can search for a determinated content on it |
| line {port} {number} | config the line of console an the port 0 (line console 0) |
| password cisco | Sets console line mode password to console |
| login | Enables password xxxx at login |
| show ip interface brief | show a list of the interfaces that are installed in the cisco router device |
| ip host hostname address | Set a name to an address |
| no ip domain-lookup | Turns off trying to automatically resolve an unrecognized command to a local host name |
| exec-timeout minutes seconds | Sets the time limit when the console automatically logs off. (It is a bad practise to set the min and second to 0, but in a lab environment is the best option xd) |
| copy running-config startup-config | Saved the running configuration to local NVRAM |
| copy running-config tftp | Saves the running configuration remotely to a TFTP server |
| erase startup-config | Deletes the startup configuration file from NVRAM |
| clock set xx:xx:xx Mon Day Year | Set the time of the router |
| do show command | Execute command in privileged mode while being in configure mode |
| copy run start | Save the running-config file to startup-file |
| write memory | Save the running-config file to startup-file |
| clock rate 250000 | DCE end of the serial cable |
| router RIP | Activate the RIP(Routing Information Protocol)protocol |
| network address | You set up the addresses that devices can be assigned. using the first address of the subnet |
| debug ip rip | Start to debug the protocol rip and we will receive logs of its actions |

## Interface Names

| Router model | Port location/Slot number | Slot/Port Type | Slot Numbering Range | Example |
| ------------ | ------------------------- | -------------- | -------------------- | ------- |
| 2501 | On board | Ethernet | Interface-type number | ethernet0 (e0) |
|  | On board | Serial | Interface-type number | serial0 (s0) & s1 |
| 2514 | On board | Ethernet | Interface-type number | e0 & e1 |
|  | On board | Serial | Interface-type number | s0 & s1 |
| 1721 | On board | Fast Ethernet | Interface-type number | fastethernet0 (fa0) |
|  | Slot 0 | WAC(WIN interface card) (serial) | Interface-type number | s0 & s1 |
