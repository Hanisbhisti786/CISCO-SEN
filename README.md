# Secure Enterprise Campus Network Design using Cisco Packet Tracer

## Project Overview

This project demonstrates the design and implementation of a secure enterprise-level campus network using Cisco Packet Tracer.

The network simulates a college/enterprise environment consisting of multiple departments connected through Layer 2 and Layer 3 infrastructure. Security features such as SSH remote management, Port Security, VLAN segmentation, Inter-VLAN Routing, and Multilayer Switching have been implemented to provide a scalable and secure architecture.

## Objectives

- Design a scalable enterprise network.
- Implement departmental network segmentation.
- Configure secure remote device management using SSH.
- Implement Port Security to prevent unauthorized access.
- Configure Layer 3 routing between multiple networks.
- Connect servers and end devices across different departments.
- Simulate a real-world campus network architecture.

---

## Network Architecture

The network consists of:

### Core Layer
- Cisco 2811 Routers
- Cisco 3650 Multilayer Switches

### Access Layer
- Cisco 2960 Switches
- PCs
- Laptops
- Printers

### Services Layer
- Application Servers
- Department Servers
- DNS/HTTP capable infrastructure

---

## Key Features Implemented

### VLAN Segmentation
Separate departmental networks have been created for:

- Lab 1
- Lab 2
- Lab 3
- Academic Departments
- Student Networks
- Faculty Networks

This improves security and reduces broadcast traffic.

---

### Inter-VLAN Routing

Inter-VLAN communication is achieved using:

- Multilayer Switches
- Layer 3 Routing

This allows devices from different VLANs to communicate securely.

---

### SSH Secure Remote Access

SSH Version 2 has been configured on network devices.

Features:

- Encrypted remote management
- Username-based authentication
- Secure administration access

Example Configuration:

```bash
ip domain-name bhartiya.com
crypto key generate rsa
ip ssh version 2

username admin privilege 15 secret ********

line vty 0 4
login local
transport input ssh
```

---

### Port Security

Port Security has been implemented on access switches.

Configured Features:

- Maximum MAC addresses limit
- Restrict mode
- Shutdown mode
- Unauthorized device detection

Example:

```bash
switchport port-security
switchport port-security maximum 2
switchport port-security violation restrict
```

---

### Hierarchical Network Design

The project follows the Cisco hierarchical design model:

1. Core Layer
2. Distribution Layer
3. Access Layer

Benefits:

- Scalability
- Easy Troubleshooting
- Better Performance
- High Availability

---

## IP Addressing Plan

Example Network Segments:

| Department | Network |
|------------|----------|
| Lab 1 | 10.0.0.0/12 |
| Lab 2 | 10.16.0.0/12 |
| Department A | 10.48.0.0/12 |
| Department B | 10.64.0.0/12 |
| Department C | 10.112.0.0/12 |
| Department D | 10.128.0.0/12 |
| Department E | 10.144.0.0/12 |
| Department F | 10.160.0.0/12 |

---

## Security Controls

### Device Security
- SSH Version 2
- Encrypted Passwords
- Local User Authentication

### Access Security
- Port Security
- MAC Address Limitation
- Violation Protection

### Network Security
- VLAN Isolation
- Controlled Routing
- Segmented Architecture

---

## Technologies Used

- Cisco Packet Tracer
- Cisco 2811 Routers
- Cisco 3650 Multilayer Switches
- Cisco 2960 Switches
- VLANs
- Inter-VLAN Routing
- SSH
- Port Security
- Static Routing
- Enterprise LAN Design

---

## Skills Demonstrated

This project demonstrates practical knowledge of:

- Network Design
- VLAN Configuration
- Layer 2 Switching
- Layer 3 Switching
- Routing
- Enterprise Network Architecture
- Network Security
- SSH Configuration
- Port Security
- Troubleshooting
- Cisco IOS

---

## Project Outcome

Successfully designed and implemented a secure enterprise campus network supporting multiple departments, secure management access, traffic segmentation, and scalable routing infrastructure.

The project reflects real-world networking concepts commonly used in enterprise environments and demonstrates hands-on Cisco networking skills.
