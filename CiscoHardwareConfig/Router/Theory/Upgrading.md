# Upgrading the IOS

__TFTP(Trivial File Transfer Protocol)__ this is the protocol that we are going to use to transfer the binary file from the computer to the router.

We are going to use a __console__ port and a __Ethernet__ port

If we want to see the content of the flash memory, we could use __show flash__

If we want to see the version of the router, we could use __show version__

If we want to delete some file from the flash memory we could use __delete flash:/file__

When we want to transfer the files from the TFTP to the router, we are going to use 
the command __copy tftp flash__

Then, the router will prompt three questions:

* The address of where the file is

* The path of the file

* The name of the file in the flash memory

When the file was downloaded by the router, we will use the command __boot system flash:/nameOfTheBinFile.bin__ to reboot the system using this new IOS file
