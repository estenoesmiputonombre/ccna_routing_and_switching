# Router Memory

When we are booting up the router, the first thing that we load after POST is 
__bootstrap__.

## Bootstrap

The __bootstrap__ is located in a little chip on the router called __EEPFROM(Electronic Erasable Programmable Read-Only Memory)__.

## IOS

When the router boots up, it will look for the __Operating System__ file in the __ROM__ chip.

Then the bootstrap calls the __IOS(Internetworking Operating System)__.
The IOS is stored in the __Flash memory__.

IOS is an Operating System that is written __uniquely__ for each device that Cisco manufactures.

We have the __platform__ which is the type of device (Router, Switch or Layer 3 Switch)

We have also __Trains__ which are the Major Releases. 12.2-12.4-15.0-15.1

We have also __Throttles__ which are the Minor Releases. 12.2(10) - 12.4(20) - 15.0(1) - 15.1(3)

And finally we have __Rebuilds__ which are rebuilds of minor releases that doesnt succeed. 12.2(10b) - 12.4(20)T3 - 15.0(1)M8 - 15.1(3)T2

### Old version of IOS naming

c1841-adventerprisek9-mz.124-24.T5.bin:

* c1841 -> Cisco 1800 Series router model 1841.

* adventerprisek9 -> Advanced Enterprise Feature Set.

* 124 -> Train (12.4).

* 24 -> Throttle.

* T5 -> Rebuild.

* bin -> Binary File System.

### New version of IOS naming

c1900-universalk9-ms.SPA.153-3.M4.bin

* c1900 -> Cisco 1900 Series router.

* universalk9 -> Universal Feature Key. The __k9__ allows us to ssh into the device and to use VPN

The process is, you go the the __VAS(Valkue Added Reseller)__ and pick up a license.

Then, I combine the license with the ID of my product and it is sent to a Cisco License Server and they send back a number, which is the key that is necessary to enter into the device to unlocks the feature set that you purchase.

## Startup-config

The next thing that we need are the __startup-config__ file.

This file is stored in a special place on the router called __NVRAM(Non-Volatile Random Access Memory)__

## Running-config

When we are configuring the router we are modifying the file __running-config__.

This files is stored in the __RAM(Random Access Memory)__.

When we power off the router, the file runing-config will be blank. So the idea is to
save the contents of this file to the startup-config file.