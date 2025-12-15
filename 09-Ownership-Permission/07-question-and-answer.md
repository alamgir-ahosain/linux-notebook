

# **1. Directory Access**

What access does user **bob** have on `abc.txt`?

```text
drwxr-xr-x. 17 root root 4096 23:38 /
drwxr-xr--. 10 root root 128  03:38 /data
-rwxr-xr--.  1 bob  bob  100  21:08 /data/abc.txt
```

## **Answer** : **None**

#### **Explanation**

* File permissions suggest **bob** has full access (`rwx`) to `abc.txt`.
* But to access a file, the user must have **execute (`x`) permission on all parent directories**.
* On `/data`, bob has **others permissions: `r--`**.
* Without execute (`x`) on `/data`, bob:

  * Cannot `cd` into the directory
  * Cannot access, read, write, or execute the file

### **Lesson Learned**

> **Always check parent directory permissions before file permissions.**
> File permissions only apply **after directory access is allowed**.



---
# 2. Viewing Directory Contents

Who can use `ls /data` to display the contents of the `/data` directory?

```text
drwxr-xr-x. 17 root root 4096 23:38 /
drwxr-xr--. 10 root root 128  03:38 /data
-rwxr-xr--.  1 bob  bob  100  21:08 /data/abc.txt
```

## **Answer** : **All users**

#### **Explanation**

* To list directory contents, a user needs **read (`r`) permission** on the directory.
* All users have:

  * **Execute (`x`) on `/`** → can traverse to `/data`
  * **Read (`r`) on `/data`** → can run `ls /data`
* Therefore, **any user can view the directory contents**, including hidden files (`ls -a`).


### **Lesson Learned**

> **Read (`r`) permission allows listing directory contents.**
> Execute (`x`) permission is required for detailed access.


---
# 3. Deleting Directory Contents



Who can delete the file `/data/abc.txt`?

### **Permissions**

```text
drwxr-xr-x. 17 root root 4096 23:38 /
drwxrw-rw-. 10 root root 128  03:38 /data
-rwxr-xr--.  1 bob  bob  100  21:08 /data/abc.txt
```

### **Answer** : **Only the root user**

#### **Explanation**

* **File permissions do NOT control deletion.**
* To delete a file, a user needs:

  * **Write (`w`) permission on the directory**
  * **Execute (`x`) permission on the directory**
* Although everyone has **write (`w`)** on `/data`,

  * Only **root** has **execute (`x`)** on `/data`.
* Without execute permission, users cannot access the directory to remove files.

### **Lesson Learned**

> **Write (`w`) allows file deletion only when execute (`x`) is also present on the directory.**


---

# 4. Accessing the Contents of a Directory


True or False: Can user **bob** successfully run `more /data/abc.txt`?

```text
drwxr-xr-x. 17 root root 4096 23:38 /
dr-xr-x--x. 10 root root 128  03:38 /data
-rwxr-xr--.  1 bob  bob  100  21:08 /data/abc.txt
```

### **Answer** : **True**

#### **Explanation**

* To access a file, a user needs:

  * **Execute (`x`) permission on all parent directories**
  * **Read (`r`) permission on the file**
* The **read (`r`) permission on the directory is NOT required** to access a known file.
* User **bob** has:

  * `x` on `/`
  * `x` on `/data`
  * `r` on `/data/abc.txt`
* Therefore, the command executes successfully.

### **Lesson Learned**

> **Execute (`x`) allows entering a directory; read (`r`) on the directory is only needed to list files.**


---
# 5. The Complexity of Users and Groups


True or False: Can user **bob** run `more /data/abc.txt`?


```text
drwxr-xr-x. 17 root root    4096 23:38 /
dr-xr-x---. 10 sue  payroll 128  03:38 /data
-rwxr-xr--.  1 bob  bob     100  21:08 /data/abc.txt
```

### **Answer** : **Not enough information**

#### **Explanation**

* To access the file, user **bob** needs:

  * `x` on `/`
  * `x` on `/data`
  * `r` on `/data/abc.txt`
* Bob already has required permissions on `/` and the file.
* Access to `/data` depends on **group membership**:

  * **If bob is in `payroll` group** → permissions are `r-x` → command works
  * **If not** → permissions are `---` → command fails

### **Lesson Learned**

> **Always consider user, group, and group membership when evaluating permissions.**


---
# 6. Permission Priority


True or False: Can user **bob** run `more /data/abc.txt`?


```text
drwxr-xr-x. 17 root root 4096 23:38 /
dr-xr-x---. 10 bob  bob  128  03:38 /data
----rw-rwx.  1 bob  bob  100  21:08 /data/abc.txt
```

### **Answer** : **False**

#### **Explanation**

* The file owner is **bob**
* Owner permissions on `abc.txt` are `---`
* Only **owner permissions** are checked for the owner
* Group and others permissions are **ignored** for bob
* Without `r` permission, `more` cannot read the file

### **Lesson Learned**

> **File owner permissions override group and others permissions.**

---
