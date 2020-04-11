# Blog 8A (April 3, 2020)

### Topic - Imaging

Currently while I am working from home, I have some training I do during the downtime that is focused into Office 365 and one of the topics they talked about was different methods of how to deploy multiple desktops for a company/organization. One of the things that caught my attention was "Imaging" which was a more manual method but can be beneficial or easier to understand to the end user. Today I will be talking about imaging and what it basically is and how to leverage it to maximize deployment.

Please note because I did mainly training through Windows, I will be talking about how Windows does imaging in a more buisness perspective.

#### What is imaging?

![disk backup](https://www.ubackup.com/screenshot/en/std/backup/disk-backup/add-disk.png)

So first, imaging specifically refers to disk imaging and according to [wikipedia](https://en.wikipedia.org/wiki/Disk_image) a disk image is "is a computer file containing the contents and structure of a disk volume or of an entire data storage device, such as a hard disk drive, tape drive, floppy disk, optical disc, or USB flash drive. A disk image is usually made by creating a sector-by-sector copy of the source medium, thereby perfectly replicating the structure and contents of a storage device independent of the file system. Depending on the disk image format, a disk image may span one or more computer files. The file format may be an open standard, such as the ISO image format for optical disc images, or a disk image may be unique to a particular software application. The size of a disk image can be large because it contains the contents of an entire disk. To reduce storage requirements, if an imaging utility is filesystem-aware it can omit copying unused space, and it can compress the used space".

The original use of disk images was to serve as backups and to clone the current disk, with current use is mainly focused on duplication and cloning. Disk images are also the primary method of distributing bare operating systems (Linux flavors, Windows). This file is then used as a method of installation for the operating system onto the device. But as stated before, disk images for operating systems are usually bare and only contain the standard apps and files needed to run the operating system. This is fine for a single user as they can decide what applications they would want to download/install, however in an organization of hundreds or thousands, doing this manually would be stupid and painful.

How could companies use imaging to improve efficiecy? They can create a disk image of a computer with the correct applications, software, preferences and clone it onto to all the devices for the organization to use.  This makes deploying new computers or upgrading old ones to a newer system, much more convenient since you have something that is current, up to date and easily distributed to aid issues.

For example, Chris's works in IT at his company and they just bought 100 new computers as upgrades for employees.  Now because his company is engineering based, he has to download multiple different large porgrams that can do 3d modeling easily. With these large applications, it would take many many hours to download these on all the new computers. To make the job easier, Chris could consult with the lead engineers, and figure out what aspects of the applications needed to be altered, then install those applications to one computer. Then create an image off the dummy computer, and clone that image across all the new computers so they have the same exact programs and settings that are needed. This would save him a lot of time and work.

![WIM](https://docs.microsoft.com/en-us/windows/deployment/images/windows-icd.png)