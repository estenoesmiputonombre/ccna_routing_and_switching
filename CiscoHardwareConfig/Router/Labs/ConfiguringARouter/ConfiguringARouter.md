# Router

We will use the Cisco router 1841 that have mainly __2 FastEthernet ports__, a __console__ port and an __aux__ port.

The network schema will be a main router and two Personal Computers that are connected to the router like that

pc - router - pc

## Interfaces

* The first interface will be a __FastEthernet0/0__ that will have a default gateway of __10.0.0.1__ using a network mask __255.255.255.128__

* The second interface will be a __FastEthernet0/1__ that will have a default gateway of __10.0.0.129__ using a network mask __255.255.255.128__

## Configuring

To configure the router, we have to connect the PCs to the router using a __crossover cable__ from the FastEthernet of the PC to the __FastEthernet0/x__

Secondly, we have to use a console cable to connect from the RS-232 of the PC to the router to be able to configure it

## Commands

* The first command will be __enable__ which will enable the __privileged user__

* The second command will be __configure terminal__ which will permit us to configure the router 1841

* We can changet he __hostname__ of the router using the command __hostname nameHost__

* We can also change the domain name of the router so we can generate a certificate when we connect to the router using __ssh__, using the command
__ip domain-name nameOfTheDomain__

* We can also add a welcome message to the banner of the router using the command __banner motd # This is the welcome message #__

* If we want to use a password:

    + We can set a password to the console port using the command __line console 0__ to get access to the first port whose name is __console__.
    Then  we write the command __password thePassword__ to set the password to this port. We write the command __login__ also to request to the user
    the password of this console port. This is when we dont matter if the password can be seen if we use the command __show running-config__.
    If we want to encrypt the password, we could use the command __service password-encryption__, while we are logged in the console 0 serial port.

    + If we want to use a password to get privilege access mode, we have to use this command __enable secret thePassword__.

* If we want to print our actual configuration we can use the command __show running-config__

* Use the command to not get irritated by the logging messages of the router when typing a command __logging synchronous__.

* when we want to set up the interfaces we have to are in the configure mode to execute the commands:

    + __interface FastEthernet0/0__ and __ip address 10.0.0.1 255.255.255.128__

    + __interface FastEthernet0/1__ and __ip address 10.0.0.129 255.255.255.128__

* We have just finished to create configuration of our router, the last step is to make a copy to save our progress using the command
__copy running-config startup-config__


## Others

We can configure the router to connect to it using ssh keys, using the command __crypto key generate rsa general-keys__ and setting the bits from __768__ to __2048__(?). In my case I used the number of bits of 1024 because it ends faster than the most security number of bits.

We will have to turn up the version of the ssh using the command: __ip ssh version 2__

Now we will set up the username and password to enter to the router using ssh method: __username name secret password__

The maximun number of sessions that a router can support is __808__

We can limit the number of simultaneous ssh sessions to the router using the command __line vty from to__, for example, the command __line vty 0 4__
means that the router will allow 5 ssh connections, the 0, 1, 2, 3 and 4.

When we are configuring the 5 vty at the same time, we can say to this lines to allow only ssh using the command __transport input ssh__
using the local credentials __login local__ and allow them to be synchronous __logging synchronous__