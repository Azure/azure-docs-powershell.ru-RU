---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563211"
---
# Get-AzureStorageQueue

## КРАТКИй обзор
Выводит список очередей хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### QueueName (по умолчанию)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageQueue** перечисляет очереди хранения, связанные с учетной записью хранения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех очередей хранилища Azure
```
PS C:\>Get-AzureStorageQueue
```

Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.

### Пример 2: список очередей хранилища Azure с использованием подстановочных знаков
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Эта команда использует подстановочный знак для получения списка очередей хранилища, имя которого начинается с очереди.

### Пример 3: список очередей хранилища Azure с использованием префикса имени очереди
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

В этом примере используется параметр *prefix* для получения списка очередей хранилища, имена которых начинаются с очереди.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Вы можете создать его с помощью командлета **New-AzureStorageContext** .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Name (имя)
Задает имя.
Если имя не указано, командлет возвращает список всех очередей.
Если указано полное или частичное имя, командлет получает все очереди, соответствующие шаблону имени.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix (префикс)
Задает префикс, используемый в именах очередей, которые вы хотите получить.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


