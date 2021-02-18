---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224156"
---
# <span data-ttu-id="91bc8-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="91bc8-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="91bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="91bc8-103">Обновление (полная замена) правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="91bc8-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="91bc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91bc8-104">SYNTAX</span></span>

### <span data-ttu-id="91bc8-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91bc8-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
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

### <span data-ttu-id="91bc8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91bc8-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="91bc8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91bc8-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="91bc8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="91bc8-109">На замену существующего правила сбора данных можно использовать **cmdlet Set-AzDataCollectionRule.**</span><span class="sxs-lookup"><span data-stu-id="91bc8-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="91bc8-110">Правила сбора данных (DCR) определяют данные, которые в нее в нее въеются, и определяют, куда они должны быть отправлены или сохранены.</span><span class="sxs-lookup"><span data-stu-id="91bc8-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="91bc8-111">Вот полная статья [с обзором DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="91bc8-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="91bc8-112">Чтобы использовать параметр -RuleFile, можно создать json-файл, содержащий три свойства: dataSources, destinations, dataFlows (см. пример #1).</span><span class="sxs-lookup"><span data-stu-id="91bc8-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="91bc8-113">Здесь можно найти [подробные схемы.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="91bc8-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="91bc8-114">Также поддерживается вывод dcR, отреализованного с помощью ConvertTo-Json (пример #2).</span><span class="sxs-lookup"><span data-stu-id="91bc8-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="91bc8-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91bc8-115">EXAMPLES</span></span>

### <span data-ttu-id="91bc8-116">Пример 1. Обновление правила сбора данных JSON из Rest API</span><span class="sxs-lookup"><span data-stu-id="91bc8-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
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

<span data-ttu-id="91bc8-117">Эта команда заменяет существующие правила сбора данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="91bc8-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="91bc8-118">Пример 2. Обновление правила сбора данных, JSON от PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="91bc8-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
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

<span data-ttu-id="91bc8-119">Эта команда заменяет существующие правила сбора данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="91bc8-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="91bc8-120">Пример 3. Обновление правила сбора данных из объекта</span><span class="sxs-lookup"><span data-stu-id="91bc8-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="91bc8-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91bc8-121">PARAMETERS</span></span>

### <span data-ttu-id="91bc8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bc8-122">-DefaultProfile</span></span>
<span data-ttu-id="91bc8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91bc8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91bc8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="91bc8-124">-Location</span></span>
<span data-ttu-id="91bc8-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="91bc8-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="91bc8-126">-RuleFile</span></span>
<span data-ttu-id="91bc8-127">Путь к файлу JSON</span><span class="sxs-lookup"><span data-stu-id="91bc8-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91bc8-128">-ResourceGroupName</span></span>
<span data-ttu-id="91bc8-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="91bc8-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="91bc8-130">-RuleName</span></span>
<span data-ttu-id="91bc8-131">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="91bc8-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="91bc8-132">-RuleId</span></span>
<span data-ttu-id="91bc8-133">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="91bc8-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-134">-Description</span><span class="sxs-lookup"><span data-stu-id="91bc8-134">-Description</span></span>
<span data-ttu-id="91bc8-135">Описание ресурса</span><span class="sxs-lookup"><span data-stu-id="91bc8-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="91bc8-136">-Tag</span></span>
<span data-ttu-id="91bc8-137">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="91bc8-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91bc8-138">-InputObject</span></span>
<span data-ttu-id="91bc8-139">Объект PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="91bc8-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="91bc8-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91bc8-140">-Confirm</span></span>
<span data-ttu-id="91bc8-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="91bc8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91bc8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91bc8-142">-WhatIf</span></span>
<span data-ttu-id="91bc8-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91bc8-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91bc8-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91bc8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91bc8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bc8-145">CommonParameters</span></span>
<span data-ttu-id="91bc8-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bc8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bc8-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91bc8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bc8-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91bc8-148">INPUTS</span></span>

### <span data-ttu-id="91bc8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="91bc8-149">System.String</span></span>

## <span data-ttu-id="91bc8-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91bc8-150">OUTPUTS</span></span>

### <span data-ttu-id="91bc8-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="91bc8-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="91bc8-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91bc8-152">NOTES</span></span>

## <span data-ttu-id="91bc8-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91bc8-153">RELATED LINKS</span></span>

<span data-ttu-id="91bc8-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="91bc8-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>