# Version 3.6.0
## Features
* Feature - New function Import-vRAContentData (#197) (@kclinden)
* Feature - New functions New-vRAPropertyGroup, Get-vRAPropertyGroup and Remove-vRAPropertyGroup (#198) (@Stevio54)

# Version 3.5.0
## Features
* Feature - New functions Add-vRACustomForm, Get-vRACustomForm, Set-vRACustomForm and Remove-vRACustomForm (#190) (@kclinden)

# Version 3.4.0
## Features
* Feature - New function Invoke-vRATenantDirectorySync and added allusers parameter to Set-vRAEntitlement (#187) (@basvinken)

## Fixes
* Fixed #188 - Set-vRAReservation not working correct for Type 'vSphere (vCenter)'
* Fixed #189 - error code 90135 Unable to authenticate user `<domain>\\<username>` in tenant `<tenant>`

# Version 3.3.0
## Features
* Feature - New-vRABusinessGroup does not support SharedAccess User role (#183) (@thecloudxpert)

## Fixes
* Fixed #180 - Set-vRAEntitlement assumes EntitledCatalogItems (@feardamhan)

# Version 3.2.0
## Features
* Feature - New parameter ExtendedProperties and pipeline support for Get-vRABlueprint

## Fixes
* Fixed #102 - Get-vRABlueprint is using the wrong API endpoint
* Fixed #178 - Get-vRABlueprint is not using the Limit parameter

# Version 3.1.1
## Features
* Feature - Get-vRAResource enhancements (#171) (@BlackCatDeployment)

## Fixes
* Fixed #173 - Consider using Module Tags in addition to PSEditions
* Fixed #175 - Use ConvertTo-Json in Connect-vRAServer (@mponton)

# Version 3.1.0
## Features
* Feature - New function Remove-vRAReservationStorage (#157) (@skunkie)
* Feature - New function Get-vRARequestDetail (#167) (@otabut)
* Feature - Listed as PS Core compatible module in PS Gallery
* Feature - Supported on vRA 7.2 and 7.3

## Fixes
* Fixed #168 - Get-vRATenantDirectory does not support multiple directories in the API response

# Version 3.0.0
## Breaking Changes
**WARNING: This release contains breaking changes**
* The minmum supported PowerShell Versions have been raised to the following:
  * Windows PowerShell: 5.1
  * PowerShell Core: 6.0.0-rc**

## Features
* Feature - Add ability to select SSL Protocol (#159)
* Feature - Single PSM1 file to speed up load times
* Feature - Add -Wait Parameter to Request-vRAResourceAction (@Thitho007)

## Fixes
* Fixed #134 - Issue with double quotes in some functions
* Fixed #135 - Some private functions are being exported
* Fixed #137 - Help examples for Get-vRAResource are incorrect
* Fixed #148 - Request-vRAResourceAction Example Correction
* Fixed #149 - Support Reservation Type change from 'vSphere' to 'vSphere (vCenter)' in vRA 7.3
* Fixed #151 - Get-vRAReservationPolicy
* Fixed #153 - New-vRAReserveration Error
* Fixed #130 - Unable to connect after removing SSLv3/TLSv1 ciphers from vRA Appliance

# Version 2.2.0

## Features
* Feature - Remove Network Path from reservation #43
* Feature - Add -Debug capability for New / Set functions #78
* Feature - Add function to retrieve the groups that a user is a member of #81
* Feature - Add function to retrieve source-machines #123
* Feature - Add function to invoke data collection #127

## Fixes
* Fixed #124 - xRequires does not work as expected when executed in a Begin block


# Version 2.1.0

## Breaking changes
* Functions that take a Password parameter now require a SecureString #106
  * **Connect-vRAServer** - Now requires a **SecureString** for the Password parameter if you are using a Username/Password combination

## Features
* Feature - Properties-service support #119 - Thanks to @sammcgeown
  * Get-vRAPropertyDefinition, New-vRAPropertyDefinition, Remove-vRAPropertyDefinition
* Feature - Support for updating icons (including the all services icon) #117 / #37:
  * Import-vRAIcon, Export-vRAIcon, Get-vRAIcon, Remove-vRAIcon, New-vRAService, Set-vRACatalogItem, Set-vRAService

## Fixes
* Fixed #68 - Set-vRAUserPrincipal Id parameter now has an alias of PrincipalId
* Fixed #76 - Add support for LocalScopeForActions to Set-vRAEntitlement/New-vRAEntitlement
* Fixed #77 - Actions are not applied when creating a new entitlement with New-vRAEntitlement
* Fixed #105 - Fix functions using String type for Password parameters
* Fixed #110 - Issue with "Get-vRAReservationComputeResource -Type vSphere
* Fixed #111 - Build | PSAvoidUsingPlainTextForPassword | Set-vRAUserPrincipal
* Fixed #112 - Build | PSUseDeclaredVarsMoreThanAssignments| Set-vRATenantDirectory
* Fixed #113 - Build | PSUseDeclaredVarsMoreThanAssignments | New-vRATenantDirectory
* Fixed #114 - Build | PSAvoidUsingPlainTextForPassword | New-vRAUserPrincipal
* Fixed #115 - Build | PSPossibleIncorrectComparisonWithNull | Invoke-vRARestMethod
* Fixed #116 - Build | PSPossibleIncorrectComparisonWithNull | Connect-vRAServer
* Fixed #120 - Clean up issues from Properties Service PR
* Fixed #121 - Get-vRABusinessGroupName filter by Name fails on special characters

## Other fixes and improvements
* Introduces stricter checks in our CI process. The analyze task will now fail on warnings
* Introduces Pester tests for function help
  * All functions are now required to have at least a synopsis, description, one or more example section(s) and every parameter must have a description.
* Lots of other fun improvements to our CI and build process - See [here for more information](http://powervra.readthedocs.io/en/latest/build/)


## Version 2.0.0

* PowerShell Core v6.0.0-alpha.14 Support
* Module restructured to use ps1 files for functions instead of psm1 files
* Private functions are now actually private
* Public functions restructured in to endpoint folders
* Removed depricated functions: Export-vRAContentPackage, Get-vRAContentPackage, Import-vRAContentPackage, Remove-vRAContentPackage,
  Test-vRAContentPackage, Get-vRAConsumerCatalogItem, Get-vRAConsumerCatalogItemRequestTemplate, Get-vRAConsumerEntitledCatalogItem,
  Get-vRAConsumerRequest, Get-vRAConsumerResource, Get-vRAConsumerResourceOperation, Get-vRAConsumerResourceType, Get-vRAConsumerService
  Request-vRAConsumerCatalogItem
* Updated README.md to include more information regarting Core Support
* Introduction of CHANGELOG.md
* Pester Test improvements
* Build improvementss
* Bugfixes and improvements

