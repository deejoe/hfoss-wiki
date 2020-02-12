
# Introduction to Sugar using a VirtualBox virtual machine

In this exercise we will install a virtual machine (VM) that natively uses the Sugar
desktop environment (DE). This is an approach that you should be able to
follow on your own desktop or laptop computer. It complements the use of the
RIT network-hosted VMWare VM already created for your use at:

  * https://rlesvctr.main.ad.rit.edu

We will generally follow the process from 

  * [Introduction to using VMs with VirtualBox](https://github.com/ritjoe/hfoss/wiki/vm-intro-vb-finnix)

but instead of using Finnix live image, we'll be using 

  * [Sugar Live Build](https://github.com/sugarlabs/sugar-live-build)

This is a customized instance of a [Debian Live Build](https://debian-live.alioth.debian.org/live-manual/stable/manual/html/live-manual.en.html#107)


## Please download an image file (.iso) from this directory

  * [20171009 Sugar Live Build](http://people.sugarlabs.org/%7Equozl/sugar-live-build-20171009/)

## Create a virtual machine with

  * the VM name *sugar-live*
  * 1GB RAM
  * a new virtual hard drive also named *sugar-live*
  * 8GB hard drive
  * VMDK hard drive
  * break drive backing files into 2GB chunks

Remember to note the location on the host system where the image is
installed, and to associate this image file with the virtual CD-ROM drive of
the VM in the VirtualBox storage configuration window.

## Start the virtual machine


## Do the installation.

During the installation, you will be asked to create

  * a root user password
  * a name for a regular user account
  * a password for the regular user account

You can set these to whatever, but since these will always run effectively
behind a firewall, and since password resets will be a pain to effect, I
recommend keeping it simple:

  * root password 'root'
  * user account name 'hfoss'
  * user account password 'sugar'

## Reboot the virtual machine into the installed system

## Begin exploring Sugar

We ran into a current [known bug in Sugar](https://github.com/sugarlabs/sugar/issues/776) when launching our RLES VMs during Week 5.

This is easily remedied, though: 

Hitting Ctrl-2 will bring up the Home view.

Hitting F6 or Alt-Shift-f bring up the frame.

Several of the [Sugar environment hotkeys](https://wiki.sugarlabs.org/go/Hotkeys)
make more sense when considered in light of the special symbology mapped to
the keyboards of the [OLPC XO keyboard](http://wiki.laptop.org/go/Keyboard)

See also [OLPC XO Keyboard shortcuts](http://wiki.laptop.org/go/Keyboard_shortcuts).


