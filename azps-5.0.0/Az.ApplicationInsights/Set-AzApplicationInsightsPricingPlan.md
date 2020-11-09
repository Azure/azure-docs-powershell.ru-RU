---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316247"
---
# <span data-ttu-id="ba7cb-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="ba7cb-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="ba7cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7cb-103">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ba7cb-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="ba7cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba7cb-104">SYNTAX</span></span>

### <span data-ttu-id="ba7cb-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba7cb-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba7cb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba7cb-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba7cb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba7cb-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba7cb-108">DESCRIPTION</span></span>
<span data-ttu-id="ba7cb-109">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ba7cb-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="ba7cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba7cb-110">EXAMPLES</span></span>

### <span data-ttu-id="ba7cb-111">Пример 1. Установка плана ценообразования и сведений о ежедневных объемах данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ba7cb-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="ba7cb-112">Установка для плана цен значения "Basic", установка для ежедневного объема данных 400GB в день и прекращение отправки уведомлений при попадании на прописные буквы для ресурсов "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="ba7cb-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ba7cb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba7cb-113">PARAMETERS</span></span>

### <span data-ttu-id="ba7cb-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ba7cb-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ba7cb-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ba7cb-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="ba7cb-116">-DailyCapGB</span></span>
<span data-ttu-id="ba7cb-117">Ежедневные ограничения.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-117">Daily Cap.</span></span>

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

### <span data-ttu-id="ba7cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7cb-118">-DefaultProfile</span></span>
<span data-ttu-id="ba7cb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba7cb-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="ba7cb-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="ba7cb-121">Прекращение отправки уведомлений при попадании курсора на прописные.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="ba7cb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba7cb-122">-Name</span></span>
<span data-ttu-id="ba7cb-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ba7cb-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="ba7cb-124">-PricingPlan</span></span>
<span data-ttu-id="ba7cb-125">Название плана ценообразования.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="ba7cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba7cb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba7cb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba7cb-128">-ResourceId</span></span>
<span data-ttu-id="ba7cb-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ba7cb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba7cb-130">-Confirm</span></span>
<span data-ttu-id="ba7cb-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba7cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba7cb-132">-WhatIf</span></span>
<span data-ttu-id="ba7cb-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba7cb-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba7cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7cb-135">CommonParameters</span></span>
<span data-ttu-id="ba7cb-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba7cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7cb-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba7cb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7cb-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba7cb-138">INPUTS</span></span>

### <span data-ttu-id="ba7cb-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ba7cb-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ba7cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ba7cb-140">System.String</span></span>

## <span data-ttu-id="ba7cb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba7cb-141">OUTPUTS</span></span>

### <span data-ttu-id="ba7cb-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="ba7cb-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="ba7cb-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba7cb-143">NOTES</span></span>

## <span data-ttu-id="ba7cb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba7cb-144">RELATED LINKS</span></span>
