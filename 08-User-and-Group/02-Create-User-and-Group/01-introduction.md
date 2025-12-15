# Introduction

### User Accounts

* Linux creates a regular user with **sudo** or requires a **root** password.
* Administrative tasks run as **root**, directly or via **sudo**.
* Single-user systems may need one account.
* Multi-user systems should use separate accounts.

### **Advantages of Separate Accounts**

* Private **home directories** for security.
* **Selective sudo** access with logging.
* Flexible **group-based permissions**.

### **Groups & User Management**

* Some systems auto-create a **User Private Group (UPG)**.
* **UPG**: group name = username; only that user is a member.
* Without UPG, users get the **users** group as primary.
* Users must belong to **at least one group**.
* Shared groups support collaboration.

### **Best Practice**

* **Create groups first**, then users.
* Creating users first requires extra changes later.
