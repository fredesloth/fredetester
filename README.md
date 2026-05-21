# PC_Tester_Beta
A running developed PC tester for quickly test basic function of a PC

# Link to tester: 
[Hardware Tester](https://fredesloth.github.io/fredetester/hardware-test)

# Windows CMD

## CMD/PowerShell Commands

### Get serial number

#### WMIC
`wmic bios get serialnumber`

####
`get-ciminstance win32_bios | select SerialNumber`

### Get Battery Health
`powercfg /batteryreport`

## Placering af dump logs
**Memory dumps - mini dumps:** `C:\Windows\Minidump`

**Full dumps:** `C:\Windows\MEMORY.DMP `

## Check disk
- Runs in read-only mode, checking the disk without repairing errors.
	- `chkdsk`
- Fixes errors on the disk. The drive must be locked.
	- `chkdsk /f`
- Locates bad sectors and recovers readable information (implies `/f`).
	- `chkdsk /r`
- Forces the volume to dismount first if necessary (often used with `/f`).
	- `chkdsk /x`
- Comprehensive scan to fix file system errors, locate bad sectors, and dismount the drive.
	- `chkdsk /f /r /x`

# Brave debloater 
`iwr "https://raw.githubusercontent.com/ltx0101/SlimBrave/main/SlimBrave.ps1" -OutFile "SlimBrave.ps1"; .\SlimBrave.ps1`

Read more: https://github.com/ltx0101/SlimBrave
