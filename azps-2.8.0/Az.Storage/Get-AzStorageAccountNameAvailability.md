---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 60e30de4d6d55007ec659a267b1d450ac1cfeff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907034"
---
# Get-AzStorageAccountNameAvailability

## КРАТКИй обзор
Проверка доступности имени учетной записи хранения.

## Максимальное

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzStorageAccountNameAvailability** проверяет, является ли имя учетной записи службы хранилища Azure допустимым и доступным для использования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Проверка доступности имени учетной записи хранения
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

Эта команда проверяет доступность имени ContosoStorage03.

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя учетной записи хранения, которую проверяет этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Командлеты диспетчера хранилища Azure](./Az.Storage.md)


