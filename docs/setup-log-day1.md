# Setup Log - Day 1
Date: 15-02-2026

## Hyper-V
- Already enabled on Windows 11 Pro (no restart needed)
- Command: Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
- Result: Online: True, RestartNeeded: False

## Virtual Switch - SOC-Lab-Network
- Type: Internal
- Created successfully via New-VMSwitch -Name "SOC-Lab-Network" -SwitchType Internal
- Issue: Could not assign static IP 192.168.56.1 to the switch
- Windows returned "The object already exists" on every attempt
- Interface kept showing APIPA address (169.254.x.x) instead
- Methods tried: New-NetIPAddress, netsh set, netsh add, Remove + Recreate
- Resolution: Pending - will retry with clean setup

## Folders Created
- C:\SOC-Lab\ISOs\
- C:\SOC-Lab\VMs\
- C:\SOC-Lab\docs\
