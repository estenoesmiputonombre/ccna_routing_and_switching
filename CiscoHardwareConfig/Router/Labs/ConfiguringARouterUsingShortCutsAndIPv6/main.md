# Routing

We will use the lab of the ConfiguringARouter

## Shortcuts

If we dont remember how a command was or we want to write less, we can use the ? character to know what command there are:

If we type the letter e and then ? like 'e?' this will display all the commands that starts with e

## Commands

* We enter using the console cable connecting the RS-232 serial port to the console port of the router or we can connect to it using ssh

* we __enable__ to get the privileged user and __show startup-config__ to know if the device have our previous configuration that we save

* we will erase the configuration of the startup-config to start from scratch using the command __erase startup-config__

* We wil use the __reload__ command to reload the router and start with a configuration of the startup-config which is nothing.

* If we want to get all the messages from the router when using an ssh session, we should use the command __terminal monitor__ from the privileged mode.

* We could use the comnmand __ipv6 unicast-routing__ to enable routing IPv6 messages, this will allow us to create a IPv6 routing table. Then
use the command __interface FastEthernet0/0__ to enter in the FastEthernet port 0 and __ipv6 enable__. Finally set the ipv6 using __ipv6 address addressIPv6__