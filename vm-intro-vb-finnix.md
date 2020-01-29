
# Introduction to using VMs with VirtualBox

This is a very general tool, we are using a very small and simple system
at first to boot a live image for our demonstration. 

Learning to use this tool will allow you to try almost any OS that provides
an image for this architecture.  (If the architecture is emulated [eg, ARM,
MIPS running on an x86/arm64 host] it will be too slow for many uses. 
Hardware virtualization is fast for another OS on the same processor type.)

  * Go to finnix.org
  * Find the x86/amd64 image 111
  * download it
  * locate it on your computer 
    * in D:\Users\\\<netid>\Downloads
    * otherwise, move it
  * start VirtualBox
  * delete old VM
  * click New to create new VM
  * name everything 'finnix' 
    * name the VM 'finnix'
    * name the new drive image finnix
    * (if you were installing, would name user account this way to match)
  * attach a CD image
  * boot
  * observe


(optional) Some other small Linux images one can also try:

http://wikka.puppylinux.com/HomePage

http://damnsmalllinux.org/download.html

http://tinycorelinux.net/downloads.html

http://www.slitaz.org/en/get/

http://minimal.linux-bg.org/#download

https://github.com/ivandavidov/minimal/releases