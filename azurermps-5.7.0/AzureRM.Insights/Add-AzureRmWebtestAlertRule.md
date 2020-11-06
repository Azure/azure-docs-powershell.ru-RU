---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563495"
---
# <span data-ttu-id="2297a-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2297a-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="2297a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2297a-102">SYNOPSIS</span></span>
<span data-ttu-id="2297a-103">Добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="2297a-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2297a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2297a-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2297a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2297a-105">DESCRIPTION</span></span>
<span data-ttu-id="2297a-106">Командлет **Add-AzureRmWebtestAlertRule** добавляет или обновляет правило оповещения типа Metric, Event или WebTest.</span><span class="sxs-lookup"><span data-stu-id="2297a-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="2297a-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="2297a-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="2297a-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="2297a-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2297a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2297a-109">EXAMPLES</span></span>

### <span data-ttu-id="2297a-110">Пример 1: Добавление правила оповещения для веб-теста</span><span class="sxs-lookup"><span data-stu-id="2297a-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2297a-111">Эта команда добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="2297a-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="2297a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2297a-112">PARAMETERS</span></span>

### <span data-ttu-id="2297a-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="2297a-113">-Action</span></span>
<span data-ttu-id="2297a-114">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="2297a-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2297a-115">-DefaultProfile</span></span>
<span data-ttu-id="2297a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2297a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="2297a-117">-Description</span></span>
<span data-ttu-id="2297a-118">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="2297a-118">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2297a-119">-DisableRule</span></span>
<span data-ttu-id="2297a-120">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="2297a-120">Disables the rule.</span></span>
<span data-ttu-id="2297a-121">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="2297a-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="2297a-122">-FailedLocationCount</span></span>
<span data-ttu-id="2297a-123">Указывает количество сбойных расположений для правил WebTest.</span><span class="sxs-lookup"><span data-stu-id="2297a-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="2297a-124">Это напоминает пороговое значение в других типах правил.</span><span class="sxs-lookup"><span data-stu-id="2297a-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-125">-Location</span><span class="sxs-lookup"><span data-stu-id="2297a-125">-Location</span></span>
<span data-ttu-id="2297a-126">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="2297a-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2297a-127">-MetricName</span></span>
<span data-ttu-id="2297a-128">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="2297a-128">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="2297a-129">-MetricNamespace</span></span>
<span data-ttu-id="2297a-130">Задает пространство имен метрик для правила.</span><span class="sxs-lookup"><span data-stu-id="2297a-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2297a-131">-Name</span></span>
<span data-ttu-id="2297a-132">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="2297a-132">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2297a-133">-ResourceGroupName</span></span>
<span data-ttu-id="2297a-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2297a-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="2297a-135">-TargetResourceUri</span></span>
<span data-ttu-id="2297a-136">Указывает идентификатор ресурса для теста.</span><span class="sxs-lookup"><span data-stu-id="2297a-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="2297a-137">-WindowSize</span></span>
<span data-ttu-id="2297a-138">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="2297a-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2297a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2297a-139">CommonParameters</span></span>
<span data-ttu-id="2297a-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2297a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2297a-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2297a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2297a-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2297a-142">INPUTS</span></span>

### <span data-ttu-id="2297a-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="2297a-143">None</span></span>
<span data-ttu-id="2297a-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2297a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2297a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2297a-145">OUTPUTS</span></span>

### <span data-ttu-id="2297a-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2297a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2297a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2297a-147">NOTES</span></span>

## <span data-ttu-id="2297a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2297a-148">RELATED LINKS</span></span>

[<span data-ttu-id="2297a-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2297a-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2297a-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2297a-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="2297a-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2297a-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2297a-152">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2297a-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


