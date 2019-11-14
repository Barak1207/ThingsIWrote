# ThingsIWrote
Some things I wrote and don't know where to save them...

RaspberryPILCD - A Python module for handling LCD screens for Raspberry pi (supports multihtreading)

IDAXrefFixerARM - A plugin for IDA
Which tries to solve the problem in which IDA doesn't recognize ARM's common way of loading 32 bit addresses into a register by splitting the address into two 16bits immediates and loading them separately into the same register.

It does so by searching instruction in close proximity that load the desired address by splitting it into MOV/W and MOVT instructions.

Usage:
Drag FixArmXrefs.py to IDA's plugins folder.
Start up IDA with an ARM binary.
Go to the address you want to fix the xrefs to.
Press Shift+X.
Make sure that the address in the form auto filled field is the one you intended.
Select tolerance, this is the maximum gap between each MOV instructions, increasing it will increase the false positives.
Pres OK.
When first running the script in a new IDA session it will take a few seconds, but after that it's pretty much immediate.
Press CTRL+X to see the newly updated xrefs.
