---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 87a5b306619bd3d16b9a7c4e76256f2d0e74d568
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998315"
---
# Get-AzHDInsightJob

## SYNOPSIS
Возвращает список заданий из кластера и перечислены в обратном хронологическом порядке или извлекает конкретное задание.

## СИНТАКСИС

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-AzHDInsightJob** можно получить последние задания для указанного кластера Azure HDInsight в обратном хронологическом порядке (последнее задание указано вверху списка).
Получите задание, задав параметр *JobId.*

## ПРИМЕРЫ

### Пример 1. Получить последние задания для указанного кластера Azure HDInsight
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

Эта команда получает все последние задания для кластера hadoop-001.

## PARAMETERS

### -ClusterName
Название кластера.

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

### -httpCredential
Определяет учетные данные для входа в кластер (HTTP).

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Определяет его ИД.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumOfJobs
Количество извлечения заданий.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzHDInsightHiveJobDefinition](./New-AzHDInsightHiveJobDefinition.md)

[Start-AzHDInsightJob](./Start-AzHDInsightJob.md)

[Stop-AzHDInsightJob](./Stop-AzHDInsightJob.md)

[Wait-AzHDInsightJob](./Wait-AzHDInsightJob.md)


