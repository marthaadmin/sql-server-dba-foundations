# GCP Project and VM Setup

This document explains how the SQL Server DBA lab environment was created using Google Cloud Platform (GCP).

The goal was to build a realistic lab that mirrors how companies provision servers for SQL Server workloads.

---

## Google Cloud Project Setup

Steps taken:

1. Created a Google Cloud account and activated the free credit.
2. Created a new GCP project named **MyLab**.
3. Enabled Compute Engine services.

This project is used exclusively for DBA learning and practice.

---

## Virtual Machine Design

Three Windows Server virtual machines were created in the same zone and network:

| Server Name | Purpose |
|------------|--------|
| SQLAD | Active Directory Domain Controller |
| SQL01 | SQL Server (Domain-joined) |
| SQL02 | SQL Server (Domain-joined) |

Keeping all servers in the same zone reduces latency and simplifies networking.

---

## IP Address Configuration

Each server was configured with:
- Static **internal IP** (for server-to-server communication)
- Static **external IP** (for RDP access)

Static IPs ensure:
- Predictable connectivity
- Easier troubleshooting
- Realistic enterprise behavior

---

## Remote Access

Remote Desktop Protocol (RDP) is used to connect to each Windows server.

RDP allows:
- Server configuration
- Software installation
- Administrative management

Credentials were documented during setup to avoid access issues later.

---

## Key Takeaways

- Cloud labs can closely replicate real enterprise environments.
- Proper naming and IP planning simplify SQL Server administration.
- Infrastructure setup is the foundation of all DBA work.
