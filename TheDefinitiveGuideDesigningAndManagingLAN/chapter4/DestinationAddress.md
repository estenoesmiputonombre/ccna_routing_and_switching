# Destination address

Also called __Physical__ or __hardware__ address.

It contains the 48-bits that corresponds to the address of the interface in the station that is the destination of the frame that can be __multicast__ address or the __broadcast__ address or even a __single host__.

## DIX Standard

The __first bit__ of the destination address is used to distinguish __physical__ address from __multicast__ address. If the value of the first bit is:

* 0 -> It is a physical address (also called __unicast address__).

* 1 -> It is a multicast address. If they are all ones, then it is a __broadcast address__.

## IEEE Standard

The __second bit__ of the destination address is used to distinguish __Locally__ and __Globally__ administered address. If the value of the second bit is:

* 0 -> It is a __Global administered address__. It was assigned by the manufacturer. (__DIX Ethernet__ address are always globally administered)

* 1 -> It is a __Locally administered address__ (for some reason). It is rarely used on Ethernet systems.

## Understanding physical address

48 bits -> 12 decimal values like aa-bb-cc-dd-ee-ff

The octect order of transmission on the Ethernet is from the __leftmost__ octet (as written or displayed) to the __rightmost__ order.

The actual transmission order of bits within the octet, however, goes from the __least significant__ bit of the octet through to the __most significant__ bit.

F0-2E-15-6C-77-9B -> 0000 1111 0111 0100 1010 1000 0011 0110 1110 1110 1101 1001

this MAC address is a unicast address because the first bit sent in the channel is 0.