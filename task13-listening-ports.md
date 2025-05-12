# 📡 Task 13: Scan for Listening Ports & Associated Processes

## 📌 Objective
Use PowerShell to find all TCP ports that are currently listening for connections, and associate them with their owning processes. This is useful for detecting unauthorized services.

---

## 🧪 Commands

```powershell
Get-NetTCPConnection -State Listen | Select-Object LocalAddress, LocalPort, OwningProcess
