# Route Summarization

The main idea is to take the general subnet of the subnets.

## Winnipeg

Taking the photo like an example we can see that for Winnipeg:

| Address | Binary |
| ------- | ------ |
| 172.16.64.0/24 | 10101100.00010000.01000000.00000000/24 |
| 172.16.65.0/24 | 10101100.00010000.01000001.00000000/24 |
| 172.16.66.0/24 | 10101100.00010000.01000010.00000000/24 |
| 172.16.67.0/24 | 10101100.00010000.01000011.00000000/24 |

The part that is common to all this IP addresses are: 10101100.00010000.01000 which are 22 bits, so
when the router Vancouver ask us(Winnipeg) we will say it that if a packet has the DA of 172.16.64.0/22

## Calgary

Taking the photo like an example we can see that Calgary:

| Address | Binary |
| ------- | ------ |
| 172.16.68.0/24 | 10101100.00010000.01000100.00000000/24 |
| 172.16.69.0/24 | 10101100.00010000.01000101.00000000/24 |
| 172.16.70.0/24 | 10101100.00010000.01000110.00000000/24 |
| 172.16.71.0/24 | 10101100.00010000.01000111.00000000/24 |

The part that is common to all this IP addresses are: 10101100.00010000.010001 which are 22 bits, so
when the router Vancouver ask us(Calgary) we will say it that if a packet has the DA of 172.16.68.0/22

## Edmonton

Taking the photo like an example we can see that Edmonton:

| Address | Binary |
| ------- | ------ |
| 172.16.72.0/24 | 10101100.00010000.01001000.00000000/24 |
| 172.16.73.0/24 | 10101100.00010000.01001001.00000000/24 |
| 172.16.74.0/24 | 10101100.00010000.01001010.00000000/24 |
| 172.16.75.0/24 | 10101100.00010000.01001011.00000000/24 |
| 172.16.76.0/24 | 10101100.00010000.01001100.00000000/24 |
| 172.16.77.0/24 | 10101100.00010000.01001101.00000000/24 |
| 172.16.78.0/24 | 10101100.00010000.01001110.00000000/24 |
| 172.16.79.0/24 | 10101100.00010000.01001111.00000000/24 |

The part that is common to all this IP addresses are: 10101100.00010000.01001 which are 21 bits, so
when the router Vancouver ask us(Calgary) we will say it that if a packet has the DA of 172.16.72.0/21


## Route Flapping