# SQL Server Foundations

This document covers core SQL Server concepts learned in Class 1–4.
These concepts form the foundation of all SQL Server administration work.

---

## What is SQL Server?

Microsoft SQL Server is a relational database management system (RDBMS).

In simple terms:
- SQL Server is where databases live
- It stores data for applications and users
- Data is accessed using SQL (Structured Query Language)

---

## SQL Server Version vs Edition

Understanding the difference between version and edition is critical.

### Version
- Refers to when SQL Server was released
- Examples: 2014, 2019, 2022, 2025
- Newer versions include performance, security, and feature improvements

### Edition
- Determines features, limits, and licensing
- Common editions:
  - Enterprise
  - Standard
  - Developer
  - Express

**Developer Edition**:
- Free
- Same features as Enterprise
- Used for learning and non-production environments only

---

## Production vs Non-Production Environments

### Production
- Live environment used by customers or business users
- Downtime directly impacts the business
- Changes must be carefully planned and tested

### Non-Production
- Used for learning, testing, and patching
- Safe place to practice and validate changes
- No impact on real users

---

## SQL Server Instances

An instance is an installation of SQL Server.

### Default Instance
- Only one per server
- Uses the server name to connect
- Default port: 1433

Example:

### Named Instance
- Multiple named instances can exist on one server
- Uses ServerName\InstanceName
- Often uses custom or dynamic ports

Example:

---

## Ports and Connectivity

Ports control how SQL Server accepts network connections.

Key points:
- Default instance uses port 1433
- Named instances may use dynamic or static ports
- Static ports are easier to manage and troubleshoot

Example connections:

---

## Why This Matters for a DBA

These concepts help DBAs:
- Troubleshoot connection issues
- Choose the correct SQL Server edition
- Separate production from non-production workloads
- Design scalable and secure environments
