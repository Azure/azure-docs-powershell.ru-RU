---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505825"
---
# <span data-ttu-id="85f83-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="85f83-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="85f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f83-102">SYNOPSIS</span></span>
<span data-ttu-id="85f83-103">Создайте источник событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="85f83-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="85f83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85f83-104">SYNTAX</span></span>

### <span data-ttu-id="85f83-105">юthub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85f83-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="85f83-106">iothub</span><span class="sxs-lookup"><span data-stu-id="85f83-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85f83-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85f83-107">DESCRIPTION</span></span>
<span data-ttu-id="85f83-108">Создайте источник событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="85f83-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="85f83-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85f83-109">EXAMPLES</span></span>

### <span data-ttu-id="85f83-110">Пример 1. Создание источника событий евартub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="85f83-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="85f83-111">Эта команда создает источник событий евартub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="85f83-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="85f83-112">Пример 2. Создание источника событий iothub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="85f83-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="85f83-113">Эта команда создает источник событий iothub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="85f83-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="85f83-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85f83-114">PARAMETERS</span></span>

### <span data-ttu-id="85f83-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="85f83-115">-ConsumerGroupName</span></span>
<span data-ttu-id="85f83-116">Имя группы потребителей события/iot-концентратора, которая содержит разделы, из которых будут читаться события.</span><span class="sxs-lookup"><span data-stu-id="85f83-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f83-117">-DefaultProfile</span></span>
<span data-ttu-id="85f83-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85f83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f83-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="85f83-119">-EnvironmentName</span></span>
<span data-ttu-id="85f83-120">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85f83-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="85f83-121">-EventHubName</span></span>
<span data-ttu-id="85f83-122">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="85f83-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="85f83-123">-EventSourceResourceId</span></span>
<span data-ttu-id="85f83-124">Код ресурса источника событий в Диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="85f83-124">The resource id of the event source in Azure Resource Manager.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="85f83-125">-IoTHubName</span></span>
<span data-ttu-id="85f83-126">Имя концентратора iot.</span><span class="sxs-lookup"><span data-stu-id="85f83-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="85f83-127">-KeyName</span></span>
<span data-ttu-id="85f83-128">Имя ключа SAS, который предоставляет службе Time Series Insights доступ к центру событий и iot.</span><span class="sxs-lookup"><span data-stu-id="85f83-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="85f83-129">-Kind</span></span>
<span data-ttu-id="85f83-130">Тип источника события.</span><span class="sxs-lookup"><span data-stu-id="85f83-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-131">-Location</span><span class="sxs-lookup"><span data-stu-id="85f83-131">-Location</span></span>
<span data-ttu-id="85f83-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="85f83-132">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-133">-Name</span><span class="sxs-lookup"><span data-stu-id="85f83-133">-Name</span></span>
<span data-ttu-id="85f83-134">Имя источника события.</span><span class="sxs-lookup"><span data-stu-id="85f83-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f83-135">-ResourceGroupName</span></span>
<span data-ttu-id="85f83-136">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="85f83-136">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="85f83-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="85f83-138">Название сервисного автобус, который содержит центр событий.</span><span class="sxs-lookup"><span data-stu-id="85f83-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="85f83-139">-SharedAccessKey</span></span>
<span data-ttu-id="85f83-140">Значение ключа общего доступа, который предоставляет службе Time Series Insights доступ с чтением к центру события или iot.</span><span class="sxs-lookup"><span data-stu-id="85f83-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85f83-141">-SubscriptionId</span></span>
<span data-ttu-id="85f83-142">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="85f83-142">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="85f83-143">-Tag</span></span>
<span data-ttu-id="85f83-144">Пары значений ключа с дополнительными свойствами для ресурса.</span><span class="sxs-lookup"><span data-stu-id="85f83-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="85f83-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="85f83-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="85f83-146">Свойство события, которое будет использоваться в качестве timestamp источника событий.</span><span class="sxs-lookup"><span data-stu-id="85f83-146">The event property that will be used as the event source's timestamp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f83-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85f83-147">-Confirm</span></span>
<span data-ttu-id="85f83-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="85f83-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f83-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f83-149">-WhatIf</span></span>
<span data-ttu-id="85f83-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f83-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f83-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="85f83-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f83-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f83-152">CommonParameters</span></span>
<span data-ttu-id="85f83-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f83-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f83-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85f83-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f83-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85f83-155">INPUTS</span></span>

## <span data-ttu-id="85f83-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85f83-156">OUTPUTS</span></span>

### <span data-ttu-id="85f83-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="85f83-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="85f83-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85f83-158">NOTES</span></span>

<span data-ttu-id="85f83-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="85f83-159">ALIASES</span></span>

## <span data-ttu-id="85f83-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85f83-160">RELATED LINKS</span></span>

