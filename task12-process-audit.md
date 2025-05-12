# 🧠 Task 12: Running Process Audit

## 📌 Objective
Use PowerShell to audit running processes, including their name, ID, and executable path. This helps in identifying suspicious or unknown applications running on the system.

---

## 🧪 Command

```powershell
Get-Process | ForEach-Object {
    try {
        $_ | Select-Object Name, Id, Path
    } Catch {
        $_ | Select-Object Name, Id
    }
}
