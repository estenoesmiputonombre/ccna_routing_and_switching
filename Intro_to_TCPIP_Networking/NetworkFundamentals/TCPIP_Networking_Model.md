# TCP/IP Networking Model

## Synonyms

* Networking model

* Networking architecture

* Networking blueprint

## Definition

Set of documents

## Documents

### Protocol

It is a set of __logical rules__ that each device must follow to **comunicate**

### Other Documents

Define some physical requirements for networking

### Example

A document could define the __voltage__ and __current levels__ on a particular __cable__ when __transmitting data__.

## History leading to TCP/IP

* 1970-1980 -> IBM -> Creates a SNA in the 1974 to have its own networking model

* 1970s -> ISO -> Took the task to create a networking model whose name is OSI

* 1970s -> DoD (US) -> Took the task to create a networking model whose name is TCP/IP

* 1990s -> Some companies took the TCP/IP, others OSI model and other took both.

* Finally, TCP/IP win at the last of 1990s

## Overview of the TCP/IP Networking Model

* The TCP/IP model both __defines__ and __references__ a large collection of protocols that allows computer to comunicate .

* TCP/IP uses documents called RFC(Request For Comments)

* TCP/IP dont override the contents that other institutes create. For example, the Ethernet LANs protocol was defined by IEEE.

### Layers

We have 5 layers in TCP/IP Networking model:

* Application:

    + HTTP, SMTP, POP3
    
    + apps that needs to __send__ and __receive__ data.

* Transport:

    + TCP, UDP

    + apps that need to __send__ and __receive__ data.

* Network:

    + IP, ICMP

    + __Delivering__ data over the __entire path__ from the original sending computer to the final destination computer.

* Data link:

    + Ethernet, 802.11 Wi-Fi, PPP

    + __Send__ data over one type of __physical link__

* Physical:

    + Ethernet, 802.11 Wi-Fi

    + __How__ to transmit bits of data over each individual __link__

## Annotation

* SNA -> Systems Network Architecture

* ISO -> International Organization Standardization

* OSI -> Open System Interconection

* DoD -> Departement of Defense

* RFC -> Request For Comments

* IEEE -> Institute of Electrical and Electronic Engineers

* HTTP -> HyperText Transfer Protocol

* SMTP -> Simple Mail Transfer Protocol

* POP3 -> Post Office Protocol

* TCP -> Transmission Control Protocol

* UDP -> User Datagram Protocol

* IP -> Internet Protocol

* ICMP -> Internet Control Message Protocol

* PPP -> Point-to-Point Protocol
