# FGC-Preseed
This is a preseed that can be used to automate the install proccess in the build area at FreeGeek Chicago.
This preseed can be used by passing it through as a URL in the boot parameters or it can be placed in the initrd.lz

To use on a usb stick or cd: 
1. Mount the iso
2. In the /casper directory of the mounted iso there is an "initrd.lz", copy it to an empty directory.
3. Run "sudo lzma -dc -S .lz ./initrd.lz | cpio -id" to extract the lzma.lz in the directory you copied it to.
4. Copy "preseed.cfg" to the directory you extracted the initrd.lz to.
5. Delete "initrd.lz"
6. Run "find . | cpio --quiet --dereference -o -H newc |lzma -7 > ./initrd.lz" in the directory with the extracted files. It will create a new initrd.lz
7. Replace the initrd.lz in the /casper directory of the iso with the new one you just made
8. Boot

*If the installer stalls at the end saying something about log files you did it right, it is just running the install script and updating
