---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951288"
---
# New-AzNotificationHub

## SYNOPSIS
Создает центр уведомлений.

## СИНТАКСИС

### InputFileParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания концентратора уведомлений создается **cmdlet New-AzNotificationHub.**
Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.
Концентраторы уведомлений примерно равны отдельным приложениям: в каждом из приложений обычно имеется собственный концентратор уведомлений.
Для **создания нового концентратора** уведомлений можно создать два способа.
Вы можете создать экземпляр объекта **NotificationHubAttributes,** а затем настроить его.
Затем вы можете скопировать значения этих свойств в новый центр с помощью *параметра NotificationHubObj.*
Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, а затем применить их с помощью параметра *InputFile.*
При использовании в сочетании с **cmdlet New-AzNotificationHub** в предыдущем примере JSON создается центр уведомлений ContosoNotificationHub, расположенный в центре обработки данных в западной части США.

## ПРИМЕРЫ

### Пример 1. Создание концентратора уведомлений
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Эта команда создает концентратор уведомлений в области имен ContosoNamespace.
Новый центр будет назначен группе ContosoNotificationsGroup.
Вам не нужно указывать имя или другие сведения конфигурации для концентратора; эта информация будет взята из файла ввода, C:\Configurations\InternalHub.jsвходной файл.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -InputFile
Путь к JSON-файлу, который содержит значения конфигурации для нового концентратора уведомлений.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Определяет пространство имен, которому будет назначен центр уведомлений.
Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.
Концентраторы уведомлений должны быть назначены существующему пространству имен.
Для создания нового пространства имен нельзя создать новый **cmdlet New-AzNotificationHub.**

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHubObj
Указывает объект **NotificationHubAttributes,** который содержит сведения о конфигурации для нового концентратора.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Указывает группу ресурсов, которой будет назначен концентратор уведомлений.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.
Необходимо использовать существующую группу ресурсов.
Для создания группы ресурсов не может быть новая группа ресурсов с новыми ресурсами **AzNotificationHub.**

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


