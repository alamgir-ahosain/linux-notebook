# Users 

#### **User Account Files**

* **`/etc/passwd`** – Stores user account details.
* **`/etc/shadow`** – Stores encrypted passwords and authentication data.

#### **Creating Users**

* **Do not edit files manually** – high risk of login failures.
* Use **`useradd`** to safely create users.
* `useradd` automatically updates `/etc/passwd` and `/etc/shadow`.

#### **Why Use `useradd`**

* Prevents syntax and permission errors.
* Ensures consistent and secure account creation.

#### **Before Adding Users**

* Check default settings used by `useradd`.
* Defaults are defined in configuration files.
* Proper defaults reduce post-creation fixes.

#### **Key Configuration Files**

| File                   | Purpose                               |
| ---------------------- | ------------------------------------- |
| `/etc/login.defs`      | Default UID, GID, password policies   |
| `/etc/default/useradd` | Default home directory, shell, groups |


> Remember : Verify useradd defaults **before** creating users to avoid reconfiguration later.

