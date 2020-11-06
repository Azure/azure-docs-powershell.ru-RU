---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569424"
---
# <span data-ttu-id="6f2a3-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6f2a3-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="6f2a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2a3-103">Добавляет или заменяет правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f2a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f2a3-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f2a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2a3-105">DESCRIPTION</span></span>
<span data-ttu-id="6f2a3-106">Командлет **Add-AzureRmLogAlertRule** добавляет или заменяет правило оповещения о событии.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="6f2a3-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="6f2a3-108">Как объявлено в предыдущих выпусках: **командлет Add-AzureRMLogAlertRule будет устаревшим в будущем выпуске.**</span><span class="sxs-lookup"><span data-stu-id="6f2a3-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="6f2a3-109">После установки 1 октября 2017 с помощью этого командлета больше не будет оказывать никакого воздействия, так как эта функция переходит в оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="6f2a3-110">**_https://aka.ms/migratemealerts_** Дополнительные сведения можно найти в разделе.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="6f2a3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f2a3-111">EXAMPLES</span></span>

### <span data-ttu-id="6f2a3-112">Пример 1: Добавление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="6f2a3-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6f2a3-113">Эта команда добавляет или обновляет правило оповещения на основе событий.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="6f2a3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2a3-114">PARAMETERS</span></span>

### <span data-ttu-id="6f2a3-115">-Actions (действия)</span><span class="sxs-lookup"><span data-stu-id="6f2a3-115">-Actions</span></span>
<span data-ttu-id="6f2a3-116">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-116">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="6f2a3-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="6f2a3-117">-Description</span></span>
<span data-ttu-id="6f2a3-118">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="6f2a3-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6f2a3-119">-DisableRule</span></span>
<span data-ttu-id="6f2a3-120">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-120">Disables a rule.</span></span>
<span data-ttu-id="6f2a3-121">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="6f2a3-122">-Level</span><span class="sxs-lookup"><span data-stu-id="6f2a3-122">-Level</span></span>
<span data-ttu-id="6f2a3-123">Указывает уровень события, которое отслеживается правилом.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="6f2a3-124">Указывайте этот параметр только для правил, основанных на событиях.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-124">Specify this parameter only for event-based rules.</span></span>

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

### <span data-ttu-id="6f2a3-125">-Location</span><span class="sxs-lookup"><span data-stu-id="6f2a3-125">-Location</span></span>
<span data-ttu-id="6f2a3-126">Указывает место для правила.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="6f2a3-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f2a3-127">-Name</span></span>
<span data-ttu-id="6f2a3-128">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="6f2a3-129">-Имя_операции</span><span class="sxs-lookup"><span data-stu-id="6f2a3-129">-OperationName</span></span>
<span data-ttu-id="6f2a3-130">Указывает имя операции.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="6f2a3-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f2a3-131">-ResourceGroup</span></span>
<span data-ttu-id="6f2a3-132">Указывает имя группы ресурсов для правила.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="6f2a3-133">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="6f2a3-133">-Status</span></span>
<span data-ttu-id="6f2a3-134">Указывает состояние.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-134">Specifies the status.</span></span>

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

### <span data-ttu-id="6f2a3-135">-Состояние</span><span class="sxs-lookup"><span data-stu-id="6f2a3-135">-SubStatus</span></span>
<span data-ttu-id="6f2a3-136">Указывает подсостояние.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-136">Specifies the substatus.</span></span>

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

### <span data-ttu-id="6f2a3-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f2a3-137">-TargetResourceGroup</span></span>
<span data-ttu-id="6f2a3-138">Указывает группу ресурсов для ресурса, который отслеживается правилом.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6f2a3-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6f2a3-139">-TargetResourceId</span></span>
<span data-ttu-id="6f2a3-140">Указывает идентификатор ресурса, отслеживаемого правилом.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-140">Specifies the ID of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6f2a3-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6f2a3-141">-TargetResourceProvider</span></span>
<span data-ttu-id="6f2a3-142">Указывает поставщика ресурсов для ресурса, который отслеживается правилом.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6f2a3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2a3-143">-DefaultProfile</span></span>
<span data-ttu-id="6f2a3-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f2a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2a3-145">CommonParameters</span></span>
<span data-ttu-id="6f2a3-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f2a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2a3-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2a3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2a3-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f2a3-148">INPUTS</span></span>

## <span data-ttu-id="6f2a3-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2a3-149">OUTPUTS</span></span>

### <span data-ttu-id="6f2a3-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6f2a3-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6f2a3-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f2a3-151">NOTES</span></span>

## <span data-ttu-id="6f2a3-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2a3-152">RELATED LINKS</span></span>

[<span data-ttu-id="6f2a3-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6f2a3-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="6f2a3-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6f2a3-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="6f2a3-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6f2a3-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6f2a3-156">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6f2a3-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="6f2a3-157">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6f2a3-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


