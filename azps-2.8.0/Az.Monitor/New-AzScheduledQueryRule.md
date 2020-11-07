---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 3a58102eb3a0fa92b176e75135c1170cd621278e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903273"
---
# <span data-ttu-id="867f1-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="867f1-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="867f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="867f1-102">SYNOPSIS</span></span>
<span data-ttu-id="867f1-103">Создание правила оповещения в журнале (тип правила для запланированных запросов)</span><span class="sxs-lookup"><span data-stu-id="867f1-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="867f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="867f1-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="867f1-105">DESCRIPTION</span></span>
<span data-ttu-id="867f1-106">Создание правила оповещения в журнале (тип правила для запланированных запросов)</span><span class="sxs-lookup"><span data-stu-id="867f1-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="867f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="867f1-107">EXAMPLES</span></span>

### <span data-ttu-id="867f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="867f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="867f1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="867f1-109">PARAMETERS</span></span>

### <span data-ttu-id="867f1-110">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="867f1-110">-Action</span></span>
<span data-ttu-id="867f1-111">Действие предупреждения запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="867f1-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="867f1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="867f1-112">-AsJob</span></span>
<span data-ttu-id="867f1-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="867f1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="867f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867f1-114">-DefaultProfile</span></span>
<span data-ttu-id="867f1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="867f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867f1-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="867f1-116">-Description</span></span>
<span data-ttu-id="867f1-117">Описание этого оповещения</span><span class="sxs-lookup"><span data-stu-id="867f1-117">The description for this alert</span></span>

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

### <span data-ttu-id="867f1-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="867f1-118">-Enabled</span></span>
<span data-ttu-id="867f1-119">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="867f1-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="867f1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="867f1-120">-Location</span></span>
<span data-ttu-id="867f1-121">Расположение для этого оповещения.</span><span class="sxs-lookup"><span data-stu-id="867f1-121">The location for this alert</span></span>

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

### <span data-ttu-id="867f1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="867f1-122">-Name</span></span>
<span data-ttu-id="867f1-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="867f1-123">The alert name</span></span>

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

### <span data-ttu-id="867f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="867f1-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="867f1-125">The resource group name</span></span>

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

### <span data-ttu-id="867f1-126">-Планирование</span><span class="sxs-lookup"><span data-stu-id="867f1-126">-Schedule</span></span>
<span data-ttu-id="867f1-127">Запланированное расписание для правила запроса</span><span class="sxs-lookup"><span data-stu-id="867f1-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="867f1-128">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="867f1-128">-Source</span></span>
<span data-ttu-id="867f1-129">Запланированный источник правил запроса</span><span class="sxs-lookup"><span data-stu-id="867f1-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="867f1-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="867f1-130">-Tag</span></span>
<span data-ttu-id="867f1-131">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="867f1-131">Resource tags</span></span>

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

### <span data-ttu-id="867f1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="867f1-132">-Confirm</span></span>
<span data-ttu-id="867f1-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="867f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867f1-134">-WhatIf</span></span>
<span data-ttu-id="867f1-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="867f1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="867f1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="867f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867f1-137">CommonParameters</span></span>
<span data-ttu-id="867f1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="867f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867f1-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="867f1-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867f1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="867f1-140">INPUTS</span></span>

### <span data-ttu-id="867f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="867f1-141">System.String</span></span>

## <span data-ttu-id="867f1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="867f1-142">OUTPUTS</span></span>

### <span data-ttu-id="867f1-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="867f1-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="867f1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="867f1-144">NOTES</span></span>

## <span data-ttu-id="867f1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="867f1-145">RELATED LINKS</span></span>
