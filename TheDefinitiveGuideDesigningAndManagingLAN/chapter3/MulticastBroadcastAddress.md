# Multicast and broadcast addresses

The __Ethernet delivery mechanism__ also supports __multicasting__, which is more efficient than sending the same frames to multiple recipients.

## Multicast address

Allows a __single Ethernet frame__ to be received by a __group of stations__.

## Broadcast address

The __48-bit__ address of all ones, is a special case __mutlicast address__. __All Ethernet interfaces__ that see a frame with this destination address will read the frame in and deliver it to the networking software on the computer.

After each frame transmission, __all stations__ on the shared half-duplex network channel with traffic to send must contend equally for the next frame transmission opportunity.