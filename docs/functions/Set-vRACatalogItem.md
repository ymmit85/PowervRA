# Set-vRACatalogItem

## SYNOPSIS
Update a vRA catalog item

## SYNTAX

### Standard (Default)
```
Set-vRACatalogItem -Id <String> [-Quota <Int32>] [-Service <String>] [-NewAndNoteworthy <Boolean>]
 [-IconId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStatus
```
Set-vRACatalogItem -Id <String> [-Status <String>] [-IconId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Update a vRA catalog item

## EXAMPLES

### EXAMPLE 1
```
Set-vRACatalogItem -Id dab4e578-57c5-4a30-b3b7-2a5cefa52e9e -Status PUBLISHED
```

### EXAMPLE 2
```
Set-vRACatalogItem -Id dab4e578-57c5-4a30-b3b7-2a5cefa52e9e -Quota 1
```

### EXAMPLE 3
```
Set-vRACatalogItem -Id dab4e578-57c5-4a30-b3b7-2a5cefa52e9e -Service "Default Service"
```

### EXAMPLE 4
```
Set-vRACatalogItem -Id dab4e578-57c5-4a30-b3b7-2a5cefa52e9e -NewAndNoteworthy $false
```

### EXAMPLE 5
```
Get-vRACatalogItem  -Name "Create cluster" | Set-vRACatalogItem -IconId "cafe_icon_CatalogItem01" -Confirm:$false
```

TODO:
- Investigate / fix authorization error

## PARAMETERS

### -Id
The id of the catalog item

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Status
The status of the catalog item (e.g.
PUBLISHED, RETIRED, STAGING)

```yaml
Type: String
Parameter Sets: SetStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Quota
The Quota of the catalog item

```yaml
Type: Int32
Parameter Sets: Standard
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
The Service to assign the catalog item to

```yaml
Type: String
Parameter Sets: Standard
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewAndNoteworthy
Mark the catalog item as New and noteworthy in the UI

```yaml
Type: Boolean
Parameter Sets: Standard
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IconId
The Icon Id of the catalog item.
This must already exist in the Service Catalog.
Typically it would have already been created via Import-vRAServiceIcon

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Int
System.String
System.Bool

## OUTPUTS

### System.Management.Automation.PSObject

## NOTES

## RELATED LINKS
