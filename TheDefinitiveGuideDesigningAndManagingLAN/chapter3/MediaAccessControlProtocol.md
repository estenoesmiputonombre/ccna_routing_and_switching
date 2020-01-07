# The Media Access Control Protocol

__Half-duplex mode__ of operation that is the basis of the original __10 Mb/s__ Ethernet system.

The original system was based on the __CSMA/CD__ protocol, which is a __set of rules__ designed to arbitrate access to a __shared channel__ among
a set of stations connected to that channel.

Today most stations use __full-duplex mode__, which provides a dedicated channel between the station and the switch port.

## Protocol

Each __Ethernet-equipped__ device operates __independently__ of all other stations on the network; There is no central controller.

Stations attached to an __Ethernet cable__ and operating in __half-duplex__ mode are connected to a __signaling channel__ that (because it is shared), requires the use of __CSMA/CD__ mechanism to control access.

Ethernet uses __Broadcast delivery__ mechanism, in which frame that is transmitted on the __shared channel__ is heard by every station.

To send data in __half-duplex__ mode, a station first __listens__ to the channel, and if the channel is idle, the station __transmits__ its data in the form of an Ethernet frame.

An interface compares the __destination address__ of the frame (second field) with its own 48-bit __unicast__ address and any __multicast address__ it has been enabled to recognize.

## Nomenclature

* CSMA/CD - Carrier Sense Multiple Access with Colision Detection

## Notes

* It is still possible for a station to use __half-duplex mode__ when connected to a switch port at __10 Mb/s__ and __100 Mb/s__ over a
__Twisted-pair__ cable. However, higher-speed media systems support __full-duplex__ mode __only__.

* __Full-duplex__ mode uses a __dedicated link__ between stations that operates in __both directions__ simultaneously, and there is no need to control access to the link.