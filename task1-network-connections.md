# 🛰️ Task 1: View Active Network Connections

## 📌 Objective
Use PowerShell to identify all active TCP connections on the system, including local and remote addresses, port numbers, state, and owning process. This helps detect suspicious activity or monitor legitimate network usage.

---

## 🧪 Command
```powershell
Get-NetTCPConnection | 
    Select-Object LocalAddress, LocalPort, RemoteAddress, RemotePort, State, OwningProcess | 
    Format-Table -AutoSize
