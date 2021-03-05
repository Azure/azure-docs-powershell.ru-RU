---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: b14d834e005f8a81666fd98b40d276825f04c0e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984570"
---
# <span data-ttu-id="84964-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="84964-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="84964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84964-102">SYNOPSIS</span></span>
<span data-ttu-id="84964-103">Создайте правило сбора данных.</span><span class="sxs-lookup"><span data-stu-id="84964-103">Create a data collection rule.</span></span>

## <span data-ttu-id="84964-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84964-104">SYNTAX</span></span>

### <span data-ttu-id="84964-105">ByFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84964-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="84964-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84964-106">DESCRIPTION</span></span>
<span data-ttu-id="84964-107">Для создания правила сбора данных будет создаваться **cmdlet New-AzDataCollectionRule.**</span><span class="sxs-lookup"><span data-stu-id="84964-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="84964-108">Правила сбора данных (DCR) определяют данные, которые в нее в нее вслали, и определяли, куда они должны быть отправлены или сохранены.</span><span class="sxs-lookup"><span data-stu-id="84964-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="84964-109">Вот полная статья [с обзором DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="84964-109">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="84964-110">Чтобы использовать параметр -RuleFile, можно создать json-файл, содержащий три свойства: dataSources, destinations, dataFlows (см. пример #1)</span><span class="sxs-lookup"><span data-stu-id="84964-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="84964-111">Здесь можно найти [подробные схемы.](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="84964-111">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="84964-112">Кроме того, поддерживается вывод dcR, отреализованного с ConvertTo-Json (см. пример #2).</span><span class="sxs-lookup"><span data-stu-id="84964-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="84964-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84964-113">EXAMPLES</span></span>

### <span data-ttu-id="84964-114">Пример 1. Создание правила сбора данных JSON из Rest API</span><span class="sxs-lookup"><span data-stu-id="84964-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="84964-115">Эта команда создает правила сбора данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="84964-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="84964-116">Пример 2. Создание правила сбора данных JSON из PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="84964-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="84964-117">Эта команда создает правила сбора данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="84964-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="84964-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84964-118">PARAMETERS</span></span>

### <span data-ttu-id="84964-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84964-119">-DefaultProfile</span></span>
<span data-ttu-id="84964-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="84964-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84964-121">-Location</span><span class="sxs-lookup"><span data-stu-id="84964-121">-Location</span></span>
<span data-ttu-id="84964-122">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="84964-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84964-123">-ResourceGroupName</span></span>
<span data-ttu-id="84964-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="84964-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="84964-125">-RuleName</span></span>
<span data-ttu-id="84964-126">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="84964-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="84964-127">-RuleFile</span></span>
<span data-ttu-id="84964-128">Путь к файлу JSON</span><span class="sxs-lookup"><span data-stu-id="84964-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-129">-Description</span><span class="sxs-lookup"><span data-stu-id="84964-129">-Description</span></span>
<span data-ttu-id="84964-130">Описание ресурса</span><span class="sxs-lookup"><span data-stu-id="84964-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="84964-131">-Tag</span></span>
<span data-ttu-id="84964-132">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="84964-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84964-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84964-133">-Confirm</span></span>
<span data-ttu-id="84964-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84964-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84964-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84964-135">-WhatIf</span></span>
<span data-ttu-id="84964-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84964-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84964-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="84964-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84964-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84964-138">CommonParameters</span></span>
<span data-ttu-id="84964-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84964-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84964-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84964-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84964-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84964-141">INPUTS</span></span>

### <span data-ttu-id="84964-142">System.String</span><span class="sxs-lookup"><span data-stu-id="84964-142">System.String</span></span>

## <span data-ttu-id="84964-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84964-143">OUTPUTS</span></span>

### <span data-ttu-id="84964-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="84964-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="84964-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84964-145">NOTES</span></span>

## <span data-ttu-id="84964-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84964-146">RELATED LINKS</span></span>

<span data-ttu-id="84964-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="84964-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>