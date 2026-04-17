# Task 1: ARP (Address Resolution Protocol)

## Aim
To understand how ARP maps IP addresses to hardware (MAC) addresses in a local network.

## Setup
- Project: Setting-IP-12314526
- 4 Linux Hosts + 1 Switch

## Commands Used

View ARP table:
ip neigh show

Ping command:
ping 10.1.1.2

---

## Observations

### Before Communication
- ARP table was empty or had very few entries

### After Ping (Host A → Host B)
- New entry added in ARP table
- IP address of Host B mapped to MAC address
- State shown as REACHABLE

### After Another Ping (Host C → Host A)
- More entries added
- ARP table updated dynamically

---

## Understanding ARP

- ARP helps find MAC address using IP address
- Entries are created automatically when devices communicate
- Entries may expire if not used

---

# Task 2: Default Gateway Configuration

## Aim
To understand how default gateways allow communication between different networks.

## Network Setup

- 4 Hosts
- 2 Routers
- 2 Switches
- 3 Subnets

### Example Subnets

- Subnet 1: 10.1.1.0/24
- Subnet 2: 10.1.2.0/24
- Router link: 10.1.3.0/24

---

## Configuration Example

### Host Configuration

auto eth0
iface eth0 inet static
    address 10.1.1.2
    netmask 255.255.255.0
    gateway 10.1.1.1
    up sysctl net.ipv4.ip_forward=0

### Router Configuration

auto eth0
iface eth0 inet static
    address 10.1.1.1
    netmask 255.255.255.0
    up sysctl net.ipv4.ip_forward=1

---

## Commands Used

View routing table:
ip route show

Ping test:
ping <destination IP>

---

## Observations

- Hosts used default gateway to reach other networks
- Routers forwarded packets between subnets
- Successful ping confirmed connectivity

---

# Key Learnings

- Understood ARP working
- Learned how IP maps to MAC address
- Learned default gateway concept
- Understood routing between networks

---

# Reflection

This lab helped me understand how devices communicate inside a network using ARP. I observed how the ARP table changes when devices start communicating. It made me realise how important MAC addresses are for local communication.

The default gateway task helped me understand how devices communicate across different networks. I learned that without a gateway, devices cannot reach other networks.

Overall, this lab improved my understanding of both local communication and network routing.

---

# Screenshots Required

- ARP-Basics-12314526-HostA-Table.png
- Default-Gateway-12314526-network.png
- Routing table screenshots
- Ping success screenshot


