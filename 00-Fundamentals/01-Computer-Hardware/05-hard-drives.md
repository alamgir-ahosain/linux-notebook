

# Hard Drives

* Store data for the operating system and programs.
* Can be connected via **motherboard, PCI card, or USB**.
* Includes HDDs, SSDs, and other storage devices.


### Partitions

* A **partition** is a logical division of a disk.
* Linux commonly uses **multiple partitions per disk**.
* Helps organize data and system files.



### Partitioning Types

* **MBR (Master Boot Record)**

  * Older technology.
  * Limited partitions and max size **2 TB**.
  * Tools: `fdisk`, `cfdisk`, `sfdisk`
* **GPT (GUID Partition Table)**

  * Newer and more flexible.
  * Supports **larger disks** and more partitions.
  * Tools: `gdisk`, `cgdisk`, `sgdisk`
* **Universal Tools**
  * `parted`, `gparted` (graphical)


### Device Files

* Stored in the **/dev** directory.
* Disk type prefix:

  * `hd` → IDE disks
  * `sd` → SATA, SCSI, USB disks

### Disk Naming

* Disk order: `/dev/sda`, `/dev/sdb`, `/dev/sdc`
* Partitions:

  * `/dev/sda1`, `/dev/sda2`, etc.


>Use `lsmod`  command to view the currently loaded modules

### View Disk Devices

* Command: `ls /dev/sd*`
* Shows disks and their partitions.



### View Partition Details

* Command: `fdisk -l /dev/sda`
* Displays size, type, and partition layout.
* **Requires root access**.

