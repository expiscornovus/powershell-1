---
applicable: SharePoint Online
external help file: PnP.PowerShell.dll-Help.xml
Module Name: PnP.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnpapplicationcustomizer
schema: 2.0.0
title: Set-PnPApplicationCustomizer
---

# Set-PnPApplicationCustomizer

## SYNOPSIS
Updates a SharePoint Framework client side extension application customizer

## SYNTAX

### Custom Action Id
```
Set-PnPApplicationCustomizer [[-Identity] <UserCustomActionPipeBind>] [-Scope <CustomActionScope>]
 [-Title <String>] [-Description <String>] [-Sequence <Int32>] [-ClientSideComponentProperties <String>]
 [-Web <WebPipeBind>] [-Connection <PnPConnection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Client Side Component Id
```
Set-PnPApplicationCustomizer [-ClientSideComponentId <GuidPipeBind>] [-Scope <CustomActionScope>]
 [-Title <String>] [-Description <String>] [-Sequence <Int32>] [-ClientSideComponentProperties <String>]
 [-Web <WebPipeBind>] [-Connection <PnPConnection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Updates a SharePoint Framework client side extension application customizer by updating its custom action. Only the properties that will be provided will be updated. Others will remain as they are.

## EXAMPLES

### EXAMPLE 1
```powershell
Set-PnPApplicationCustomizer -Identity aa66f67e-46c0-4474-8a82-42bf467d07f2
```

Updates the custom action representing the client side extension registration with the id 'aa66f67e-46c0-4474-8a82-42bf467d07f2'.

### EXAMPLE 2
```powershell
Set-PnPApplicationCustomizer -ClientSideComponentId aa66f67e-46c0-4474-8a82-42bf467d07f2 -Scope web -ClientSideComponentProperties "{`"sourceTermSet`":`"PnP-CollabFooter-SharedLinks`",`"personalItemsStorageProperty`":`"PnP-CollabFooter-MyLinks`"}
```

Updates the custom action(s) properties being registered for a SharePoint Framework solution having the id 'aa66f67e-46c0-4474-8a82-42bf467d07f2' in its manifest from the current web.

## PARAMETERS

### -ClientSideComponentId
The Client Side Component Id of the SharePoint Framework client side extension application customizer found in the manifest for which existing custom action(s) should be updated

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: GuidPipeBind
Parameter Sets: Client Side Component Id
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientSideComponentProperties
The Client Side Component Properties of the application customizer to update. Specify values as a json string : "{Property1 : 'Value1', Property2: 'Value2'}". Omit to not update this property.

Only applicable to: SharePoint Online, SharePoint Server 2019

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

### -Connection
Optional connection to be used by the cmdlet. Retrieve the value for this parameter by either specifying -ReturnConnection on Connect-PnPOnline or by executing Get-PnPConnection.

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: PnPConnection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
The description of the application customizer. Omit to not update this property.

Only applicable to: SharePoint Online, SharePoint Server 2019

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

### -Identity
The id or name of the CustomAction representing the client side extension registration that needs to be updated or a CustomAction instance itself

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: UserCustomActionPipeBind
Parameter Sets: Custom Action Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Scope
Define if the CustomAction representing the client side extension registration is to be found at the web or site collection scope. Specify All to update the component on both web and site collection level.

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: CustomActionScope
Parameter Sets: (All)
Aliases:
Accepted values: Web, Site, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sequence
Sequence of this application customizer being injected. Use when you have a specific sequence with which to have multiple application customizers being added to the page. Omit to not update this property.

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The title of the application customizer. Omit to not update this property.

Only applicable to: SharePoint Online, SharePoint Server 2019

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

### -Web
This parameter allows you to optionally apply the cmdlet action to a subweb within the current web. In most situations this parameter is not required and you can connect to the subweb using Connect-PnPOnline instead. Specify the GUID, server relative url (i.e. /sites/team1) or web instance of the web to apply the command to. Omit this parameter to use the current web.

Only applicable to: SharePoint Online, SharePoint Server 2019

```yaml
Type: WebPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[SharePoint Developer Patterns and Practices](https://aka.ms/sppnp)