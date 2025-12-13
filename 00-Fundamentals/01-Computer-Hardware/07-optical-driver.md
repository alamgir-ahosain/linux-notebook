
# Optical Drives

* Optical drives use **removable storage media**.
* Common types include **CD-ROM, DVD, and Blu-Ray**.
* Some drives are **read-only**, others support **writing (burning)** data.


### Writable Optical Disk Types

* **CD-R / CD+R** – Write once
* **CD-RW** – Rewritable
* **DVD-R / DVD+R** – Write once
* **DVD-RW / DVD+RW** – Rewritable



### Mounting Optical Drives in Linux

* Modern Linux systems mount removable media under **/media**
* Older systems commonly use **/mnt**
* Example mount point:

  ```
  /media/usbthumb
  ```


### Using Optical Media

* GUI systems usually **prompt an action** when a disk is inserted
* Examples:

  * Open file browser
  * Play media automatically
* Disks must be **unmounted** before removal

  * Using GUI option
  * Or with the `umount` command

