---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235697"
---
# Get-AzSynapsePipeline

## КРАТКИй обзор
Получение сведений о конвейерах в рабочей области.

## Максимальное

### GetByName (по умолчанию)
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByObject
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzSynapsePipeline** получает сведения о конвейерах в рабочей области. Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере. Если имя не задано, этот командлет получает сведения обо всех конвейерах в рабочей области.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

Эта команда получает сведения обо всех конвейерах в рабочей области с именем ContosoWorkspace.

### Пример 2
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace.

### Пример 3
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace с помощью конвейера.

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
Имя конвейера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Имя Synapse рабочей области.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
объект ввода в рабочую область, обычно передаваемый через конвейер.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
