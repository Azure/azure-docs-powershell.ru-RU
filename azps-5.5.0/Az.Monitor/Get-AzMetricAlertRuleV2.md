---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219041"
---
# <span data-ttu-id="2500c-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2500c-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="2500c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2500c-102">SYNOPSIS</span></span>
<span data-ttu-id="2500c-103">Получает правила метрических оповещений V2 (нестандартные)</span><span class="sxs-lookup"><span data-stu-id="2500c-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="2500c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2500c-104">SYNTAX</span></span>

### <span data-ttu-id="2500c-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="2500c-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2500c-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="2500c-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2500c-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="2500c-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2500c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2500c-108">DESCRIPTION</span></span>
<span data-ttu-id="2500c-109">Для этого с помощью **cmdlet Get-AzMetricAlertRuleV2** можно получить правило метрического оповещения по имени или URI либо все правила метрических оповещений для указанной группы ресурсов или подписки.</span><span class="sxs-lookup"><span data-stu-id="2500c-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="2500c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2500c-110">EXAMPLES</span></span>

### <span data-ttu-id="2500c-111">Пример 1. Все правила метрических оповещений в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2500c-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="2500c-112">Эта команда получает все правила метрических оповещений в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2500c-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="2500c-113">Пример 2. Получите все правила метрических оповещений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="2500c-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="2500c-114">Эта команда получает все правила метрических оповещений в группе ресурсов метрическаяAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="2500c-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="2500c-115">Пример 3. По имени получите правило метрических оповещений</span><span class="sxs-lookup"><span data-stu-id="2500c-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="2500c-116">Эта команда получает правило метрических оповещений PS3182019 в группе ресурсов metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="2500c-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="2500c-117">Пример 4. Получите правило метрических оповещений по ruleID</span><span class="sxs-lookup"><span data-stu-id="2500c-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="2500c-118">Эта команда получает правило метрических оповещений с заданным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="2500c-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="2500c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2500c-119">PARAMETERS</span></span>

### <span data-ttu-id="2500c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2500c-120">-DefaultProfile</span></span>
<span data-ttu-id="2500c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2500c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2500c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2500c-122">-Name</span></span>
<span data-ttu-id="2500c-123">Имя правила метрических оповещений</span><span class="sxs-lookup"><span data-stu-id="2500c-123">The Name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2500c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2500c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2500c-125">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2500c-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2500c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2500c-126">-ResourceId</span></span>
<span data-ttu-id="2500c-127">The Rule Id of metric alert rule</span><span class="sxs-lookup"><span data-stu-id="2500c-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2500c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2500c-128">CommonParameters</span></span>
<span data-ttu-id="2500c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2500c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2500c-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2500c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2500c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2500c-131">INPUTS</span></span>

### <span data-ttu-id="2500c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2500c-132">System.String</span></span>

## <span data-ttu-id="2500c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2500c-133">OUTPUTS</span></span>

### <span data-ttu-id="2500c-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2500c-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="2500c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2500c-135">NOTES</span></span>

## <span data-ttu-id="2500c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2500c-136">RELATED LINKS</span></span>
