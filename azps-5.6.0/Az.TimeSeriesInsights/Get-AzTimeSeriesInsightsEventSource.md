---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: c28d33e4da860a68227228564c55a151a3068329
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977619"
---
# <span data-ttu-id="47c61-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="47c61-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="47c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c61-102">SYNOPSIS</span></span>
<span data-ttu-id="47c61-103">Возвращает источник события с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="47c61-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="47c61-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47c61-104">SYNTAX</span></span>

### <span data-ttu-id="47c61-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47c61-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47c61-106">Получить</span><span class="sxs-lookup"><span data-stu-id="47c61-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47c61-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47c61-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47c61-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47c61-108">DESCRIPTION</span></span>
<span data-ttu-id="47c61-109">Возвращает источник события с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="47c61-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="47c61-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47c61-110">EXAMPLES</span></span>

### <span data-ttu-id="47c61-111">Пример 1. Список всех источников событий в указанной среде</span><span class="sxs-lookup"><span data-stu-id="47c61-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="47c61-112">Эта команда содержит список всех источников событий в указанных средах.</span><span class="sxs-lookup"><span data-stu-id="47c61-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="47c61-113">Пример 2. Получить указанный источник события по имени</span><span class="sxs-lookup"><span data-stu-id="47c61-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="47c61-114">Эта команда получает определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="47c61-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="47c61-115">Пример 3. Получить источник заданного события для объекта</span><span class="sxs-lookup"><span data-stu-id="47c61-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="47c61-116">Эта команда получает определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="47c61-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="47c61-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47c61-117">PARAMETERS</span></span>

### <span data-ttu-id="47c61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c61-118">-DefaultProfile</span></span>
<span data-ttu-id="47c61-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47c61-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c61-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="47c61-120">-EnvironmentName</span></span>
<span data-ttu-id="47c61-121">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47c61-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c61-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47c61-122">-InputObject</span></span>
<span data-ttu-id="47c61-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="47c61-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47c61-124">-Name</span><span class="sxs-lookup"><span data-stu-id="47c61-124">-Name</span></span>
<span data-ttu-id="47c61-125">Имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="47c61-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c61-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c61-126">-ResourceGroupName</span></span>
<span data-ttu-id="47c61-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="47c61-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c61-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47c61-128">-SubscriptionId</span></span>
<span data-ttu-id="47c61-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="47c61-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c61-130">CommonParameters</span></span>
<span data-ttu-id="47c61-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c61-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47c61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c61-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47c61-133">INPUTS</span></span>

### <span data-ttu-id="47c61-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="47c61-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="47c61-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47c61-135">OUTPUTS</span></span>

### <span data-ttu-id="47c61-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="47c61-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="47c61-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47c61-137">NOTES</span></span>

<span data-ttu-id="47c61-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47c61-138">ALIASES</span></span>

<span data-ttu-id="47c61-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="47c61-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47c61-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="47c61-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47c61-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47c61-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47c61-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="47c61-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47c61-143">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="47c61-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="47c61-144">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="47c61-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="47c61-145">`[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="47c61-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="47c61-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="47c61-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47c61-147">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="47c61-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="47c61-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="47c61-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="47c61-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="47c61-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="47c61-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47c61-150">RELATED LINKS</span></span>

