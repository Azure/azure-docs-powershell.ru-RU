---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002595"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Создает объект диапазона BLOB-объектов для восстановления учетной записи хранения.

## СИНТАКСИС

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet New-AzStorageBlobRangeToRestore** создает объект диапазона BLOB-объектов, который можно использовать в restore-AzStorageBlobRange.

## ПРИМЕРЫ

### Пример 1. Создание диапазона lob-lob для восстановления
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Эта команда создает диапазон BLOB-целей для восстановления, который начинается с контейнера1/blob1 (включая) и заканчивается на container2/blob2 (исключая).

### Пример 2. Создание диапазона lob-lob, который будет восстанавливать из первого BLOB-lob в алфавитном порядке, в определенный BLOB-бизнес (исключая)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Эта команда создает диапазон BLOB-lob, который будет восстанавливать из первого BLOB-части в алфавитном порядке в определенный контейнер BLOB-2/blob2 (исключая)

### Пример 3. Создание диапазона lob-lob, который будет восстанавливать из определенного BLOB-решения (включая) в последний BLOB-проект в алфавитном порядке.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Эта команда создает диапазон BLOB-то, который будет восстановлен из определенного контейнера BLOB-1/blob1 (включая) в последний BLOB-проект в алфавитном порядке.

### Пример 4. Создание диапазона lob-lob,который будет восстанавливать все BLOB-бизнесы
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Эта команда создает диапазон BLOB-lob, который будет восстанавливать все BLOB-lob-ы.

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

### -EndRange
Укажите диапазон восстановления BLOB-то еще.
Конечный диапазон исключается из BLOB-тока восстановления.
Чтобы восстановить его до конца, установите его в качестве пустой strng.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Укажите диапазон начала восстановления BLOB-ля.
Диапазон запуска будет включен в список BLOB-тонов восстановления.
Настроив ее как пустую строку для восстановления с начала.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
