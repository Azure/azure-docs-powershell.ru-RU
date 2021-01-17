---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422903"
---
# <span data-ttu-id="3b48f-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="3b48f-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="3b48f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b48f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b48f-103">Настройка тарифного плана и сведений о суточном объеме данных для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="3b48f-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="3b48f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b48f-104">SYNTAX</span></span>

### <span data-ttu-id="3b48f-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b48f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b48f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b48f-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b48f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b48f-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b48f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b48f-108">DESCRIPTION</span></span>
<span data-ttu-id="3b48f-109">Запланируйте цены и сведения о суточном объеме данных для ресурса, анализируйте информацию о приложении.</span><span class="sxs-lookup"><span data-stu-id="3b48f-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="3b48f-110">С помощью этого cmdlet нельзя настроить тарифный план по анализу приложений, созданный после апреля 2018 г.: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="3b48f-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="3b48f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b48f-111">EXAMPLES</span></span>

### <span data-ttu-id="3b48f-112">Пример 1. Оценка тарифного плана и сведений о суточном объеме данных для ресурса, анализируйте приложение</span><span class="sxs-lookup"><span data-stu-id="3b48f-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="3b48f-113">Установите тарифный план "Базовый", установите суточную громкость данных до 400 ГБ в день и остановите отправку уведомлений при нажмом cap для "тестового" ресурса в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="3b48f-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3b48f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b48f-114">PARAMETERS</span></span>

### <span data-ttu-id="3b48f-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3b48f-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3b48f-116">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="3b48f-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="3b48f-117">-DailyCapGB</span></span>
<span data-ttu-id="3b48f-118">Daily Cap.</span><span class="sxs-lookup"><span data-stu-id="3b48f-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b48f-119">-DefaultProfile</span></span>
<span data-ttu-id="3b48f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b48f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b48f-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="3b48f-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="3b48f-122">Остановить отправку уведомления при нажмем cap.</span><span class="sxs-lookup"><span data-stu-id="3b48f-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="3b48f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3b48f-123">-Name</span></span>
<span data-ttu-id="3b48f-124">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3b48f-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="3b48f-125">-PricingPlan</span></span>
<span data-ttu-id="3b48f-126">Название плана цен.</span><span class="sxs-lookup"><span data-stu-id="3b48f-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b48f-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b48f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b48f-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b48f-129">-ResourceId</span></span>
<span data-ttu-id="3b48f-130">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3b48f-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b48f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b48f-131">-Confirm</span></span>
<span data-ttu-id="3b48f-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3b48f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b48f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b48f-133">-WhatIf</span></span>
<span data-ttu-id="3b48f-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b48f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b48f-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b48f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b48f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b48f-136">CommonParameters</span></span>
<span data-ttu-id="3b48f-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b48f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b48f-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b48f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b48f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b48f-139">INPUTS</span></span>

### <span data-ttu-id="3b48f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3b48f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3b48f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3b48f-141">System.String</span></span>

## <span data-ttu-id="3b48f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b48f-142">OUTPUTS</span></span>

### <span data-ttu-id="3b48f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="3b48f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="3b48f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b48f-144">NOTES</span></span>

## <span data-ttu-id="3b48f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b48f-145">RELATED LINKS</span></span>
