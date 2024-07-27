## Linux Mint offers a variety of tools for network troubleshooting. Here are some of the most useful commands and utilities:

### Basic Network Troubleshooting Commands

1. **ifconfig**:
   - Displays network interfaces and their configurations.
   ```bash
   ifconfig
   ```

2. **ip**:
   - A more modern replacement for `ifconfig` with additional features.
   ```bash
   ip addr show
   ```

3. **ping**:
   - Checks connectivity to a host.
   ```bash
   ping google.com
   ```

4. **netstat**:
   - Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
   ```bash
   netstat -tuln
   ```

5. **traceroute**:
   - Traces the route packets take to a network host.
   ```bash
   traceroute google.com
   ```

6. **nslookup**:
   - Queries DNS to obtain domain name or IP address mapping.
   ```bash
   nslookup google.com
   ```

7. **dig**:
   - Another DNS query tool, often preferred for its detailed output.
   ```bash
   dig google.com
   ```

8. **arp**:
   - Displays and modifies the ARP (Address Resolution Protocol) cache.
   ```bash
   arp -a
   ```

9. **tcpdump**:
   - Captures and analyzes network packets.
   ```bash
   sudo tcpdump -i eth0
   ```

### Advanced Tools

1. **nmap**:
   - Network exploration tool and security/port scanner.
   ```bash
   sudo apt-get install nmap
   nmap -sP 192.168.1.0/24
   ```

2. **wireshark**:
   - A graphical network protocol analyzer.
   ```bash
   sudo apt-get install wireshark
   sudo wireshark
   ```

3. **iperf**:
   - Network bandwidth measurement tool.
   ```bash
   sudo apt-get install iperf3
   iperf3 -s  # Start server
   iperf3 -c [server_ip]  # Run client
   ```

4. **ethtool**:
   - Displays and changes Ethernet device settings.
   ```bash
   sudo ethtool eth0
   ```

5. **mtr**:
   - Combines the functionality of `ping` and `traceroute`.
   ```bash
   sudo apt-get install mtr
   mtr google.com
   ```

These tools should help you diagnose and troubleshoot network issues on your Linux Mint system¹²³⁴⁵. If you need more detailed instructions or have specific issues, feel free to ask!

Source: Conversation with Copilot, 7/19/2024
- [(1) 13 Linux Network Configuration and Troubleshooting Commands - Tecmint.](https://www.tecmint.com/linux-network-configuration-and-troubleshooting-commands/.)
- [(2) The Ultimate Guide to Linux Mint Network Configuration.](https://www.fosslinux.com/105545/the-ultimate-guide-to-linux-mint-network-configuration.htm.)
- [(3) 5 Linux network troubleshooting commands | Enable Sysadmin.](https://www.redhat.com/sysadmin/five-network-commands.)
- [(4) The 9 Best Linux Network Troubleshooting Commands - MUO.](https://www.makeuseof.com/best-network-troubleshooting-commands-linux/.)
- [(5) 21 Basic Linux Networking Commands You Should Know - It's FOSS.](https://itsfoss.com/basic-linux-networking-commands/.)