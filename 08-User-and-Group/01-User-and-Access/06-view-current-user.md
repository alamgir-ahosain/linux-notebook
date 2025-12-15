#  Viewing Current Users

Linux provides commands to view users currently logged in and system status: **`who`** and **`w`**.


---

## **1. `who` Command**

* **Purpose:** Shows currently logged-in users, terminals, login time, and host info.

![alt text](image/vcurrent.png)


  | Column   | Description                                                                 |
  |----------|-----------------------------------------------------------------------------|
  | USER     | Name of the logged-in user                                                 |
  | TTY      | Terminal type; `tty` = local, `pts` = pseudo terminal (remote/login)       |
  | DATE     | Login date and time                                                        |
  | HOST     | - Remote host name, domain, or IP (if applicable)<br> -  `(:number)` Local graphical login shows<br> - **No host info** → Local command-line login |

 **Options:**
  | Option   | Description                                           | Example                |
  |----------|-------------------------------------------------------|------------------------|
  | `-b`     | Show last system boot time                             | `who -b`               |
  | `-r`     | Show current runlevel                                  | `who -r`               |
  | Combined | `who -b -r`                                           | Shows boot time & runlevel |


## **2. `w` Command**

* **Purpose:** Provides detailed info about current users and system load.
![alt text](image/w.png)

  | Column  | Description                                                                 |
  |---------|-----------------------------------------------------------------------------|
  | USER    | Username of the logged-in user                                              |
  | TTY     | Terminal window in use                                                      |
  | FROM    | Source of login (host or IP)                                               |
  | LOGIN@  | Time of login                                                              |
  | IDLE    | Time since last activity                                                   |
  | JCPU    | Total CPU time for all processes since login                               |
  | PCPU    | CPU time for the current process                                           |
  | WHAT    | Command/process currently running                                           |


---



>* `who` is for **simple user check**.
>* `w` gives **detailed info**, including system load and user activity.
