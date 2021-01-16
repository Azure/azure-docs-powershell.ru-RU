---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392156"
---
# <span data-ttu-id="d3240-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d3240-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="d3240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3240-102">SYNOPSIS</span></span>
<span data-ttu-id="d3240-103">Создает правило оповещения журнала (тип правила запланированного запроса)</span><span class="sxs-lookup"><span data-stu-id="d3240-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="d3240-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3240-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3240-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3240-105">DESCRIPTION</span></span>
<span data-ttu-id="d3240-106">Создание правила оповещения журнала (типа "Правило запланированного запроса")</span><span class="sxs-lookup"><span data-stu-id="d3240-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="d3240-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3240-107">EXAMPLES</span></span>

### <span data-ttu-id="d3240-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3240-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="d3240-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3240-109">PARAMETERS</span></span>

### <span data-ttu-id="d3240-110">-Action</span><span class="sxs-lookup"><span data-stu-id="d3240-110">-Action</span></span>
<span data-ttu-id="d3240-111">Действие оповещения для запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="d3240-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3240-112">-AsJob</span></span>
<span data-ttu-id="d3240-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d3240-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3240-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3240-114">-DefaultProfile</span></span>
<span data-ttu-id="d3240-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3240-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3240-116">-Description</span><span class="sxs-lookup"><span data-stu-id="d3240-116">-Description</span></span>
<span data-ttu-id="d3240-117">Описание этого оповещения</span><span class="sxs-lookup"><span data-stu-id="d3240-117">The description for this alert</span></span>

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

### <span data-ttu-id="d3240-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d3240-118">-Enabled</span></span>
<span data-ttu-id="d3240-119">Состояние оповещения Azure : допустимые значения — $true, $false</span><span class="sxs-lookup"><span data-stu-id="d3240-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d3240-120">-Location</span></span>
<span data-ttu-id="d3240-121">Расположение этого оповещения</span><span class="sxs-lookup"><span data-stu-id="d3240-121">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d3240-122">-Name</span></span>
<span data-ttu-id="d3240-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="d3240-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3240-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3240-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d3240-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-126">-Расписание</span><span class="sxs-lookup"><span data-stu-id="d3240-126">-Schedule</span></span>
<span data-ttu-id="d3240-127">Расписание запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="d3240-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-128">-Source</span><span class="sxs-lookup"><span data-stu-id="d3240-128">-Source</span></span>
<span data-ttu-id="d3240-129">Источник правил для запланированного запроса</span><span class="sxs-lookup"><span data-stu-id="d3240-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3240-130">-Tag</span></span>
<span data-ttu-id="d3240-131">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="d3240-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3240-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3240-132">-Confirm</span></span>
<span data-ttu-id="d3240-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3240-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3240-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3240-134">-WhatIf</span></span>
<span data-ttu-id="d3240-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3240-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3240-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3240-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3240-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3240-137">CommonParameters</span></span>
<span data-ttu-id="d3240-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3240-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3240-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3240-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3240-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3240-140">INPUTS</span></span>

### <span data-ttu-id="d3240-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d3240-141">System.String</span></span>

## <span data-ttu-id="d3240-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3240-142">OUTPUTS</span></span>

### <span data-ttu-id="d3240-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="d3240-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="d3240-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3240-144">NOTES</span></span>

## <span data-ttu-id="d3240-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3240-145">RELATED LINKS</span></span>
