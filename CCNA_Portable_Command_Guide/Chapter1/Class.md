# Subnetting

## Class

| Class | Leading Bit Pattern | First Octect in Decimal | Notes |
| ----- | ------------------- | ----------------------- | ----- |
| A | 0xxxxxxx | 0-127 | 0 is invalid and 127 is reserved for loopback testing |
| B | 10xxxxxx | 128-191 | |
| C | 110xxxxx | 192-223 | |
| D | 1110xxxx | 224-239 | Reserved for multicasting |
| E | 1111xxxx | 240-255 | Reserved for future use\testing |

## Formulae

The number of total subnets created is __2^N__ where N is equal to the number of bits borrowed.

The number of valid subnets created is __2^N - 2__.

The number of total hosts per subnet is __2^H__ where H is equal to number of host bits.

The number of valid hosts per subnet is __2^H - 2__.

### Examples

Converting IP addresses to binary

* 138.101.114.250 -> 10001010.01100101.01110010.11111010

* (Subnet mask) 255.255.255.192 -> 11111111.11111111.11111111.11000000

## Subnetting a Class C Network using binary

192.168.100.0/24 which means that we have a Network Mask of 255.255.255.0

To create 9 subnets: 2^N - 2 >= 9 -> N = 4, so we need to borrow 4 H bits and turn them into N bits.

Subnet mask 255.255.255.240 because we borrowed 4 bits: 11111111.11111111.11111111.11110000

192.168.100.0   - 192.168.100.15
192.168.100.16  - 192.168.100.31
192.168.100.32  - 192.168.100.47
192.168.100.48  - 192.168.100.63
192.168.100.64  - 192.168.100.79
192.168.100.80  - 192.168.100.95
192.168.100.96  - 192.168.100.111
192.168.100.112 - 192.168.100.127
192.168.100.128 - 192.168.100.143
192.168.100.144 - 192.168.100.159
192.168.100.160 - 192.168.100.175
192.168.100.176 - 192.168.100.191
192.168.100.192 - 192.168.100.207
192.168.100.208 - 192.168.100.223
192.168.100.224 - 192.168.100.239
192.168.100.240 - 192.168.100.255

## Subnetting a Class B Network using binary

172.16.0.0/16 and we need 9 subnets

To create 9 subnets: 2^N-2 >= 9 -> N=4 bits

How many hosts we can achieve per subnet: 2^H - 2 = 2^(4+8) - 2 = 4094

So, we will use the Net Mask 255.255.240.0

172.16.0.0   - 172.16.15.255
172.16.16.0  - 172.16.31.255
172.16.32.0  - 172.16.47.255
172.16.48.0  - 172.16.63.255
172.16.64.0  - 172.16.79.255
172.16.80.0  - 172.16.95.255
172.16.96.0  - 172.16.111.255
172.16.112.0 - 172.16.127.255
172.16.128.0 - 172.16.143.255
172.16.144.0 - 172.16.159.255
172.16.160.0 - 172.16.175.255
172.16.176.0 - 172.16.191.255
172.16.192.0 - 172.16.207.255
172.16.208.0 - 172.16.223.255
172.16.224.0 - 172.16.239.255
172.16.240.0 - 172.16.255.255

## ANDing

0 and 0 = 0
1 and 0 = 0
0 and 1 = 0
1 and 1 = 1

### Question 1

What is the network number of IP address 192.168.100.115 if it has a subnet mask of 255.255.255.240?

192.168.100.115 = 11000000.10101000.01100100.01110011
255.255.255.240 = 11111111.11111111.11111111.11110000
ANDed result    = 11000000.10101000.01100100.01110000 -> 192.168.100.112

### Question 2

What is the network number of IP address 192.168.100.115 if it has a subnet mask of 255.255.255.192?

192.168.100.115 = 11000000.10101000.01100100.01110011
255.255.255.192 = 11111111.11111111.11111111.11000000
ANDed result    = 11000000.10101000.01100100.01000000 -> 192.168.100.64

### Question 3

What is the network number of IP address 192.168.100.164 if it has a subnet mask of 255.255.255.248

192.168.100.164 = 11000000.10101000.01100100.10100100
255.255.255.248 = 11111111.11111111.11111111.11111000
ANDed result    = 11000000.10101000.01100100.10100000 -> 192.168.100.160