---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400087"
---
# <span data-ttu-id="81023-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="81023-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="81023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81023-102">SYNOPSIS</span></span>
<span data-ttu-id="81023-103">Добавляет или обновляет правило оповещения веб-тест.</span><span class="sxs-lookup"><span data-stu-id="81023-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="81023-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81023-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81023-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81023-105">DESCRIPTION</span></span>
<span data-ttu-id="81023-106">Для **параметра Add-AzWebtestAlertRule** добавляется или обновляется правило оповещения метрики, события или типа webtest.</span><span class="sxs-lookup"><span data-stu-id="81023-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="81023-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="81023-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="81023-108">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="81023-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="81023-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81023-109">EXAMPLES</span></span>

### <span data-ttu-id="81023-110">Пример 1. Добавление правила оповещения веб-тестирование</span><span class="sxs-lookup"><span data-stu-id="81023-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="81023-111">Эта команда добавляет или обновляет правило оповещения веб-тестирование.</span><span class="sxs-lookup"><span data-stu-id="81023-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="81023-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81023-112">PARAMETERS</span></span>

### <span data-ttu-id="81023-113">-Action</span><span class="sxs-lookup"><span data-stu-id="81023-113">-Action</span></span>
<span data-ttu-id="81023-114">Определяет список действий, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="81023-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81023-115">-DefaultProfile</span></span>
<span data-ttu-id="81023-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81023-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81023-117">-Description</span><span class="sxs-lookup"><span data-stu-id="81023-117">-Description</span></span>
<span data-ttu-id="81023-118">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="81023-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="81023-119">-DisableRule</span></span>
<span data-ttu-id="81023-120">Отключает правило.</span><span class="sxs-lookup"><span data-stu-id="81023-120">Disables the rule.</span></span>
<span data-ttu-id="81023-121">Если этот параметр не задан, правило включено.</span><span class="sxs-lookup"><span data-stu-id="81023-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="81023-122">-FailedLocationCount</span></span>
<span data-ttu-id="81023-123">Определяет количество сбойных расположений для правил веб-тестирование.</span><span class="sxs-lookup"><span data-stu-id="81023-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="81023-124">Это аналогично пороговому значению в правилах других типов.</span><span class="sxs-lookup"><span data-stu-id="81023-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-125">-Location</span><span class="sxs-lookup"><span data-stu-id="81023-125">-Location</span></span>
<span data-ttu-id="81023-126">Определяет расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="81023-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="81023-127">-MetricName</span></span>
<span data-ttu-id="81023-128">Указывает имя метрик.</span><span class="sxs-lookup"><span data-stu-id="81023-128">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="81023-129">-MetricNamespace</span></span>
<span data-ttu-id="81023-130">Указывает пространство имен метрики для правила.</span><span class="sxs-lookup"><span data-stu-id="81023-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-131">-Name</span><span class="sxs-lookup"><span data-stu-id="81023-131">-Name</span></span>
<span data-ttu-id="81023-132">Указывает имя правила.</span><span class="sxs-lookup"><span data-stu-id="81023-132">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81023-133">-ResourceGroupName</span></span>
<span data-ttu-id="81023-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81023-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="81023-135">-TargetResourceUri</span></span>
<span data-ttu-id="81023-136">Определяет ИД ресурса веб-части "Вебтест".</span><span class="sxs-lookup"><span data-stu-id="81023-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="81023-137">-WindowSize</span></span>
<span data-ttu-id="81023-138">Определяет размер окна времени, заданный правилом для вычисления данных.</span><span class="sxs-lookup"><span data-stu-id="81023-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81023-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81023-139">-Confirm</span></span>
<span data-ttu-id="81023-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="81023-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81023-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81023-141">-WhatIf</span></span>
<span data-ttu-id="81023-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81023-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81023-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81023-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81023-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81023-144">CommonParameters</span></span>
<span data-ttu-id="81023-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81023-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81023-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81023-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81023-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81023-147">INPUTS</span></span>

### <span data-ttu-id="81023-148">System.String</span><span class="sxs-lookup"><span data-stu-id="81023-148">System.String</span></span>

### <span data-ttu-id="81023-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="81023-149">System.TimeSpan</span></span>

### <span data-ttu-id="81023-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="81023-150">System.Int32</span></span>

### <span data-ttu-id="81023-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81023-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="81023-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="81023-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81023-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81023-153">OUTPUTS</span></span>

### <span data-ttu-id="81023-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="81023-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="81023-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81023-155">NOTES</span></span>

## <span data-ttu-id="81023-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81023-156">RELATED LINKS</span></span>

[<span data-ttu-id="81023-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="81023-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="81023-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="81023-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="81023-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="81023-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="81023-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="81023-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


