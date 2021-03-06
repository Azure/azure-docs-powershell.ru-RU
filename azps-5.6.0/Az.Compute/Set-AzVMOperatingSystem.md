---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990447"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Задает свойства операционной системы для виртуальной машины.

## СИНТАКСИС

### Windows (по умолчанию)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Set-AzVMOperatingSystem** задает свойства операционной системы для виртуальной машины.
Вы можете указать учетные данные для входа, имя компьютера и тип операционной системы.

## ПРИМЕРЫ

### Пример 1. Настройка свойств операционной системы для новой виртуальной машины
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword.
Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .
Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимый в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.
Для получения дополнительных сведений введите `Get-Help New-Object` .
Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.
Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Следующие четыре команды присваивают значения переменным, которые нужно использовать в следующей команде:
Поскольку эти строки можно указать непосредственно в команде **Set-AzVMOperatingSystem,** этот подход используется только для учитаемости.
Однако в сценариях можно использовать такой подход.
Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.
Для этой команды используются учетные данные, хранимые в $Credential.
В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.

### Пример 2. Настройка свойств операционной системы для новой виртуальной машины с включенным исправлением
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword безопасности.
Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .
Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимые в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.
Для получения дополнительных сведений введите `Get-Help New-Object` .
Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.
Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Следующие четыре команды присваивают значения переменным, которые нужно использовать в следующей команде:
Поскольку эти строки можно указать непосредственно в команде **Set-AzVMOperatingSystem,** этот подход используется только для учитаемости.
Однако в сценариях можно использовать такой подход.
Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.
Для этой команды используются учетные данные, хранимые в $Credential.
В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.
Эта команда включает "Hotpatching" на виртуальной машине.

### Пример 3. Настройка свойств операционной системы для новой виртуальной машины Linux
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword безопасности.
Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .
Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимые в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.
Для получения дополнительных сведений введите `Get-Help New-Object` .
Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.
Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Следующие две команды присваивают значения переменным, которые нужно использовать в следующей команде:
Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.
Для этой команды используются учетные данные, хранимые в $Credential.
В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.
Эта команда задает для режима исправления на виртуальной машине значение AutomaticByPlatform.

## PARAMETERS

### -ComputerName
Указывает имя компьютера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Указывает имя пользователя и пароль виртуальной машины в качестве **объекта PSCredential.**
Для получения учетных данных используйте Get-Credential управления.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Указывает строку, которая будет передана виртуальной машине. Дополнительные сведения см. [в подмногах Azure Custom Data (Настраиваемые данные).](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)
**Примечание. Хранить конфиденциальную информацию в пользовательских данных не рекомендуется.**


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Указывает на то, что этот cmdlet отключает проверку подлинности паролем.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Отключить агент VM для предоставления.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Указывает на то, что этот cmdlet включает автоматическое обновление.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableHotpatching
Позволяет клиентам исправление своих VMs Azure без необходимости перезагрузки. Для enableHotpatching для "provisionVMAgent" должно быть задано истинное, а для исправления должно быть задано "AutomaticByPlatform".

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Указывает на то, что тип операционной системы — Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Определяет режим исправления в гостях на виртуальной машине IaaS.<br><br>
Возможные значения:<br>
**Вручную** — вы управляете применением исправлений на виртуальной машине. Для этого нужно вручную применить исправления внутри VM-управления. В этом режиме автоматические обновления отключены. свойство WindowsConfiguration.enableAutomaticUpdates должно быть ложным.<br>
**AutomaticByOS** — виртуальная машинка будет автоматически обновлена операционной системами. Свойство WindowsConfiguration.enableAutomaticUpdates должно быть истинным. <br >
**AutomaticByPlatform** — виртуальная машину будет автоматически обновляться операционной системами. Свойства provisionVMAgent и WindowsConfiguration.enableAutomaticUpdates должны быть истинными.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Указывает на то, что в параметрах на виртуальной машине должен быть установлен агент виртуальной машины.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Определяет часовой пояс виртуальной машины. Например, по \" тихоокеанскому \" времени. <br>
Возможные значения могут [быть](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект локальной виртуальной машины, для которого нужно настроить свойства операционной системы.
Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..
Создайте объект виртуальной машины с помощью New-AzVMConfig..

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
Указывает на то, что типом операционной системы является Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Определяет URI сертификата WinRM.
Он должен храниться в хранилище ключей.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Указывает на то, что в этой операционной системе используется winRM HTTP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Указывает на то, что в этой операционной системе используется winRM HTTPS.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


