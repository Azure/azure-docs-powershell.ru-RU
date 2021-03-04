---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: c8085f4f760ff3f2c4c1fa7310eef2c2f2bb33bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952323"
---
# <span data-ttu-id="d4822-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4822-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="d4822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4822-102">SYNOPSIS</span></span>
<span data-ttu-id="d4822-103">Удаляет правило метрических оповещений V2 (нестандартное).</span><span class="sxs-lookup"><span data-stu-id="d4822-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="d4822-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4822-104">SYNTAX</span></span>

### <span data-ttu-id="d4822-105">ByMetricRuleResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4822-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4822-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d4822-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4822-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4822-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4822-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4822-108">DESCRIPTION</span></span>
<span data-ttu-id="d4822-109">С **помощью cmdlet Remove-AzMetricAlertRuleV2** удаляется правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="d4822-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="d4822-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4822-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d4822-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4822-111">EXAMPLES</span></span>

### <span data-ttu-id="d4822-112">Пример 1. Удаление правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="d4822-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="d4822-113">Эта команда удаляет правило оповещения PsSdk.</span><span class="sxs-lookup"><span data-stu-id="d4822-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="d4822-114">Пример 2. Удаление правила оповещения по ИД</span><span class="sxs-lookup"><span data-stu-id="d4822-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="d4822-115">Эта команда удаляет правило оповещения с ИД ресурса `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="d4822-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="d4822-116">Пример 3. Получите и удалите оповещение</span><span class="sxs-lookup"><span data-stu-id="d4822-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="d4822-117">Эта команда получает оповещение и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="d4822-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="d4822-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4822-118">PARAMETERS</span></span>

### <span data-ttu-id="d4822-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4822-119">-AsJob</span></span>
<span data-ttu-id="d4822-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d4822-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4822-121">-DefaultProfile</span></span>
<span data-ttu-id="d4822-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4822-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4822-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4822-123">-InputObject</span></span>
<span data-ttu-id="d4822-124">Объект правила метрики</span><span class="sxs-lookup"><span data-stu-id="d4822-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d4822-125">-Name</span></span>
<span data-ttu-id="d4822-126">Имя правила метрических оповещений</span><span class="sxs-lookup"><span data-stu-id="d4822-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4822-127">-PassThru</span></span>
<span data-ttu-id="d4822-128">Возвращается истина после успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="d4822-128">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4822-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4822-130">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4822-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4822-131">-ResourceId</span></span>
<span data-ttu-id="d4822-132">The RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d4822-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4822-133">-Confirm</span></span>
<span data-ttu-id="d4822-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d4822-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4822-135">-WhatIf</span></span>
<span data-ttu-id="d4822-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4822-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4822-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4822-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4822-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4822-138">CommonParameters</span></span>
<span data-ttu-id="d4822-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4822-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4822-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4822-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4822-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4822-141">INPUTS</span></span>

### <span data-ttu-id="d4822-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d4822-142">System.String</span></span>

### <span data-ttu-id="d4822-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4822-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="d4822-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4822-144">OUTPUTS</span></span>

### <span data-ttu-id="d4822-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4822-145">System.Boolean</span></span>

## <span data-ttu-id="d4822-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4822-146">NOTES</span></span>

## <span data-ttu-id="d4822-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4822-147">RELATED LINKS</span></span>
