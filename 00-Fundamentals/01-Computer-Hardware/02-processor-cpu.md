
# Processors (CPU)

* CPU (processor) is the **brain of the computer**.
* Executes programs and performs calculations.
* Installed directly on the **motherboard**.


### **Processor Types**

* **Single processor** → one CPU
* **Multiprocessor** → multiple CPUs
* **Multi-core** → multiple cores in one CPU chip



### **CPU Architectures**

* **x86 (32-bit)** → processes 32 bits at a time
* **x86_64 (64-bit)** → processes 64 bits (also supports 32-bit)
* **64-bit advantages**:

  * Uses **more memory**
  * Better performance
  * Improved security



### **x86 History**

* Originated by **Intel (8086, 1978)**
* Common generations:

  * i386, i486
  * Pentium (i586)
  * Pentium Pro (i686)
* Other makers: **AMD, Cyrix**
* Many Linux distros support **i686 or newer**



### **Modern Systems**

* Most modern CPUs are **x86_64**
* Some software is still **32-bit**

### Check CPU Architecture

```bash
arch
```

**Example output:**

```text
x86_64
```

### View Detailed CPU Info

```bash
lscpu
```

Shows:

* Architecture (32/64-bit)
* Number of CPUs
* Cores and threads
* Vendor (Intel/AMD)
