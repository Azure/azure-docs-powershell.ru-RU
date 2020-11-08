---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243728"
---
# <span data-ttu-id="d19ec-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="d19ec-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="d19ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d19ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d19ec-103">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d19ec-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="d19ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d19ec-104">SYNTAX</span></span>

### <span data-ttu-id="d19ec-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d19ec-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19ec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d19ec-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d19ec-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d19ec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19ec-108">DESCRIPTION</span></span>
<span data-ttu-id="d19ec-109">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d19ec-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="d19ec-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d19ec-110">EXAMPLES</span></span>

### <span data-ttu-id="d19ec-111">Пример 1. Установка плана ценообразования и сведений о ежедневных объемах данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d19ec-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="d19ec-112">Установка для плана цен значения "Basic", установка для ежедневного объема данных 400GB в день и прекращение отправки уведомлений при попадании на прописные буквы для ресурсов "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="d19ec-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="d19ec-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d19ec-113">PARAMETERS</span></span>

### <span data-ttu-id="d19ec-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d19ec-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d19ec-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d19ec-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d19ec-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="d19ec-116">-DailyCapGB</span></span>
<span data-ttu-id="d19ec-117">Ежедневные ограничения.</span><span class="sxs-lookup"><span data-stu-id="d19ec-117">Daily Cap.</span></span>

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

### <span data-ttu-id="d19ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19ec-118">-DefaultProfile</span></span>
<span data-ttu-id="d19ec-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d19ec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19ec-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="d19ec-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="d19ec-121">Прекращение отправки уведомлений при попадании курсора на прописные.</span><span class="sxs-lookup"><span data-stu-id="d19ec-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="d19ec-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d19ec-122">-Name</span></span>
<span data-ttu-id="d19ec-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d19ec-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d19ec-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="d19ec-124">-PricingPlan</span></span>
<span data-ttu-id="d19ec-125">Название плана ценообразования.</span><span class="sxs-lookup"><span data-stu-id="d19ec-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="d19ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="d19ec-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d19ec-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d19ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19ec-128">-ResourceId</span></span>
<span data-ttu-id="d19ec-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d19ec-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d19ec-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d19ec-130">-Confirm</span></span>
<span data-ttu-id="d19ec-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d19ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19ec-132">-WhatIf</span></span>
<span data-ttu-id="d19ec-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d19ec-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d19ec-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d19ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19ec-135">CommonParameters</span></span>
<span data-ttu-id="d19ec-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d19ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19ec-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19ec-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19ec-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d19ec-138">INPUTS</span></span>

### <span data-ttu-id="d19ec-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d19ec-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="d19ec-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d19ec-140">System.String</span></span>

## <span data-ttu-id="d19ec-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19ec-141">OUTPUTS</span></span>

### <span data-ttu-id="d19ec-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="d19ec-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="d19ec-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d19ec-143">NOTES</span></span>

## <span data-ttu-id="d19ec-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d19ec-144">RELATED LINKS</span></span>
