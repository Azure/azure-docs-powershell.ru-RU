---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517797"
---
# <span data-ttu-id="f238d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="f238d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="f238d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f238d-102">SYNOPSIS</span></span>
<span data-ttu-id="f238d-103">Отклонять агрегированное оповещение</span><span class="sxs-lookup"><span data-stu-id="f238d-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="f238d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f238d-104">SYNTAX</span></span>

### <span data-ttu-id="f238d-105">SolutionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f238d-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f238d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f238d-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f238d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f238d-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f238d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f238d-108">DESCRIPTION</span></span>
<span data-ttu-id="f238d-109">Этот Disable-AzIotSecurityAnalyticsAggregatedAlert отклонить определенное оповещение на устройствах iot-концентратора.</span><span class="sxs-lookup"><span data-stu-id="f238d-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="f238d-110">Имя агрегированных оповещений — это сочетание типа оповещений и совокупной даты, разделенных на "/".</span><span class="sxs-lookup"><span data-stu-id="f238d-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="f238d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f238d-111">EXAMPLES</span></span>

### <span data-ttu-id="f238d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f238d-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="f238d-113">Отклонение агрегированного оповещения "IoT_SucessfulLocalLogin/2020-03-15" (имя из типа оповещения и даты его обобщения) из решения для безопасности IoT "MySolutionName" в группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="f238d-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="f238d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f238d-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="f238d-115">Отклонение агрегированного оповещения с помощью ИД ресурса "/subscriptions/XXXXXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="f238d-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="f238d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f238d-116">PARAMETERS</span></span>

### <span data-ttu-id="f238d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f238d-117">-DefaultProfile</span></span>
<span data-ttu-id="f238d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f238d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f238d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f238d-119">-InputObject</span></span>
<span data-ttu-id="f238d-120">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="f238d-120">Input Object.</span></span>

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

### <span data-ttu-id="f238d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f238d-121">-Name</span></span>
<span data-ttu-id="f238d-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f238d-122">Resource name.</span></span>

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

### <span data-ttu-id="f238d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f238d-123">-PassThru</span></span>
<span data-ttu-id="f238d-124">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="f238d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f238d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f238d-125">-ResourceGroupName</span></span>
<span data-ttu-id="f238d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f238d-126">Resource group name.</span></span>

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

### <span data-ttu-id="f238d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f238d-127">-ResourceId</span></span>
<span data-ttu-id="f238d-128">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="f238d-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f238d-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="f238d-129">-SolutionName</span></span>
<span data-ttu-id="f238d-130">Название решения</span><span class="sxs-lookup"><span data-stu-id="f238d-130">Solution name</span></span>

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

### <span data-ttu-id="f238d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f238d-131">-Confirm</span></span>
<span data-ttu-id="f238d-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f238d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f238d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f238d-133">-WhatIf</span></span>
<span data-ttu-id="f238d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f238d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f238d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f238d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f238d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f238d-136">CommonParameters</span></span>
<span data-ttu-id="f238d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f238d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f238d-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f238d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f238d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f238d-139">INPUTS</span></span>

### <span data-ttu-id="f238d-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="f238d-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="f238d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f238d-141">System.String</span></span>

## <span data-ttu-id="f238d-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f238d-142">OUTPUTS</span></span>

### <span data-ttu-id="f238d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f238d-143">System.Boolean</span></span>

## <span data-ttu-id="f238d-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f238d-144">NOTES</span></span>

## <span data-ttu-id="f238d-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f238d-145">RELATED LINKS</span></span>
