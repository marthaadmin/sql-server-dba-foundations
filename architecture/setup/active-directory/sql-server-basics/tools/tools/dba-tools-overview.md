# DBA Tools Overview

This document explains the core tools used to manage and troubleshoot SQL Server
in the DBA foundations lab.

---

## Remote Desktop Protocol (RDP)

RDP is used to remotely access Windows servers.

In this lab:
- RDP is used to connect to SQLAD, SQL01, and SQL02
- It allows full control of the server desktop
- DBAs use RDP to install software, check services, and troubleshoot issues

If a server cannot be accessed via RDP, the DBA cannot manage SQL Server on that machine.

---

## SQL Server Configuration Manager

SQL Server Configuration Manager is used to manage SQL Server services
and network configuration.

Key uses:
- Start and stop SQL Server services
- Enable or disable TCP/IP
- Configure SQL Server ports
- Troubleshoot connectivity issues

This is the first tool checked when:
- SQL Server is not running
- Clients cannot connect
- Ports or protocols may be misconfigured

---

## SQL Server Management Studio (SSMS)

SSMS is the primary interface used to connect to and manage SQL Server.

DBAs use SSMS to:
- Connect to SQL Server instances
- Run SQL queries
- Create and manage databases
- Manage logins, users, and permissions
- Monitor performance and activity

SSMS does not run SQL Server itself.
It connects to the SQL Server Database Engine.

---

## How These Tools Work Together

Typical DBA workflow:
1. Use RDP to access the server
2. Use Configuration Manager to verify SQL services and network settings
3. Use SSMS to connect to SQL Server and manage databases

Understanding when to use each tool is critical for effective troubleshooting.
