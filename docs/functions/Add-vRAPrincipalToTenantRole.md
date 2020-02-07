# Add-vRAPrincipalToTenantRole

## SYNOPSIS
Add a vRA Principal to a Tenant Role

## SYNTAX

```
Add-vRAPrincipalToTenantRole [-TenantId] <String> [-PrincipalId] <String[]> [-RoleId] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Add a vRA Principal to a Tenant Role

## EXAMPLES

### EXAMPLE 1
```
Add-vRAPrincipalToTenantRole -TenantId Tenant01 -PrincipalId Tenantadmin@vrademo.local -RoleId CSP_TENANT_ADMIN
```

### EXAMPLE 2
```
Get-vRAUserPrincipal -UserName Tenantadmin@vrademo.local | Add-vRAPrincipalToTenantRole -TenantId Tenant01 -RoleId CSP_TENANT_ADMIN
```

## PARAMETERS

### -TenantId
Specify the Tenant Id

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrincipalId
Specify the Principal Id

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -RoleId
Specify the Role Id

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### System.String

## OUTPUTS

### System.Management.Automation.PSObject.

## NOTES

## RELATED LINKS
