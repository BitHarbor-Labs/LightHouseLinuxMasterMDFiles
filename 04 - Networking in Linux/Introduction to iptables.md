# Iptables is a firewall utility program for Linux systems. It allows system administrators to define rules and policies for filtering network traffic. Let's explore some key concepts related to iptables:

## 1. Overview:
   - Iptables acts as a user-space firewall, filtering connections based on user-defined rules.
   - It helps protect networks by controlling incoming and outgoing traffic.

### 2. Installation:
   - Iptables usually comes pre-installed on Linux distributions.
   - To verify the installation, run:
     ```
     sudo iptables -L -v
     ```
   - This command displays the default rules for the filter table, which is the most widely used table¹.

#### 3. Tables:
   - Iptables maintains different tables:
     - **filter**: Used for every input packet. Decides whether to accept or drop data.
     - **nat**: Handles Network Address Translation (NAT) rules.
     - **mangle**: Allows altering IP headers.
   - The **filter** table is the default and widely used one.

##### 4. Example:
   - To view default rules for the **nat** table:
     ```
     sudo iptables -t nat -L -v
     ```

- [(1) Introduction to iptables | Baeldung on Linux.](https://www.baeldung.com/linux/iptables-intro.)
- [(2) Iptables Tutorial: Ultimate Guide to Linux Firewall - phoenixNAP.](https://phoenixnap.com/kb/iptables-linux.)
- [(3) Linux Iptables For Beginners - CertCube Labs.](https://blog.certcube.com/linux-iptables-for-beginners/.)