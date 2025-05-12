# 👥 Task 2: Check Logged-In Users

## 📌 Objective
Use PowerShell to find out which users are currently logged into the system. This is essential for monitoring system activity and detecting unauthorized access.

---

## 🧪 Command
```powershell
Get-WmiObject -Class Win32_ComputerSystem
