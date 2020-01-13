# OSPF

* The __Open Shortest Path First(OSPF)__ protocol, defined in __RFC2328__.

* It is an __Interior Gateway__ protocol used to distribute routing information within a single __Autonomous System__.

* Was developed due to the need in the internet comunity to introduce a high funcionality non-propietary __Internal Gateway Protocol(IGP)__ for the __TCP/IP__ protocol family.

* The discussion of the creation of a common interoperable Gateway Protocol (IGP) for the Internet started in __1988__ and did not formalized until __1991__

* The OSPF protocol is based on __link-state technology__, which is a departure from the __Bellam-Ford vector__ based algorithms used in traditional Internet routing protocols such as __RIP(Routing Information Protocol)__.

* OSPF has introduced new concepts such as __authentication of routing tables__, __Variable Length Subnet Masks(VLSM)__, __route summarization__, and so forth.

## RIP

The rapid growth and expansion of today's networks has pushed RIP to its limits.

* RIP has a limits of __15 hops__. A RIP network that expands more than 15 hops(15 routers) is considered __unreachable__.

* RIP cannot handle __Variable Length Subnet Masks(VLSM)__. Given the shortage of IP addresses and the flexibility VLSM gives in the efficient assignment of IP addresses, this is considered a __major flaw__.