# Preamble

The frame begins with the 64-bit preamble field, which was originally incorporated to allow __10 Mbps__ Ethernet interfaces to __synchronize__ with the __incomming data stream__ before the fields relevant to carrying the content arrived.

The __preamble__ was initially provided to __allow__ for the __loss of a few bits__ due to __signal start-up delays__ as the signal propagates through a cabling system.

The __preamble__ was originally developed as a __shield__ to protect the bits in the rest of the frame when operating at __10 Mbps__.

## DIX Standard

In the __DIX__ standard, the preamble consists of 8 Bytes. The first seven comprise a sequence of alternating ones and zeros. The last two bits of the last byte are __11__ because this means that the end of the preamble has been reached.

## IEEE Standard

The same as the DIX standard, but the first seventh Bytes are called __Preamble__ and the last one is called __SFD(Start Frame Delimiter)__ with the same pattern at the final of this one, __11__