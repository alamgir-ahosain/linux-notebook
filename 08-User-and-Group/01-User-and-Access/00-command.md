
# Switch User and  Privileged Commands
1. **`su -`** – Switch to another user with a **login shell**.
    1. **`su -l`** – Same as `su -`; start a **login shell** for the target user.
    2. **`su --login`** – Same as `su -`; execute a **login shell**.
2. **`su - root`** – Switch to the **root user** with a login shell.
3. **`sudo apt update`** – Update package lists from repositories (requires root privileges).



# User Account
1. **`grep username /etc/passwd`** – Check if a user exists

# System Account
1. **`cat /etc/passwd`** – Check system account

# Group Account
1. **`grep "mail" /etc/group`** –  Check group for **mail**

# User User info
1. **`id`** – Shows info about the current user
2. **`id username`** – Show info for a specified user
3. **`id -g`** – Print only the primary group ID
4. **`id -G`** – Print all group IDs (primary + secondary)
5.  **`cat /etc/group | grep username`** –  Verify user groups

# View Current User
1. **`who`** – Shows currently logged-in users
2. **`who -b`** – Show last system boot time
3. **`who -r`** – Show current runlevel
4. **`who -b -r`** – Shows boot time & runlevel
5. **`w`** – detailed info about current users and system load.

# Viewing Login History
1. **last** – Shows login and logout history of users