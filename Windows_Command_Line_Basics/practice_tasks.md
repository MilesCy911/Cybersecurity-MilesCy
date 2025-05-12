# Command Line Practice Tasks

These tasks simulate how cybersecurity professionals use Windows CMD and PowerShell for investigation and monitoring.

---

## 🔍 Task 1: View Active Network Connections

**Command:**
```powershell
Get-NetTCPConnection | Select-Object LocalAddress, LocalPort, RemoteAddress, RemotePort, State, OwningProcess

---

## 👥 Task 2: **Check Logged-In Users**

**Command:**
```powershell
Get-WmiObject -Class Win32_ComputerSystem

---

## 👥 Task 3: **List Running Process**

tasklist

---

## 👥 Task 4: **Check for Open Ports**

netstat -an | findstr LISTEN

---

## 👥 Task 5: **Review Event Logs for Suspicious Activity**

eventvwr.msc

---

## 👥 Task 6: **Investigate Suspicious Processes**

get-process

---

## 👥 Task 7: **Use OSINT to Investigate IP Addresses**

nslookup <IP_address>

--

## 👥 Task 8: **Check for Startup Programs**

Get-CimInstance -ClassName Win32_StartupCommand | Select-Object Name, Command, Location

--

## 👥 Task 9: **User Account & Privileges Audit**

Get-LocalUser | Select-Object Name, Enabled, LastLogon

Get-LocalGroupMember -Group "Administrators"

---

## 👥 Task 10: **Firewall Rules Check**

Get-NetFirewallRule | Where-Object {$_.Enabled -eq "True"} | Select-Object DisplayName, Direction, Action, Profile

---

## 👥 Task 11: **Detect Hidden Files**

Get-ChildItem -Path C:\ -Recurse -Force -ErrorAction SilentlyContinue | Where-Object { $_.Attributes -match "Hidden" } | Select-Object FullName, Attributes

---

## 👥 Task 12: **Running Process Audit**

Get-Process | ForEach-Object {
    try {
        $_ | Select-Object Name, Id, Path
    } Catch {
        $_ | Select-Object Name, Id
    }
}

---

## 👥 Task 13: **Scan for Listening Ports & Associated Processes**

Get-NetTCPConnection -State Listen | Select-Object LocalAddress, LocalPort, OwningProcess

Get-Process -Id 1344

---

## 👥 Task 14: **DNS Cache Review**

Get-DnsClientCache













