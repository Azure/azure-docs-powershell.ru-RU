---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732391"
---
# <span data-ttu-id="eb9ed-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="eb9ed-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="eb9ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9ed-103">Настройка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="eb9ed-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb9ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb9ed-104">SYNTAX</span></span>

### <span data-ttu-id="eb9ed-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb9ed-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb9ed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb9ed-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb9ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb9ed-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb9ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb9ed-108">DESCRIPTION</span></span>
<span data-ttu-id="eb9ed-109">Настройка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="eb9ed-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="eb9ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb9ed-110">EXAMPLES</span></span>

### <span data-ttu-id="eb9ed-111">Пример 1. Установка дневного ограничения объема данных для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="eb9ed-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="eb9ed-112">Установка ежедневной volumen данных в 400GB в день и прекращение отправки уведомлений при попадании на прописные буквы для ресурсов "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="eb9ed-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="eb9ed-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb9ed-113">PARAMETERS</span></span>

### <span data-ttu-id="eb9ed-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eb9ed-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="eb9ed-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="eb9ed-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb9ed-116">-Confirm</span></span>
<span data-ttu-id="eb9ed-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9ed-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="eb9ed-118">-DailyCapGB</span></span>
<span data-ttu-id="eb9ed-119">Ежедневные ограничения.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-119">Daily Cap.</span></span>

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

### <span data-ttu-id="eb9ed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9ed-120">-DefaultProfile</span></span>
<span data-ttu-id="eb9ed-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb9ed-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="eb9ed-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="eb9ed-123">Прекращение отправки уведомлений при попадании курсора на прописные.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="eb9ed-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb9ed-124">-Name</span></span>
<span data-ttu-id="eb9ed-125">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-125">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="eb9ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb9ed-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb9ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb9ed-128">-ResourceId</span></span>
<span data-ttu-id="eb9ed-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="eb9ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9ed-130">-WhatIf</span></span>
<span data-ttu-id="eb9ed-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb9ed-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9ed-133">CommonParameters</span></span>
<span data-ttu-id="eb9ed-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9ed-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9ed-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb9ed-136">INPUTS</span></span>

### <span data-ttu-id="eb9ed-137">System. String</span><span class="sxs-lookup"><span data-stu-id="eb9ed-137">System.String</span></span>
<span data-ttu-id="eb9ed-138">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb9ed-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="eb9ed-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb9ed-139">OUTPUTS</span></span>

### <span data-ttu-id="eb9ed-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="eb9ed-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="eb9ed-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb9ed-141">NOTES</span></span>

## <span data-ttu-id="eb9ed-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb9ed-142">RELATED LINKS</span></span>

