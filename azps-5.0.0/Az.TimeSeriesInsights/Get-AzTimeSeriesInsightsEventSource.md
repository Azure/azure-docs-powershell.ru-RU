---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247906"
---
# <span data-ttu-id="cf266-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="cf266-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="cf266-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf266-102">SYNOPSIS</span></span>
<span data-ttu-id="cf266-103">Возвращает источник событий с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="cf266-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="cf266-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf266-104">SYNTAX</span></span>

### <span data-ttu-id="cf266-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf266-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf266-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cf266-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf266-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf266-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf266-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf266-108">DESCRIPTION</span></span>
<span data-ttu-id="cf266-109">Возвращает источник событий с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="cf266-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="cf266-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf266-110">EXAMPLES</span></span>

### <span data-ttu-id="cf266-111">Пример 1: список всех источников событий в указанной среде</span><span class="sxs-lookup"><span data-stu-id="cf266-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="cf266-112">Эта команда перечисляет все источники событий в указанных средах.</span><span class="sxs-lookup"><span data-stu-id="cf266-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="cf266-113">Пример 2: получение указанного источника событий по имени</span><span class="sxs-lookup"><span data-stu-id="cf266-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="cf266-114">Эта команда возвращает определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="cf266-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="cf266-115">Пример 3: получение указанного источника событий по объекту</span><span class="sxs-lookup"><span data-stu-id="cf266-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="cf266-116">Эта команда возвращает определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="cf266-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="cf266-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf266-117">PARAMETERS</span></span>

### <span data-ttu-id="cf266-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf266-118">-DefaultProfile</span></span>
<span data-ttu-id="cf266-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf266-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf266-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="cf266-120">-EnvironmentName</span></span>
<span data-ttu-id="cf266-121">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf266-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="cf266-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf266-122">-InputObject</span></span>
<span data-ttu-id="cf266-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cf266-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf266-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf266-124">-Name</span></span>
<span data-ttu-id="cf266-125">Название источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="cf266-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="cf266-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf266-126">-ResourceGroupName</span></span>
<span data-ttu-id="cf266-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cf266-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="cf266-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf266-128">-SubscriptionId</span></span>
<span data-ttu-id="cf266-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cf266-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cf266-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf266-130">CommonParameters</span></span>
<span data-ttu-id="cf266-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf266-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf266-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf266-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf266-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf266-133">INPUTS</span></span>

### <span data-ttu-id="cf266-134">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="cf266-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="cf266-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf266-135">OUTPUTS</span></span>

### <span data-ttu-id="cf266-136">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="cf266-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="cf266-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf266-137">NOTES</span></span>

<span data-ttu-id="cf266-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cf266-138">ALIASES</span></span>

<span data-ttu-id="cf266-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cf266-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf266-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf266-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf266-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf266-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf266-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="cf266-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf266-143">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="cf266-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="cf266-144">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="cf266-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="cf266-145">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="cf266-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="cf266-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cf266-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf266-147">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="cf266-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="cf266-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cf266-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="cf266-149">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cf266-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cf266-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf266-150">RELATED LINKS</span></span>

