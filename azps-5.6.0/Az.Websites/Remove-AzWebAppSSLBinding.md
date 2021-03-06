---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: b1d9aa1f212ce31a8bb7fadeff4e0ca8afcf05e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959315"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Удаляет привязку SSL из загруженного сертификата.

## СИНТАКСИС

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Remove-AzWebAppSSLBinding** удаляется привязка SSL из Azure Web App.
Привязки SSL используются для связывания Веб-приложения с сертификатом.

## ПРИМЕРЫ

### Пример 1. Удаление привязки SSL для веб-приложения
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Эта команда удаляет привязку SSL для веб-приложения ContosoWebApp.
Так как *параметр DeleteCertificate* не включен, сертификат будет удален, если он больше не содержит привязки SSL.

### Пример 2. Удаление привязки SSL без удаления сертификата
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Как и в примере 1, эта команда также удаляет привязку SSL для веб-приложения ContosoWebApp.
Однако в этом случае параметр *DeleteCertificate* включается, а его значением является $False.
Это означает, что сертификат не будет удален независимо от того, имеет ли он привязку SSL.

### Пример 3. Удаление привязки SSL с помощью ссылки на объект
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

В этом примере используется ссылка на веб-сайт Web App для удаления привязки SSL для веб-приложения.
Первая команда использует Get-AzWebApp для создания ссылки на веб-приложение ContosoWebApp.
Эта ссылка на объект хранится в переменной с именем $WebApp.
Вторая команда использует ссылку на объект и командлет **Remove-AzWebAppSSLBinding** для удаления привязки SSL.

## PARAMETERS

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

### -DeleteCertificate
Указывает действие, которое будет происходить, если SSL-привязка удаляется только из сертификата.
Если *для действия DeleteCertificate* задано значение $False, сертификат не будет удален при удалении привязки.
Если *команда DeleteCertificate* имеет значение $True или не включена в команду, сертификат будет удален вместе с привязкой SSL.
Сертификат удаляется только в том случае, если удаляется привязка SSL.
Если сертификат имеет несколько привязки, сертификат не будет удален независимо от значения параметра *DeleteCertificate.*

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Запуск команды без запроса подтверждения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя веб-приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которая назначена сертификату.
В одной команде нельзя использовать параметр *ResourceGroupName* и *параметр WebApp.*

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Указывает слот развертывания Web App.
Чтобы получить слот развертывания, воспользуйтесь Get-AzWebAppSlot управления.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Определяет веб-приложение.
Чтобы получить веб-приложение, воспользуйтесь Get-AzWebApp.
Нельзя использовать параметр *WebApp* в той же команде, что и параметр *ResourceGroupName* или *WebAppName.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Указывает имя веб-приложения.
В одной команде нельзя использовать *параметры WebAppName* и *WebApp.*

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


