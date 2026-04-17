# Task 1: Viewing Routing Tables

## Aim
To understand routing tables and packet forwarding between different subnets.

## Network Setup
- Project: View-Routes-12314526
- Devices:
  - 3 Linux Hosts
  - 1 Linux Router
  - 1 Switch

## Network Design
Two subnets were created:

- Subnet 1: 10.1.1.0/24  
- Subnet 2: 10.1.2.0/24  

## IP Configuration

### Hosts
- Host1: 10.1.1.1
- Host2: 10.1.1.2
- Host3: 10.1.2.2

### Router
- Interface1: 10.1.1.254
- Interface2: 10.1.2.254

## Configuration Example

auto eth0
iface eth0 inet static
    address 10.1.1.1
    netmask 255.255.255.0
    gateway 10.1.1.254
    up sysctl net.ipv4.ip_forward=0

## Router Forwarding

Enable forwarding:
sysctl net.ipv4.ip_forward=1

Check status:
sysctl net.ipv4.ip_forward

## View Routing Table

Command:
ip route show

## Observation
- Hosts had default gateway set
- Router forwarded packets between subnets
- Routing table showed destination networks and next hops

## Connectivity Test

Command:
ping 10.1.2.2

Result:
- Successful communication between subnets

---

# Task 2: Dynamic Routing (OSPF)

## Aim
To observe how OSPF dynamically updates routes.

## Setup
- Imported OSPF template project
- Started all nodes (FRR routers)

## Commands Used (FRR)

show ip ospf neighbor  
show ip ospf route  
show ip route  

## Observations

- Routers discovered neighbors automatically
- OSPF created dynamic routes
- Routing tables updated automatically

## Traceroute Test

Command:
traceroute <destination IP>

- Observed path through routers

## Link Failure Test

- Stopped NETem node
- Ran traceroute again

Result:
- Path changed automatically
- OSPF selected alternate route

---

# Key Learnings

- Learned how routing tables work
- Understood difference between static and dynamic routing
- Learned how OSPF adapts to network changes
- Understood packet forwarding between subnets

---

# Reflection

This lab helped me understand how routers work in real networks. Before this, I only knew basic IP addressing, but now I understand how devices communicate across different networks using routing tables.

The OSPF part was very interesting because it showed how networks automatically adjust when a link fails. It made me realise how important dynamic routing protocols are in real-world systems.

Overall, this lab improved my understanding of routing, forwarding, and network design.

---

# Screenshots Required

- View-Routes-12314526-network.png
- Routing table outputs
- Ping test screenshot
- OSPF network screenshot
- Traceroute outputs (before and after)


