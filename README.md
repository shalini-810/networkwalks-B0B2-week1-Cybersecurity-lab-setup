# networkwalks-B0B2-week1-Cybersecurity-lab-setup

# Kali Linux VirtualBox Lab Setup 🐉

A virtual cybersecurity lab built using Oracle VirtualBox and Kali Linux to establish a practical environment for learning networking, system administration, and defensive security fundamentals.

## 🎯 Objective

Set up a Kali Linux virtual machine with network connectivity, DNS configuration, and host-to-guest file sharing as part of my cybersecurity training with Network Walks.

## 🛠️ Tools & Technologies

- **Virtualization:** Oracle VirtualBox
- **Operating System:** Kali Linux
- **Networking:** NAT Network
- **Network Subnet:** `10.0.0.0/24`
- **DNS:** Google Public DNS (`8.8.8.8`), once verified
- **File Sharing:** VirtualBox Shared Folders

## ⚙️ Configurations Completed

- [x] Installed and configured Oracle VirtualBox.
- [x] Imported the Kali Linux virtual machine.
- [x] Configured a NAT Network using the `10.0.0.0/24` subnet.
- [x] Verified connectivity to the virtual network gateway.
- [x] Verified internet connectivity from Kali Linux.
- [x] Created and configured a shared `downloads` folder between the host and guest.
- [x] Verified access to the shared folder from Kali Linux.
- [x] Enabled bidirectional shared clipboard.
- [x] Enabled bidirectional drag-and-drop.

## 🧪 Validation & Testing

The following checks were used to validate the environment.

**1. Check network interface configuration**
```bash
ip -br addr
```

**2. Test gateway connectivity**
```bash
ping -c 4 10.0.0.1
```

**3. Test internet connectivity and DNS resolution**
```bash
ping -c 4 google.com
```

**4. Check the active DNS configuration**
```bash
nmcli device show eth0 | grep IP4.DNS
```

**5. Verify the shared folder**
```bash
ls /media/sf_downloads
```

The gateway and internet connectivity tests succeeded, and the shared folder was accessible from Kali Linux.

## 📚 Key Learnings

- Configuring a virtual machine for cybersecurity practice.
- Understanding NAT networking and private IPv4 addressing.
- Testing network connectivity using `ping`.
- Inspecting DNS configuration in Linux.
- Configuring host-to-guest file sharing in VirtualBox.
- Using Linux terminal commands to validate a lab environment.
