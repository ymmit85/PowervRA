![Build status](https://jakkulabs.visualstudio.com/_apis/public/build/definitions/b9938934-bc30-4bf9-8ee8-91138dde4db8/1/badge)

# Welcome to PowervRA
PowervRA is a PowerShell module built on top of the services exposed by the vRealize Automation 7 REST API.

Note: this module is not in any way developed or supported by anyone officially affiliated with VMware

## Compatibility

### vRealize Automation

|||||||
| --- | --- | --- | --- | --- | --- |
|6.2.4*|7.0|7.0.1|7.1|7.2|7.3|


* Support for 6.2.4 is limited given API restrictions. Functions which don't support 6.2.4 will exit early and cleanly.

### PowerShell Editions

|Edition|Version|
| --- | --- |
|Desktop|5.1|
|Core|6.0.0-rc**|

To get up and running with PowerShell Core follow the instructions for your operating system [here](https://github.com/PowerShell/PowerShell/blob/master/README.md#get-powershell).

## Download

PowerShell v5.1 & v6 users: You grab the latest version of the module from the PowerShell Gallery by running the following command:

```
Install-Module -Name PowervRA -Scope CurrentUser
```

## Quick Start

Once you have installed and imported PowervRA, use Connect-vRAServer to connect to your vRA instance:

```PowerShell
Connect-vRAServer -Server vra.corp.local -Tenant tenant01 -Credential (Get-Credential)
```

If your instance has a self signed certificate you must use the **IgnoreCertRequirements** switch:

```PowerShell
Connect-vRAServer -Server vra.corp.local -Tenant tenant01 -Credential (Get-Credential) -IgnoreCertRequirements
```

## Running Locally
When developing, use the provided build script and import the module that is inside the Release directory.

You **do not** have to manually edit src\PowervRA.psd1 when adding new functions

```PowerShell
# --- Run the build script
.\tools\build.ps1

# --- Import release module
Import-Module .\Release\PowervRA\PowervRA.psd1 -Force
```
The default build will run some quick tests to catch any errors before you push your changes.

## Documentation

Documentation for each command can be viewed with Get-Help, e.g.:

```
Get-Help Get-vRAEntitlement
```

Alternatively check out our [Read the Docs site](https://powervra.readthedocs.org/en/latest/)
