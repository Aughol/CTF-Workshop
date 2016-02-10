# So you've decided to install Linux.

There's a ton of ways to go about it, most of them relatively easy. In this guide we'll be covering a concise, step-by-step guide to installing Linux.
This guide only covers two distros of Linux, and there will be a section on the reasons for choosing one over the other.
We will also be covering three different ways of installing Linux for both distros discussed.

The distros used in this guide are:
* 	Kali Linux
* 	Ubuntu
	
The Installation methods we will cover are:
* 	Installing the OS on a [Virtual Machine](http://wikipedia.org/Virtual_Machine)_ (We will cover both VMWare and VirtualBox)
* 	Installing the OS on a USB drive with Persistence enabled
* 	Wiping the Hard Drive and performing a clean installation of the OS

## 1\. What OS should you use?

There are a lot of similarities between the two distros, however there are significant differences to both of them.

### 1.1 Ubuntu

Ubuntu was designed from the ground up to be an OS that is welcoming to newcomers and easy to install and use regularly.
The releases are usually stable and tested, and the two versions of the distro have a guaranteed life cycle that range depending on the service version.

*	Ubuntu Long Term Support (LTS) has a guaranteed five-year securrity and maintenance update lifetime.
*	Ubuntu (Short Term Support) is a newer version, but only has a nine month update lifetime.

The current version of short term support is 15.10, and the latest version of the LTS is 14.04.3.

Ubuntu is based on another distro named Debian, which means tools like `apt-get` which will allow you to install most programs with a single line of code.
It also comes with its own software store, similar to that of MAC OS X.

Basically, if you have intermediate to no experience with Linux, then you should get Ubuntu. 
The version of the distro doesn't particularly matter, meaning it is your perogative depending on whether you prefer stability (14.04.3) or newness (15.10).

[Ubuntu ISO Download Link](http://www.ubuntu.com/download/desktop)

### 1.2 Kali Linux

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

[Kali Linux ISO Download Link](https://www.kali.org/downloads/)

### 1.3 Which OS is for you?

Ubuntu | Kali
---|---
Made for beginners and intermediate users | Made for advanced users
Better User Safety | Root-only policy
Made for general use | Made specifically for security testing
Easier to install | More difficult to install
Helpful online community | Very unhelpful online community
Command line and software store installation | Command line only installation
Good for people who want general functionality | Good for people who are considering pentesing as a career
Better Stability Record | Occasionally releases bad ISOs

## 2\. What method of installation do you want?

Currently, the guide will only cover three ways of installing Linux for use. There is a fourth one, but...

### 2.1 Why isn't Dual-Boot installation covered?

Because it breaks everything if you don't clean install **ALL** OSes first. It's rediculous, as Windows will freak out and run `chkdsk` on every. single. boot.

Essentially there's little redeeming quality for dual-booting. You can just as easily use a USB with persistence to acheive the same benefits with added portability.

**TL;DR** You really must want to break your computer.

### 2.2 Using a Virtual Machine

This is by far the easiest solution, as it simply involves installing some extra software. 
Currently, there are three hypervisors (thing that makes and runs VMs) covered in this program: *Oracle VirtualBox 5.0*, *Microsoft Hyper-V* and *VMWare Workstation/Fusion Pro*.
If you have a mid-range or high-end laptop, using a VM is probably your best choice.
Keep in mind to watch how many resources you allocate to a VM.

#### 2.2.1 Oracle VirtualBox 5.0

VirtualBox is a product made by Oracle, the same company that currently develops the Java Language and Java Virtual Machine.
Like many of their non-enterprise products, it is provided free of charge and can be downloaded and used by anyone with a semi-modern computer and an internet connection.
It is a stable platform that can be used to run most operating systems that run on the same CPU architecture.

VirtualBox has a separate add-on pack that adds a ton of functionality to VirtualBox and the Virtual Machines that are on it.
These additions include 3D acceleration support, full screen support, and a virtual CD to add extra drivers/programs to run on VirtualBox more easily.

VirtualBox is also released under the GPL 2 FOSS License, meaning that you can download the source code and compile it yourself, even work on it if you so choose.
If you decide that you want to get into the FOSS development scene, then you may want to consider using VirtualBox to familiarize yourself with the environment.

The latest version of VirtualBox is 5.0.14.

[The VirtualBox Package and Extension Pack can be downloaded here.](https://www.virtualbox.org/wiki/Downloads)

#### 2.2.2 VMWare Workstation/Fusion Pro

VMWare is a product produced by... VMWare. It isn't open source, and is sold at a fairly high price.
The basic price of VMWare Workstation 12 Pro is $250 for basic support and a lifetime license.
VMWare Fusion 8 Pro costs $199 for the same terms.
UCF does own multiple Dreamspark Premium stores that give you free yearly licenses that you can apply for each academic year.

VMWare Workstation Pro performs remarkedly better than VirtualBox and has more features out of box. 
Many utilities, such as fullscreen and USB support are better supported than VirtualBox.

The latest version of VMWare Workstation (Windows\Linux) is 12, and the latest version of VMWare Fusion (Macintosh) is 8.

*A note about some recent news involving VMWare, inc.*  
VMWare has recently fired the entirety of its developers working on Workstation and Fusion who happen to live in the United States.
This was due to a restructuring effort, as the company deemed the US developers were not worth the cost, and have decided to move the development effort into another country.
VMWare has confirmed that they are not axing the Workstation/Fusion product line. 
Many people have echoed the sentiment that they're killing the whole product, which is simply untrue.
It is possible that the quality of the product may dip, but it still currently performs better than VirtualBox.

**We cannot provide a direct download link to VMWare as it is located in the Dreamspark Premium store. 
You must sign into your account, select "VMWare," then "Software." Select *Workstation 12 Pro* for Windows and Linux systems and *Fusion 8 Pro* for Macintosh.
If you have no Dreamspark Premium account then search your Knights email for a message that allows you to sign up. It's worth the effort.**

#### 2.2.3 Microsoft Hyper-V

Hyper-V is a product designed by Microsoft and is slightly more powerful than VMWare. 
It allows for an extreme amount of customizability and supports features such as dynamic RAM allocation, virtual Secure Boot, and TPM encryption.
Like VMWare and VirtualBox, Hyper-V can run VMs in the background.

Hyper-V only comes packaged with any Windows Server past 2008, and with any version of Windows 8/8.1/10 that runs the Pro or Enterprise/Education tier.
It is considered a feature and is therefore already part of Windows. 
It needs to be activated by turning the feature on under the "Programs and Features" section of Control Panel.

If you are ever considering developing apps using the Universal Windows Application (UWA) standard, it is likely you'll have to install this to emulate Windows phones so that your application meets specifications.
However, it is important to note that **activating Hyper-V will lock all other applications out of using your computer's virtualization (vt-x/amd-v) abilities and will cause all other 64-bit VMs to stop working until Hyper-V is disabled.**
This means that if you use applications that rely on 64-bit VMs not used by Hyper-V to work, you are unable to use them until you disable Hyper-V, which requires a reboot.

The latest version of Hyper-V is 10.0.10586.0, which mirrors the Windows 10 consumer version number. 
Expect it to change once the announced Windows 10 RedStone-1 (RS1) update gets released this Summer.

**We cannot provide a download link as it is a feature pre-built into Windows. 
If you want it, get a Pro or Enterprise/Education edition of Windows 8, 8.1, or 10 from the Dreamspark Premium store for free.
After upgrading, enable it in the features menu of the "Programs and Features" applet in the Control Panel.**

#### 2.2.4 Which VM should you choose?

VirtualBox | VMWare | Hyper-V
---|---|---
Download | Download | Pre-Built into Windows 8+ Non-Home editions
Open-Source | Proprietary | Proprietary
Linux/OSX/Windows Versions | Linux/OSX/Windows Versions | Windows Exclusive
Free | $200-$250\* | Cost of OS\*\*
Cannot run x64 OSes with Hyper-V enabled | Cannot run x64 OSes with Hyper-V enabled | N/A
Slower than VMWare/Hyper-V | Performs as fast as Hyper-V | Performs as fast as VMWare
Stable Releases | Questionable quality in the future | Stable Releases
RDP Encryption with Extension Pack | (Unknown Method of) Encryption out of the Box | Secure Boot / TPM Encryption Avaliable

\*Yearly licenses VMWare Workstation/Fusion Pro can be freely taken from Dreamspark Premium in lieu of the ~$250 permanent license.  
\*\*The product keys for the Pro and Enterprise/Education versions of Windows 8, 8.1, and 10 can be found for free in the Dreamspark Premium store.

### 2.3 Using a USB with Persistence

Typically, this is the next best option for people who want to run a Linux/GNU OS but for some reason cannot use a VM.

It could be that:
*	Your computer is not powerful enough to run a VM.
*	Your computer is too low-end or too old to support hardware acceleration.
*	Some other program is preventing VMs to run.
*	Unsolvable VM error.
*	Not enough hard drive space for a VM.
*	You want to utilize *all* of your computer's resources for running Linux.
*	You want a portable OS
*	etc.

Simply put, this option will in essence turn your USB into a small, bootable hard drive that you can plug into any computer and boot off of it.
This allows you to bypass the hypervisor and host OS of a VM setup, allowing your Linux build to use more resources and perform faster.
USB builds are completely portable, and there are just a few pieces of software needed.

#### 2.3.1 Required Software for Making a Persistant Linux USB on Windows

*	[PenDrive Linux -- Universal USB Installer](http://www.pendrivelinux.com/downloads/Universal-USB-Installer/Universal-USB-Installer-1.9.6.3.exe)
*	[MiniTool Partition Wizard -- Disk Partitioner](http://download.cnet.com/MiniTool-Partition-Wizard-Free-Edition/3001-2094_4-10962200.html?hlndr=1&part=dl-)_

*Universal USB Installer* will format a USB that is plugged in, and copy the contents of a provided ISO file. At the end of the process, the USB will be bootable without persistence.  
*Partition Wizard* will partition the USB so that the second partition can be used as persistant space.

#### 2.3.2 Required Software for Making a Persistant Linux USB on Windows

All software needed for a USB install comes already in Linux, but for the sake of clarity:  
*	`dd` Terminal command
*	GParted Disk Partitioner

The syntax for the `dd` command will be given and explained later, but it simply erases the content of a drive/folder and overwrites it with the content of a folder/ISO.  
*GParted* will partition the drive, a step that's needed to enable persistence.

#### 2.3.3 Reccomended Hardware

Obviously any computer that supports booting from USB will do, however the USB itself needs to be a certain size.  
*	A USB running Ubuntu should have at least **8 GB of space minimum.**
*	A USB running Kali should have at least **16 GB of space minimum.**

Be forewarned that **ALL DATA PREVIOUSLY STORED ON THE USB WILL BE LOST FOREVER ONCE INSTALLATION BEGINS.** Make sure to back your data up.

Also keep in mind that **YOUR USB DRIVE'S PERSISTENT SPACE WILL BE RENDERED UNREADABLE TO WINDOWS.** So don't count on transferring data to and from your Windows hard drive.

#### 2.3.4 Security Concerns

USB Persistence is by no means more secure than using a VM.
People running Windows 7 or earlier will find that their USB OS has the ability to read and write to the hard drive without Windows being active.
Normally this wouldn't be a problem, but this obviously opens up security problems.

If you run computers that came with Windows 8 or later, you will have noticed that Secure Boot is running on your computer.
Secure Boot keeps the user from being able to access BIOS or the Boot Options menu, effectively barring them from being able to boot from the USB.
Secure Boot can be disabled, but by the same terms, anyone with bootable media can use your computer.

Interestingly enough, another addition to Windows 8+ is the addition of *Hybrid Shutdown*. 
This is why boot times between 7 and 8/8.1, along with 8/8.1 and 10 have decreased significantly; 
the computer enters a state where much of the software shuts down, except for a few components that stay active.
This allows Windows to boot very quickly, by keeping certain parts active, and shutting others (like those with pending updates) down.

*Hybrid Shutdown* has an unintended side effect; it forces any Linux OS that is booted to either reject mounting the Windows drive, or forces it into mounting it as read only.
With this in mind, it makes sense to say that security concerns over booting from USB to be significantly diminished if your computer runs Windows 8, 8.1, or 10.

### 2.4 Wiping a hard drive and clean installing the OS

This option is best for people who have an extra laptop lying around somewhere. 
It's fairly self-explanatory, you're just erasing the contents of the hard drive and installing the new OS where Windows used to be.
This process results in a computer that can run Linux without any VM or bootable medium. 
You press the power button and the computer immediately loads into whatever distro you installed.

Technically, this could be considered the most secure option, as it requires the wiping of all personal data.

#### 2.4.1 Hardware Requirements

There's two hardware requirements, mainly your computer and a bootable device containing a Linux installation media:  
*	If you want to use a USB device for installation, your USB drive must be at least 4GB for Ubuntu and 8GB for Kali.
*	If you want to use a DVD for installation, your DVD must be blank (if not a DVD-RW or DVD+RW) and over 3GB in size.

Similar to USB Persistence requirements, if you want to install Linux on your hard drive, you *must* disable Secure Boot.
This option is generally found in computers that came with Windows 8 and later.

#### 2.4.2 Warnings before Choosing this Option

It should go without saying, but **wiping your hard drive will result in the lost of ALL data on the drive.** 
Not only will the disk be formatted, but the file system itself will change, and any data will be lost forever.

Another warning is that **while Linux distros generally have stable releases, occasionally something can flub up and result in the temporary or permanent inability to use the computer.**
Sometimes, a bad header can be shipped, and break the graphics driver. Other times, the window manager simply stops. 
It's very rare for these to happen, especially with modern Linux distributions.
However, it can still happen and it still does happen. 
Most of the time, this can be solved by getting a slightly older version of an OS, using a different distro, or if you know your way around Linux you can try to fix it yourself.
Generally, a permanent break is fairly difficult to acheive, so it's only there for the sake of a disclaimer.

### 2.5 Which install method is for you?

Virtual Machine | USB with Persistence | Wiping Hard Drive and Installing
---|---|---
Least Effort to Make | Hardest to Make | Medium Effort to Make
Works as OS Layer | Interfaces with Hardware | Interfaces with Hardware
Slowest | Second Fastest | Fastest
Sometimes portable | Completely Portable | Not Portable
Fairly Secure | Less Secure | Most Secure
Needs ISO only | Needs ISO and USB | Needs ISO and USB/DVD
Can use Windows | Can use Windows | Must erase Windows
Cannot Make Computer Unusable | Cannot Make Computer Unusable | Can Rarely Make Computer Unusable
Keep Personal Data | Must Erase Personal Data on USB | Must Erase Personal Data on Hard Drive
Keep Secure Boot Enabled | Must Disable Secure Boot | Must Disable Secure Boot
Must Download Software to Use | Must Download Software to Use | Can Use Tools that Come with OS
