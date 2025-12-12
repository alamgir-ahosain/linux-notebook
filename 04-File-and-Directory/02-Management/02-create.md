
# **Creating Files (`touch` Command)**

The `touch` command is used to **create an empty file** or **update the timestamp** of an existing file.

 **Command Structure:** `touch FILE_NAME`




### **Notes**

* If the file **does not exist**, `touch` creates a **new empty file**.
* If the file **already exists**, `touch` will only **update the last modified time**.




## **Examples**

```bash
touch notes.txt                 # Create a single empty file
touch a.txt b.txt c.txt         # Create multiple files at the same time
touch report.pdf                # Create a non-text file (empty)
touch *.txt                     # Update timestamps of all .txt files
```

---

# **Creating Directories (`mkdir` Command)**

The `mkdir` command is used to **create new directories (folders)**.

**Command Structure:**`mkdir DIRECTORY_NAME`




## **Important Notes**


* `mkdir` can create **one or multiple directories** at once.
* Use `-p` to create **parent directories** that do not exist (nested folders).



## **Examples**

```bash
mkdir Projects                 # Create a single directory
mkdir Work Personal Docs       # Create multiple directories at once
mkdir -p School/Class6/Notes   # Create nested directories (parents included)
mkdir -m 755 MyFolder          # Create a directory with specific permissions
```

