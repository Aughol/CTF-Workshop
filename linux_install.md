# So you've decided to install Linux.

There's a ton of ways to go about it, most of them relatively easy. In this guide we'll be covering a concise, step-by-step guide to installing Linux.
This guide only covers two distros of Linux, and there will be a section on the reasons for choosing one over the other.
We will also be covering three different ways of installing Linux for both distros discussed.

The distros used in this guide are:
* 	Kali Linux
* 	Ubuntu
	
The Installation methods we will cover are:
* 	Installing the OS on a [Virtual Machine](http://wikipedia.org/Virtual_Machine) _(We will cover both VMWare and VirtualBox)
* 	Installing the OS on a USB drive with Persistence enabled
* 	Wiping the Hard Drive and performing a clean installation of the OS

## What OS should you use?

There are a lot of similarities between the two distros, however there are significant differences to both of them.

### Ubuntu

Ubuntu was designed from the ground up to be an OS that is welcoming to newcomers and easy to install and use regularly.
The releases are usually stable and tested, and the two versions of the distro have a guaranteed life cycle that range depending on the service version.

*	Ubuntu Long Term Support (LTS) has a guaranteed five-year securrity and maintenance update lifetime.
*	Ubuntu (Short Term Support) is a newer version, but only has a nine month update lifetime.

The current version of short term support is 15.10, and the latest version of the LTS is 14.04.3.

Ubuntu is based on another distro named Debian, which means tools like `apt-get` which will allow you to install most programs with a single line of code.
It also comes with its own software store, similar to that of MAC OS X.

Basically, if you have intermediate to no experience with Linux, then you should get Ubuntu. 
The version of the distro doesn't particularly matter, meaning it is your perogative depending on whether you prefer stability (14.04.3) or newness (15.10).

### Kali Linux

Kali Linux is not made for beginners. Hell, it's not made for _intermediate_ users. 
All operations are run as root, which is generally considered to be a terrible decision by other OS dev teams.
Kali has the exception because most operations _have_ to be performed as root, it's considered counterintuitive to the OS's purpose.

Kali Linux was designed to be a penetration testing (read: hack shit) OS, designed with a number of tools and programs to break into systems efficiently (hence why typing `sudo` for every command is unnacceptable).
Because of this, Kali comes with many different utilities geared towards security exploitation, from tracking web packets with a dummy router, to communicating by using your computer as a HAM Radio.

Although much of the tools allow for various uses, not only is the all-root policy dangerous to the inexperienced, but the Kali Linux community is notorious for distrusting and abandoning newcomers to the pentesting scene.
Because of this, it is hard to find comprehensive lessons on Kali Linux that aren't paid courses made by the developers.

It should also be noted that the Kali ISOs are not released with quality assurance in mind. The release before the latest actually had an unsupported Linux kernel.  
The Kali Linux ISO comes in three versions:
*	Normal -- Comes with all pre-packaged software, which can be completely installed without an internet connection.
*	Light -- The bare minimum code required to boot from a CD/DVD/USB. The rest is downloaded over the internet during installation.
*	Mini -- Similar to Normal, but comes with a more lightweight Window Manager, and has quite a few tools removed.

All versions are based on Debian, so similar to Ubuntu, you can use the `apt-get` command from the terminal to install new programs.
Kali does not come with the Ubuntu Software Store for obvious reasons.
The latest version of Kali Linux is working, and is version 2016.1.

### Which one is for you?

Ubuntu | Kali
---|---
Made for beginners and intermediate users | Made for advanced users
Better User Safety | Root-only policy
Made for general use | Made specifically for security testing
Easier to install | More difficult to install
Helpful online community | Very unhelpful online community
Command line and software store installation | Command line only installation
Good for people who want general functionality | Good for people who are considering pentesing as a career

## What method of installation do you want?

Currently, the guide will only cover three ways of installing Linux for use. There is a fourth one, but...

### Why isn't Dual-Boot installation covered?

Because it breaks everything if you don't clean install **ALL** OSes first. It's rediculous, as Windows will freak out and run `chkdsk` on every. single. boot.

Essentially there's little redeeming quality for dual-booting. You can just as easily use a USB with persistence to acheive the same benefits with added portability.

**TL;DR** You really must want to break your computer.

### Method 1: Using a Virtual Machine

This is by far the easiest solution, as it simply involves installing some extra software. Currently, there are two VMs covered in this program: **VirtualBox** and **VMWare**

#### VirtualBox

#### VMWare

### Method 2: Using a USB with Persistence

### Method 3: Wiping a hard drive and clean installing the OS