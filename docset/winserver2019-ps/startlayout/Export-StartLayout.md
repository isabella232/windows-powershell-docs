---
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.Windows.StartLayout.Commands.dll-Help.xml
Module Name: StartLayout
ms.date: 12/20/2016
online version: https://docs.microsoft.com/powershell/module/startlayout/export-startlayout?view=windowsserver2019-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Export-StartLayout
---

# Export-StartLayout

## SYNOPSIS
Exports the layout of the Start screen.

## SYNTAX

### Non-literal
```
Export-StartLayout [-Path] <String> [-UseDesktopApplicationID] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Literal
```
Export-StartLayout -LiteralPath <String> [-UseDesktopApplicationID] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### For Windows 11 Start menu
```
Export-StartLayout -Path <String>
```

## DESCRIPTION
The **Export-StartLayout** cmdlet exports the layout of the tiles on Start of the current user.
You can export layout and use Import-StartLayout as well as other management policies for the Start layout.
Specify the .xml file name extension in the name of the file.

## EXAMPLES

### Example 1: Export the layout
```
PS C:\> Export-StartLayout -Path "C:\Layouts\Marketing.xml"
```

This command exports the layout of the tiles on Start to a file named Marketing.xml in the C:\Layouts folder.

### Example 2: Export the layout of the Windows 11 Start menu
```
PS C:\> Export-StartLayout -Path "C:\Layouts\Marketing.json"
```

This command exports the layout of the tiles on the Windows 11 Start menu to a file named Marketing.json in the C:\Layouts folder. Note that JSON is the only supported format for the output file and only the `-Path` parameter is supported.

### Example 3: Export the layout with the applications' IDs
```
PS C:\> Export-StartLayout -UseDesktopApplicationID  -Path "C:\Layouts\Marketing.json"
```

This command exports the layout of the tiles on the Start menu of a computer running Windows 10, version 1809 or later, to a file named Marketing.json in the C:\Layouts folder. It exports the applications' IDs instead of paths to a shortcut link.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -LiteralPath
Specifies a literal path to a layout file.
Include the file .xml file name extension.
This parameter does not accept the wildcard character (*).
If the path includes an escape character (\\), enclose the string in single quotes (').

```yaml
Type: String
Parameter Sets: Literal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies an absolute path to a layout file.

```yaml
Type: String
Parameter Sets: Non-literal
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDesktopApplicationID
Specifies that the layout file should export the DesktopApplicationID value instead of DesktopApplicationLinkPath which is the default.
DesktopApplicationID is the application's ID and DesktopApplicationLinkPath is a path to a shortcut link (.lnk file) to a Windows desktop application. It is available on computers running Windows 10, version 1809 or later.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Enum
You can specify the following file format: 

- XML.
Export as an .xml file.

## OUTPUTS

## NOTES

## RELATED LINKS

[Import-StartLayout](./Import-StartLayout.md)

