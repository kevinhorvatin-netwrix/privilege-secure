## Disable Terminal Service / RDP

Disables the Terminal Service and RDP Service.
Sets the registry keys to disable terminal services.
Optionally disables Firewall.

Use this custom action to completely disable RDP/Terminal Services instead of the `Disable RDP` action that ships with Netwrix Privilege Secure.

**NOTE** This should be be used with Remote Desktop Services servers or Citrix Servers as shutting down the TermService service may disrupt services for all servers hosted by that server.

## To install

1. Download the Zip file to your NPS server.
2. Unzip the file.
3. Start PowerShell as Administrator.
4. CD to the directory you unzipped to.
5. Run `Install-Addon.ps1`
