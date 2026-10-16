Writing

# Cisco Packet Tracer Network Topology Project

This project demonstrates the design of a small network using **Cisco Packet Tracer**, featuring a central router connected to three separate LAN segments. Each LAN contains a network switch and end devices, enabling communication between computers and a server through the network infrastructure.

## Table of Contents

- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author

## Project Overview

The purpose of this project is to design and simulate a network infrastructure using Cisco Packet Tracer to demonstrate basic networking concepts, device connectivity, and inter-network communication.

The project aims to:

- Design a **star-based hierarchical network topology** with a central router and multiple switches.
- Connect end devices, including computers and a server, to their respective LAN segments.
- Establish communication between devices using appropriate IP addressing and routing configurations.
- Understand the roles of routers, switches, servers, and end devices in a computer network.
- Test connectivity and identify potential network configuration issues.

## Network Topology

The network consists of a central router connected to three access switches. Each switch serves a separate LAN segment containing end devices.

### Network Components

- **1 Router:** Provides connectivity between the three LAN segments.
- **3 Switches:** Connect end devices within each LAN and provide uplinks to the central router.
- **1 Server:** Connected to the first switch to provide network services.
- **6 PCs:** Two computers connected to each switch.
- **Network Connections:** Ethernet links connect the router, switches, server, and PCs.

### Network Layout

The topology is organized as follows:

1. **LAN 1:** Switch 1 connects PC0, PC1, and Server0. The switch uplinks to the central router.
2. **LAN 2:** Switch 2 connects PC2 and PC3 and uplinks to the central router.
3. **LAN 3:** Switch 3 connects PC4 and PC5 and uplinks to the central router.

### IP Addressing

The uploaded topology image does not display IP addresses or subnet masks. These values must be assigned during configuration.

A suggested addressing plan is shown below. It assumes three separate IPv4 subnets, one for each LAN.

| Network Segment | Suggested Network | Default Gateway | Devices |
| --- | --- | --- | --- |
| LAN 1 | `192.168.10.0/24` | `192.168.10.1` | PC0, PC1, Server0 |
| LAN 2 | `192.168.20.0/24` | `192.168.20.1` | PC2, PC3 |
| LAN 3 | `192.168.30.0/24` | `192.168.30.1` | PC4, PC5 |

**Note:** The IP addresses above are proposed examples, not verified configurations from the uploaded topology. Each router interface connected to a LAN should receive the corresponding gateway address. End devices should use unique IP addresses within their subnet and the appropriate subnet mask and default gateway.

## Tools and Technologies

- **Cisco Packet Tracer:** Network design, configuration, and simulation.
- **Router:** Provides Layer 3 connectivity between separate IP networks.
- **Ethernet Switches:** Provide Layer 2 connectivity between devices within each LAN.
- **Server:** Represents a server connected to the first LAN.
- **PCs:** Represent client devices used for connectivity testing.
- **IPv4 Addressing:** Identifies devices and separates the LAN segments into subnets.
- **Routing:** Enables communication between different LANs.
- **ICMP /****`ping`****:** Tests reachability between network devices.
- **Cisco IOS CLI:** Used to configure router interfaces and verify network status.

## Configuration Steps

1. **Build the topology**
   - Open Cisco Packet Tracer.
   - Add one router, three switches, six PCs, and one server.
   - Arrange the devices according to the uploaded topology.
2. **Connect the devices**
   - Connect the router to each of the three switches using Ethernet links.
   - Connect two PCs to each switch.
   - Connect Server0 to Switch 1.
   - Use appropriate Ethernet cables and interface assignments.
3. **Assign IP addresses**
   - Configure the router interfaces with the gateway addresses for the three LANs.
   - Assign each PC a unique IP address and the correct subnet mask.
   - Configure Server0 with an IP address in the first LAN.
   - Set the default gateway on each end device to the corresponding router interface address.
4. **Configure the router**Example configuration for a router interface:
   ```
   enable
   configure terminal
   interface gigabitEthernet 0/0
   ip address 192.168.10.1 255.255.255.0
   no shutdown
   exit
   ```
   Repeat the interface configuration for the other two LANs, using their corresponding IP addresses and the actual interface names available on the router.
   - Open the router CLI.
   - Enter privileged EXEC mode and global configuration mode.
   - Configure each connected interface with its IP address and subnet mask.
   - Enable each interface using the `no shutdown` command.
5. **Verify the router configuration**
   - Run `show ip interface brief` to inspect interface addresses and status.
   - Run `show ip route` to verify that the connected LAN routes appear in the routing table.
   - Confirm that all required router interfaces are operational.
6. **Configure end devices**
   - Open each PC or server's IP configuration settings.
   - Enter its IP address, subnet mask, and default gateway.
   - Ensure that each device belongs to the intended subnet.
7. **Test connectivity**
   - Use `ping` to test connectivity between devices on the same LAN.
   - Test communication between devices on different LANs.
   - Test connectivity between the PCs and Server0.
   - Investigate failed tests by checking IP addresses, subnet masks, gateways, cables, and interface status.
8. **Save the project**
   - Save the Packet Tracer project as `network_topology.pkt`.
   - Document the IP addressing scheme and any configuration changes.
   - Capture screenshots of the completed topology and successful connectivity tests for documentation.

## Results and Findings

The topology illustrates how a central router can connect multiple LANs through separate switches. It provides a practical environment for learning network segmentation, IPv4 addressing, interface configuration, and routing.

The following outcomes are expected after correct configuration:

- **Successful LAN connectivity:** Devices connected to the same switch can communicate when their addressing and local network settings are correct.
- **Inter-LAN communication:** The router can forward traffic between the three subnets when its interfaces and end-device gateways are configured correctly.
- **Server accessibility:** PCs should be able to communicate with Server0 when addressing and routing are configured properly.
- **Network troubleshooting:** Connectivity tests and router status commands can help identify addressing errors, disabled interfaces, and connection problems.

**Verification status:** The uploaded image confirms the visible network layout and connected devices, but it does not establish that IP addressing, routing, or end-to-end connectivity tests have been completed successfully. These results should be verified in Packet Tracer before being reported as achieved.

## Author

- **Name:** \[Your Name\]
- **Email:** \[Your Email Address\]
- **GitHub:** \[Your GitHub Profile URL\]
- **Project:** Cisco Packet Tracer Network Topology****
