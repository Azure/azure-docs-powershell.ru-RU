---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568023"
---
# <span data-ttu-id="e5e46-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="e5e46-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="e5e46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5e46-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e46-103">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="e5e46-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5e46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5e46-104">SYNTAX</span></span>

### <span data-ttu-id="e5e46-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5e46-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e46-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5e46-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e46-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5e46-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5e46-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e46-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e46-109">Настройка плана ценообразования и сведений об объеме ежедневных данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="e5e46-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="e5e46-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5e46-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e46-111">Пример 1. Установка плана ценообразования и сведений о ежедневных объемах данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="e5e46-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="e5e46-112">Установка для плана цен значения "Basic", установка ежедневной volumen данных на 400GB в день и прекращение отправки уведомлений при попадании на прописные буквы для ресурсов "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="e5e46-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e5e46-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5e46-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e46-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e5e46-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e5e46-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e5e46-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5e46-116">-Confirm</span></span>
<span data-ttu-id="e5e46-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5e46-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="e5e46-118">-DailyCapGB</span></span>
<span data-ttu-id="e5e46-119">Ежедневные ограничения.</span><span class="sxs-lookup"><span data-stu-id="e5e46-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e46-120">-DefaultProfile</span></span>
<span data-ttu-id="e5e46-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e46-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e46-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="e5e46-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="e5e46-123">Прекращение отправки уведомлений при попадании курсора на прописные.</span><span class="sxs-lookup"><span data-stu-id="e5e46-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5e46-124">-Name</span></span>
<span data-ttu-id="e5e46-125">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e5e46-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="e5e46-126">-PricingPlan</span></span>
<span data-ttu-id="e5e46-127">Название плана ценообразования.</span><span class="sxs-lookup"><span data-stu-id="e5e46-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e46-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5e46-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5e46-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e46-130">-ResourceId</span></span>
<span data-ttu-id="e5e46-131">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e5e46-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e46-132">-WhatIf</span></span>
<span data-ttu-id="e5e46-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5e46-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5e46-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5e46-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e46-135">CommonParameters</span></span>
<span data-ttu-id="e5e46-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5e46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e46-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e46-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e46-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5e46-138">INPUTS</span></span>

### <span data-ttu-id="e5e46-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e46-139">System.String</span></span>
<span data-ttu-id="e5e46-140">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e46-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="e5e46-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e46-141">OUTPUTS</span></span>

### <span data-ttu-id="e5e46-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="e5e46-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="e5e46-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5e46-143">NOTES</span></span>

## <span data-ttu-id="e5e46-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5e46-144">RELATED LINKS</span></span>

