---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079537"
---
# <span data-ttu-id="78dc2-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="78dc2-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="78dc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="78dc2-103">Добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="78dc2-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="78dc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78dc2-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78dc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="78dc2-106">Командлет **Add-AzWebtestAlertRule** добавляет или обновляет правило оповещения типа Metric, Event или WebTest.</span><span class="sxs-lookup"><span data-stu-id="78dc2-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="78dc2-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="78dc2-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="78dc2-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="78dc2-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="78dc2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="78dc2-110">Пример 1: Добавление правила оповещения для веб-теста</span><span class="sxs-lookup"><span data-stu-id="78dc2-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="78dc2-111">Эта команда добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="78dc2-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="78dc2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78dc2-112">PARAMETERS</span></span>

### <span data-ttu-id="78dc2-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="78dc2-113">-Action</span></span>
<span data-ttu-id="78dc2-114">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="78dc2-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="78dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="78dc2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78dc2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78dc2-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="78dc2-117">-Description</span></span>
<span data-ttu-id="78dc2-118">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="78dc2-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="78dc2-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="78dc2-119">-DisableRule</span></span>
<span data-ttu-id="78dc2-120">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="78dc2-120">Disables the rule.</span></span>
<span data-ttu-id="78dc2-121">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="78dc2-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="78dc2-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="78dc2-122">-FailedLocationCount</span></span>
<span data-ttu-id="78dc2-123">Указывает количество сбойных расположений для правил WebTest.</span><span class="sxs-lookup"><span data-stu-id="78dc2-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="78dc2-124">Это напоминает пороговое значение в других типах правил.</span><span class="sxs-lookup"><span data-stu-id="78dc2-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="78dc2-125">-Location</span><span class="sxs-lookup"><span data-stu-id="78dc2-125">-Location</span></span>
<span data-ttu-id="78dc2-126">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="78dc2-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="78dc2-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="78dc2-127">-MetricName</span></span>
<span data-ttu-id="78dc2-128">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="78dc2-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="78dc2-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="78dc2-129">-MetricNamespace</span></span>
<span data-ttu-id="78dc2-130">Задает пространство имен метрик для правила.</span><span class="sxs-lookup"><span data-stu-id="78dc2-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="78dc2-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78dc2-131">-Name</span></span>
<span data-ttu-id="78dc2-132">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="78dc2-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="78dc2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78dc2-133">-ResourceGroupName</span></span>
<span data-ttu-id="78dc2-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78dc2-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78dc2-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="78dc2-135">-TargetResourceUri</span></span>
<span data-ttu-id="78dc2-136">Указывает идентификатор ресурса для теста.</span><span class="sxs-lookup"><span data-stu-id="78dc2-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="78dc2-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="78dc2-137">-WindowSize</span></span>
<span data-ttu-id="78dc2-138">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="78dc2-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="78dc2-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78dc2-139">-Confirm</span></span>
<span data-ttu-id="78dc2-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78dc2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78dc2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78dc2-141">-WhatIf</span></span>
<span data-ttu-id="78dc2-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78dc2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78dc2-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78dc2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78dc2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78dc2-144">CommonParameters</span></span>
<span data-ttu-id="78dc2-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78dc2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78dc2-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78dc2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78dc2-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78dc2-147">INPUTS</span></span>

### <span data-ttu-id="78dc2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="78dc2-148">System.String</span></span>

### <span data-ttu-id="78dc2-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="78dc2-149">System.TimeSpan</span></span>

### <span data-ttu-id="78dc2-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="78dc2-150">System.Int32</span></span>

### <span data-ttu-id="78dc2-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78dc2-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="78dc2-152">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. RuleAction; Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="78dc2-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="78dc2-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78dc2-153">OUTPUTS</span></span>

### <span data-ttu-id="78dc2-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78dc2-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="78dc2-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="78dc2-155">NOTES</span></span>

## <span data-ttu-id="78dc2-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78dc2-156">RELATED LINKS</span></span>

[<span data-ttu-id="78dc2-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="78dc2-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="78dc2-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="78dc2-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="78dc2-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="78dc2-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="78dc2-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="78dc2-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


