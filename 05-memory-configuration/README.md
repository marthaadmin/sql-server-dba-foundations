# SQL Server Memory Configuration

## Why This Matters
SQL Server uses memory aggressively by default.
If not configured, it can consume all server memory and starve the operating system.

Configuring memory is a core DBA responsibility.

---

## Where This Is Configured
Memory is configured at the **server level** in SQL Server Management Studio (SSMS):

Server name → Right-click → Properties → Memory

---

## Lab Environment
- Platform: GCP
- Server: SQL01 / SQL02
- Total Memory: 8 GB (8188 MB)

---

## Memory Configuration Used

### Maximum Server Memory
Best practice is to allocate about 80% of server memory to SQL Server.

Calculation:
- 80% × 8188 MB ≈ 6550 MB

Configured Value:
- Max Server Memory = **6550 MB**

---

### Minimum Server Memory
Minimum memory prevents SQL Server from shrinking memory too aggressively.

Calculation:
- 30% × 8188 MB ≈ 2456 MB

Configured Value:
- Min Server Memory = **2456 MB**

---

## Common Misconfiguration Scenarios

### Max Memory Not Set
- SQL Server consumes all memory
- OS becomes unstable
- RDP and SSMS become slow

### Max Memory Too Low
- Poor query performance
- Constant cache flushing

### No Min Memory
- Memory fluctuates
- Inconsistent performance

---

## DBA Takeaway
Most performance issues blamed on queries often start with memory misconfiguration.
Correct memory settings prevent many production outages.
