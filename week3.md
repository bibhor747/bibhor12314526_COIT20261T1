# Task 1: Netcat Communication

## Aim
To understand how to use Netcat (nc) for simple communication between two hosts.

## Setup
- Project: Setting-IP-12314526
- 4 Linux Hosts + 1 Switch

## Netcat Server

Command used:
nc -l -p 12346

## Netcat Client

Command used:
nc 10.10.10.47 12346

## Communication

- Sent Name from client:
  Bibhor Subedi

- Sent Student ID from server:
  12314526

## Observation
- Messages successfully sent and received
- Verified communication between two hosts

---

# Task 2: Packet Capture

## Aim
To capture network packets and export them.

## Steps Performed

1. Started capture on link (Host A ↔ Switch)
2. Ran ping:
   ping -c 3 10.1.1.2

3. Used netcat:
   nc 10.1.1.3 12346

4. Stopped capture

## Output File
Capture-Basics-12314526-ping-netcat.pcap

---

# Key Learnings

- Learned difference between Ping and Netcat
- Understood TCP communication
- Learned packet capturing in GNS3
- Understood basic network traffic flow

---

# Reflection

This lab helped me understand real communication between devices using Netcat. Compared to ping, Netcat allowed sending actual messages, which made it easier to understand application-level communication.

Packet capture was also very useful. It helped me see how data travels in the network. Overall, this practical improved my understanding of networking concepts in a real environment.

---

# Screenshots Required

- Netcat-Basics-12314526-client-server.png
- Capture file (.pcap)


