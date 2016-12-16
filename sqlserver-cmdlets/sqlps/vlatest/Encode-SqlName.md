---
external help file: Microsoft.SqlServer.Management.PSProvider.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 82C64D81-2B08-4F54-9793-AEEA4617F15E
updated_at: 12/8/2016 7:20 PM
ms.date: 12/8/2016
content_git_url: https://github.com/MicrosoftDocs/sql-docs-powershell/blob/live/sqlserver-cmdlets/sqlps/vlatest/Encode-SqlName.md
original_content_git_url: https://github.com/MicrosoftDocs/sql-docs-powershell/blob/live/sqlserver-cmdlets/sqlps/vlatest/Encode-SqlName.md
gitcommit: https://github.com/MicrosoftDocs/sql-docs-powershell/blob/b925b18b49186ab91cfeb5201e061d569d0eeae2/sqlserver-cmdlets/sqlps/vlatest/Encode-SqlName.md
ms.topic: reference
author: stevestein
ms.author: sstein
keywords: powershell, cmdlet
manager: jhubbard
open_to_public_contributors: true
ms.service: sql-server
---

# Encode-SqlName

## SYNOPSIS
Encodes special characters in SQL Server names to characters that can be used in PowerShell paths.

## SYNTAX

## DESCRIPTION
The **Encode-SqlName** cmdlet encodes special characters in SQL Server identifier names to characters that can be used in PowerShell paths.
SQL Server delimited identifiers can contain characters that are not normally supported in PowerShell object names.
When using delimited identifiers in SQL Server provider paths, these extended characters must be either encoded to their hexadecimal representation or escaped using the \` character.
Certain characters cannot be escaped.
The hexadecimal encoding for the characters is in the format %nn.
The characters encoded by this cmdlet are: \:./%\<\>*?\[\]|.

## EXAMPLES

### Example 1: Encode a SQL Server table name
```
PS C:\>Encode-SqlName -SqlName "My:Table/"
My%3ATable%2F
```

This command encodes a SQL Server table name that contains the colon (:) and forward-slash (/) characters.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### String

## OUTPUTS

### String

## NOTES

## RELATED LINKS

