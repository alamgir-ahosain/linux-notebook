#  The `dig` Command

* **Purpose:** Tests **DNS server functionality** and performs **DNS queries**.
* **Use case:** Determine if a DNS server can resolve a hostname to an IP address.



### **Basic Usage** : `dig example.com`


![alt text](image/dig.png)
* Indicates the DNS server resolved `example.com` to `192.168.1.2`.


 **Example Output Sections:**

| Section           | Description                                                    |
| ----------------- | -------------------------------------------------------------- |
| QUESTION SECTION  | The domain and query type (e.g., A record)                     |
| ANSWER SECTION    | IP address or requested information returned by the DNS server |
| AUTHORITY SECTION | DNS server authority for the domain                            |
| SERVER            | DNS server used for the query                                  |
| QUERY TIME        | Time taken to get the response                                 |



### Error Example

```bash
dig sample.com
```

* If the DNS server cannot resolve the name:
![alt text](image/dig2.png)
---

> `dig` is a powerful tool for **troubleshooting DNS issues** and verifying server responses.
