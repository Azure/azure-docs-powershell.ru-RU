---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422911"
---
# <span data-ttu-id="8eea2-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="8eea2-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="8eea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eea2-102">SYNOPSIS</span></span>
<span data-ttu-id="8eea2-103">Установить суточную громкость данных для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="8eea2-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="8eea2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8eea2-104">SYNTAX</span></span>

### <span data-ttu-id="8eea2-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8eea2-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eea2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eea2-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eea2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eea2-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8eea2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8eea2-108">DESCRIPTION</span></span>
<span data-ttu-id="8eea2-109">Установить суточную громкость данных для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="8eea2-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="8eea2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8eea2-110">EXAMPLES</span></span>

### <span data-ttu-id="8eea2-111">Пример 1. Настройка ежедневных объемов данных для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="8eea2-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="8eea2-112">Установите суточную громкость данных до 400 ГБ в день и остановите отправку уведомлений, когда нажмем cap для "test" ресурса в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="8eea2-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8eea2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eea2-113">PARAMETERS</span></span>

### <span data-ttu-id="8eea2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eea2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8eea2-115">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="8eea2-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8eea2-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="8eea2-116">-DailyCapGB</span></span>
<span data-ttu-id="8eea2-117">Daily Cap.</span><span class="sxs-lookup"><span data-stu-id="8eea2-117">Daily Cap.</span></span>

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

### <span data-ttu-id="8eea2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eea2-118">-DefaultProfile</span></span>
<span data-ttu-id="8eea2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8eea2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eea2-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="8eea2-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="8eea2-121">Остановить отправку уведомления при нажмем cap.</span><span class="sxs-lookup"><span data-stu-id="8eea2-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="8eea2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8eea2-122">-Name</span></span>
<span data-ttu-id="8eea2-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8eea2-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8eea2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eea2-124">-ResourceGroupName</span></span>
<span data-ttu-id="8eea2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8eea2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8eea2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eea2-126">-ResourceId</span></span>
<span data-ttu-id="8eea2-127">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8eea2-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8eea2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8eea2-128">-Confirm</span></span>
<span data-ttu-id="8eea2-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8eea2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eea2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eea2-130">-WhatIf</span></span>
<span data-ttu-id="8eea2-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eea2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8eea2-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8eea2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eea2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eea2-133">CommonParameters</span></span>
<span data-ttu-id="8eea2-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eea2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eea2-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eea2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eea2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8eea2-136">INPUTS</span></span>

### <span data-ttu-id="8eea2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eea2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8eea2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8eea2-138">System.String</span></span>

## <span data-ttu-id="8eea2-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8eea2-139">OUTPUTS</span></span>

### <span data-ttu-id="8eea2-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8eea2-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="8eea2-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8eea2-141">NOTES</span></span>

## <span data-ttu-id="8eea2-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8eea2-142">RELATED LINKS</span></span>
