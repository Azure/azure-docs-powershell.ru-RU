---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078254"
---
# Get-AzHDInsightProperty

## КРАТКИй обзор
Получение свойств службы HDInsight, например доступных местоположений и емкости.

## Максимальное

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzHDInsightProperty** получает свойства, специфические для Azure HDInsight, например список доступных местоположений, версий кластера HDInsight и доступной вычислительной мощности.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств кластера HDInsight для Azure
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

Эта команда получает свойства из службы HDInsight из расположения "Восток США 2.

## ПАРАМЕТРЫ

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

### -Location
Указывает расположение, для которого требуется получить свойства HDInsight.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего
## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. HDInsight. Models. AzureHDInsightCapabilities
## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
