---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 3f46445bbdf8f3b9e7a25f4ab5bda0fd11961e00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731652"
---
# <span data-ttu-id="15646-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="15646-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="15646-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15646-102">SYNOPSIS</span></span>
<span data-ttu-id="15646-103">Настройка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="15646-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="15646-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15646-104">SYNTAX</span></span>

### <span data-ttu-id="15646-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15646-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15646-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15646-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15646-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15646-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15646-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15646-108">DESCRIPTION</span></span>
<span data-ttu-id="15646-109">Настройка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="15646-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="15646-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15646-110">EXAMPLES</span></span>

### <span data-ttu-id="15646-111">Пример 1. Установка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="15646-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="15646-112">Установка ежедневной volumen данных в 400GB в день и прекращение отправки уведомлений при попадании на прописные буквы для ресурсов "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="15646-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="15646-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15646-113">PARAMETERS</span></span>

### <span data-ttu-id="15646-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="15646-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="15646-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="15646-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="15646-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="15646-116">-DailyCapGB</span></span>
<span data-ttu-id="15646-117">Ежедневные ограничения.</span><span class="sxs-lookup"><span data-stu-id="15646-117">Daily Cap.</span></span>

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

### <span data-ttu-id="15646-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15646-118">-DefaultProfile</span></span>
<span data-ttu-id="15646-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15646-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15646-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="15646-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="15646-121">Прекращение отправки уведомлений при попадании курсора на прописные.</span><span class="sxs-lookup"><span data-stu-id="15646-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="15646-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15646-122">-Name</span></span>
<span data-ttu-id="15646-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="15646-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="15646-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15646-124">-ResourceGroupName</span></span>
<span data-ttu-id="15646-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15646-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="15646-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15646-126">-ResourceId</span></span>
<span data-ttu-id="15646-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="15646-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="15646-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15646-128">-Confirm</span></span>
<span data-ttu-id="15646-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15646-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15646-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15646-130">-WhatIf</span></span>
<span data-ttu-id="15646-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15646-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15646-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15646-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15646-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15646-133">CommonParameters</span></span>
<span data-ttu-id="15646-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15646-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15646-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15646-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15646-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15646-136">INPUTS</span></span>

### <span data-ttu-id="15646-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="15646-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="15646-138">System. String</span><span class="sxs-lookup"><span data-stu-id="15646-138">System.String</span></span>

## <span data-ttu-id="15646-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15646-139">OUTPUTS</span></span>

### <span data-ttu-id="15646-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="15646-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="15646-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="15646-141">NOTES</span></span>

## <span data-ttu-id="15646-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15646-142">RELATED LINKS</span></span>
