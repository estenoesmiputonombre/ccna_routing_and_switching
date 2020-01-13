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

## Interface Names

| Router model | Port location/Slot number | Slot/Port Type | Slot Numbering Range | Example |
| ------------ | ------------------------- | -------------- | -------------------- | ------- |
| 2501 | On board | Ethernet | Interface-type number | ethernet0 (e0) |
|  | On board | Serial | Interface-type number | serial0 (s0) & s1 |
| 2514 | On board | Ethernet | Interface-type number | e0 & e1 |
|  | On board | Serial | Interface-type number | s0 & s1 |
| 1721 | On board | Fast Ethernet | Interface-type number | fastethernet0 (fa0) |
|  | Slot 0 | WAC(WIN interface card) (serial) | Interface-type number | s0 & s1 |
