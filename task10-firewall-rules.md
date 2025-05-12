# 🔥 Task 10: Firewall Rules Check

## 📌 Objective
Use PowerShell to list all enabled firewall rules on the system. This helps security analysts ensure the system is not exposing unnecessary ports or services.

---

## 🧪 Command

```powershell
Get-NetFirewallRule | Where-Object {$_.Enabled -eq "True"} | Select-Object DisplayName, Direction, Action, Profile
