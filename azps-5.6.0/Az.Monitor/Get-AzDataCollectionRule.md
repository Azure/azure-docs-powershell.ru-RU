---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 6c1ea4cd7abbf50fb00a5f7fe1b04b7112b8f6c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980088"
---
# <span data-ttu-id="c64ce-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="c64ce-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="c64ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c64ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c64ce-103">Получает правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="c64ce-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="c64ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c64ce-104">SYNTAX</span></span>

### <span data-ttu-id="c64ce-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c64ce-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="c64ce-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c64ce-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="c64ce-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c64ce-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="c64ce-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c64ce-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="c64ce-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c64ce-109">DESCRIPTION</span></span>
<span data-ttu-id="c64ce-110">Для получения одного или более правил сбора данных можно получить одно или несколько правил сбора данных для **get-AzDataCollectionRule.**</span><span class="sxs-lookup"><span data-stu-id="c64ce-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="c64ce-111">Правила сбора данных (DCR) определяют данные, которые в нее в нее вются, и определяют, куда они должны быть отправлены или сохранены.</span><span class="sxs-lookup"><span data-stu-id="c64ce-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="c64ce-112">Вот полная статья [с обзором DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="c64ce-112">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="c64ce-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c64ce-113">EXAMPLES</span></span>

### <span data-ttu-id="c64ce-114">Пример 1. Получите правила сбора данных по ИД подписки</span><span class="sxs-lookup"><span data-stu-id="c64ce-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c64ce-115">Эта команда содержит все правила сбора данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c64ce-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="c64ce-116">Пример 2. Получить правила сбора данных для данной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c64ce-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c64ce-117">Эта команда содержит список правил сбора данных для заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c64ce-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="c64ce-118">Пример 3. Получите правило сбора данных</span><span class="sxs-lookup"><span data-stu-id="c64ce-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c64ce-119">Эта команда содержит одно правило сбора данных (список с одним элементом).</span><span class="sxs-lookup"><span data-stu-id="c64ce-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="c64ce-120">Пример 4. Получите правило сбора данных по ИД правила</span><span class="sxs-lookup"><span data-stu-id="c64ce-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c64ce-121">Эта команда содержит одно правило сбора данных (список с одним элементом).</span><span class="sxs-lookup"><span data-stu-id="c64ce-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="c64ce-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c64ce-122">PARAMETERS</span></span>

### <span data-ttu-id="c64ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64ce-123">-DefaultProfile</span></span>
<span data-ttu-id="c64ce-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c64ce-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c64ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="c64ce-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c64ce-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ce-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c64ce-127">-RuleName</span></span>
<span data-ttu-id="c64ce-128">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="c64ce-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ce-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="c64ce-129">-RuleId</span></span>
<span data-ttu-id="c64ce-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c64ce-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64ce-131">CommonParameters</span></span>
<span data-ttu-id="c64ce-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64ce-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c64ce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64ce-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c64ce-134">INPUTS</span></span>

### <span data-ttu-id="c64ce-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c64ce-135">System.String</span></span>

## <span data-ttu-id="c64ce-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c64ce-136">OUTPUTS</span></span>

### <span data-ttu-id="c64ce-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="c64ce-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="c64ce-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c64ce-138">NOTES</span></span>

## <span data-ttu-id="c64ce-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c64ce-139">RELATED LINKS</span></span>

<span data-ttu-id="c64ce-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="c64ce-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
