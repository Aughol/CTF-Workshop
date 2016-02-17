# So you've decided to install Linux.

There's a ton of ways to go about it, most of them relatively easy. In this guide we'll be covering a concise, step-by-step guide to installing Linux.
This guide only covers two distros of Linux, and there will be a section on the reasons for choosing one over the other.
We will also be covering three different ways of installing Linux for both distros discussed.

The distros used in this guide are:
* 	Kali Linux
* 	Ubuntu
	
The Installation methods we will cover are:
* 	Installing the OS on a [Virtual Machine](http://wikipedia.org/Virtual_Machine)_ (We will cover VMWare, Hyper-V, and VirtualBox)
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

\*Yearly licenses for VMWare Workstation/Fusion Pro can be freely taken from Dreamspark Premium in lieu of the ~$250 permanent license.  
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
*	(For USB) `dd` Terminal command
*	(For DVD) `wodim` Terminal command
*	GParted Disk Partitioner

The syntax for the `dd` command will be given and explained later, but it simply erases the content of a drive/folder and overwrites it with the content of a folder/ISO.  
*GParted* will partition the drive, a step that's needed to enable persistence.

#### 2.3.3 recommended Hardware

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

# 3\. Installation Instructions

## 3.1 Instructions for Making a VM

**The required items for this section is:**  
*	The Hypervisor of your choice.
*	The ISO file of the OS of your choice.

*This section assumes you have been able to install the hypervisor of your choice correctly.*

### 3.1.1 Making a VM in VirtualBox

#### For Ubuntu:

##### Installing the Guest Additions

*The guest extensions add some functionality that makes using a VirtualBox VM easier, like adding fullscreen. It is recommended you install it.*

1.	Download the *VirtualBox Extension Pack*. The download link can be found in Section 2.2.1.
2.	Launch VirtualBox, Select *File*, then *Preferences*, *Extension*, and *Add New* (small blue box with yellow arrow).
3.	Browse the File System until you find the pack you just downloaded, then select it.
4.	A Dialog box will warn you Extension packs can be harmful. Click *Install*.
5.	Select *OK* to exit the preferences window.

##### Creating the Virtual Machine

*These steps create the Virtual Machine that will soon run the OS.*

1.	Select *New* up at the top-left.
2.	Name it whatever you want, but naming it "Ubuntu" will auto-config the setting of that screen.
3.	If you didn't auto-config, select *Linux* from the first drop-down list, then *Ubuntu 32/64 bit* from the second. Click *Next*.
4.	On this screen, you'll allocate RAM for the VM. *1GB is the absolute minimum, but it is recommended to allocate 2GB to 4GB if you can*. Click *Next*.
5.	This screen allows you to decide if you want to allocate Hard Drive space via a Virtual Hard Drive. Select *Create a Virtual Hard Disk Now*, then click *Create*.
6.	Select *VDI (VirtualBox Disk Image)*, then *Next*.
7.	If you want slightly better performance, select *Fixed Size*. Otherwise, leave it at *Dynamically Allocated*. Click *Next*.
8.	Adjust the slider to the amount of hard drive space you want the VM to have. *You must have at least 8GB, though 20GB is recommended.* Click *Create*.

##### Installing the OS on the Virtual Machine

*By now you should have downloaded your ISO. Don't continue the instructions until it is completely downloaded.*

1.	Select the newly added VM, then select *Start*.
2. 	A prompt will appear asking for the location of the "Start up Disk." Direct the prompt to the location of the ISO file and then select *Start*.
3.	It may take a moment for the GUI to fully appear. As it does, make sure *English* is selected from the left panel, then click *Install Ubuntu*.
4.	If the VM is connected to the Internet (it should have automatically done that), select *Download Updates while Installing*. Choosing *Install Third-Party Software* is optional. Click *Continue*.
5.	Select *Erase Disk and Install Ubuntu*. Click *Continue*.
6.	Select the Time Zone you live in. Click *Continue*.
7.	Select the configuration of your keyboard. It should be *English (US)* and *English (US)* as default. Click *Continue*.
8.	Set your Name (doesn't have to be real), username, and password. Click *Continue*.
9.	Wait for the installation to finish. Once it has, select *Restart Now*.

##### Logging in for the First Time

*At this point the OS is fully installed on the VM and now should boot into Ubuntu when launched.*

1. 	Select the VM that you just installed the OS on, then click *Start*.
2. 	Wait for the GUI to load, then enter your username you set, and the corresponding password.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

#### For Kali Linux:

##### Installing the Guest Additions

*The guest extensions add some functionality that makes using a VirtualBox VM easier, like adding fullscreen. It is recommended you install it.*

1.	Download the *VirtualBox Extension Pack*. The download link can be found in Section 2.2.1.
2.	Launch VirtualBox, Select *File*, then *Preferences*, *Extension*, and *Add New* (small blue box with yellow arrow).
3.	Browse the File System until you find the pack you just downloaded, then select it.
4.	A Dialog box will warn you Extension packs can be harmful. Click *Install*.
5.	Select *OK* to exit the preferences window.

##### Creating the Virtual Machine

*These steps create the Virtual Machine that will soon run the OS.*

1.	Select *New* up at the top-left.
2.	Name it whatever you want, but there's no auto-detect for "Kali."
3.	Select *Linux* from the first drop-down list, then *Debian* from the second. Click *Next*.
4.	On this screen, you'll allocate RAM for the VM. *1GB is the absolute minimum, but it is recommended to allocate 2GB to 4GB if you can*. Click *Next*.
5.	This screen allows you to decide if you want to allocate Hard Drive space via a Virtual Hard Drive. Select *Create a Virtual Hard Disk Now*, then click *Create*.
6.	Select *VDI (VirtualBox Disk Image)*, then *Next*.
7.	If you want slightly better performance, select *Fixed Size*. Otherwise, leave it at *Dynamically Allocated*. Click *Next*.
8.	Adjust the slider to the amount of hard drive space you want the VM to have. *You must have at least 10GB, though 20GB is recommended.* Click *Create*.

##### Installing the OS on the Virtual Machine

*By now you should have downloaded your ISO. Don't continue the instructions until it is completely downloaded.*

1.	Select the newly added VM, then select *Start*.
2. 	A prompt will appear asking for the location of the "Start up Disk." Direct the prompt to the location of the ISO file and then select *Start*.
3. 	A splash screen will appear, with a list of options. Select *Graphical Install*, then press enter.
4. 	Once the GUI comes up, select *English*, then click *Continue*.
5. 	Select your country (*United States*), then click *Continue*.
6.	Select your keyboards map (*American English*), then click *Continue*.
7.	After some component loading, type in your computers Hostname. This is inconsequential, so name it whatever you want. Click *Continue*.
8. 	Set the root password, then click *Continue*.
9.	If a screen appears, asking for a Time Zone, select *Eastern*, then click *Continue*.
10.	A list of installation options will appear. Select *Guided - Use entire Disk*, then click *Continue*.
11.	There's only one item in the list for installing the OS. Select it, then click *Continue*.
12.	Select *All Files in One Partition (recommended for New Users)*, then click *Continue*.
13.	Do not change any of the settings, click *Continue*.
14.	Confirm the Virtual Hard Disk changes by selecting *Yes*. Click *Continue*.
15.	The installation will now begin, after it's completed, select *Yes* for network downloading.
16.	If you have any proxy info, enter it there. If not, leave it blank. Click *Continue*.
17.	Select *Yes* to install GRUB, then click *Continue*.
18.	In the next list, there should be only one item besides *Enter Device Manually*. Select it (it should look similar to */dev/sda (gibberish)*). Click *Continue*.
19.	The next screen should notify you that the installation is completed. Click *Continue*.
20.	The VM will automatically reboot.

##### Logging in for the First Time

*At this point the OS is fully installed on the VM and now should boot into Kali Linux when launched.*

1. 	Select the VM that you just installed the OS on, then click *Start*.
2. 	Select *Kali GNU/Linux* from the GRUB menu or simply wait for the computer to do it for you.
3.	Wait for the GUI to appear, then enter *root* as the username. Click *Next*.
4. 	Enter the password you set during install. Then select *Sign In*.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

### 3.1.2 Making a VM in VMWare

#### For Ubuntu:

##### Creating the Virtual Machine

*Unlike VirtualBox, you must have the ISO before you make the VM.*

1.	Click *Create a New Virtual Machine*. When the New VM Wizard appears, select *Typical (recommended) Install*, then click *Next*.
2.	Select *Installer Disc Image (iso)* and set the location to the ISO File. You'll notice the message that says *The Operating System will Use Easy Install*.
3.	Click *Next*. Set your name, username, and password. Click *Next.*
4.	Name the Virtual Machine and set the location if needed. Click *Next*.
5.	Set the Hard Disk size. 10GB is the minimum, 20GB is recommended. Click *Next*.
6.	Review the settings, then click *Finish*. Keep *Power on this Virtual Machine after Creation* selected.

##### Installing the OS on the Virtual Machine

1.	VMWare has a feature called *Easy Install*, which sets the VM up according to the info you set earlier. Just sit back and wait.
2.	As soon as the splines have finished reticulating, the VM will automatically reboot.

##### Logging in for the First Time

1.	If you are not automatically rebooting, select the VM you just installed the OS on from the left panel.
2.	Click the *Power on this Virtual Machine* button.
3.	Wait for the GUI to appear. Type the password you set during VM creation.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

#### For Kali Linux:

##### Creating the Virtual Machine

*Unlike VirtualBox, you must have the ISO before you make the VM.*

1.	Click *Create a New Virtual Machine*. When the New VM Wizard appears, select *Typical (recommended) Install*, then click *Next*.
2.	Select *Installer Disc Image (iso)* and set the location to the ISO File. Click *Next*.
3.	Set the Guest OS as *Linux*. Set the Version as *Debian 8.x 64-bit*.
4.	Name the Virtual Machine and set the location if needed. Click *Next*.
5.	Set the Hard Disk size. 10GB is the minimum, 20GB is recommended. Click *Next*.
6.	Before finishing the creation wizard, select *Customize Hardware...*, then select the *Memory* section from the left pane.
7.	Adjust the slider to at least 1GB (1024MB). 2GB to 4GB is recommended.
8.	Review the settings, then click *Finish*.

##### Installing the OS on the Virtual Machine

1.	The VM should have appeared in a new tab. If it hasn't, select it from the left pane.
2.	Select *Power on this Virtual Machine*.
3. 	A splash screen will appear, with a list of options. Select *Graphical Install*, then press enter.
4. 	Once the GUI comes up, select *English*, then click *Continue*.
5. 	Select your country (*United States*), then click *Continue*.
6.	Select your keyboards map (*American English*), then click *Continue*.
7.	After some component loading, type in your computers Hostname. This is inconsequential, so name it whatever you want. Click *Continue*.
8. 	Set the root password, then click *Continue*.
9.	If a screen appears, asking for a Time Zone, select *Eastern*, then click *Continue*.
10.	A list of installation options will appear. Select *Guided - Use entire Disk*, then click *Continue*.
11.	There's only one item in the list for installing the OS. Select it, then click *Continue*.
12.	Select *All Files in One Partition (recommended for New Users)*, then click *Continue*.
13.	Do not change any of the settings, click *Continue*.
14.	Confirm the Virtual Hard Disk changes by selecting *Yes*. Click *Continue*.
15.	The installation will now begin, after it's completed, select *Yes* for network downloading.
16.	If you have any proxy info, enter it there. If not, leave it blank. Click *Continue*.
17.	Select *Yes* to install GRUB, then click *Continue*.
18.	In the next list, there should be only one item besides *Enter Device Manually*. Select it (it should look similar to */dev/sda (gibberish)*). Click *Continue*.
19.	The next screen should notify you that the installation is completed. Click *Continue*.
20.	The VM will automatically reboot.

##### Logging in for the First Time

1.	If you are not automatically rebooting, select the VM you just installed the OS on from the left panel. Select *Power on this virtual machine*.
2. 	Select *Kali GNU/Linux* from the GRUB menu or simply wait for the computer to do it for you.
3.	Wait for the GUI to appear, then enter *root* as the username. Click *Next*.
4. 	Enter the password you set during install. Then select *Sign In*.

##### Installing VMWare-Specific Drivers

*VMWare automatically installs some drivers for Ubuntu, but it must be manually done for Kali Linux. It isn't required, but it is highly recommended.*

1.	After logging in, click the *VM* menu from the VMWare toolbar, and select *Install VMWare Tools...*.
2.	In a moment a disc icon will appear on the Desktop titled *VMWare Tools*. Open it.
3.	In the virtual CD, there should be a `tar.gz` file that begins with "VMWareTools". Drag it to the Desktop.
4.	Close out of the CD file window. Right click the Desktop and select *Open Terminal*.
5.	In the terminal, type `cd Desktop` (case sensitive) to change the directory to the Desktop. 
6.	In the terminal, type `tar -zxvf <name of tar.gz>` to extract the archive.
7.	After the process completes, type `cd vmware-tools-distrib` to move into the driver directory.
8.	Type `./vmware-install.pl` to begin installation. **Press enter for all options given. Do not type anything.**
9.	After the process is done, type `reboot` to reboot the computer and utilize the new drivers.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

### 3.1.3 Making a VM in Hyper-V

*Please note the term "disabling security" refers to the VM, not the host computer.*

*Hyper-V is set up so exiting the VM window will not shut down the VM. To shut it down, click the Shut Down or Turn Off buttons located in the VM window as well as the right panel Hyper-V Manager window.*

#### Allowing VMs to access the internet

Hyper-V allows for VMs to access the internet, but it must be enabled first.

1.	If the center panel has a section titled *Introduction*, then click the computer in the left panel under *Hyper-V Manager*.
2.	On the right panel, click *Virtual Switch Manager...*.
3.	On the *New virtual network switch* panel, select *External* and then click *Create Virtual Switch*.
4.	Name the switch whatever you want, but make sure that the *Connection Type* section has *External* selected, as well as the name of the device you want to use for internet connection selected from the dropdown list.
5.	Leave *Allow Management Operating System to Share this Network Adapter* enabled. Click *OK*.
6.	A popup will warn you that your internet connection may drop for a moment. Click *Yes*.
7.	Allow the process to complete and exit the Virtual Switch Manager.

#### For Ubuntu:

##### Creating the Virtual Machine and Disabling Security

*At this point, the ISO file of your choice should be completely downloaded*.

1.	If the center panel has a section titled *Introduction*, then click the computer in the left panel under *Hyper-V Manager*.
2.	On the right panel, click *New*, then click *Virtual Machine...*.
3.	Click *Next* on the introduction screen. Name the new virtual machine whatever you want, then click *Next*.
4.	Selecting *Generation 2* is highly recommended. Click *Next*.
5.	You must allocate at least 1GB of RAM. Allocating 2GB to 4GB is recommended if you can afford it.
6.	Leaving *Use Dynamic Memory for this virtual machine* will generally lessen the impact on computer performance, but will slow the VM slightly. Select it if you want, then click *Next*.
7.	Select the Virtual Switch you made earlier from the drop-down list. Click *Next*.
8.	Select *Create a New Virtual Hard Disk* and name it whatever you want. If you want to change the location, do so.
9.	**The size of the Virtual Hard Disk will be automatically set to the size of your Hard Drive's free space. Resize it or you won't have any free space on your computer.** At least 10GB should be allocated, 20GB is recommended.
10.	Select *Install an Operating System from a Bootable Image File*, and set the *Image File (.iso)* prompt to where your downloaded ISO file is. Click *Next*.
11.	Review the VM's settings, then click *Finish*.

***These next settings are only doable if you opted to make a Generation 2 VM. Skip these if you made a Generation 1 VM.***  

12.	After the process completes, select the VM from the center panel, then click *Settings...* on the right panel.
13.	Select *Security* from the side panel, then uncheck the box that says *Enable Secure Boot*. Click *OK*.

##### Installing the OS on the Virtual Machine

*In Hyper-V, the VM uses a different MAC address than the host computer. If this causes your ISP to not provide a connection to the VM, you **must** use a web browser on the VM and set up your connection between steps 2 and 3.*

1.	Select the VM from the center panel; click *Start*, then click *Connect...* from the right panel.
2.	Once the GRUB menu appears, select *Try Ubuntu without Installing*, then press enter.
3.	Select the Network Icon on the task bar (two arrows moving in different directions), and select the network type you want (it should be *Wired Connection 1*).
4.	Exit the *Keyboard Shortcuts* window and launch *Install Ubuntu <version>*.
5.	On the *Welcome* screen, make sure *English* is selected, then click *Continue*.
6.	If the VM is connected to the Internet, select *Download Updates while Installing*. Choosing *Install Third-Party Software* is optional. Click *Continue*.
7.	Select *Erase Disk and Install Ubuntu*. Click *Continue*. Click *Continue* again if a summary of hardware changes appears.
8.	Select the Time Zone you live in. Click *Continue*.
9.	Select the configuration of your keyboard. It should be *English (US)* and *English (US)* as default. Click *Continue*.
10.	Set your Name (doesn't have to be real), username, and password. Click *Continue*.
11.	Wait for the installation to finish. Once it has, select *Restart Now*.
12.	Wait for the text to appear on the screen, then click the *Turn Off* icon at the top. It is grey with a black sqare.

##### Logging in for the First Time

1.	Click the *Connect...* button if you closed the window after installation. Click the *Start* button in the VM connection window.
2.	Wait for the GUI to appear. Enter your password.

##### Changing Screen Resolution

*If the resolution of the VM is bothering you, these steps are here to fix the problem.*

1.	Press `Ctrl+Alt+T` to open a new terminal.
2.	Type the command `sudo gedit /etc/default/grub` and enter your password when asked.
3.	Find the line that says `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`
4.	At the end of the line, add `video=hyperv_fb:<width>x<height>`. If you wanted a standard laptop resolution, the line would read `GRUB_CMDLINE_LINUX_DEFAULT="quite splash video=hyperv_fb:1366x768"`.
5.	Save the file and exit. In the terminal, type the command `updte-grub` and type the password when asked.
6.	Type the command `reboot` in the terminal to restart the computer.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

#### For Kali Linux:

##### Creating the Virtual Machine

*At this point, the ISO file of your choice should be completely downloaded*.

1.	If the center panel has a section titled *Introduction*, then click the computer in the left panel under *Hyper-V Manager*.
2.	On the right panel, click *New*, then click *Virtual Machine...*.
3.	Click *Next* on the introduction screen. Name the new virtual machine whatever you want, then click *Next*.
4.	**Kali Linux will not install on a Generation 2 VM. Do not select it. The developers of Kali are working on a fix to this situation.**
5.	You must allocate at least 1GB of RAM. Allocating 2GB to 4GB is recommended if you can afford it.
6.	**Unselect *Use Dynamic Memory for this Virtual Machine*** , then click *Next*.
7.	Select the Virtual Switch you made earlier from the drop-down list. Click *Next*.
8.	Select *Create a New Virtual Hard Disk* and name it whatever you want. If you want to change the location, do so.
9.	**The size of the Virtual Hard Disk will be automatically set to the size of your Hard Drive's free space. Resize it or you won't have any free space on your computer.** At least 10GB should be allocated, 20GB is recommended.
10.	Select *Install an Operating System from a Bootable CD/DVD-ROM*, select and set the *Image File (.iso)* prompt to where your downloaded ISO file is. Click *Next*.
11.	Review the VM's settings, then click *Finish*.

##### Installing the OS on the Virtual Machine

1.	Select the VM from the center panel; click *Start*, then click *Connect...* from the right panel.
2. 	A splash screen will appear, with a list of options. Select *Graphical Install*, then press enter.
3. 	Once the GUI comes up, select *English*, then click *Continue*.
4. 	Select your country (*United States*), then click *Continue*.
5.	Select your keyboards map (*American English*), then click *Continue*.
6.	After some component loading, type in your computers Hostname. This is inconsequential, so name it whatever you want. Click *Continue*.
7. 	Set the root password, then click *Continue*.
8.	If a screen appears, asking for a Time Zone, select *Eastern*, then click *Continue*.
9.	A list of installation options will appear. Select *Guided - Use entire Disk*, then click *Continue*.
10.	There's only one item in the list for installing the OS. Select it, then click *Continue*.
11.	Select *All Files in One Partition (recommended for New Users)*, then click *Continue*.
12.	Do not change any of the settings, click *Continue*.
13.	Confirm the Virtual Hard Disk changes by selecting *Yes*. Click *Continue*.
14.	The installation will now begin; afterwards *Yes* for network downloading.
15.	If you have any proxy info, enter it there. If not, leave it blank. Click *Continue*.
16.	Select *Yes* to install GRUB, then click *Continue*.
17.	In the next list, there should be only one item besides *Enter Device Manually*. Select it (it should look similar to */dev/sda (gibberish)*). Click *Continue*.
18.	The next screen should notify you that the installation is completed. Click *Continue*.
19.	The VM will automatically reboot.

##### Logging in for the First Time

1.	Click the *Connect...* button if you closed the window after installation. Click the *Start* button in the VM connection window.
2.	Wait for the GUI to appear. Enter *root* as the username, then enter the password you set earlier.

##### Changing Screen Resolution

*If the resolution of the VM is bothering you, these steps are here to fix the problem.*

1.	Right click the desktop and select *Open Terminal* to open a new terminal.
2.	Type the command `gedit /etc/default/grub` and enter your password when asked.
3.	Find the line that says `GRUB_CMDLINE_LINUX_DEFAULT="quiet"`
4.	At the end of the line, add `splash video=hyperv_fb:<width>x<height>`. If you wanted a standard laptop resolution, the line would read `GRUB_CMDLINE_LINUX_DEFAULT="quite splash video=hyperv_fb:1366x768"`.
5.	Save the file and exit. In the terminal, type the command `update-grub` and type the password when asked.
6.	Type the command `reboot` in the terminal to restart the computer.

At this point, you now have a working Virtual Machine that can run the Binary Exploitation Workshop Exercises.

## 3.2 Making a Bootable USB with Persistence

**The required items for this section is:**  
*	A USB of appropriate size (8GB for Ubuntu, 16GB for Kali Linux).
*	(Windows Only) Partition Wizard Disk Partitioner.
*	(Windows Only) PenDrive Linux Universal USB Installer.
*	The ISO file of the OS of your choice.

### 3.2.1 Using Windows to Install:

#### Disabling Secure Boot

*Many current computers now come with Secure Boot enabled; this will essentially lock you out from accessing the boot options menu.
The easiest way to determine if your computer has Secure Boot enabled is by restarting the computer and seeing if the startup splash screen gives you the option to load into the boot options menu.*

*If you have this option, then skip this section. If not, then check what version of Windows you are running and follow the appropriate instructions.*

*Windows 7 does not support Secure Boot, so this section can only be applied to computers running Windows 8 or later.*

##### Accessing Advanced Startup

*Disabling Secure Boot in Windows required the use of Advanced Startup to get into the BIOS/UEFI settings.*

***For Windows 8:***  
1.	Open the Start Charms, click *Settings*, then click *Change PC Settings*.  
2.	Click *General*. Scroll down to *Advanced Startup*, then under that section, click *Restart Now*.  

***For Windows 8.1:***  
1.	Open the Start Charms, click *Settings*, then click *Change PC Settings*.  
2.	Click *Update and Recovery*, then click *Recovery*.  
3.	Scroll down to *Advanced Startup*, then under that section, click *Restart Now*.  

***For Windows 10:***  
1.	Open the Start Menu, then click *Settings*.  
2.	Click *Update and Security*, then click *Recovery*.  
3.	Under *Advanced Startup*, then under that section, click *Restart Now*.  

##### Accessing BIOS

*The option to disable secure boot is located in BIOS. These steps will get you there.*

1.	Once Advanced Startup begins, click *Troubleshooting*.
2.	Select *Advanced Options*.
3.	There will be an option that reads *BIOS Firmware Settings* or *UEFI Firmware Settings*. Select it.
4.	The computer will confirm that you will access the BIOS/UEFI settings. Click *Restart*.

##### Disabling Secure Boot

*Here's how to actually disable Secure Boot in BIOS.*

1.	Move throughout the options menu until you find the option for *Secure Boot*. There's too many different ways to do this, but it will usually be located under the *Boot* or *Security* menu.
2.	If the option can be changed, set *Secure Boot* to "Disabled." If it cannot be changed, set a Supervisor Password and see if that allows the change of the option. This is a known issue with certain ACER laptops.
3.	Save the settings and exit. As the computer restarts, you should see options for BIOS/UEFI as well as the Boot Options menu. Take note of the button needed for Boot Options.

#### For Ubuntu:

##### Installing the OS on a USB

*By now, you need to have the entire ISO downloaded. These instructions will make the USB boot the installable version of Ubuntu.*

1.	Plug in the USB, and take note of what drive letter it is.
2.	Launch PenDrive Linux Universal USB Installer. A Terms of Service article will appear. Agree to the terms.
3.	The first thing you need to do is select *Ubuntu* (under the *Ubuntu 32/64 bit* section) from the drop-down list.
4.	Select *Browse* and navigate to and select the ISO you downloaded.
5.	Select the correct drive letter from the second drop-down list.
6.	Select the checkbox to enable formatting the drive.
7.	Set the Persistent File slider as high as it can go. Select *Create*. If a "not enough space" error gets thrown, repeat the same steps, but lower the slider just a bit.
8.	Wait for installation to complete. This can take several minutes.
9.	Once installation completes, click *Close*.

##### Enabling Persistence

1.	The USB should have persistence automatically enabled.

##### Using your USB

1.	Shut down the computer, then plug the USB in.
2.	Boot the computer up, and press the key that launches the Boot Options menu.
3.	Select the USB boot option, then as the splash screen appears, select *Try Ubuntu without installing*.
4.	It should load directly into a usable Ubuntu environment.

*If you want to change the title of "Try Ubuntu without installing", then plug the USB drive into a running computer,
 open /boot/grub/grub.cfg then edit the phrase to whatever you like.
 Make sure to keep the carat (\^) character there.*

#### For Kali Linux:

##### Installing the OS on a USB

*By now, you need to have the entire ISO downloaded.*

1.	Plug in the USB, and take note of what drive letter it is.
2.	Launch PenDrive Linux Universal USB Installer. A Terms of Service article will appear. Agree to the terms.
3.	The first thing you need to do is select *Kali Linux* (under the *Security and Penetration Testing* section) from the drop-down list.
4.	Select *Browse* and navigate to and select the ISO you downloaded.
5.	Select the correct drive letter from the second drop-down list.
6.	Select the checkbox to enable formatting the drive.
7.	Select *Create*. Wait for installation to complete. This can take several minutes.
8.	Once installation completes, click *Close*.

##### Enabling Persistence

*While the "Live USB Persistence" option can be selected, it won't actually be usuable until these steps are taken.

1.	Launch MiniTool Partition Wizard, then select *Launch Application*.
2.	Select the USB Partition, then select *Move/Resize*.
3.	Dragging the slider from the right, shrink the partition as much as possible. Click *OK*.
4.	Select the newly made unallocated space and select *Create*.
5.	Set the File System as *Ext4*, set it as *Primary*, then name it `persistence`. Click *OK*.
6.	Click *Apply* then wait for the process to complete.
7.	Shut down the computer, then make sure the USB is plugged in.
8.	Boot the computer up, and press the key that launches the Boot Options menu.
9.	Select the entry that boots from USB, then once the splash screen is, select *Live USB Persistence*.
10. Once it boots up, open the second partition, named `persistence`.
11.	Right click in the file explorer window that appeared and select *Open Terminal*.
12.	In the terminal, type `echo "/ union" > persistence.conf` and press Enter.
13.	Type `reboot` and press Enter. The computer should now restart.

##### Using your USB

1.	Shut down the computer, then make sure the USB is plugged in.
2.	Boot the computer up, and press the key that launches the Boot Options menu.
3.	Select the entry that boots from USB, then once the splash screen is, select *Live USB Persistence*.

*At this point, the "persistence" drive will disappear from the desktop and will now be used to hold peristent data.*

### 3.2.2 Using Linux to Install

#### For Ubuntu:

##### Installing the OS on a USB

##### Enabling Persistence

##### Using your USB

#### For Kali Linux:

##### Installing the OS on a USB

##### Enabling Persistence

##### Using your USB

## 3.3 Wiping the Hard Drive and Installing the OS

**The required items for this section is:**  
*	A blank DVD-R/DVD+R, a reusable DVD-RW/DVD+RW, or a USB Drive.
*	The ISO file of the OS of your choice.
*	(For USB Install on Windows) PenDrive Linux Universal USB Installer.

### 3.3.1 Creating the Installer on Windows

#### Disabling Secure Boot

*Many current computers now come with Secure Boot enabled; this will essentially lock you out from accessing the boot options menu.
The easiest way to determine if your computer has Secure Boot enabled is by restarting the computer and seeing if the startup splash screen gives you the option to load into the boot options menu.*

*If you have this option, then skip this section. If not, then check what version of Windows you are running and follow the appropriate instructions.*

*Windows 7 does not support Secure Boot, so this section can only be applied to computers running Windows 8 or later.*

##### Accessing Advanced Startup

*Disabling Secure Boot in Windows required the use of Advanced Startup to get into the BIOS/UEFI settings.*

***For Windows 8:***  
1.	Open the Start Charms, click *Settings*, then click *Change PC Settings*.  
2.	Click *General*. Scroll down to *Advanced Startup*, then under that section, click *Restart Now*.  

***For Windows 8.1:***  
1.	Open the Start Charms, click *Settings*, then click *Change PC Settings*.  
2.	Click *Update and Recovery*, then click *Recovery*.  
3.	Scroll down to *Advanced Startup*, then under that section, click *Restart Now*.  

***For Windows 10:***  
1.	Open the Start Menu, then click *Settings*.  
2.	Click *Update and Security*, then click *Recovery*.  
3.	Under *Advanced Startup*, then under that section, click *Restart Now*.  

##### Accessing BIOS

*The option to disable secure boot is located in BIOS. These steps will get you there.*

1.	Once Advanced Startup begins, click *Troubleshooting*.
2.	Select *Advanced Options*.
3.	There will be an option that reads *BIOS Firmware Settings* or *UEFI Firmware Settings*. Select it.
4.	The computer will confirm that you will access the BIOS/UEFI settings. Click *Restart*.

##### Disabling Secure Boot

*Here's how to actually disable Secure Boot in BIOS.*

1.	Move throughout the options menu until you find the option for *Secure Boot*. There's too many different ways to do this, but it will usually be located under the *Boot* or *Security* menu.
2.	If the option can be changed, set *Secure Boot* to "Disabled." If it cannot be changed, set a Supervisor Password and see if that allows the change of the option. This is a known issue with certain ACER laptops.
3.	Save the settings and exit. As the computer restarts, you should see options for BIOS/UEFI as well as the Boot Options menu. Take note of the button needed for Boot Options.

#### Using a DVD:

#### Using a USB:

### 3.3.2 Creating the Installer on Linux

#### Using a DVD:

#### Using a USB:

### 3.3.3 Installing the OS

#### For Ubuntu:

#### For Kali Linux:

## 4\. Final Notes?