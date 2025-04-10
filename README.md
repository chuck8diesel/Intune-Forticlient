# FortiClient VPN Deployment (PSAppDeployToolkit)

This project provides a fully functional PowerShell-based deployment script using the PSAppDeployToolkit framework for FortiClient VPN (version 7.4.3.1790).

## Features

- Silent installation via MSI
- Optional configuration import via `FCConfig.exe`
- Robust uninstallation (via MSI GUID or `uninst.exe`)
- Repair mode support
- Intune-ready with support for return codes (3010, 1641, etc.)
- Logging and error handling via PSADT

## Usage

Deploy with Microsoft Intune or ConfigMgr using the following command lines:

### Install & Uninstall
```powershell
Deploy-Application.exe -DeploymentType "Install" -DeployMode "Silent" -AllowRebootPassThru


Deploy-Application.exe -DeploymentType "Uninstall" -DeployMode "Silent"
