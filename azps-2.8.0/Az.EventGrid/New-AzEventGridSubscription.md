---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 5aa5089520663d6679df44eae19bcfd322bbaff7
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395362"
---
# <span data-ttu-id="20f39-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="20f39-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="20f39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20f39-102">SYNOPSIS</span></span>
<span data-ttu-id="20f39-103">Создает новую подписку на событие сетки событий Azure в разделе, ресурсе Azure, подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20f39-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="20f39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20f39-104">SYNTAX</span></span>

### <span data-ttu-id="20f39-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20f39-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20f39-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f39-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f39-113">DESCRIPTION</span></span>
<span data-ttu-id="20f39-114">Создайте новую подписку на событие в разделе сетки событий Azure — поддерживаемом ресурсе Azure, подпиской на Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20f39-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="20f39-115">Чтобы создать подписку на события для выбранной подписки Azure, укажите имя и конечную точку для события.</span><span class="sxs-lookup"><span data-stu-id="20f39-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="20f39-116">Чтобы создать подписку на событие для группы ресурсов, укажите имя группы ресурсов в дополнение к имени подписки на событие и конечной точке назначения.</span><span class="sxs-lookup"><span data-stu-id="20f39-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="20f39-117">Чтобы создать подписку на события в разделе сетки событий Azure, укажите название раздела также.</span><span class="sxs-lookup"><span data-stu-id="20f39-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="20f39-118">Чтобы создать подписку на событие для поддерживаемого ресурса Azure, укажите полный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="20f39-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="20f39-119">Чтобы просмотреть список поддерживаемых типов, выполните командлет Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="20f39-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="20f39-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20f39-120">EXAMPLES</span></span>

### <span data-ttu-id="20f39-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20f39-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="20f39-122">Создает новую подписку \` на событие EventSubscription1 \` на сетку событий Azure, \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="20f39-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="20f39-123">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20f39-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="20f39-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20f39-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="20f39-125">Создает новую подписку на событие \` EventSubscription1 \` к группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="20f39-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="20f39-126">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20f39-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="20f39-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="20f39-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="20f39-128">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="20f39-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="20f39-129">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20f39-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="20f39-130">Пример 4</span><span class="sxs-lookup"><span data-stu-id="20f39-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="20f39-131">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="20f39-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="20f39-132">Эта подписка на события указывает дополнительные фильтры для типов событий и субъектов, и только события, соответствующие этим фильтрам, будут доставляться в конечную точку назначения.</span><span class="sxs-lookup"><span data-stu-id="20f39-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="20f39-133">Пример 5</span><span class="sxs-lookup"><span data-stu-id="20f39-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="20f39-134">Создает новую подписку на \` событие \` , EventSubscription1 на текущую выбранную подписку Azure с указанным центром событий в качестве места назначения для событий.</span><span class="sxs-lookup"><span data-stu-id="20f39-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="20f39-135">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20f39-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="20f39-136">Пример 6</span><span class="sxs-lookup"><span data-stu-id="20f39-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="20f39-137">Создает новую подписку на событие, \` EventSubscription1 \` с заданной конечной точкой веб-перехватчика в пространстве имен EventHub `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="20f39-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="20f39-138">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20f39-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="20f39-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20f39-139">PARAMETERS</span></span>

