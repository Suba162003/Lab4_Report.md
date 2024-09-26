# Lab 4: IP Addressing and Subnetting (VLSM)

## Objective
To understand and implement IP addressing and Variable Length Subnet Masking (VLSM).

## Materials Required
- Packet Tracer software

## Theory
### Basics of IP Addressing and Subnetting
IP addressing involves assigning unique identifiers to devices on a network. Subnetting divides a larger network into smaller, manageable segments, improving efficiency and security.

### Overview of VLSM
Variable Length Subnet Masking (VLSM) allows for the creation of subnets of different sizes, optimizing IP address usage based on the number of hosts required for each subnet.

## Procedure
1. **Design a Network**:
   - Create a network topology with multiple subnets based on the following requirements:
     - Subnet A: 50 hosts
     - Subnet B: 30 hosts
     - Subnet C: 10 hosts
     - Subnet D: 5 hosts

2. **Calculate the Subnets Using VLSM**:
   - Starting with a Class C network, e.g., `192.168.1.0/24`:
     - Subnet A: `192.168.1.0/26` (64 addresses; 62 usable)
     - Subnet B: `192.168.1.64/27` (32 addresses; 30 usable)
     - Subnet C: `192.168.1.96/28` (16 addresses; 14 usable)
     - Subnet D: `192.168.1.112/29` (8 addresses; 6 usable)

3. **Assign IP Addresses**:
   - Assign IP addresses to devices within each subnet:
     - **Subnet A**: 
       - Router Interface: `192.168.1.1`
       - Hosts: `192.168.1.2` to `192.168.1.62`
     - **Subnet B**: 
       - Router Interface: `192.168.1.65`
       - Hosts: `192.168.1.66` to `192.168.1.95`
     - **Subnet C**: 
       - Router Interface: `192.168.1.97`
       - Hosts: `192.168.1.98` to `192.168.1.111`
     - **Subnet D**: 
       - Router Interface: `192.168.1.113`
       - Hosts: `192.168.1.114` to `192.168.1.118`

4. **Test Connectivity**:
   - Use the ping command from devices in different subnets to test connectivity.
   - Ensure that devices in different subnets can communicate through the router.

## Observations
- **Subnet Calculations**:
  - Documented subnet addresses and the number of usable hosts.
  - Ensured proper allocation of IP addresses based on VLSM.

- **Test Results**:
  - Devices successfully pinged each other across different subnets, indicating proper configuration and routing.

## Conclusion
This lab reinforced the significance of proper IP addressing and subnetting. Utilizing VLSM allows for efficient use of IP addresses while meeting the specific needs of different network segments. Proper subnetting enhances network performance, security, and management.
