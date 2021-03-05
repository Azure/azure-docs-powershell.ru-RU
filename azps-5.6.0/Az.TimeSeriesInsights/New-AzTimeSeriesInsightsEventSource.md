---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995840"
---
# <span data-ttu-id="17389-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="17389-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="17389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17389-102">SYNOPSIS</span></span>
<span data-ttu-id="17389-103">Создайте источник событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="17389-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="17389-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17389-104">SYNTAX</span></span>

### <span data-ttu-id="17389-105">юthub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17389-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17389-106">iothub</span><span class="sxs-lookup"><span data-stu-id="17389-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17389-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17389-107">DESCRIPTION</span></span>
<span data-ttu-id="17389-108">Создайте источник событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="17389-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="17389-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17389-109">EXAMPLES</span></span>

### <span data-ttu-id="17389-110">Пример 1. Создание источника событий евартub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="17389-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="17389-111">Эта команда создает источник событий евартub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="17389-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="17389-112">Пример 2. Создание источника событий iothub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="17389-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="17389-113">Эта команда создает источник событий iothub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="17389-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="17389-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17389-114">PARAMETERS</span></span>

### <span data-ttu-id="17389-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="17389-115">-ConsumerGroupName</span></span>
<span data-ttu-id="17389-116">Имя группы потребителей события/iot-концентратора, которая содержит разделы, из которых будут читаться события.</span><span class="sxs-lookup"><span data-stu-id="17389-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="17389-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17389-117">-DefaultProfile</span></span>
<span data-ttu-id="17389-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17389-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17389-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="17389-119">-EnvironmentName</span></span>
<span data-ttu-id="17389-120">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17389-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="17389-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="17389-121">-EventHubName</span></span>
<span data-ttu-id="17389-122">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="17389-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="17389-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="17389-123">-EventSourceResourceId</span></span>
<span data-ttu-id="17389-124">Код ресурса источника событий в Диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="17389-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="17389-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="17389-125">-IoTHubName</span></span>
<span data-ttu-id="17389-126">Имя концентратора iot.</span><span class="sxs-lookup"><span data-stu-id="17389-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="17389-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="17389-127">-KeyName</span></span>
<span data-ttu-id="17389-128">Имя ключа SAS, который предоставляет службе Time Series Insights доступ к центру событий и iot.</span><span class="sxs-lookup"><span data-stu-id="17389-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="17389-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="17389-129">-Kind</span></span>
<span data-ttu-id="17389-130">Тип источника события.</span><span class="sxs-lookup"><span data-stu-id="17389-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="17389-131">-Location</span><span class="sxs-lookup"><span data-stu-id="17389-131">-Location</span></span>
<span data-ttu-id="17389-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="17389-132">The location of the resource.</span></span>

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

### <span data-ttu-id="17389-133">-Name</span><span class="sxs-lookup"><span data-stu-id="17389-133">-Name</span></span>
<span data-ttu-id="17389-134">Имя источника события.</span><span class="sxs-lookup"><span data-stu-id="17389-134">Name of the event source.</span></span>

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

### <span data-ttu-id="17389-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17389-135">-ResourceGroupName</span></span>
<span data-ttu-id="17389-136">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="17389-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="17389-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="17389-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="17389-138">Название сервисного автобус, который содержит центр событий.</span><span class="sxs-lookup"><span data-stu-id="17389-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="17389-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="17389-139">-SharedAccessKey</span></span>
<span data-ttu-id="17389-140">Значение ключа общего доступа, который предоставляет службе Time Series Insights доступ с чтением к центру события или iot.</span><span class="sxs-lookup"><span data-stu-id="17389-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="17389-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17389-141">-SubscriptionId</span></span>
<span data-ttu-id="17389-142">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="17389-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="17389-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="17389-143">-Tag</span></span>
<span data-ttu-id="17389-144">Пары ключевых значений дополнительных свойств для ресурса.</span><span class="sxs-lookup"><span data-stu-id="17389-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="17389-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="17389-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="17389-146">Свойство события, которое будет использоваться в качестве timestamp источника событий.</span><span class="sxs-lookup"><span data-stu-id="17389-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="17389-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17389-147">-Confirm</span></span>
<span data-ttu-id="17389-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17389-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17389-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17389-149">-WhatIf</span></span>
<span data-ttu-id="17389-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17389-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17389-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17389-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17389-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17389-152">CommonParameters</span></span>
<span data-ttu-id="17389-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17389-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17389-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17389-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17389-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17389-155">INPUTS</span></span>

## <span data-ttu-id="17389-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17389-156">OUTPUTS</span></span>

### <span data-ttu-id="17389-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="17389-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="17389-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17389-158">NOTES</span></span>

<span data-ttu-id="17389-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="17389-159">ALIASES</span></span>

## <span data-ttu-id="17389-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17389-160">RELATED LINKS</span></span>

