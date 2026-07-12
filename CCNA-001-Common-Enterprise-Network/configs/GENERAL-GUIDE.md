# Topology

![Network Topology](screenshoots/TOPOLOGY.png)

This project simulates a small enterprise network consisting of two LANs connected by a Cisco router. The topology includes network infrastructure devices, servers, wireless clients, and essential network services such as DHCP, DNS, Web, and TFTP.

---

# Router (R1)

> Configuration file: `configs/R1.txt`

The router serves as the core device connecting **LAN 1** and **LAN 2**. It acts as the default gateway for both networks, enabling communication between them.

| Interface | IP Address | Purpose |
|-----------|------------|---------|
| GigabitEthernet0/1 | 192.168.1.1 | Default Gateway (LAN 1) |
| GigabitEthernet0/0 | 192.168.2.1 | Default Gateway (LAN 2) |

---

# Switch 1 (SW1)

> Configuration file: `configs/SW1.txt`

SW1 provides Layer 2 connectivity for client devices in **LAN 1**.

Connected devices include:

- Access Point (AP)
- Laptop 1 (Wireless)
- Laptop 2 (Wireless)
- DHCP Server
- Laptop 0
- PC 1

Management IP Address:

```text
192.168.1.2
```

---

# Switch 2 (SW2)

> Configuration file: `configs/SW2.txt`

SW2 provides Layer 2 connectivity for enterprise servers located in **LAN 2**.

Connected devices include:

- DNS Server
- Web Server
- TFTP Server

Management IP Address:

```text
192.168.2.2
```

---

# Access Point (AP)

The Access Point provides wireless connectivity for Laptop 1 and Laptop 2.

Configuration:

- Install the wireless network module before powering on the device.
- Power off the Access Point before installing the module.
- Power it on again after installation.
- Keep the default Port 0 and Port 1 configuration.
- Wireless clients will automatically connect once the Access Point is enabled.

---

# Client Devices

All laptops obtain their IP addresses automatically from the DHCP Server.

| Device | IP Assignment |
|---------|---------------|
| Laptop 0 | DHCP (192.168.1.10) |
| Laptop 1 | DHCP (192.168.1.11) |
| Laptop 2 | DHCP (192.168.1.12) |

PC 1 uses a static IP configuration.

| Device | IP Address |
|---------|------------|
| PC 1 | 192.168.1.3 |

---

# DHCP Server

IP Address

```text
192.168.1.254
```

![DHCP Configuration](screenshoots/DHCP-CONFIGURATION.png)

The DHCP server automatically assigns IP addresses to client devices.

Configuration:

- DHCP Service: **On**
- Default Gateway: **192.168.1.1**
- DNS Server: **192.168.2.10**
- Address Pool:
  - Start IP Address: **192.168.1.10**
  - Maximum Users: **3**

Assigned IP Range:

```text
192.168.1.10
↓

192.168.1.12
```

---

# DNS Server

IP Address

```text
192.168.2.10
```

The DNS server translates domain names into IP addresses.

DNS Record:

| Domain Name | Record Type | IP Address |
|-------------|-------------|------------|
| dns-trial.com | A | 192.168.2.30 |

When users access **dns-trial.com**, the DNS server resolves the domain name to the Web Server's IP address.

---

# TFTP Server

IP Address

```text
192.168.2.20
```

The TFTP service is enabled to back up network device configurations and Cisco IOS images.

Functions:

- Running Configuration Backup
- Startup Configuration Backup
- Cisco IOS (Flash) Backup

---

# Web Server

IP Address

```text
192.168.2.30
```

HTTP Service: **On**

The Web Server hosts a simple webpage that can be accessed through either:

```text
http://192.168.2.30
```

or

```text
http://dns-trial.com
```

after successful DNS resolution.
