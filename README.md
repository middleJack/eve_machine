# eve_machine
Windows 10 setup to just run EvE online


# Removing Cortana
1. Powershell
2. Run:
`Get-AppxPackage -AllUsers | where-object {$_.name –notlike "*store*"} | Remove-AppxPackage
Get-appxprovisionedpackage –online | where-object {$_.packagename –notlike "*store*"} | Remove-AppxProvisionedPackage -online`

# Disabling Windows Defender (the antimalware that hogs CPU)
1. WIN key + R -> `regedit`
2. HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender
3. New `DWORD (32-bit) Value` called `DisableAntiSpyware`
4. Double click and set it to 1
5. Restart.
