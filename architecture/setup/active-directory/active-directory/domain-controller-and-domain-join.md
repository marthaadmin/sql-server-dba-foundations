# Active Directory Domain Controller and Domain Join

This document explains how Active Directory was configured for the SQL Server DBA lab
and how SQL servers were joined to the domain.

Active Directory is used in real environments to centrally manage users, authentication,
and access across servers.

---

## Domain Controller Setup (SQLAD)

The server **SQLAD** was configured as the Active Directory Domain Controller.

High-level steps:

1. Installed Active Directory Domain Services (AD DS).
2. Promoted SQLAD to a Domain Controller.
3. Created a new domain for the lab environment.
4. Verified DNS services were running.

Once completed, SQLAD became the central authority for authentication.

---

## Domain Users and Credentials

Domain user accounts were created in Active Directory to simulate real enterprise users.

Example:
- `tekypro\martha.admin`

Using domain accounts allows:
- Centralized password management
- Consistent login across servers
- Easier access control for SQL Server

---

## Joining SQL Servers to the Domain

Both SQL Server machines were joined to the domain:

- **SQL01**
- **SQL02**

Steps performed on each SQL Server:

1. Updated network settings to point DNS to SQLAD.
2. Joined the server to the domain.
3. Restarted the server.
4. Logged in using domain credentials.

After joining the domain, SQL01 and SQL02 trusted SQLAD for authentication.

---

## Why This Matters for a DBA

Active Directory integration allows DBAs to:
- Use Windows Authentication for SQL Server
- Assign permissions using domain users or groups
- Follow enterprise security best practices

This setup closely reflects how SQL Server is managed in production environments.
