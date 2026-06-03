````md
# Networking Task 01: Understanding Your Network Environment

## Objective
The goal of this task is to identify the key components of a network and examine the network configuration of a personal device.

---

## 📡 Part A: Network Information

The following network details were collected from the system terminal:

- **Hostname (Device Name):** `kali`
- **IPv4 Address:** `192.168.162.128`
- **MAC Address:** `00:0C:29:75:11:77`
- **Default Gateway:** `192.168.162.2`
- **DNS Server:** `192.168.162.2`

### Terminal Configuration Screenshot

![Network Configuration](./screenshots/network_config.png)

---

## 🧠 Part B: Basic Networking Concepts

### What is an IP Address?

An Internet Protocol (IP) address is a unique logical address assigned to a device connected to a network. It enables devices to identify and communicate with one another by specifying the source and destination of data packets.

### What is a MAC Address?

A Media Access Control (MAC) address is a unique hardware identifier assigned to a network interface card (NIC). It operates at the data link layer and is used for communication between devices on the same local network.

### What is a Default Gateway?

A Default Gateway is a network device, typically a router, that acts as an access point to other networks. When data needs to be sent outside the local network, it is forwarded to the default gateway for routing.

### What is DNS?

The Domain Name System (DNS) is a service that translates human-readable domain names, such as `google.com`, into numerical IP addresses that computers use to locate and communicate with each other on the internet.

### Difference Between Public and Private IP Addresses

#### Private IP Address
- Used within local networks (LANs).
- Not accessible directly from the internet.
- Can be reused across different private networks.

#### Public IP Address
- Assigned by an Internet Service Provider (ISP).
- Globally unique and accessible over the internet.
- Used to identify a network externally.

![Ping Results](./screenshots/ping_results.png)

![Traceroute Results](./screenshots/traceroute_results.png)

---

## 🗺️ Part C: Basic Network Diagram

The diagram below illustrates how the local device communicates with external networks through a router and the internet.

```text
           [ Internet ]
                │
                ▼
      [ Router / Wi-Fi Access Point ]
                │
      (Gateway: 192.168.162.2)
                │
                ▼
         [ Kali Linux System ]
      IP Address: 192.168.162.128
      MAC Address: 00:0C:29:75:11:77
````
---

## 🧪 Part D: Network Connectivity Test

### Was the Ping Successful?

Yes. The ping test completed successfully with 0% packet loss, indicating that the device was able to communicate with Google's servers and that internet connectivity was functioning properly.

### How Many Hops Were Detected?

The traceroute successfully reached the destination and recorded a total of 30 hops along the route between the source and destination.

### What is the Purpose of Traceroute?

`traceroute` is a network diagnostic utility used to identify the path that packets take from a source device to a destination host. It displays each intermediate router (hop) and measures the response time at every stage, helping administrators troubleshoot routing issues, latency problems, and packet loss within a network.
