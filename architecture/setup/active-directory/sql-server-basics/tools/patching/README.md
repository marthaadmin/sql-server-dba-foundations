# SQL Server Patching

## What is SQL Server patching?
SQL Server patching is the process of applying Microsoft updates, such as Cumulative Updates (CUs) and security fixes, to an existing SQL Server instance.

The purpose of patching is to fix security vulnerabilities, resolve bugs, and improve performance without changing the SQL Server version.

Example:
- SQL Server 2022 CU9 → CU10 = patching  
- SQL Server 2019 → SQL Server 2022 = upgrade (not patching)

---

## Pre-Patch Checks
Before applying any SQL Server patch, I verify the following:

- Confirm the environment (Production or Non-Production)
- RDP into the server to ensure it is online
- Confirm SQL Server services are running
- Check TCP/IP is enabled and confirm the port number using SQL Server Configuration Manager
- Check the current SQL Server version and build number

---

## What Happens During Patching
During SQL Server patching:

- SQL Server services stop
- Patch updates SQL Server binaries and components
- SQL Server services restart
- Databases come back online

Downtime is expected during this process.

---

## Post-Patch Validation
After patching, I validate the following:

- SQL Server service restarted successfully
- SQL Server Agent is running
- SSMS connectivity works
- TCP/IP and port configuration remain unchanged
- Applications can reconnect to SQL Server

To confirm the patch level, I run:


SELECT  
    @@VERSION AS SQLVersion,
    SERVERPROPERTY('ProductVersion') AS ProductVersion,
    SERVERPROPERTY('ProductLevel') AS ProductLevel,
    SERVERPROPERTY('Edition') AS Edition;
This confirms the patch was applied successfully and the build number changed.
Common Patching Issues & Troubleshooting

SQL Server service does not start → Check SQL Server Configuration Manager

Users cannot connect → Verify TCP/IP, port number, and firewall rules

Named instance connectivity issues → Check SQL Server Browser service


---

### Next step (don’t skip this)
Commit this file with a message like:
> `Added SQL Server patching documentation`

Once committed, tell me **“README committed”** and we’ll move to screenshots.
