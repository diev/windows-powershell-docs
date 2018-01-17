---
external help file: DhcpServer_Cmdlets.xml
online version: 
schema: 2.0.0
ms.assetid: E19950F4-B072-4E9A-8B62-A997F27B7EC2
---

# Add-DhcpServerv4OptionDefinition

## SYNOPSIS
Adds a new DHCPv4 option definition on the Dynamic Host Configuration Protocol (DHCP) server service.

## SYNTAX

```
Add-DhcpServerv4OptionDefinition [-Name] <String> [-OptionId] <UInt32> [-Type] <String> [-AsJob]
 [-CimSession <CimSession[]>] [-ComputerName <String>] [-DefaultValue <String[]>] [-Description <String>]
 [-MultiValued] [-PassThru] [-ThrottleLimit <Int32>] [-VendorClass <String>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
Adds a new DHCPv4 option definition on the Dynamic Host Configuration Protocol (DHCP) server service.
An option definition needs to exist before an option value of that type can be configured.

## EXAMPLES

### EXAMPLE 1
```
PS C:\>Add-DhcpServerv4OptionDefinition -Name WPAD -OptionId 252 -Type String
```

This example adds the IPv4 option definition for web proxy auto detection (wpad) to the DHCPv4 server service.

### EXAMPLE 2
```
PS C:\>Add-DhcpServerv4OptionDefinition -Name UCIdentifier -OptionId 1 -Type BinaryData -VendorClass MS-UC-Client -Description "UC Identifier"
```

This example adds the option definition for the Unified Communications (UC) identifier for the vendor class named MS-UC-Client.

## PARAMETERS

### -AsJob
ps_cimcommon_asjob

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the DNS name, or IPv4 or IPv6 address, of the target computer running the DHCP server service.

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

### -DefaultValue
Specifies the default value for the option for which a definition is created.
The syntax to specify the default value for the option as follows: 

 - Byte, Word, DWord, DWordDword: These values can be specified as decimal or hexadecimal strings. 

 - IPAddress, IPv6Address: These values can be specified as IP address strings. 

 - String: This value can be specified as a string. 

 - BinaryData, EncapsulatedData: These values can be specified as hexadecimal strings.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Description
Specifies the description of the option definition being added.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MultiValued
Allows for multiple values.
The acceptable values for this parameter are: True or False.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the DHCPv4 option.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OptionId
Specifies the numerical identifier of the option.
The acceptable values for this parameter are: 1 through 255.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

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

### -Type
Specifies the data type of the values for this option.
The acceptable values for this parameter are: Byte, Word, DWord, DWordDword, IPAddress, String, BinaryData, EncapsulatedData or IPv6Address.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VendorClass
Adds the Option Definition for the specified vendor class.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

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
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Microsoft.Management.Infrastructure.CimInstance#root/Microsoft/Windows/DHCP/DhcpServerv4OptionDefinition
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

### Microsoft.Management.Infrastructure.CimInstance#root/Microsoft/Windows/DHCP/DhcpServerv4OptionValue
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance#root/Microsoft/Windows/DHCP/DhcpServerv4OptionDefinition
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## NOTES

## RELATED LINKS

[Get-DhcpServerv4OptionDefinition](./Get-DhcpServerv4OptionDefinition.md)

[Remove-DhcpServerv4OptionDefinition](./Remove-DhcpServerv4OptionDefinition.md)

[Set-DhcpServerv4OptionDefinition](./Set-DhcpServerv4OptionDefinition.md)
