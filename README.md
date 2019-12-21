# FGC-Preseed
This is a preseed that can be used to automate the install proccess in the build area at FreeGeek Chicago.
This preseed can be used by passing it through as a URL in the boot parameters or it can be placed in the initrd.lz

To use on a usb stick: 
1. Copy the contents of preseed.cfg to preseed/linuxmint.seed (On your USB-Stick)
2. Change "only-ubiquity" to "automatic-ubiquity" in the boot parameters for the ISO.

*If the installer stalls at the end saying something about log files you did it right, it is just running the install script and updating
