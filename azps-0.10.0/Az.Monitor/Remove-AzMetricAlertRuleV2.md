---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 7688907a2a8b4f8a11a7290fa01294538e24f29f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910191"
---
# <span data-ttu-id="04928-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04928-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="04928-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04928-102">SYNOPSIS</span></span>
<span data-ttu-id="04928-103">Удаляет правило оповещения о метрике v2 (не классический).</span><span class="sxs-lookup"><span data-stu-id="04928-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="04928-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04928-104">SYNTAX</span></span>

### <span data-ttu-id="04928-105">ByMetricRuleResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04928-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04928-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="04928-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04928-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="04928-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04928-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04928-108">DESCRIPTION</span></span>
<span data-ttu-id="04928-109">Командлет **Remove-AzMetricAlertRuleV2** удаляет правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="04928-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="04928-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="04928-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="04928-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04928-111">EXAMPLES</span></span>

### <span data-ttu-id="04928-112">Пример 1: Удаление правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="04928-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="04928-113">Эта команда удаляет правило оповещения с именем PsSdk</span><span class="sxs-lookup"><span data-stu-id="04928-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="04928-114">Пример 2: Удаление правила оповещения по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="04928-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="04928-115">Эта команда удаляет правило оповещения с ИД ресурса `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="04928-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="04928-116">Пример 3: Получение оповещения и его удаление</span><span class="sxs-lookup"><span data-stu-id="04928-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="04928-117">Эта команда возвращает оповещение и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="04928-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="04928-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04928-118">PARAMETERS</span></span>

### <span data-ttu-id="04928-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04928-119">-AsJob</span></span>
<span data-ttu-id="04928-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04928-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04928-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04928-121">-DefaultProfile</span></span>
<span data-ttu-id="04928-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04928-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04928-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04928-123">-InputObject</span></span>
<span data-ttu-id="04928-124">Объект правила метрики</span><span class="sxs-lookup"><span data-stu-id="04928-124">The Metric rule object</span></span>

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

### <span data-ttu-id="04928-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04928-125">-Name</span></span>
<span data-ttu-id="04928-126">Имя правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="04928-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="04928-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04928-127">-PassThru</span></span>
<span data-ttu-id="04928-128">При успешном удалении возвращает значение "истина".</span><span class="sxs-lookup"><span data-stu-id="04928-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="04928-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04928-129">-ResourceGroupName</span></span>
<span data-ttu-id="04928-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04928-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="04928-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04928-131">-ResourceId</span></span>
<span data-ttu-id="04928-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="04928-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="04928-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04928-133">-Confirm</span></span>
<span data-ttu-id="04928-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04928-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04928-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04928-135">-WhatIf</span></span>
<span data-ttu-id="04928-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04928-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04928-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04928-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04928-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04928-138">CommonParameters</span></span>
<span data-ttu-id="04928-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04928-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04928-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04928-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04928-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04928-141">INPUTS</span></span>

### <span data-ttu-id="04928-142">System. String</span><span class="sxs-lookup"><span data-stu-id="04928-142">System.String</span></span>

### <span data-ttu-id="04928-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04928-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="04928-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04928-144">OUTPUTS</span></span>

### <span data-ttu-id="04928-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04928-145">System.Boolean</span></span>

## <span data-ttu-id="04928-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="04928-146">NOTES</span></span>

## <span data-ttu-id="04928-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04928-147">RELATED LINKS</span></span>
