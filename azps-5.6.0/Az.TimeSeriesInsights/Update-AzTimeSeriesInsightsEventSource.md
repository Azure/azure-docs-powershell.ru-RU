---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7e4063858edaa6180e1f57bc05898ae170284546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987426"
---
# <span data-ttu-id="ae7d3-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="ae7d3-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="ae7d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7d3-103">Обновляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="ae7d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae7d3-104">SYNTAX</span></span>

### <span data-ttu-id="ae7d3-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae7d3-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ae7d3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ae7d3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae7d3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae7d3-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7d3-108">Обновляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="ae7d3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae7d3-109">EXAMPLES</span></span>

### <span data-ttu-id="ae7d3-110">Пример 1. Обновление указанного источника событий по имени</span><span class="sxs-lookup"><span data-stu-id="ae7d3-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="ae7d3-111">Эта команда обновляет определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="ae7d3-112">Пример 3. Обновление источника события с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="ae7d3-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="ae7d3-113">Эта команда обновляет определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="ae7d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae7d3-114">PARAMETERS</span></span>

### <span data-ttu-id="ae7d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7d3-115">-DefaultProfile</span></span>
<span data-ttu-id="ae7d3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ae7d3-117">-EnvironmentName</span></span>
<span data-ttu-id="ae7d3-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae7d3-119">-InputObject</span></span>
<span data-ttu-id="ae7d3-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ae7d3-121">-Name</span></span>
<span data-ttu-id="ae7d3-122">Имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae7d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae7d3-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae7d3-125">-SubscriptionId</span></span>
<span data-ttu-id="ae7d3-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae7d3-127">-Tag</span></span>
<span data-ttu-id="ae7d3-128">Пары значений ключа с дополнительными свойствами для источника событий.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-128">Key-value pairs of additional properties for the event source.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae7d3-129">-Confirm</span></span>
<span data-ttu-id="ae7d3-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7d3-131">-WhatIf</span></span>
<span data-ttu-id="ae7d3-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae7d3-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7d3-134">CommonParameters</span></span>
<span data-ttu-id="ae7d3-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7d3-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae7d3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7d3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae7d3-137">INPUTS</span></span>

### <span data-ttu-id="ae7d3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="ae7d3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ae7d3-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae7d3-139">OUTPUTS</span></span>

### <span data-ttu-id="ae7d3-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="ae7d3-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="ae7d3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae7d3-141">NOTES</span></span>

<span data-ttu-id="ae7d3-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae7d3-142">ALIASES</span></span>

<span data-ttu-id="ae7d3-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ae7d3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae7d3-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae7d3-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae7d3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ae7d3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae7d3-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ae7d3-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="ae7d3-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ae7d3-149">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ae7d3-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ae7d3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae7d3-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ae7d3-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ae7d3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="ae7d3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ae7d3-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae7d3-154">RELATED LINKS</span></span>

