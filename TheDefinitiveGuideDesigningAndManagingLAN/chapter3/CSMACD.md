# The CSMA/CD protocol

So good example:

The __CSMA/CD__ protocol functions somewhat like a __dinner party__ in a __dark room__, where the participants hear, but do not see, one another.

* Everyone around the table __must listen__ for a period of quiet before speaking - __Carrier Sense__

* Once a space occurs, everyone has an __equal chance__ to say something - __Multiple access__

* If two people start talking at the same instant, they __detect__ that fact and quit speaking - __Collision detection__

## Carrier

Each __interface__ must wait until __there is no signal__ on the shared channel before it can begin transmitting. If another interface is __transmitting__, there will be a signal on the channel; this condition is called __carrier__.

## Deferral

All other interfaces __must wait__ until __carrier__ ceases and the signal channel is idle before trying to transmit.

## Multiple access

All Ethernet interfaces have the __same priority__ when it comes to __sending frames__ on the network, and all interfaces can attempt to access the channel when it is idle.

## Collision detection

Because of the multiple access property, all Ethernet interfaces have the same priority to send frames, so it is possible that the Ethernet __signaling devices__ connected to the shared channel sense the __collision__ of signals. When this happens, the Ethernet signaling devices connected to the shared channel sense the collision of signals, which tell these Ethernet interfaces to __stop transmitting__.

## Backoff

__Random retransmission__ time that each Interface will choose to resend its __frames__ after the __collision__.

The expanding __backoff__ process, formally known as __truncated exponential backoff__

## Loop

Only after __16__ consecutive __collisions__ for a given transmission attempt will the interface finally discard the Ethernet frame.

## Nomenclature

* Carrier signal - Historically, it is defined as a __continuous constant-frequency signal__, such as the one used to carry the modulated signal in an __AM__ or __FM__ radio system. There is no such continuous carrier signal in Ethernet; instead, "carrier" in Ethernet simple means the __presence of traffic on the network__.