
# Viewing User Information

The **`id`** command displays user and group information.


Example : 
```bash
id                             # Shows info about the current user
cat /etc/group | grep username # Verify Groups
```
![alt text](image/viewuinfo.png)


#### **Output Fields**

| Field      | Example                        | Description                                           |
| ---------- | ------------------------------ | ----------------------------------------------------- |
| **uid**    | 1001(sysadmin)                 | User ID and username                                 |
| **gid**    | 1001(sysadmin)                 | Primary group ID and name                           |
| **groups** | 1001(sysadmin),4(adm),27(sudo) | All groups the user belongs to (primary + secondary) |


#### **Options**

| Option        | Description                                   | Example               |
| ------------- | --------------------------------------------- | --------------------- |
| `id username` | Show info for a specified user                | `id root`             |
| `-g`          | Print only the **primary group ID**           | `id -g` → `1001`      |
| `-G`          | Print **all group IDs** (primary + secondary) | `id -G` → `1001 4 27` |
