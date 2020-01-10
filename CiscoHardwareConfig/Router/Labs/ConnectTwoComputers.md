# Lab routing two computers

We will use a router __4321__ and __two PC__

## First

Connect each PC to the Router 4321 using a __copper crossover__ connecting the __FastEthernet0__ port to the __FastEthetnet0/0__ port
and the __FastEthernet0__ of the other PC to the __FastEthetnet0/1__ port.

## Config Router

We will have to open the __CLI__ to write our commands:

```
Router>             enable
Router#             configure terminal
Router(config)      hostname cisco
cisco(config)       interface FastEthernet0/0
cisco(config-if)    ip address 192.168.10.1 255.255.255.0
cisco(config-if)    no shutdown
cisco(config-if)    exit
cisco(config)       interface FastEthernet0/1
cisco(config-if)    ip address 192.168.11.1 255.255.255.0
cisco(config-if)    no shutdown
cisco(config-if)    exit
```

### Explaining the commands

* enable -> Logs you into __enable__ mode, which is also known as user __exec__ mode or __privileged__ mode.

* configure terminal -> Logs you into configuration mode.

* hostname name -> Changes the hostname of the device that we are configuring.

* interface IP NetMask -> Assigns an IP address and a subnet mask.

* no shutdown -> brings up the interface of the device.

* shutdown -> brings down the interface of the device

* exit -> It exist from the actual configuration that you are mading.