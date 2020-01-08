# The Ethernet Frame

The frame was first defined in the original __Ethernet DEC-Intel-Xerox(DIX)__ standard, and was later redefined and modified in the __IEEE 802.3__ standard.

## Type field

The DIX standard defined a __type__ field in the frame.

The first IEEE 802.3 standard (1985) specified this field as a __length field__, with a mecanism that allowed __both versions__ of frames to coexist on the same Ethernet System.

Most networking software kept using the type field version of the frame.

A later version of the IEEE 802.3 standard was changed to define this field of the frame as being either __length__ or __type__, depending on usage.

## Types of frames

### DIX Basic Frame

DIX Basic Frame = Min 64 Bytes, Max 1518 Bytes + preamble.

| Name | Size |
| ---- | ---- |
| Preamble | 8 Bytes |
| I/G(Individual/Group address bit) | 1 bit |
| Destination Address | 47 bits |
| Source Address | 6 Bytes |
| Type | 2 Bytes |
| Data | 46-1500 Bytes |
| FCS(Frame Check Sequence) | 4 Bytes |

### IEEE 802.3 Basic Frame

IEEE 802.3 Basic Frame = Min 64 Bytes, Max 1518 Bytes + preamble

| Name | Size |
| ---- | ---- |
| Preamble | 7 Bytes |
| SFD(Start Frame Delimiter) | 1 Bytes |
| I/G(Individual/Group address) | 1 bit |
| G/L(Global/Local administered bit) | 1bit |
| Destination address | 46 bits |
| Source address | 6 Bytes |
| Length/Type | 2 Bytes |
| Data/LLC(Logical Link Control) | 46-1500 Bytes |
| FCS(Frame Check Sequence) | 4 Bytes |

### IEEE 802.3 Basic Frame with Q-tag

IEEE 802.3 Basic Frame with Q-tag = Min 64 Bytes, Max 1522 Bytes + preamble

| Name | Size |
| ---- | ---- |
| Preamble | 7 Bytes |
| SFD(Start Frame Delimiter) | 1 Byte |
| I/G(Individual/Group address bit) | 1 bit |
| G/L(Global/Local administered bit) | 1 bit |
| Destination address | 46 bits |
| Source address | 6 Bytes |
| Q-tag | 4 Bytes |
| Length/Type | 2 Bytes |
| Data/LLC(Logical Link Control) | 46-1500 Bytes |
| FCS(Frame Check Sequence) | 4 Bytes |

### IEEE 802.3 Frame with Envelope Prefix and/or Suffix

IEEE 802.3 Frame with Envelope Prefix and/or Suffix = Min 64 Bytes, Max 2000 Bytes + preamble

| Name | Size |
| ---- | ---- |
| Preamble | 7 Bytes |
| SFD(Start Frame Delimiter) | 1 Byte |
| I/G(Individual/Group address bit) | 1 bit |
| G/L(Global/Local administered bit) | 1 bit |
| Destination address | 46 bits |
| Source address | 6 Bytes |
| Envelope Prefix | 2-482 Bytes |
| Length/Type | 2 Bytes |
| Data/LLC(Logical Link Control) | 46-1500 Bytes |
| Envelope Suffix | 0-482 |
| FCS(Frame Check Sequence) | 4 Bytes |

## Notes

DIX Basic Ethernet and IEEE 802.3 Basic Ethernet are the same, so we can use one or the other. Because the max length is 1518 and the single difference is the Type/Length field

## Nomenclature

* DEC -> Digital Equipment Corporation.