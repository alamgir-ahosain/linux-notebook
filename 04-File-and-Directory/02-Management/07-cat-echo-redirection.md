

### **Redirection**

Redirection allows command output (STDOUT) to be sent to files instead of the terminal.

**File Descriptors:**

| Descriptor      | Abbreviation | Meaning                          |
| --------------- | ------------ | -------------------------------- |
| Standard Input  | STDIN        | Input to a command (keyboard)    |
| Standard Output | STDOUT       | Normal command output (terminal) |
| Standard Error  | STDERR       | Error messages                   |



### **Basic Redirection**
```bash
[COMMAND] > [FILE]  # Redirect STDOUT to a file (overwrites content)
[COMMAND] >> [FILE] # Append STDOUT to a file
```



### **Example: Redirecting cat Output**

![alt text](image/cat.png)

### **Example: Using echo with Redirection**

![alt text](image/echo.png)


>**Important:**
>* Using `>` **overwrites** existing file content.
>* Using `>>` **appends** to existing file content.
>* User must have **write permissions** on the file to redirect content.

