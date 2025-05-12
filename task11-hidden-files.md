# 🕵️ Task 11: Detect Hidden Files

## 📌 Objective
Use PowerShell to recursively scan directories for hidden files. This is useful for uncovering files that may have been deliberately concealed by malicious software.

---

## 🧪 Command

```powershell
Get-ChildItem -Path C:\ -Recurse -Force -ErrorAction SilentlyContinue | 
    Where-Object { $_.Attributes -match "Hidden" } | 
    Select-Object FullName, Attributes
