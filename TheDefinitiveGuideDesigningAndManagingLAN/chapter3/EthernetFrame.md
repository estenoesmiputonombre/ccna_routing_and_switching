# Ethenet Frame

The heart of the Ethernet system is the __frame__. The network hardware - which includes
__Ethernet interface__, __media cables__ and so on - exists simply to move Ethernet frames
between computers, or stations.

## Formed by

| Name | Size |
| ---- | ---- |
| Preamble | 64 bits |
| Destination Address | 48 bits |
| Source address | 48 bits |
| Type/Length | 16 bits |
| Data | 46 to 1500 bytes |
| Frame Check Sequence (FCS-CRC) | 32 bits |

Describing each of the parts of the Ethernet frame:

* Preamble - 

    + __Start-up time__ provided to the hardware and electronics in the original __10 Mb/s__ Ethernet system to recognize that a frame is being transmitted, alerting it to start receiving the data.
    
    + Newer Ethernet systems running at higher speeds use __constant signaling__, which avoids the need for a preamble. 
    
    + It is __still transmitted__ to avoid making any changes in the structure of the frame.

* Destination address and source address - 

    + The __assignment__ of one portion of the address is controlled by the __IEEE Standards Association__ (IEEE SA). It provides a __24-bit__ __organizationally unique identifier__(OUI). An OUI is assigned to each organization that builds __Ethernet interfaces__.

    + A __manufacturer__ of Ethernet interfaces creates an __unique 48-bit__ Ethernet addres for each interface by using its assigned OUI.

    + The resulting 48-bit address is often called __hardware (or physical) address__. It can also be called __media access control__ (MAC), because the Ethernet MAC system includes the __frame__ and its __addressing__.

* Type - Most often this field is used to __identify__ what type of __high-level network protocol__ is being carried in the __data field__(TCP/IP ej)

* Data - 

    + The data field must have the minimun length of 46 bits because this assured that the __frame signals__ stayed on the network __long enough__ for every Ethernet station in the original __10 Mb/s half-duplex__ system to hear the frame within the correct time limits.

    + If the high-level protocol data carried in the data field is __shorter__ than 46 bytes, then __padding__ data is used to fill out the data field.

* Frame Check Sequence (FCS) - 

    + Contains the __Cyclic Redundancy Check__(CRC) that provides a check of the integrity of the data in the entire frame.

    + The CRC is a __unique value__ that is generated by applying a __polynomial__ to the __pattern of bits__ that make up the frame.

    + In the receive host, it uses the same polynomial to determinate the value using the pattern of bits that make up the frame, an compare the two values.

## Nomenclature

* Station - It is a network device