---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235187"
---
# <span data-ttu-id="950f0-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="950f0-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="950f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="950f0-102">SYNOPSIS</span></span>
<span data-ttu-id="950f0-103">Обновляет источник события с указанным именем в указанной подписке, группе ресурсов и средой.</span><span class="sxs-lookup"><span data-stu-id="950f0-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="950f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="950f0-104">SYNTAX</span></span>

### <span data-ttu-id="950f0-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="950f0-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="950f0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="950f0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="950f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="950f0-107">DESCRIPTION</span></span>
<span data-ttu-id="950f0-108">Обновляет источник события с указанным именем в указанной подписке, группе ресурсов и средой.</span><span class="sxs-lookup"><span data-stu-id="950f0-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="950f0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="950f0-109">EXAMPLES</span></span>

### <span data-ttu-id="950f0-110">Пример 1: обновление указанного источника событий по имени</span><span class="sxs-lookup"><span data-stu-id="950f0-110">Example 1: Update a specified event source by name</span></span>
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

<span data-ttu-id="950f0-111">Эта команда обновляет определенный источник событий.</span><span class="sxs-lookup"><span data-stu-id="950f0-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="950f0-112">Пример 3: обновление указанного источника событий по объекту</span><span class="sxs-lookup"><span data-stu-id="950f0-112">Example 3: Update a specified event source by object</span></span>
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

<span data-ttu-id="950f0-113">Эта команда обновляет определенный источник событий.</span><span class="sxs-lookup"><span data-stu-id="950f0-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="950f0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="950f0-114">PARAMETERS</span></span>

### <span data-ttu-id="950f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950f0-115">-DefaultProfile</span></span>
<span data-ttu-id="950f0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="950f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="950f0-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="950f0-117">-EnvironmentName</span></span>
<span data-ttu-id="950f0-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="950f0-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="950f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="950f0-119">-InputObject</span></span>
<span data-ttu-id="950f0-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="950f0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="950f0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="950f0-121">-Name</span></span>
<span data-ttu-id="950f0-122">Название источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="950f0-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="950f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="950f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="950f0-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="950f0-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="950f0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="950f0-125">-SubscriptionId</span></span>
<span data-ttu-id="950f0-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="950f0-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="950f0-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="950f0-127">-Tag</span></span>
<span data-ttu-id="950f0-128">Пары "ключ-значение" дополнительных свойств для источника событий.</span><span class="sxs-lookup"><span data-stu-id="950f0-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="950f0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="950f0-129">-Confirm</span></span>
<span data-ttu-id="950f0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="950f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="950f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="950f0-131">-WhatIf</span></span>
<span data-ttu-id="950f0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="950f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="950f0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="950f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="950f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950f0-134">CommonParameters</span></span>
<span data-ttu-id="950f0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="950f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950f0-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="950f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950f0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="950f0-137">INPUTS</span></span>

### <span data-ttu-id="950f0-138">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="950f0-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="950f0-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="950f0-139">OUTPUTS</span></span>

### <span data-ttu-id="950f0-140">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="950f0-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="950f0-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="950f0-141">NOTES</span></span>

<span data-ttu-id="950f0-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="950f0-142">ALIASES</span></span>

<span data-ttu-id="950f0-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="950f0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="950f0-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="950f0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="950f0-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="950f0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="950f0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="950f0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="950f0-147">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="950f0-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="950f0-148">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="950f0-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="950f0-149">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="950f0-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="950f0-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="950f0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="950f0-151">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="950f0-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="950f0-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="950f0-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="950f0-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="950f0-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="950f0-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="950f0-154">RELATED LINKS</span></span>

