# PC_Tester_Beta
A running developed PC tester for quickly test basic function of a PC

# Link to tester: 
[Hardware Tester](https://fredesloth.github.io/fredetester/hardware-test)

# Windows CMD

## CMD/PowerShell Commands

### Serienummer
```bash
wmic bios get serialnumber
```


#### Nyere windows uden WMIC
```bash
get-ciminstance win32_bios | select SerialNumber
```


### Batteri Rapport
```bash
powercfg /batteryreport
```

### WiFi
```bash
netsh wlan show interfaces
```

## Placering af dump logs
**Memory dumps - mini dumps:** 
```
C:\Windows\Minidump
```


**Full dumps:** `
```
C:\Windows\MEMORY.DMP 
```
`

## Check disk
- Runs in read-only mode, checking the disk without repairing errors.
```bash
chkdsk
```

- Fixes errors on the disk. The drive must be locked.
```bash
chkdsk /f
```

- Locates bad sectors and recovers readable information (implies `/f`).
```bash
chkdsk /r
```

- Forces the volume to dismount first if necessary (often used with `/f`).
```bash
chkdsk /x
```

- Comprehensive scan to fix file system errors, locate bad sectors, and dismount the drive.
```bash
chkdsk /f /r /x
```


# Tools & Programs
## Brave debloater
```bash
iwr "https://raw.githubusercontent.com/ltx0101/SlimBrave/main/SlimBrave.ps1" -OutFile "SlimBrave.ps1"; .\SlimBrave.ps1
```
Read more: https://github.com/ltx0101/SlimBrave

## Chris Titus - WinUtil
Run in an elevated PowerShell (Run as Administrator):
```bash
irm christitus.com/win | iex
```
