## Configuring IP routing and traffic control on Linux Mint involves using tools like `iproute2` and `tc` (traffic control). Here's a guide to help you get started:

### IP Routing

1. **View Routing Table**:
   - Use the `ip route` command to view the current routing table:
     ```bash
     ip route show
     ```

2. **Add a Static Route**:
   - To add a static route, use the following command:
     ```bash
     sudo ip route add 192.168.2.0/24 via 192.168.1.1
     ```
   - This command routes traffic destined for the `192.168.2.0/24` network through the gateway `192.168.1.1`.

3. **Delete a Route**:
   - To delete a route, use:
     ```bash
     sudo ip route del 192.168.2.0/24
     ```

4. **Default Gateway**:
   - Set the default gateway with:
     ```bash
     sudo ip route add default via 192.168.1.1
     ```

### Traffic Control

1. **Install `tc`**:
   - The `tc` command is part of the `iproute2` package, which should already be installed. If not, install it with:
     ```bash
     sudo apt-get install iproute2
     ```

2. **Basic Traffic Shaping**:
   - To limit the bandwidth of a network interface (e.g., `eth0`), use:
     ```bash
     sudo tc qdisc add dev eth0 root tbf rate 1mbit burst 32kbit latency 400ms
     ```
   - This command sets a token bucket filter (TBF) to limit the bandwidth to 1 Mbps.

3. **Remove Traffic Control Rules**:
   - To remove all traffic control rules from an interface:
     ```bash
     sudo tc qdisc del dev eth0 root
     ```

4. **Advanced Traffic Control**:
   - For more advanced traffic control, you can use class-based queuing (CBQ) or hierarchical token bucket (HTB). Here's an example of setting up HTB:
     ```bash
     sudo tc qdisc add dev eth0 root handle 1: htb default 30
     sudo tc class add dev eth0 parent 1: classid 1:1 htb rate 1mbit
     sudo tc class add dev eth0 parent 1:1 classid 1:10 htb rate 512kbit
     sudo tc class add dev eth0 parent 1:1 classid 1:20 htb rate 256kbit
     sudo tc class add dev eth0 parent 1:1 classid 1:30 htb rate 128kbit
     ```

### Additional Resources

For more detailed information, you can refer to the [Linux Advanced Routing & Traffic Control HOWTO](https://lartc.org/howto/)²³. This guide provides comprehensive instructions on using `iproute2`, `tc`, and other related tools.

If you have any specific questions or need further assistance, feel free to ask!

Source: Conversation with Copilot, 7/19/2024
- [(1) Linux Advanced Routing & Traffic Control HOWTO.](https://lartc.org/howto/.)
- [(2) Linux Advanced Routing & Traffic Control HOWTO.](https://tldp.org/HOWTO/Adv-Routing-HOWTO/.)
- [(3) Linux Advanced Routing & Traffic Control HOWTO.](https://lartc.org/.)
- [(4) View Network Routing Table Using the IP Route Command in Linux Mint 21.](https://linuxgenie.net/view-network-routing-table-using-the-ip-route-command-in-linux-mint-21/.)
- [(5) How to Turn a Linux Server into a Router to Handle Traffic ... - Tecmint.](https://www.tecmint.com/setup-linux-as-router/.)
