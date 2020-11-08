---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236943"
---
# <span data-ttu-id="8a2e7-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="8a2e7-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="8a2e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2e7-103">Создание источника событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="8a2e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a2e7-104">SYNTAX</span></span>

### <span data-ttu-id="8a2e7-105">eventhub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a2e7-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a2e7-106">iothub</span><span class="sxs-lookup"><span data-stu-id="8a2e7-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a2e7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="8a2e7-108">Создание источника событий в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="8a2e7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-109">EXAMPLES</span></span>

### <span data-ttu-id="8a2e7-110">Пример 1: создание источника событий eventhub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="8a2e7-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="8a2e7-111">Эта команда создает источник событий eventhub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="8a2e7-112">Пример 2: создание источника событий iothub в указанной среде</span><span class="sxs-lookup"><span data-stu-id="8a2e7-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="8a2e7-113">Эта команда создает источник события iothub в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="8a2e7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-114">PARAMETERS</span></span>

### <span data-ttu-id="8a2e7-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-115">-ConsumerGroupName</span></span>
<span data-ttu-id="8a2e7-116">Имя группы потребителей "событие/центр Интернета вещей", в которой хранятся разделы, из которых будут считываться события.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="8a2e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2e7-117">-DefaultProfile</span></span>
<span data-ttu-id="8a2e7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2e7-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-119">-EnvironmentName</span></span>
<span data-ttu-id="8a2e7-120">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="8a2e7-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-121">-EventHubName</span></span>
<span data-ttu-id="8a2e7-122">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="8a2e7-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8a2e7-123">-EventSourceResourceId</span></span>
<span data-ttu-id="8a2e7-124">Идентификатор ресурса источника событий в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="8a2e7-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-125">-IoTHubName</span></span>
<span data-ttu-id="8a2e7-126">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="8a2e7-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-127">-KeyName</span></span>
<span data-ttu-id="8a2e7-128">Имя ключа SAS, предоставляющего службе аналитики временной последовательности доступ к узлу Event/IOT.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="8a2e7-129">-Видах</span><span class="sxs-lookup"><span data-stu-id="8a2e7-129">-Kind</span></span>
<span data-ttu-id="8a2e7-130">Выводятся данные о типе источника событий.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="8a2e7-131">-Location</span><span class="sxs-lookup"><span data-stu-id="8a2e7-131">-Location</span></span>
<span data-ttu-id="8a2e7-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-132">The location of the resource.</span></span>

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

### <span data-ttu-id="8a2e7-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a2e7-133">-Name</span></span>
<span data-ttu-id="8a2e7-134">Имя источника событий.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-134">Name of the event source.</span></span>

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

### <span data-ttu-id="8a2e7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-135">-ResourceGroupName</span></span>
<span data-ttu-id="8a2e7-136">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8a2e7-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="8a2e7-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="8a2e7-138">Имя служебной шины, содержащей концентратор событий.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="8a2e7-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="8a2e7-139">-SharedAccessKey</span></span>
<span data-ttu-id="8a2e7-140">Значение общего ключа доступа, предоставляющее службе аналитики временной последовательности доступ к ресурсам для просмотра событий и Интернет-центра Интернета.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="8a2e7-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a2e7-141">-SubscriptionId</span></span>
<span data-ttu-id="8a2e7-142">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8a2e7-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="8a2e7-143">-Tag</span></span>
<span data-ttu-id="8a2e7-144">Пары "ключ-значение" дополнительных свойств ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="8a2e7-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="8a2e7-146">Свойство события, которое будет использоваться в качестве метки источника событий.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="8a2e7-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a2e7-147">-Confirm</span></span>
<span data-ttu-id="8a2e7-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a2e7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a2e7-149">-WhatIf</span></span>
<span data-ttu-id="8a2e7-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a2e7-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a2e7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2e7-152">CommonParameters</span></span>
<span data-ttu-id="8a2e7-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2e7-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a2e7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2e7-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a2e7-155">INPUTS</span></span>

## <span data-ttu-id="8a2e7-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-156">OUTPUTS</span></span>

### <span data-ttu-id="8a2e7-157">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="8a2e7-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="8a2e7-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a2e7-158">NOTES</span></span>

<span data-ttu-id="8a2e7-159">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-159">ALIASES</span></span>

## <span data-ttu-id="8a2e7-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a2e7-160">RELATED LINKS</span></span>
