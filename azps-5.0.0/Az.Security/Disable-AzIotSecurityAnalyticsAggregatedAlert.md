---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248177"
---
# <span data-ttu-id="40c4d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="40c4d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="40c4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="40c4d-103">Закрыть агрегированное оповещение IOT</span><span class="sxs-lookup"><span data-stu-id="40c4d-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="40c4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40c4d-104">SYNTAX</span></span>

### <span data-ttu-id="40c4d-105">SolutionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40c4d-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c4d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="40c4d-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c4d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="40c4d-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c4d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="40c4d-109">Командлет Disable-AzIotSecurityAnalyticsAggregatedAlert закрывает конкретное оповещение aggragated на устройствах центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="40c4d-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="40c4d-110">Имя статистического оповещения — это сочетание типа оповещения и даты aggragted оповещения, отделенное друг от друга.</span><span class="sxs-lookup"><span data-stu-id="40c4d-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="40c4d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40c4d-111">EXAMPLES</span></span>

### <span data-ttu-id="40c4d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40c4d-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="40c4d-113">Отклонить агрегированное оповещение "IoT_SucessfulLocalLogin/2020-03-15" (имя объединено из типа оповещения и его агрегированная Дата) из решения безопасности IoT "MySolutionName" в группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="40c4d-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="40c4d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40c4d-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="40c4d-115">Закрыть объединенное оповещение с идентификатором ресурса "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="40c4d-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="40c4d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40c4d-116">PARAMETERS</span></span>

### <span data-ttu-id="40c4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c4d-117">-DefaultProfile</span></span>
<span data-ttu-id="40c4d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40c4d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c4d-119">-InputObject</span></span>
<span data-ttu-id="40c4d-120">Объект input.</span><span class="sxs-lookup"><span data-stu-id="40c4d-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40c4d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40c4d-121">-Name</span></span>
<span data-ttu-id="40c4d-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="40c4d-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c4d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40c4d-123">-PassThru</span></span>
<span data-ttu-id="40c4d-124">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="40c4d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="40c4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="40c4d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40c4d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40c4d-127">-ResourceId</span></span>
<span data-ttu-id="40c4d-128">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="40c4d-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c4d-129">-Имя_решения</span><span class="sxs-lookup"><span data-stu-id="40c4d-129">-SolutionName</span></span>
<span data-ttu-id="40c4d-130">Имя решения</span><span class="sxs-lookup"><span data-stu-id="40c4d-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c4d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40c4d-131">-Confirm</span></span>
<span data-ttu-id="40c4d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40c4d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c4d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c4d-133">-WhatIf</span></span>
<span data-ttu-id="40c4d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40c4d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c4d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40c4d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c4d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c4d-136">CommonParameters</span></span>
<span data-ttu-id="40c4d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40c4d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c4d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40c4d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c4d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40c4d-139">INPUTS</span></span>

### <span data-ttu-id="40c4d-140">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="40c4d-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="40c4d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="40c4d-141">System.String</span></span>

## <span data-ttu-id="40c4d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c4d-142">OUTPUTS</span></span>

### <span data-ttu-id="40c4d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40c4d-143">System.Boolean</span></span>

## <span data-ttu-id="40c4d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="40c4d-144">NOTES</span></span>

## <span data-ttu-id="40c4d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40c4d-145">RELATED LINKS</span></span>
