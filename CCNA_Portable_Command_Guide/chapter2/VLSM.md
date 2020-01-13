# VLSM (Variable Length Subnet Mask)

When we are subnetting by the classical way, we dont use the broadcast and the gateway address to a subnet, but in cisco we can use those subnets, as long 
as the command __ip subnet-zero__ is in the configuration. This command is on by default in Cisco IOS Software Release 12.0 and later.

## Example_1

A Class C network - 192.168.100.0/24 is assigned. We need to create an IP plan for this network using VLSM.

* Router A with 50 hosts

* Router B with 27 hosts

* Router C with 12 hosts

* Router D with 12 hosts

### Step 1

Determine How many H bits will be needed to satisfy the largest network.

2 ^ H - 2 = Number of valid hosts per subnet

2 ^ H - 2 >= 50 -> H = 6 this is the number of bits that we will use to the maximun number of hosts in a subnet

So we left 2 bits to create subnets, which in fact is 4 subnets because 2 ^ 2 = 4

### Step 2

We have to choose now a subnet to the router that will have 50 hosts

because of is 2 bits of netowrk, we have a net mask of /26 or 255.255.255.196

The subnets available are:

00000000-00111111 / 0-63
01000000-01111111 / 64-127
10000000-10111111 / 128-191
11000000-11111111 / 192-255

We will pick the second subnet from 64 to 127 (Why?? I dont know)

### Step 3

Determine the number of H bits needed for this network:

Router B with 27 hosts

2 ^ H - 2 >= 27 -> H = 5

We will have to maintain the pattern of 2N and 6H bits for Network A. 

Pick one of the remaining /26 networks to work with Network B.

We will pick the third network 128/26

We need only 5 Bits so:

10N00000

With this extra bit we create a subnet as follows:

10000000=128
10100000=160

New net mask of this subnet of subnet is 255.255.255.224 or /27

Resume:

| Binary | Standard | Network |
| ------ | -------- | ------- |
| 00000000 | 0/26 | Nothing |
| 01000000 | 64/26 | A |
| 10000000 | 128/27 | B |
| 10100000 | 160/27 |  |
| 11000000 | 192/26 | nothing |

# Step 4

2 ^ H - 2 >= 12 -> 4

we want a subnet with 4 bits dedicated for hosts, so we can take the 160/27 and subnet it

101N0000 with extra bit we can create 2 different subnets

so:

10100000 - 160/28
10110000 - 176/28

| Binary | Standard | Network |
| ------ | -------- | ------- |
| 00000000 | 0/26 | Nothing |
| 01000000 | 64/26 | A |
| 10000000 | 128/27 | B |
| 10100000 | 160/28 | C |
| 10110000 | 176/28 | D |
| 11000000 | 192/26 | nothing |

### Step 5

Determine Network Number For Serial Links

We need 2 hosts so 2 ^ H - 2 >= 2 -> H = 2

All serial links between routers have the same property in that they only need two addresses in a network - one for each router interface.

We need 2 H bits to satisfy the requirements of Networks E, F, G and H.

Because we need only 2 H bits

00NNNN00

meaning a Network Mask of 255.255.255.252 or /30