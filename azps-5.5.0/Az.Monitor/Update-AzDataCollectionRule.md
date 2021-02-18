---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: a655ac87dcc99eca1a8c5a5329d2073d54614ceb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224132"
---
# <span data-ttu-id="a0336-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="a0336-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="a0336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0336-102">SYNOPSIS</span></span>
<span data-ttu-id="a0336-103">Обновляет свойство тегов правил сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a0336-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="a0336-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0336-104">SYNTAX</span></span>

### <span data-ttu-id="a0336-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0336-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="a0336-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0336-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="a0336-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0336-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="a0336-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0336-108">DESCRIPTION</span></span>
<span data-ttu-id="a0336-109">Командлет **Update-AzDataCollectionRule** обновляет свойство "Теги" правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a0336-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="a0336-110">Правила сбора данных (DCR) определяют данные, которые в нее в нее вслали, и определяли, куда они должны быть отправлены или сохранены.</span><span class="sxs-lookup"><span data-stu-id="a0336-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="a0336-111">Вот полная статья [с обзором DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="a0336-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="a0336-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0336-112">EXAMPLES</span></span>

### <span data-ttu-id="a0336-113">Пример 1. Обновление тегов правил сбора данных</span><span class="sxs-lookup"><span data-stu-id="a0336-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="a0336-114">Эта команда обновляет свойство тегов для заданного правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a0336-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="a0336-115">Пример 2. Обновление тегов правил сбора данных</span><span class="sxs-lookup"><span data-stu-id="a0336-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="a0336-116">Эта команда обновляет свойство тегов для заданного правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a0336-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="a0336-117">Пример 3. Обновление тегов правил сбора данных</span><span class="sxs-lookup"><span data-stu-id="a0336-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="a0336-118">Эта команда обновляет свойство тегов для заданного правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a0336-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="a0336-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0336-119">PARAMETERS</span></span>

### <span data-ttu-id="a0336-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0336-120">-DefaultProfile</span></span>
<span data-ttu-id="a0336-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a0336-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0336-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0336-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0336-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0336-123">The resource group name</span></span>

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

### <span data-ttu-id="a0336-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a0336-124">-RuleName</span></span>
<span data-ttu-id="a0336-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="a0336-125">The resource name</span></span>

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

### <span data-ttu-id="a0336-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a0336-126">-RuleId</span></span>
<span data-ttu-id="a0336-127">ИД ресурса правила сбора данных</span><span class="sxs-lookup"><span data-stu-id="a0336-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="a0336-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0336-128">-InputObject</span></span>
<span data-ttu-id="a0336-129">Объект PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="a0336-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="a0336-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0336-130">-Tag</span></span>
<span data-ttu-id="a0336-131">Свойство "Теги" правила сбора данных</span><span class="sxs-lookup"><span data-stu-id="a0336-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0336-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0336-132">-Confirm</span></span>
<span data-ttu-id="a0336-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a0336-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0336-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0336-134">-WhatIf</span></span>
<span data-ttu-id="a0336-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0336-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0336-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a0336-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0336-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0336-137">CommonParameters</span></span>
<span data-ttu-id="a0336-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0336-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0336-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0336-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0336-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0336-140">INPUTS</span></span>

### <span data-ttu-id="a0336-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a0336-141">System.String</span></span>

## <span data-ttu-id="a0336-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0336-142">OUTPUTS</span></span>

### <span data-ttu-id="a0336-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="a0336-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="a0336-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0336-144">NOTES</span></span>

## <span data-ttu-id="a0336-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0336-145">RELATED LINKS</span></span>

<span data-ttu-id="a0336-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="a0336-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>