### <span data-ttu-id="20f39-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="20f39-140">-AdvancedFilter</span></span>
<span data-ttu-id="20f39-141">Расширенный фильтр, указывающий массив из нескольких значений Hashtable, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="20f39-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="20f39-142">У каждого значения Hashtable есть следующие ключи: сведения об операции, ключе, значении или значениях.</span><span class="sxs-lookup"><span data-stu-id="20f39-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="20f39-143">Может принимать одно из следующих значений: Number in, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringNotIn, StringBeginsWith или StringEndsWith.</span><span class="sxs-lookup"><span data-stu-id="20f39-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="20f39-144">Key представляет свойство полезных данных, к которому применяются дополнительные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="20f39-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="20f39-145">Наконец, значение или значения представляют значение или набор значений, которые должны быть сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="20f39-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="20f39-146">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="20f39-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="20f39-147">В качестве примера параметров расширенного фильтра: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1 = @ {operator = "Number in"; Key = "Data. key1"; Значения = @ (1; 2)} и $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Тема"; Значения = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="20f39-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="20f39-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="20f39-149">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="20f39-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="20f39-150">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="20f39-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="20f39-151">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="20f39-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f39-152">-DefaultProfile</span></span>
<span data-ttu-id="20f39-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20f39-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20f39-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="20f39-154">-DomainInputObject</span></span>
<span data-ttu-id="20f39-155">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="20f39-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-156">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="20f39-156">-DomainName</span></span>
<span data-ttu-id="20f39-157">Имя домена сетки событий, для которого нужно создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="20f39-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="20f39-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="20f39-159">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="20f39-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="20f39-160">-DomainTopicName</span></span>
<span data-ttu-id="20f39-161">Имя домена, для которого требуется создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="20f39-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-162">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="20f39-162">-Endpoint</span></span>
<span data-ttu-id="20f39-163">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="20f39-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="20f39-164">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub, очередь хранилища, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="20f39-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="20f39-165">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="20f39-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="20f39-166">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="20f39-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="20f39-167">-EndpointType</span></span>
<span data-ttu-id="20f39-168">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="20f39-168">Endpoint Type.</span></span>
<span data-ttu-id="20f39-169">Это может быть веб-перехватчик, eventhub, storagequeue, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="20f39-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="20f39-170">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="20f39-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="20f39-171">-EventSubscriptionName</span></span>
<span data-ttu-id="20f39-172">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="20f39-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="20f39-173">-EventTtl</span></span>
<span data-ttu-id="20f39-174">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="20f39-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="20f39-175">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="20f39-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-176">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="20f39-176">-ExpirationDate</span></span>
<span data-ttu-id="20f39-177">Определяет дату и время окончания срока действия для подписки на события, после которого подписку на события будут аннулированы.</span><span class="sxs-lookup"><span data-stu-id="20f39-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="20f39-178">-IncludedEventType</span></span>
<span data-ttu-id="20f39-179">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="20f39-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f39-180">-InputObject</span></span>
<span data-ttu-id="20f39-181">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="20f39-181">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-182">-Label</span><span class="sxs-lookup"><span data-stu-id="20f39-182">-Label</span></span>
<span data-ttu-id="20f39-183">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="20f39-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="20f39-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="20f39-185">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="20f39-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="20f39-186">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="20f39-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f39-187">-ResourceGroupName</span></span>
<span data-ttu-id="20f39-188">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="20f39-188">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-189">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20f39-189">-ResourceId</span></span>
<span data-ttu-id="20f39-190">Идентификатор ресурса, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="20f39-190">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="20f39-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="20f39-192">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="20f39-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="20f39-193">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="20f39-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="20f39-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="20f39-195">Фильтр, указывающий, что поле темы должно сравниваться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="20f39-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="20f39-196">Если не указано, тема будет сравниваться без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="20f39-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="20f39-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="20f39-197">-SubjectEndsWith</span></span>
<span data-ttu-id="20f39-198">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="20f39-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="20f39-199">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="20f39-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-200">-TopicName</span><span class="sxs-lookup"><span data-stu-id="20f39-200">-TopicName</span></span>
<span data-ttu-id="20f39-201">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="20f39-201">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f39-202">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20f39-202">-Confirm</span></span>
<span data-ttu-id="20f39-203">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20f39-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f39-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f39-204">-WhatIf</span></span>
<span data-ttu-id="20f39-205">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20f39-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f39-206">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20f39-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f39-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f39-207">CommonParameters</span></span>
<span data-ttu-id="20f39-208">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20f39-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f39-209">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f39-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f39-210">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20f39-210">INPUTS</span></span>

### <span data-ttu-id="20f39-211">System. String</span><span class="sxs-lookup"><span data-stu-id="20f39-211">System.String</span></span>

### <span data-ttu-id="20f39-212">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="20f39-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="20f39-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="20f39-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="20f39-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="20f39-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="20f39-215">System. String []</span><span class="sxs-lookup"><span data-stu-id="20f39-215">System.String[]</span></span>

### <span data-ttu-id="20f39-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="20f39-216">System.Int32</span></span>

## <span data-ttu-id="20f39-217">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f39-217">OUTPUTS</span></span>

### <span data-ttu-id="20f39-218">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="20f39-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="20f39-219">Пуск</span><span class="sxs-lookup"><span data-stu-id="20f39-219">NOTES</span></span>

## <span data-ttu-id="20f39-220">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20f39-220">RELATED LINKS</span></span>
