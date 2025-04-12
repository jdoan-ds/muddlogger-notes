---

## 💻 3. `powershell_cheat_sheet.md`

```markdown
# 🖥 PowerShell Cheat Sheet

Useful commands and scripting patterns for Windows PowerShell.

---

## 📁 Navigation

```powershell
Get-Location             # current directory
Set-Location path        # cd into folder
Get-ChildItem            # list files (like ls)
```

---

## 📄 File Commands

```powershell
New-Item -Path . -Name "file.txt" -ItemType "File"
Remove-Item file.txt
Rename-Item file.txt newname.txt
Copy-Item file.txt backup.txt
```

---

## 📦 Install Packages (Winget)

```powershell
winget install Notepad++
```

Or use choco if Chocolatey is installed.

---

## 🔧 Admin Tasks

```powershell
Start-Process powershell -Verb runAs     # launch admin shell
```

---

## 🔍 Searching

```powershell
Select-String -Path file.txt -Pattern "keyword"
```

---

## 🧪 Scripts

```powershell
# HelloWorld.ps1
Write-Output "Hello, PowerShell!"
```

Run with:

```powershell
.\HelloWorld.ps1
```

---

## 🧠 Tips

- Use Get-Help for documentation
- PowerShell uses Cmdlets (Verb-Noun syntax)
- Pipes and filters are powerful: |, Where-Object, Select-Object

----