# 👥 Task 8: Check for Startup Programs

## 📌 Objective
Use PowerShell to check for programs set to run at system startup. This helps identify any potentially malicious or unnecessary programs that could be slowing down the system.

---

## 🧪 Command
```powershell
Get-CimInstance -ClassName Win32_StartupCommand | Select-Object Name, Command, Location
