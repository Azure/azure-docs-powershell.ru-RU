---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914686"
---
# Remove-AzureRmADApplication

## КРАТКИй обзор
Удаляет приложение Azure Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ObjectIdParameterSet (по умолчанию)
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Удаляет приложение Azure Active Directory.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление приложения по идентификатору объекта

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

Удаляет приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" из клиента.

### Пример 2: Удаление приложения по идентификатору приложения

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

Удаляет приложение с идентификатором приложения "f9c5ea4f-28f0-401A-a491-491a037fa346" из клиента.

### Пример 3-Удаление приложения с помощью трубопроводов

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

Возвращает приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzureRmADApplication.

## ПАРАМЕТРЫ

### -ApplicationId
Идентификатор приложения, которое нужно удалить.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Отображаемое имя приложения.

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Переключение на удаление приложения без подтверждения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект, представляющий приложение, которое нужно удалить.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Идентификатор объекта приложения, которое нужно удалить.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Если указать это, будет возвращено значение истина, если команда была выполнена успешно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication
Параметры: InputObject (ByValue)

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmADApplication](./New-AzureRmADApplication.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)



[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

