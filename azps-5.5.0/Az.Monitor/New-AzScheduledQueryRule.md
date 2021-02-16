---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219009"
---
# <span data-ttu-id="b0b81-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b0b81-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="b0b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b81-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b81-103">Создание правила оповещения журнала (типа "Правило запланированного запроса")</span><span class="sxs-lookup"><span data-stu-id="b0b81-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="b0b81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0b81-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0b81-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b81-106">Создает правило оповещения журнала (тип правила запланированного запроса)</span><span class="sxs-lookup"><span data-stu-id="b0b81-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="b0b81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0b81-107">EXAMPLES</span></span>

### <span data-ttu-id="b0b81-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0b81-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="b0b81-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b81-109">PARAMETERS</span></span>

### <span data-ttu-id="b0b81-110">-Action</span><span class="sxs-lookup"><span data-stu-id="b0b81-110">-Action</span></span>
<span data-ttu-id="b0b81-111">Действие оповещения для запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="b0b81-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="b0b81-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b81-112">-AsJob</span></span>
<span data-ttu-id="b0b81-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0b81-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0b81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b81-114">-DefaultProfile</span></span>
<span data-ttu-id="b0b81-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b81-116">-Description</span><span class="sxs-lookup"><span data-stu-id="b0b81-116">-Description</span></span>
<span data-ttu-id="b0b81-117">Описание этого оповещения</span><span class="sxs-lookup"><span data-stu-id="b0b81-117">The description for this alert</span></span>

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

### <span data-ttu-id="b0b81-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b0b81-118">-Enabled</span></span>
<span data-ttu-id="b0b81-119">Состояние оповещения Azure : допустимые значения — $true, $false</span><span class="sxs-lookup"><span data-stu-id="b0b81-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="b0b81-120">-Location</span><span class="sxs-lookup"><span data-stu-id="b0b81-120">-Location</span></span>
<span data-ttu-id="b0b81-121">Расположение этого оповещения</span><span class="sxs-lookup"><span data-stu-id="b0b81-121">The location for this alert</span></span>

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

### <span data-ttu-id="b0b81-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b81-122">-Name</span></span>
<span data-ttu-id="b0b81-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="b0b81-123">The alert name</span></span>

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

### <span data-ttu-id="b0b81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b81-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0b81-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0b81-125">The resource group name</span></span>

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

### <span data-ttu-id="b0b81-126">-Расписание</span><span class="sxs-lookup"><span data-stu-id="b0b81-126">-Schedule</span></span>
<span data-ttu-id="b0b81-127">Расписание запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="b0b81-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="b0b81-128">-Source</span><span class="sxs-lookup"><span data-stu-id="b0b81-128">-Source</span></span>
<span data-ttu-id="b0b81-129">Источник правил для запланированного запроса</span><span class="sxs-lookup"><span data-stu-id="b0b81-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="b0b81-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0b81-130">-Tag</span></span>
<span data-ttu-id="b0b81-131">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0b81-131">Resource tags</span></span>

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

### <span data-ttu-id="b0b81-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0b81-132">-Confirm</span></span>
<span data-ttu-id="b0b81-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b0b81-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b81-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b81-134">-WhatIf</span></span>
<span data-ttu-id="b0b81-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0b81-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0b81-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0b81-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b81-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b81-137">CommonParameters</span></span>
<span data-ttu-id="b0b81-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b81-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b81-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b81-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b81-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b81-140">INPUTS</span></span>

### <span data-ttu-id="b0b81-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b81-141">System.String</span></span>

## <span data-ttu-id="b0b81-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b81-142">OUTPUTS</span></span>

### <span data-ttu-id="b0b81-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="b0b81-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="b0b81-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0b81-144">NOTES</span></span>

## <span data-ttu-id="b0b81-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0b81-145">RELATED LINKS</span></span>
