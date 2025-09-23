# System Engineering & DevOps

This repository contains resources and projects related to system engineering and DevOps practices. Below are key concepts and explanations for various infrastructure topics.

## Table of Contents
1. [Network Basics](#network-basics)
2. [Server](#server)
3. [Web Server](#web-server)
4. [DNS (Domain Name System)](#dns)
5. [Load Balancer](#load-balancer)
6. [Monitoring](#monitoring)
7. [Database](#database)
8. [Web Server vs Application Server](#web-server-vs-application-server)
9. [DNS Record Types](#dns-record-types)
10. [Single Point of Failure](#single-point-of-failure)
11. [Zero Downtime Deployment](#zero-downtime-deployment)
12. [High Availability Clusters](#high-availability-clusters)
13. [HTTPS](#https)
14. [Firewall](#firewall)

## Network Basics
Networking fundamentals form the backbone of system infrastructure:
- **IP Addressing**: Unique identifiers for devices on a network (IPv4/IPv6)
- **Protocols**: Rules for communication (TCP, UDP, HTTP, etc.)
- **OSI Model**: 7-layer model for network communication
- **Subnetting**: Dividing networks into smaller, manageable sub-networks
- **Ports & Sockets**: Endpoints for communication between applications

## Server
A server is a computer or system that provides resources, data, services, or programs to other computers (clients) over a network.

**Key Aspects:**
- **Types**: Web servers, database servers, file servers, etc.
- **Hardware**: Optimized for reliability and performance
- **Operating Systems**: Linux, Windows Server, etc.
- **Virtualization**: Running multiple virtual servers on physical hardware

## Web Server
A web server is software that serves web content to clients over HTTP/HTTPS.

**Key Functions:**
- Handles HTTP requests (GET, POST, etc.)
- Serves static content (HTML, CSS, JS, images)
- May include security features (SSL/TLS termination)
- Examples: Nginx, Apache, Microsoft IIS

## DNS (Domain Name System)
DNS translates human-readable domain names to IP addresses.

**How it works:**
1. User enters a URL
2. Browser queries DNS resolver
3. Resolver contacts root nameservers
4. Request is directed to TLD nameservers
5. Authoritative nameserver provides IP address
6. Browser connects to the IP address

## Load Balancer
Distributes network or application traffic across multiple servers to improve responsiveness and availability.

**Types:**
- **Layer 4 (Transport)**: Routes based on TCP/UDP data
- **Layer 7 (Application)**: Routes based on HTTP headers
- **Hardware**: Dedicated load balancing devices
- **Software**: Nginx, HAProxy, AWS ELB

## Monitoring
Continuous observation of system metrics to ensure optimal performance and availability.

**Key Components:**
- **Metrics Collection**: CPU, memory, disk I/O, network
- **Alerting**: Notifications for abnormal conditions
- **Logging**: Storing system/application logs
- **Tracing**: Following requests through distributed systems
- **Tools**: Prometheus, Grafana, ELK Stack, Datadog

## Database
A structured collection of data that can be easily accessed, managed, and updated.

**Types:**
- **Relational (SQL)**: MySQL, PostgreSQL, Oracle
- **NoSQL**: MongoDB, Cassandra, Redis
- **NewSQL**: CockroachDB, Google Spanner

## Web Server vs Application Server

| Feature          | Web Server                | Application Server         |
|------------------|---------------------------|----------------------------|
| Primary Role     | Serves static content     | Executes application logic |
| Processing       | Limited processing        | Business logic processing  |
| Examples        | Nginx, Apache            | Node.js, Tomcat, JBoss     |
| Use Case        | Simple websites           | Complex web applications   |

## DNS Record Types

| Type  | Purpose                          | Example                     |
|-------|----------------------------------|-----------------------------|
| A     | Maps hostname to IPv4 address    | example.com → 93.184.216.34 |
| AAAA  | Maps hostname to IPv6 address    | example.com → 2606:2800:220:1::248 |
| CNAME | Alias of one name to another     | www → example.com           |
| MX    | Mail server for the domain       | mail.example.com            |
| TXT   | Text information for verification | "v=spf1 include:_spf.google.com ~all" |
| NS    | Authoritative nameserver         | ns1.example.com             |
| SOA   | Start of Authority record        | Contains admin and zone info |

## Single Point of Failure
A component whose failure would stop the entire system from functioning.

**Examples:**
- A single database server
- One network switch
- A single power supply

**Mitigation Strategies:**
- Redundancy at all levels
- Load balancing
- Failover mechanisms
- Regular backups

## Zero Downtime Deployment
Techniques to update applications without service interruption.

**Strategies:**
1. **Blue-Green Deployment**: Maintain two identical environments, switch traffic after update
2. **Canary Releases**: Gradually roll out changes to a small user base
3. **Rolling Updates**: Update instances one by one
4. **Feature Flags**: Enable/disable features without deployment

## High Availability Clusters
Groups of servers that work together to ensure continuous service.

**Types:**
- **Active-Active**: All nodes handle traffic
- **Active-Passive**: Backup nodes take over if primary fails

**Benefits:**
- Increased reliability
- Load distribution
- Automatic failover

## HTTPS
Secure version of HTTP that uses encryption (TLS/SSL) to protect data in transit.

**Key Aspects:**
- Encrypts data between client and server
- Uses port 443 by default
- Requires SSL/TLS certificate
- Improves SEO rankings
- Prevents man-in-the-middle attacks

## Firewall
Network security system that monitors and controls incoming and outgoing network traffic.

**Types:**
- **Network Firewall**: Filters traffic between networks
- **Host-based Firewall**: Protects individual devices
- **Web Application Firewall (WAF)**: Protects web applications

**Functions:**
- Packet filtering
- Stateful inspection
- Proxy service
- Network Address Translation (NAT)
- VPN support