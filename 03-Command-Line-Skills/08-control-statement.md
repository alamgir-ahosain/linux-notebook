# Control Statement

*  let  **run multiple commands** or **conditionally execute commands**.
* Commonly used in **scripts**, but also on the **command line**.


## 1. Semicolon 

*  Run multiple commands **sequentially**, **regardless of success**.
Format: `command1; command2; command3`

Example : 

```bash
echo "Hello Alamgir"; ls /fakefolder; echo "Done"
# Hello Alamgir
# ls: cannot access '/fakefolder': No such file or directory
# Done
```

## 2. Double Ampersand

* a logical **AND operation**
*  Run the second command **only if the first succeeds**.
* Format : `command1 && command2`
Example:
```bash
echo "Hello Alamgir" && ls /fakefolder && echo "Done"
# Hello Alamgir
# ls: cannot access '/fakefolder': No such file or directory
```

## 3. Double Pipe 

* a logical **OR operation**
* Run the second command **only if the first fails** ,skips it if the first succeeds.
* Format  : `command1 || command2`
Example:

```bash
echo "Hello Alamgir" || ls /fakefolder || echo "Done"
# Hello Alamgir

ls /fakefolder || echo "Hello Alamgir" || echo "Done" || echo "4th Command"
# ls: cannot access '/fakefolder': No such file or directory
# Hello Alamgir


```