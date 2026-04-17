
## Task 1: Setting Static IP Addresses

### Aim
Understand three different methods to assign static IP addresses.

### Network Setup
- Project: Setting-IP-12314526
- 4 Linux Hosts + 1 Switch
- Network: 10.1.1.0/24

### IP Configuration
- Host1: 10.1.1.1 (GNS3)
- Host2: 10.1.1.2 (GNS3)
- Host3: 10.1.1.3 (/etc/network/interfaces)
- Host4: 10.1.1.4 (ip command)

### Commands

#### Method 1 (GNS3)
auto eth0
iface eth0 inet static
    address 10.1.1.1
    netmask 255.255.255.0

#### Method 2 (interfaces)
nano /etc/network/interfaces

auto eth0
iface eth0 inet static
    address 10.1.1.3
    netmask 255.255.255.0

ifdown eth0
ifup eth0

#### Method 3 (ip command)
ip address add 10.1.1.4/24 dev eth0

#### Verification
ip address show

---

## Task 2: Ping Testing

### Basic Ping
ping 10.1.1.2

### Wrong IP
ping 10.1.1.10

### Ping with Options
ping -c 5 -i 2 -s 100 10.1.1.2

---

## Key Learnings
- Learned static IP configuration methods
- Understood ping and RTT
- Learned packet loss concept

---

## Reflection
This lab helped me understand networking basics practically. I learned how to assign IP addresses in different ways and how ping works to test connectivity.

---

## Screenshots to Upload
- Setting-IP-12314526-network.png
- Host screenshots
- Ping screenshots
