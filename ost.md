# OST exam notes

- [OST exam notes](#ost-exam-notes)
    - [Overview](#overview)
        - [What's the difference between open source software and other types of software?](#whats-the-difference-between-open-source-software-and-other-types-of-software)
        - [Open source  licenses](#open-source-licenses)
    - [Operating System](#operating-system)
        - [Features of Linux](#features-of-linux)
        - [Linux Distributions](#linux-distributions)
        - [Logical Volume Manager](#logical-volume-manager)
        - [File Hierarchy Standards](#file-hierarchy-standards)
        - [Swap partition](#swap-partition)
        - [RAID](#raid)
        - [Dual boot hard-disk partitioning](#dual-boot-hard-disk-partitioning)
        - [Role of bootloader](#role-of-bootloader)
        - [Partitioning ?](#partitioning)
        - [Hosting parts on different partitions ?](#hosting-parts-on-different-partitions)
        - [File permissions](#file-permissions)
        - [Directory permissions](#directory-permissions)
        - [Links and types. Compare](#links-and-types-compare)
        - [inode](#inode)
        - [Power commands](#power-commands)
            - [halt](#halt)
            - [shutdown](#shutdown)
        - [mount umount](#mount-umount)
            - [mount](#mount)
            - [unmount](#unmount)
    - [System Administration](#system-administration)
        - [chmod chown chgrp](#chmod-chown-chgrp)
            - [chmod](#chmod)
            - [chown](#chown)
            - [chgrp](#chgrp)
        - [/etc/{passwd, group, shadow, gshadow}](#etcpasswd-group-shadow-gshadow)
        - [**Processes**](#processes)
        - [Overview](#overview)
        - [Relevant commands](#relevant-commands)
        - [Process Creation / fork-exec-wait-exit](#process-creation-fork-exec-wait-exit)
        - [init ?](#init)
        - [daemon processes](#daemon-processes)
        - [user processes](#user-processes)
        - [parent process](#parent-process)
        - [child processes](#child-processes)
        - [background process](#background-process)
        - [foreground process](#foreground-process)
    - [Backup commands](#backup-commands)
    - [Networking and Security](#networking-and-security)
        - [Networking commands](#networking-commands)
            - [netstat (snetstat?)](#netstat-snetstat)
            - [ping](#ping)
            - [arp](#arp)
            - [host](#host)
            - [traceroute](#traceroute)
            - [ifconfig](#ifconfig)
            - [nslookup](#nslookup)
            - [route](#route)
        - [Apache RPM installation](#apache-rpm-installation)
        - [Iptables](#iptables)
        - [http.conf](#httpconf)
            - [Keepalive](#keepalive)
            - [Keepalive Timeout](#keepalive-timeout)
            - [MaxClients](#maxclients)
            - [ServerLimit](#serverlimit)
            - [StartServers](#startservers)
        - [DNS](#dns)
        - [Configuration as MasterDNS](#configuration-as-masterdns)
        - [SSL](#ssl)
        - [Obtaining digital certificate](#obtaining-digital-certificate)
    - [Shell Programming](#shell-programming)
        - [Overview. How exprs are evaluated??](#overview-how-exprs-are-evaluated)
        - [vi](#vi)
        - [Environment Variables](#environment-variables)
        - [pipes and redirects](#pipes-and-redirects)
        - [clearscreen](#clearscreen)
        - [pwd](#pwd)
        - [name of logged  in users](#name-of-logged-in-users)
        - [sed](#sed)
            - [Convert lower to upper](#convert-lower-to-upper)
        - [gawk](#gawk)
        - [grep (c, i ,v)](#grep-c-i-v)
        - [tr](#tr)
        - [sort](#sort)
        - [export](#export)
        - [Working with Web using Shell script ?](#working-with-web-using-shell-script)
    - [Mobile Programming](#mobile-programming)
        - [Major Components](#major-components)
        - [Limux Kernel](#limux-kernel)
        - [Native Android Libraries](#native-android-libraries)
        - [AmdroidManifest.xml](#amdroidmanifestxml)
        - [Activity](#activity)
            - [Creation](#creation)
            - [Life Cycle](#life-cycle)
        - [Intents](#intents)
        - [Layouts View Group](#layouts-view-group)
        - [Sms manager](#sms-manager)
        - [Location Based  Services](#location-based-services)
        - [Publishing Android](#publishing-android)

---
## Overview

### What's the difference between open source software and other types of software?

>* proprietary/closed source
>    * exclusive control over modification
>    * licence must be signed for usage
>* open source
>    * source code is made available
>    * copy learn alter share
>    * must accept license but legal terms vary
>    * some stipulate that source code must be provided
>    * others also want that there should be no licensing fee

Some software has source code that only the person, team, or organization who created it—and maintains exclusive control over it—can modify. People call this kind of software "proprietary" or "closed source" software.

Only the original authors of proprietary software can legally copy, inspect, and alter that software. And in order to use proprietary software, computer users must agree (usually by signing a license displayed the first time they run this software) that they will not do anything with the software that the software's authors have not expressly permitted. Microsoft Office and Adobe Photoshop are examples of proprietary software.

Open source software is different. Its authors make its source code available to others who would like to view that code, copy it, learn from it, alter it, or share it. LibreOffice and the GNU Image Manipulation Program are examples of open source software.

As they do with proprietary software, users must accept the terms of a license when they use open source software—but the legal terms of open source licenses differ dramatically from those of proprietary licenses.

Open source licenses affect the way people can use, study, modify, and distribute software. In general, open source licenses grant computer users permission to use open source software for any purpose they wish. Some open source licenses—what some people call "copyleft" licenses—stipulate that anyone who releases a modified open source program must also release the source code for that program alongside it. Moreover, some open source licenses stipulate that anyone who alters and shares a program with others must also share that program's source code without charging a licensing fee for it.

By design, open source software licenses promote collaboration and sharing because they permit other people to make modifications to source code and incorporate those changes into their own projects. They encourage computer programmers to access, view, and modify open source software whenever they like, as long as they let others do the same when they share their work.

### Open source  licenses

>* GNU: AGPLv3, GPLv3, LGPLv3; Mozilla Public License 2.0; Apache License 2.0; >MIT license; Unlicense
>* All allow Commercial, Distribution, Modification, Patent, Private
>* MIT, Unlicense no clause for Patent
>* All licenses have limitation of liability and do not provide warranty
>* MPL, AL explicitly deny trademark rights

[All from here](https://choosealicense.com/licenses/)  
BSD requirements from appendix

---

## Operating System

### Features of Linux

>* General Features
>	* Process scheduling, prioritizing
>	* Memory management
>	* Devices and kernel management
>	* File System
>	* Security
>	* Networking
>	* Server
>	* Multiuser
>	* Multitasking
>* Special
>	* X Window
>	* No reboot for install
>	* Start and stop individual
>	* Portable Software
>	* Application package manager for installation
>	* Selection of various distributions with source code
>	* Swap

Refer from M15-5 and pg16

### Linux Distributions  
![Hierarchy](https://tellmeinsimpleterms.files.wordpress.com/2013/07/linux-tree.png)

### Logical Volume Manager

>* Creates abstraction layer
>* Hides actual storage
>* Dynamic change in config without change in hardware and vice versa
>* Advantages
>	* Availability
>	* Dynamic moving
>	* Dynamic resizing
>	* Concatenation and striping
>	* Shared storage clusters
>	* Snapshots
>	* Independence of disk location
>* Layers
>	* Physical volume: regular hd
>	* Volume group: group of pv
>	* Logical volume: small segment of vg, defined by extents
>		* Physical extent: smallest allocation of physical; contiguous
>		* Logical extent: non-contiguous allocation of pe

```bash
pvcreate /dev/sdb1 /dev/sdb3
vgcreate /dev/sdb
lvcreate -l 2G -n lvname vgname
vgextend
lvextend
vgremove
lvremove
pvremove
```
From notes

[LVM explanation](https://www.centos.org/docs/5/html/Deployment_Guide-en-US/ch-lvm.html)

### File Hierarchy Standards

>* boot: files necessary for booting and installer; no config file
>* etc: configuration files for applications and services; change settings
>* opt: files which might be used for system installation and functioning
>* var: log files
>* lost+found: information about corrupt files
>* dev: special  files for representing various hardware devices
>* srb: files related to running services
>* proc: subdirectories correspond to the number of processes running in the system
>* tmp: temporary files
>* root: home directoy for root/superuser
>* home: subdirectories that act as home for each user
>* bin: executable files for linux shell environment, file management etc
>* sbin: binary exec files for system eg. fdisk, init
>* lib: programs used by system from bin and sbin
>* usr: user applications
>* mnt: mount external storage devices (Redhat based)
>* media: mounting for other dstributions

From notes

[Exra info](https://www.centos.org/docs/5/html/Deployment_Guide-en-US/s1-filesystem-fhs.html)

### Swap partition

>* vram -> linux
>* moves ram overflow, currently unneeded parts to disk
>* if required something else is swapped from ram
>* paging
>* should be partition

pg21

General Rule:
```
If M < 2
	S = M *2
Else
	S = M + 2
```    
Advantages:
* Provides overflow space when your memory fills up completely
* Can move rarely-needed items away from your high-speed memory
* Allows you to hibernate

Disadvantages:
* Takes up space on your hard drive as SWAP partitions do not resize dynamically
* Can increase wear and tear to your hard drive
* Does not necessarily improve performance 

### RAID

You know it

### Dual boot hard-disk partitioning
What are we supposed to write?

[Cool Stuff](https://askubuntu.com/questions/581902/how-to-efficiently-partition-a-single-windows-ubuntu-dual-boot-disk)

### Role of bootloader

* helps boot operating system
* GRUB/LILO
* first process on computer start
* BIOS/BIOS POST(Power ON Self Test)
	* Performs integrity check on hardware devices
	* Locates available boot sectors
	* Finds primary bootable device
	* Loads bootloader to RAM, passes control to MBR
* MBR (Master Boot Record)
	* 512 bytes
		* 446 bootloader
		* 64 partition table
		* 2 validation
	* Loads 1st part: GRUB
* GRUB (GRand Unified Bootloader)
	* Identifies all OS
	* Shows snapshot of all
	* On selection, loads kernel
	* Filesystem is identified


from notes

### Partitioning ?

### Hosting parts on different partitions ?

### File permissions

-l lists:
* File type and permissoin
* Link attribute
* Ownership
* Group
* Size
* Last Modified
* Name

[chmod](#chmod)
Notes

### Directory permissions

same as above d _ _ _ _ _ _ _ _ _

### Links and types. Compare

* A link is an entry in your file system which connects a file name to the actual bytes of data on the disk. 
* link and ln commands can be used

	ln [OPTION]... TARGET [...] [LINKNAME [...]]

Hard:
![Hard](https://www.computerhope.com/unix/images/link-diagram.jpg)

Soft:
![Soft](https://www.computerhope.com/unix/images/symlink-diagram.jpg)

	ln -s documents/ dox

| Hard                                                  | Soft                                          |
| ----------------------------------------------------- | --------------------------------------------- |
| Same inode number                                     | Different inode number                        |
| ls -l link column shows number of links               | shows value 1                                 |
| Actual file contents                                  | Only path                                     |
| Removal reduces link count                            | Doesnt affect anything                        |
| Cannot create for directory                           | Can                                           |
| If original file is removed, will still show contents | Dangling link: points to nonexistant location |

### inode

Short for index node, an inode is information contained within a Unix system that contains details about each file, such as the node, owner, file, location of file, etc.

When a file is created, it is assigned both a name and an inode number, which is an integer that is unique within the filesystem. Both the file names and their corresponding inode numbers are stored as entries in the directory that appears to the user to contain the files. That is, the directory associates file names with inodes.

Whereas a file contains only its own content and a directory holds only the names of the files that appear to the user to be contained in it and their inode numbers, an inode contains all the other information describing a file. 
This metadata includes 
1. the size of the file (in bytes) and its physical location 
2. the file's owner and group
3. the file's access permissions 
4. timestamps telling when the inode was created, last modified and last accessed
5. a reference count telling how many hard links point to the inode.

Filesystem can run out of space by consuming all of its inodes

Why inode unique only within filesystem?

### Power commands

![halt vs shutdown](https://lh3.googleusercontent.com/1xa839vuZY8LPqkqXDdPbr7ZI6RTQf8Yk2wY8r4Z_6223cr6pbMAN8LAmCyA0HliIPQ_qcW26wGTx8mOjxyo=w1366-h672-rw)

#### halt

halt instructs the hardware to stop all CPU functions.

	halt [OPTION]...

f, --force	Does not invoke shutdown and instead performs the actual action you would expect from the name.

#### shutdown
The shutdown command brings the system down in a secure way. All logged-in users are notified that the system is going down, and login operations are blocked. It is possible to shut the system down immediately, or after a specified delay.

	shutdown [-t sec] time [message]

time The time argument specifies when to perform the shutdown operation.
message	A message to be sent to all users, along with the standard shutdown notification.


The -H option just sets the init environment variable INIT_HALT to HALT, and the -P option just sets that variable to POWEROFF. The shutdown script that calls halt as the last thing in the shutdown sequence should check these environment variables and call halt with the right options for these options to actually have any effect.

[ref](https://www.computerhope.com/unix/uhalt.htm)


### mount umount

#### mount

The mount command mounts a storage device or filesystem, making it accessible and attaching it to an existing directory structure.

	mount -t type device dir 

Printing mounts

	mount [-l] [-t type]

| File             | descr                                                                    |
| ---------------- | ------------------------------------------------------------------------ |
| /etc/fstab       | filesystem table                                                         |
| /etc/mtab        | table of filesystems that are mounted. This file is also used by umount. |
| /etc/mtab~       | lock file                                                                |
| /etc/mtab.tmp    | temporary file                                                           |
| /etc/filesystems | list of filesystem types to try                                          |

#### unmount

The umount command "unmounts" a mounted filesystem, informing the system to complete any pending read or write operations, and safely detaching it.

Same as above

[ref](https://www.computerhope.com/unix/umount.htm)

## System Administration

### chmod chown chgrp

#### chmod
chmod is used to change the permissions of files or directories.

	chmod [options] mode[,mode] file1 [file2 ...]

Usual implemented options include:  
* -R recursive, i.e. include objects in subdirectories
* -f force, forge ahead with all objects even if errors occur
* -v verbose, show objects processed

There are 2 ways to indicate permissions:

Numeric/Octal modes:  
Binary rwx -> uga

```sh
$ ls -l sharedFile
-rw-r--r--  1 jsmith programmers 57 Jul  3 10:13  sharedFile
$ chmod 664 sharedFile
$ ls -l sharedFile
-rw-rw-r--  1 jsmith programmers 57 Jul  3 10:13  sharedFile
```

Symbolic modes
| Reference | Class  | Description                                                            |
| --------- | ------ | ---------------------------------------------------------------------- |
| u         | owner  | file's owner                                                           |
| g         | group  | users who are members of the file's group                              |
| o         | others | users who are neither the file's owner nor members of the file's group |
| a         | all    | all three of the above, same as ugo                                    |

| Operator | Description                                                                  |
| -------- | ---------------------------------------------------------------------------- |
| +        | adds the specified modes to the specified classes                            |
| -        | removes the specified modes from the specified classes                       |
| =        | the modes specified are to be made the exact modes for the specified classes |

```sh
$ ls -ld referenceLib
drwxr-----   2 teamleader  usguys 96 Apr 8 12:53 referenceLib
$ chmod ug=rx referenceLib
$ ls -ld referenceLib
dr-xr-x---   2 teamleader  usguys 96 Apr 8 12:53 referenceLib
```

#### chown

The chown command changes ownership of files and directories in a Linux filesystem.

```sh
chown [-c|--changes] [-v|--verbose] [-f|--silent|--quiet]
      [--from=currentowner:currentgroup]
      [-R|--recursive] 
      {new-owner} file ...
```
Changing Owner:

	sudo chown myuser myfile.txt

Changing owner and group:

	sudo chown notme:notmygroup myfile.txt

Changing recursively:

	sudo chown -R myuser:mygroup otherfiles

#### chgrp

Changes group ownership of a file or files

```sh
chgrp [OPTION]... GROUP FILE...
chgrp hope file.txt 
```

Options are same as above

Extra:
[Other user commands](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Introduction_To_System_Administration/s1-acctsgrps-apps.html)

### /etc/{passwd, group, shadow, gshadow}

[/etc/passwd](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Introduction_To_System_Administration/s2-acctsgrps-files.html)
[/etc/shadow](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Introduction_To_System_Administration/s3-acctsgrps-shadow.html)
[/etc/group](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Introduction_To_System_Administration/s3-acctspgrps-group.html)
[/etc/gshadow](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Introduction_To_System_Administration/s3-acctsgrps-gshadow.html)

### **Processes**

Notes page 6 onwarrds
### Overview

* Instance of program
* Brought into memory for execution
* Alive till completion
* Attributes in process table
	* PID
	* PPID: Parent PID
	* Process state: Ready Running Wait Zombie Orphan
	* UID: User ID
	* GID
	* File descriptor table
	* Process usage information
	* Signal disposition table

### Relevant commands

### Process Creation / fork-exec-wait-exit

1. fork
	1. Creates copy of parent and assigns new PID
2. exec
	1. Copies details and initiates running
3. After child starts executing
	1. parent waits for child to complete job: wait system call
	1. Continues own work
4. After child dies, exit call reurns exit status and informs parent, else: zombie


### init ?

### daemon processes

A daemon is a type of program on Unix-like operating systems that runs unobtrusively in the background, rather than under the direct control of a user, waiting to be activated by the occurance of a specific event or condition.

Daemons are recognized by the system as any processes whose parent process has a PID of one, which always represents the process init. init is always the first process that is started when a Linux computer is booted up (i.e., started), and it remains on the system until the computer is turned off. init adopts any process whose parent process dies (i.e., terminates) without waiting for the child process's status. Thus, the common method for launching a daemon involves forking (i.e., dividing) once or twice, and making the parent (and grandparent) processes die while the child (or grandchild) process begins performing its normal function.

### user processes

processes created by a user

	top -U [username]

	ps -u [username]

### parent process



### child processes

### background process

### foreground process


## Backup commands
---

## Networking and Security

### Networking commands

#### netstat (snetstat?)

netstat ("network statistics") is a command-line tool that displays network connections (both incoming and outgoing), routing tables, and a number of network interface (network interface controller or software-defined network interface) and network protocol statistics.

General statistics:  

	netstat

Shows information about all active connections to the server, including the source and destination IP addresses and ports, if you have proper permissions.

	netstat -rn

#### ping

Short for Packet InterNet Groper, ping is a utility used to verify whether or not a network data packet is capable of being distributed to an address without errors. The ping utility is commonly used to check for network errors.

	ping

-a audible  
-b broadcast  
-f flood

#### arp 

arp manipulates or displays the kernel's IPv4 network neighbour cache. It can add entries to the table, delete one, or display the current content.  

ARP stands for Address Resolution Protocol, which is used to find the address of a network neighbor for a given IPv4 address.

arp with no mode specifier will print the current content of the table. It is possible to limit the number of entries printed, by specifying an hardware address type, interface name or host address.

arp -d address will delete a ARP table entry. Root privilege is required to do this. The entry is found by IP address. If a hostname is given, it will be resolved before looking up the entry in the ARP table.

```bash 
arp -s address hw_addr
```
#### host

host is a simple utility for performing **DNS lookups**. It is normally used to convert names to IP addresses and vice versa. When no arguments or options are given, host prints a short summary of its command line arguments and options.

name is the domain name that is to be looked up. It can also be a dotted-decimal IPv4 address or a colon-delimited IPv6 address, in which case host will by default perform a reverse lookup for that address. server is an optional argument which is either the name or IP address of the name server.

-4 IPv4 force  
-6 IPv6 force

#### traceroute 

traceroute prints the route that packets take to a network host.

	traceroute computerhope.com

-4, -6  
-I ICMP  
-T TCP

[More](https://www.computerhope.com/unix/utracero.htm)

#### ifconfig


ifconfig stands for **"interface configuration"**. It is used to view and change the configuration of the network interfaces on your system

Running the ifconfig command with no arguments, like this:

	ifconfig

...will display information about all network interfaces currently in operation. The output will resemble the following:
  
Here, eth0, lo and wlan0 are the names of the active network interfaces on the system.

eth0 is the first ethernet interface. (Additional ethernet interfaces would be named eth1, eth2, etc.) 
lo is the loopback interface. This is a special network interface that the system uses to communicate with itself.
wlan0 is the name of the first wireless network interface on the system. Additional wireless interfaces would be named wlan1, wlan2, etc.

#### nslookup

The nslookup command is used to query internet name servers interactively for information.

nslookup, which stands for "name server lookup", is a useful tool for finding out information about a named domain.

By default, nslookup will translate a domain name to an IP address (or vice versa). For instance, to find out what the IP address of microsoft.com is, you could run the command:

	nslookup microsoft.com

-type = {ns, mx, soa, any}
-debug

#### route

Show or manipulate the IP routing table.

In computer networking, a router is a device responsible for forwarding network traffic. When datagrams arrive at a router, the router must determine the best way to route them to their destination.

	route [-CFvnee]
	Destination     Gateway         Genmask         Flags Metric Ref    Use Iface


### Apache RPM installation

### Iptables

Pdf

### http.conf

#### Keepalive

#### Keepalive Timeout

#### MaxClients

#### ServerLimit

#### StartServers

### DNS

### Configuration as MasterDNS

### SSL

### Obtaining digital certificate 

---

## Shell Programming

### Overview. How exprs are evaluated??

### vi

![Graphical Cheatsheet](http://www.viemu.com/vi-vim-cheat-sheet.gif) 
![Detailed Vim Cheatsheet](https://rumorscity.com/wp-content/uploads/2014/08/10-Best-VIM-Cheat-Sheet-02.jpg)
Commands to move cursor around: hjkl  
insert text: i, a  
delete text: d

### Environment Variables

### pipes and redirects

### clearscreen

### pwd

### name of logged  in users

### sed

#### Convert lower to upper

### gawk

### grep (c, i ,v)

### tr

### sort

### export

### Working with Web using Shell script ?

---

## Mobile Programming

### Major Components

### Limux Kernel

### Native Android Libraries

### AmdroidManifest.xml

```xml

<?xml version="1.0" encoding="utf-8"?>

<manifest>

    <uses-permission />
    <permission />
    <permission-tree />
    <permission-group />
    <uses-sdk />
    <uses-configuration /> 

    <application>

        <activity>
            <intent-filter>
                <action />
                <category />
                <data />
            </intent-filter>
            <meta-data />
        </activity>

        <activity-alias>
            <intent-filter> . . . </intent-filter>
            <meta-data />
        </activity-alias>

        <service>
            <intent-filter> . . . </intent-filter>
            <meta-data/>
        </service>

        <receiver>
            <intent-filter> . . . </intent-filter>
            <meta-data />
        </receiver>

        <provider>
            <grant-uri-permission />
            <meta-data />
            <path-permission />
        </provider>

        <uses-library />

    </application>

</manifest>
```


Conditions:
* \<manifest> and \<application> elements are required. They each must be present and can occur only once.
* All of the values are set through attributes, not as character data within an element.
* An \<activity-alias> element must follow the \<activity> for which it is an alias.
* The \<application> element must be the last element inside the \<manifest> element. In other words, the \</application> closing tag must appear immediately before the </manifest> closing tag.



### Activity

#### Creation

#### Life Cycle

![Android Life cycle](https://www.javatpoint.com/images/androidimages/Android-Activity-Lifecycle.png)

### Intents

### Layouts View Group

### Sms manager

### Location Based  Services

### Publishing Android