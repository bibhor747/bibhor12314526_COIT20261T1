## 1. Week 01 Overview
This portfolio entry documents my completion of the Week 01 tutorial activities for **COIT20261 Network Services and Automation**. The purpose of this week was to become familiar with the unit requirements, install the required software, set up a GitHub repository, and complete an introductory GNS3 activity.

---

## 2. Understanding the Unit
In Week 01, I reviewed the unit profile to understand the structure of the unit and the assessment requirements. This helped me become aware of the portfolio expectations and the practical tasks that will be completed throughout the term.

### Key points understood
- The unit includes weekly practical activities.
- Portfolio work should be maintained regularly.
- GitHub will be used to store and organise portfolio evidence.
- Clear documentation, screenshots, commands, and reflections are expected.

---

## 3. Software Setup
I checked and confirmed the installation of the software required for this unit.

### Required software
- **VirtualBox** – used for virtualization
- **GNS3** – used for network simulation and practical networking tasks

### Setup notes
Both applications were checked before starting the practical task. This ensured that the environment was ready for creating and testing network topologies in later weeks.

## 4. GitHub Repository Setup
A private GitHub repository was created for this unit using the naming format required in the tutorial.

### Required repository name
```text
[student-number]-[COIT20261]-[2026T1]
```

### Example
```text
12345678-COIT20261-2026T1
```

### Repository preparation
- Created the repository as **private**
- Added the Week 01 portfolio file
- Prepared the repository to store screenshots and exported project files
- Shared the repository with the tutor as required

---

## 5. Task 1 – Introduction to GNS3 Basics

### Aim
The aim of this task was to gain basic familiarity with GNS3 by creating a project, adding a Linux Host, configuring a static IP address, adding annotations, starting the node, opening the web console, and checking the IP address using Linux commands.

---

## 6. Project Details

### Project name
```text
GNS3-Intro-[studentid]
```

### Example
```text
GNS3-Intro-12345678
```

### Node used
- 1 × Linux Host

### IP address used
For this task, the Linux Host was assigned the following static IP address:

```text
10.10.1.1/24
```

---

## 7. Annotation Added in GNS3
Text was added in the GNS3 workspace to show:
- Project title
- Student name
- Student number
- Date
- Optional class details such as unit code, campus, or teacher name

A separate label was also added near the Linux Host to show the IP address.

---

## 8. Static IP Configuration
Before starting the Linux Host, the IP address was configured in the `/etc/network/interfaces` file.

### Configuration used
```bash
auto eth0
iface eth0 inet static
    address 10.10.1.1
    netmask 255.255.255.0
    up sysctl net.ipv4.ip_forward=0
```

### Explanation
- `auto eth0` starts the interface automatically
- `iface eth0 inet static` sets a static IPv4 address
- `address 10.10.1.1` assigns the IP address
- `netmask 255.255.255.0` defines the subnet mask
- `up sysctl net.ipv4.ip_forward=0` disables IP forwarding so the node acts like a normal host

---

## 9. Starting the Node and Checking the IP Address
After configuring the interface file, the Linux Host was started and a web console was opened.

### Command used
```bash
ip address show
```

### Observation
The command displayed the configured IP address for `eth0`, confirming that the static addressing was applied successfully.

---

## 10. Commands Used
The following commands or actions were used during this task:

```bash
ip address show
```

### Other actions completed
- Created a new GNS3 project
- Added a Linux Host node
- Added text annotations and a rectangle
- Edited `/etc/network/interfaces`
- Started the node
- Opened the web console in the browser
- Verified the IP address

---

## 11. Screenshots to Include in GitHub
The following evidence files should be uploaded to the repository:

1. **Exported project file**  
   `GNS3-Intro-[studentid].gns3project`

2. **Network screenshot**  
   `GNS3-Intro-[studentid]-network.png`

3. **Console screenshot showing IP address**  
   `GNS3-Intro-[studentid]-ipaddress.png`

---

## 12. Suggested GitHub Folder Structure



---
## 13. Reflection
This week helped me understand the practical structure of the unit and how to document networking tasks properly. I learned how to create a basic GNS3 project, assign a static IP address to a Linux Host, and verify the configuration using the command line. I also understood the importance of keeping portfolio work organised in GitHub, because it will make future weekly submissions easier to manage and present professionally.

---

## 14. What I Learned
From this task, I learned:
- how to create a project in GNS3
- how to add and start a Linux Host
- how to configure a static IP address in `/etc/network/interfaces`
- how to use `ip address show` to check network settings
- how to add annotations in GNS3
- how to organise weekly portfolio work in GitHub

---

## 15. Conclusion
Overall, Week 01 was useful for preparing the software, repository, and practical workflow needed for the rest of the term. The task provided a simple but important introduction to GNS3 and basic Linux network configuration. It also set the foundation for maintaining a clear and organised GitHub-based portfolio throughout the unit.

---
