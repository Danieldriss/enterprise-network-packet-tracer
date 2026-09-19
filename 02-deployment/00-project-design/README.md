# NexaCorp - Initial Network Design

## 1. Project Overview

NexaCorp is a fictional technology company used to design and implement a complete enterprise network infrastructure in Cisco Packet Tracer.

The main objective of this project is to learn networking concepts progressively, from basic network fundamentals to more advanced enterprise technologies, while documenting the complete design, implementation, verification, and troubleshooting process.

The network will be designed with scalability, segmentation, security, availability, and centralized management in mind.

---

## 2. Company Locations

NexaCorp has approximately 320 employees distributed across three locations:

| Location | Type | Employees |
|---|---|---:|
| Málaga | Headquarters (HQ) | 200 |
| Madrid | Branch Office 01 | 80 |
| Sevilla | Branch Office 02 | 40 |
| **Total** | | **320** |

---

## 3. Málaga Headquarters

Málaga is the main NexaCorp headquarters and contains the largest number of users and most of the company's central infrastructure.

### Departments

| Department | Employees |
|---|---:|
| Management | 10 |
| Administration | 20 |
| Finance | 20 |
| Human Resources | 15 |
| Sales | 50 |
| Development | 60 |
| IT / Systems | 25 |
| **Total** | **200** |

In addition to employee devices, the headquarters will contain network infrastructure and services such as:

- Servers
- Network printers
- IP phones
- Wireless access points
- Switches
- Routers
- Firewall
- Network management devices
- Corporate WiFi
- Guest WiFi
- Internal server network
- DMZ

---

## 4. Madrid Branch Office

Madrid is NexaCorp's largest branch office, with approximately 80 employees. It has its own local network infrastructure while maintaining connectivity with the Málaga headquarters.

### Departments

| Department | Employees |
|---|---:|
| Administration | 10 |
| Sales | 35 |
| IT / Support | 10 |
| Operations | 25 |
| **Total** | **80** |

The Madrid branch will include:

- Employee computers and laptops
- Network printers
- IP phones
- Wireless access points
- Corporate WiFi
- Guest WiFi
- Switches
- Router
- Network management devices

---

## 5. Sevilla Branch Office

Sevilla is NexaCorp's smallest branch office, with approximately 40 employees. Its network infrastructure will be simpler than Málaga and Madrid while still providing the necessary corporate services and connectivity.

### Departments

| Department | Employees |
|---|---:|
| Administration | 5 |
| Sales | 20 |
| Operations | 10 |
| IT / Support | 5 |
| **Total** | **40** |

The Sevilla branch will include:

- Employee computers and laptops
- Network printers
- IP phones
- Wireless access points
- Corporate WiFi
- Switches
- Router

---

## 6. Network Requirements

The NexaCorp network must provide reliable and controlled connectivity between users, departments, services, branch offices, and the Internet.

The main network requirements are:

- All corporate users must have access to the Internet.
- Devices must automatically receive the appropriate network configuration whenever possible.
- Different departments must be logically separated from each other.
- Communication between different network segments must be controlled.
- Málaga, Madrid, and Sevilla must be able to communicate through the corporate network.
- Users from branch offices must be able to access authorized services located at the Málaga headquarters.
- Internal servers must be separated from regular user networks.
- Public-facing services must be separated from the internal corporate network.
- Corporate WiFi and Guest WiFi must operate as separate networks.
- Guest users must have Internet access but must not be able to access the internal corporate network.
- IP phones must be logically separated from regular user devices.
- Network devices must have a dedicated management network.
- IT administrators must be able to remotely manage network infrastructure securely.
- The network must support centralized services such as DNS, DHCP, NTP, AAA, and Syslog.
- The network must be designed so that new users, departments, devices, and branch offices can be added in the future.

---

## 7. Security Requirements

The NexaCorp network must protect internal resources and restrict access according to the type of user, device, and network segment.

The main security requirements are:

- Guest users must not be able to access any internal corporate network.
- Only authorized users and departments should be able to access sensitive internal services.
- The IT department must have secure administrative access to network devices.
- Management access to routers and switches must not be available from regular user networks.
- Network devices must use secure remote management methods.
- User networks, server networks, management networks, voice networks, and guest networks must remain logically separated.
- Access between different network segments must follow the principle of least privilege.
- Unauthorized devices should be restricted from connecting to access ports whenever possible.
- The network must include protection against common Layer 2 attacks and misconfigurations.
- Public-facing services must be isolated from the internal corporate network.
- Network events and relevant security information should be centrally logged when possible.

---

## 8. Scalability and Availability Requirements

The NexaCorp network must be designed to support future growth while minimizing service interruptions caused by network failures.

The main scalability and availability requirements are:

- The network must allow new users and devices to be added without requiring a complete redesign.
- New departments and network segments should be easy to integrate.
- The IP addressing scheme must reserve enough capacity for future growth.
- Additional branch offices should be able to connect to the corporate network in the future.
- The Málaga headquarters must avoid critical single points of failure whenever possible.
- Critical network connections should provide redundancy.
- The network should remain operational whenever an alternative path is available after a link failure.
- Critical network devices should use redundant designs where appropriate.
- The routing infrastructure must be capable of adapting to network topology changes.
- The design must remain manageable as the network grows.

---

## 9. Initial Network Objectives

Based on the company scenario and requirements defined above, the NexaCorp network will be designed and implemented progressively.

The main objectives of the project are:

- Design a structured and scalable enterprise network.
- Create an efficient IP addressing plan for all locations and network segments.
- Segment the network according to departments, services, and device types.
- Provide controlled communication between different network segments.
- Establish connectivity between Málaga, Madrid, and Sevilla.
- Provide centralized network services for corporate users.
- Provide secure Internet connectivity.
- Separate internal, public, guest, voice, server, and management networks.
- Implement secure management of network infrastructure.
- Introduce redundancy and high availability for critical infrastructure.
- Implement network monitoring and centralized logging.
- Apply security mechanisms at different layers of the network.
- Test and verify every implemented technology.
- Create troubleshooting scenarios to understand common network failures.
- Document the complete design, configuration, verification, and troubleshooting process.

The infrastructure will be built progressively in Cisco Packet Tracer. Each stage will introduce new networking concepts only after the necessary theoretical foundations have been studied and documented.