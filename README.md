# Enterprise Network Infrastructure Lab

## Overview

This project simulates a full enterprise network infrastructure using **Cisco Packet Tracer**.  
The goal of the lab was to design and implement a scalable, redundant, and segmented network architecture that mirrors real-world enterprise environments.

The network includes multiple VLANs, redundant core switching, dynamic routing, a DMZ network, internet edge connectivity, and integrated infrastructure services.

In addition to core networking features, the environment also incorporates enterprise endpoints and services such as **VoIP phones, wireless access points, network printers, centralized logging, DNS, and DHCP** to simulate a realistic operational network.

This project demonstrates practical experience with enterprise network design, routing and switching, infrastructure services, redundancy, and edge connectivity.

---

## Network Topology

The network architecture follows a common enterprise design model

The topology includes:

- ISP router simulating external internet connectivity
- Edge router handling NAT and external traffic
- Two core switches providing gateway redundancy
- Access switches for endpoint connectivity
- Multiple VLAN segments for departments and services
- A dedicated DMZ network for externally accessible services
- Branch office connectivity via OSPF

---

## Technologies Implemented

### VLAN Segmentation

The network is segmented using multiple VLANs to isolate departments, services, and management traffic.

VLAN segmentation improves security, organization, and traffic management within the enterprise network.

---

### HSRP Gateway Redundancy

HSRP (Hot Standby Router Protocol) is implemented on the core switches to provide gateway redundancy for internal networks.

This ensures that if one core switch fails, the standby switch immediately takes over as the default gateway.

This design increases network reliability and prevents single points of failure.

---

### OSPF Dynamic Routing

OSPF is used between the edge router and branch router to dynamically exchange routing information.

This allows the network to automatically learn routes between sites and adapt to topology changes.

Dynamic routing ensures scalability and simplifies route management.

---

### DMZ Web Server

A dedicated **DMZ network (VLAN 100)** hosts a web server that can be accessed both internally and externally.

The DMZ isolates public services from internal networks to improve security.

---

### NAT Edge Connectivity

The edge router publishes the DMZ web server to the internet using **static NAT / port forwarding**.


External users access the service through the public IP:

This simulates how organizations expose public services while protecting internal networks.

---

### DHCP and DNS Services

Internal clients receive IP addresses automatically via **DHCP** and resolve internal services using a **DNS server**.

Example DNS resolution:

These services simplify network administration and improve usability.

---

### Centralized Logging

All network devices send logs to a centralized **Syslog server** for monitoring and troubleshooting.


Centralized logging helps network administrators track events and diagnose issues across the infrastructure.

---

### Enterprise Endpoints

The network includes a variety of endpoint devices to simulate a real enterprise environment:

- VoIP Phones
- Wireless Access Points
- Network Printers
- Client PCs
- Infrastructure Servers

Voice VLANs are used to support IP phones while maintaining separation from data traffic.


---

## Skills Demonstrated

This project demonstrates hands-on experience with:

- Enterprise network architecture
- VLAN segmentation
- Layer 3 switching
- First-hop redundancy (HSRP)
- Dynamic routing (OSPF)
- Network Address Translation (NAT)
- DMZ security architecture
- Infrastructure services (DNS, DHCP)
- Centralized logging and monitoring
- VoIP and wireless integration
- Network troubleshooting

---

## Running the Lab

1. Download the `.pkt` file
2. Open it in **Cisco Packet Tracer**
3. Start the simulation
4. Test connectivity between VLANs and devices
5. Access the DMZ web server internally and from the simulated internet client

---

## Lessons Learned

This lab provided practical experience designing and troubleshooting enterprise network infrastructure.

Key concepts reinforced through this project include:

- Redundant network design
- Dynamic routing behavior
- VLAN segmentation strategies
- NAT and DMZ service publishing
- Infrastructure service integration
- Real-world network troubleshooting workflows

---

Jace Pennycuff

This project was created as part of ongoing networking study and practical lab development to build real-world skills in enterprise networking.


