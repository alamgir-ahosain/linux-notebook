
#### **CPU Information**

* Display detailed CPU architecture info: `lscpu`
* Show first 20 lines of `/proc/cpuinfo` (detailed CPU specs): `head -n 20 /proc/cpuinfo`


#### **Memory Information**

* Display RAM and swap usage in **megabytes**: `free -m`
* Display RAM and swap usage in **gigabytes**: `free -g`



#### **PCI Devices**

* List all devices on the PCI bus: `lspci`
* List PCI devices **with kernel driver and module info**: `lspci -k`

#### **USB Devices**

* List all USB connected devices: `lsusb`

#### **Kernel Modules**

* View currently loaded kernel modules (drivers): `lsmode`


#### **Disk Devices and Partitions**

* List disk devices and partition tables: `fdisk -l`

