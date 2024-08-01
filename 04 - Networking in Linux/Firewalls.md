# Firewalls

## 1. **UFW (Uncomplicated Firewall)**:
   - UFW is a straightforward and reliable firewall interface with both command-line and graphical tools.
   - To install UFW, open the terminal and run:
     ```
     sudo apt install ufw
     ```
   - Verify if UFW is active with:
     ```
     sudo systemctl status ufw
     ```
   - To allow specific ports (e.g., OpenSSH), use:
     ```
     sudo ufw allow 22/tcp
     ```
   - To disable a port, run:
     ```
     sudo ufw deny 22/tcp
     ```

### 2. **Gufw (GUI for UFW)**:
   - Gufw provides a graphical interface for managing UFW.
   - Install it with:
     ```
     sudo apt install gufw
     ```
   - Open it from the menu: "Firewall Configuration."

- [(1) How to open a firewall on Linux Mint | FOSS Linux.](https://www.fosslinux.com/50961/open-a-firewall-on-linux-mint.htm.)
- [(2) LINUX Firewall - GeeksforGeeks.](https://www.geeksforgeeks.org/linux-firewall/.)
- [(3) firewalld-cmd Command in Linux: 24 Examples.](https://linuxhandbook.com/firewalld-cmd/.)