---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569415"
---
# <span data-ttu-id="6b9ae-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b9ae-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="6b9ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9ae-103">Добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b9ae-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9ae-106">Командлет **Add-AzureRmWebtestAlertRule** добавляет или обновляет правило оповещения типа Metric, Event или WebTest.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="6b9ae-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="6b9ae-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b9ae-108">EXAMPLES</span></span>

### <span data-ttu-id="6b9ae-109">Пример 1: Добавление правила оповещения для веб-теста</span><span class="sxs-lookup"><span data-stu-id="6b9ae-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6b9ae-110">Эта команда добавляет или обновляет правило оповещения для веб-теста.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="6b9ae-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b9ae-111">PARAMETERS</span></span>

### <span data-ttu-id="6b9ae-112">-Actions (действия)</span><span class="sxs-lookup"><span data-stu-id="6b9ae-112">-Actions</span></span>
<span data-ttu-id="6b9ae-113">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="6b9ae-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="6b9ae-114">-Description</span></span>
<span data-ttu-id="6b9ae-115">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="6b9ae-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6b9ae-116">-DisableRule</span></span>
<span data-ttu-id="6b9ae-117">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-117">Disables the rule.</span></span>
<span data-ttu-id="6b9ae-118">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="6b9ae-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="6b9ae-119">-FailedLocationCount</span></span>
<span data-ttu-id="6b9ae-120">Указывает количество сбойных расположений для правил WebTest.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="6b9ae-121">Это напоминает пороговое значение в других типах правил.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="6b9ae-122">-Location</span><span class="sxs-lookup"><span data-stu-id="6b9ae-122">-Location</span></span>
<span data-ttu-id="6b9ae-123">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="6b9ae-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="6b9ae-124">-MetricName</span></span>
<span data-ttu-id="6b9ae-125">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="6b9ae-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="6b9ae-126">-MetricNamespace</span></span>
<span data-ttu-id="6b9ae-127">Задает пространство имен метрик для правила.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="6b9ae-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b9ae-128">-Name</span></span>
<span data-ttu-id="6b9ae-129">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="6b9ae-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b9ae-130">-ResourceGroup</span></span>
<span data-ttu-id="6b9ae-131">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b9ae-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="6b9ae-132">-TargetResourceUri</span></span>
<span data-ttu-id="6b9ae-133">Указывает идентификатор ресурса для теста.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="6b9ae-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="6b9ae-134">-WindowSize</span></span>
<span data-ttu-id="6b9ae-135">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="6b9ae-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9ae-136">-DefaultProfile</span></span>
<span data-ttu-id="6b9ae-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9ae-138">CommonParameters</span></span>
<span data-ttu-id="6b9ae-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b9ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9ae-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9ae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9ae-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b9ae-141">INPUTS</span></span>

## <span data-ttu-id="6b9ae-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b9ae-142">OUTPUTS</span></span>

### <span data-ttu-id="6b9ae-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6b9ae-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6b9ae-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b9ae-144">NOTES</span></span>

## <span data-ttu-id="6b9ae-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b9ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="6b9ae-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b9ae-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="6b9ae-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b9ae-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="6b9ae-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6b9ae-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6b9ae-149">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6b9ae-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


