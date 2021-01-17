---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412908"
---
# <span data-ttu-id="ee3d9-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ee3d9-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="ee3d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3d9-103">Создание подписки на событие сетки событий Azure для темы, ресурса Azure, подписки Azure или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="ee3d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee3d9-104">SYNTAX</span></span>

### <span data-ttu-id="ee3d9-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee3d9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3d9-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3d9-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3d9-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee3d9-113">DESCRIPTION</span></span>
<span data-ttu-id="ee3d9-114">Создайте подписку на новое событие для темы сетки событий Azure, поддерживаемых ресурсов Azure, подписки Azure или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="ee3d9-115">Чтобы создать подписку на событие для выбранной подписки Azure, укажите имя подписки на событие и конечную точку.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="ee3d9-116">Чтобы создать подписку на событие для группы ресурсов, укажите имя группы ресурсов в дополнение к имени подписки на событие и конечной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="ee3d9-117">Чтобы создать подписку на тему сетки событий Azure, укажите имя темы.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="ee3d9-118">Чтобы создать подписку на событие для поддерживаемого ресурса Azure, укажите полный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="ee3d9-119">Чтобы просмотреть список поддерживаемых типов, запустите Get-AzEventGridTopicType>.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="ee3d9-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee3d9-120">EXAMPLES</span></span>

### <span data-ttu-id="ee3d9-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee3d9-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee3d9-122">Создает новую подписку на событие EventSubscription1 для темы Azure Event Grid Topic1 в группе ресурсов \` \` \` \` \` MyResourceGroupName с конечной точкой \` `https://requestb.in/19qlscd1` webhook.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="ee3d9-123">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ee3d9-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee3d9-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee3d9-125">Создание подписки на событие EventSubscription1 для группы ресурсов \` \` \` MyResourceGroupName с конечной точкой \` веб-приложения. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="ee3d9-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="ee3d9-126">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ee3d9-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee3d9-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee3d9-128">Создает новую подписку на событие EventSubscription1 для выбранной в данный момент подписки Azure с конечной точкой назначения \` \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="ee3d9-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="ee3d9-129">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ee3d9-130">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ee3d9-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="ee3d9-131">Создает новую подписку на событие EventSubscription1 для выбранной в данный момент подписки Azure с конечной точкой назначения \` \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="ee3d9-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="ee3d9-132">В этой подписке на событие указаны дополнительные фильтры для типов событий и темы, и только те события, которые соответствуют этим фильтрам, будут доставляться в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="ee3d9-133">Пример 5</span><span class="sxs-lookup"><span data-stu-id="ee3d9-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="ee3d9-134">Создает новую подписку \` на событие EventSubscription1 для выбранной в данный момент подписки Azure с указанным центром событий в качестве места \` назначения событий.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="ee3d9-135">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ee3d9-136">Пример 6</span><span class="sxs-lookup"><span data-stu-id="ee3d9-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee3d9-137">Создает новую подписку на событие EventSubscription1 для пространства имен EventHub с указанной конечной точкой \` \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="ee3d9-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="ee3d9-138">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="ee3d9-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee3d9-139">PARAMETERS</span></span>

### <span data-ttu-id="ee3d9-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="ee3d9-140">-AdvancedFilter</span></span>
<span data-ttu-id="ee3d9-141">Расширенный фильтр, задающий массив из нескольких hashtable значений, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="ee3d9-142">Каждое значение в режиме hashtable имеет следующие сведения о значении ключа: operation, Key и Value или Values.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="ee3d9-143">Оператор может быть одним из следующих значений: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith или StringContains.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="ee3d9-144">Ключ представляет свойство полезной нагрузки, в котором применяются расширенные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="ee3d9-145">Наконец, значения представляют собой совпадают со значением или набором значений.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="ee3d9-146">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="ee3d9-147">Пример параметров расширенных фильтров: $AdvancedFilters=@($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter 2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="ee3d9-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="ee3d9-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="ee3d9-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="ee3d9-149">ИД приложения Azure Active Directory (AAD) или Uri для получения маркера доступа, который будет включен в запросы на доставку в качестве маркера. Применимо только для webhook в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="ee3d9-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="ee3d9-151">ИД клиента Azure Active Directory (AAD) для получения маркера доступа, который будет включен в запросы на доставку в качестве маркера для получения. Применимо только для webhook в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="ee3d9-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="ee3d9-153">Конечная точка, используемая для хранения неоставных событий.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="ee3d9-154">Укажите ИД ресурсов Azure для контейнера BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="ee3d9-155">Например: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="ee3d9-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="ee3d9-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3d9-156">-DefaultProfile</span></span>
<span data-ttu-id="ee3d9-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ee3d9-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee3d9-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="ee3d9-158">-DeliverySchema</span></span>
<span data-ttu-id="ee3d9-159">Схема, используемая при доставке событий в место назначения.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="ee3d9-160">Возможные значения: eventgridschema, CustomInputSchema или cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="ee3d9-161">Значение по умолчанию — CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ee3d9-162">-DomainInputObject</span></span>
<span data-ttu-id="ee3d9-163">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ee3d9-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ee3d9-164">-DomainName</span></span>
<span data-ttu-id="ee3d9-165">Имя домена сетки событий, для которого нужно создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ee3d9-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ee3d9-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="ee3d9-167">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="ee3d9-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ee3d9-168">-DomainTopicName</span></span>
<span data-ttu-id="ee3d9-169">Имя темы домена, для которой нужно создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ee3d9-170">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="ee3d9-170">-Endpoint</span></span>
<span data-ttu-id="ee3d9-171">Конечная точка назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="ee3d9-172">Это может быть URL-адрес веб-приложения или ИД ресурса Azure из EventHub, очереди хранения, гибридного подключения или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="ee3d9-173">Например, код ресурса для гибридного подключения имеет следующую форму: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="ee3d9-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="ee3d9-174">Предполагается, что конечная точка будет создана и доступна для использования перед выполнением любых cmdletов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="ee3d9-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ee3d9-175">-EndpointType</span></span>
<span data-ttu-id="ee3d9-176">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-176">Endpoint Type.</span></span>
<span data-ttu-id="ee3d9-177">Это может быть webhook, eventhub, объем хранилища, гибридное подключение или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="ee3d9-178">Значением по умолчанию является webhook.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ee3d9-179">-EventSubscriptionName</span></span>
<span data-ttu-id="ee3d9-180">Название подписки на событие</span><span class="sxs-lookup"><span data-stu-id="ee3d9-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="ee3d9-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="ee3d9-181">-EventTtl</span></span>
<span data-ttu-id="ee3d9-182">Время доставки события в минутах.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="ee3d9-183">Это значение должно быть в возрасте от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="ee3d9-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="ee3d9-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ee3d9-184">-ExpirationDate</span></span>
<span data-ttu-id="ee3d9-185">Определяет срок действия даты и времени окончания срока действия подписки на событие, после которого подписка на событие будет соединяема.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="ee3d9-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="ee3d9-186">-IncludedEventType</span></span>
<span data-ttu-id="ee3d9-187">Фильтр, который определяет список типов событий, которые нужно включить. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee3d9-188">-InputObject</span></span>
<span data-ttu-id="ee3d9-189">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ee3d9-190">-Label</span><span class="sxs-lookup"><span data-stu-id="ee3d9-190">-Label</span></span>
<span data-ttu-id="ee3d9-191">Метки для подписки на событие</span><span class="sxs-lookup"><span data-stu-id="ee3d9-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3d9-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="ee3d9-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="ee3d9-193">Максимальное количество попыток проведения события.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="ee3d9-194">Это значение должно быть в возрасте от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="ee3d9-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="ee3d9-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="ee3d9-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="ee3d9-196">Максимальное количество событий в пакете.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="ee3d9-197">Это значение должно быть в возрасте от 1 до 5000.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="ee3d9-198">Этот параметр действителен, если типом конечных страниц является только веб-ook.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="ee3d9-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="ee3d9-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="ee3d9-200">Предпочитаемый размер пакета в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="ee3d9-201">Это значение должно быть в период от 1 до 1024.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="ee3d9-202">Этот параметр действителен, если типом конечных страниц является только веб-ook.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="ee3d9-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee3d9-203">-ResourceGroupName</span></span>
<span data-ttu-id="ee3d9-204">Группа ресурсов по теме.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="ee3d9-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3d9-205">-ResourceId</span></span>
<span data-ttu-id="ee3d9-206">Идентификатор ресурса, для которого создается подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ee3d9-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ee3d9-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="ee3d9-208">Фильтр, который указывает, что будут включены только события, которые соответствуют указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="ee3d9-209">Если не указано, будут включены события со всеми префиксами темы.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="ee3d9-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="ee3d9-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="ee3d9-211">Фильтр, который указывает, что поле темы должно быть сравнивается с учетом особенности дела.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="ee3d9-212">Если не указано, то будет сравнена тема без учетом того, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="ee3d9-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="ee3d9-213">-SubjectEndsWith</span></span>
<span data-ttu-id="ee3d9-214">Фильтр, который указывает, что будут включены только события, которые соответствуют указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="ee3d9-215">Если не указано, будут включены события со всеми суффиксами темы.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="ee3d9-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ee3d9-216">-TopicName</span></span>
<span data-ttu-id="ee3d9-217">Название темы, для которой нужно создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ee3d9-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee3d9-218">-Confirm</span></span>
<span data-ttu-id="ee3d9-219">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3d9-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3d9-220">-WhatIf</span></span>
<span data-ttu-id="ee3d9-221">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee3d9-222">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3d9-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3d9-223">CommonParameters</span></span>
<span data-ttu-id="ee3d9-224">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3d9-225">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee3d9-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3d9-226">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee3d9-226">INPUTS</span></span>

### <span data-ttu-id="ee3d9-227">System.String</span><span class="sxs-lookup"><span data-stu-id="ee3d9-227">System.String</span></span>

### <span data-ttu-id="ee3d9-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ee3d9-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ee3d9-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ee3d9-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ee3d9-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ee3d9-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ee3d9-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ee3d9-231">System.String[]</span></span>

### <span data-ttu-id="ee3d9-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ee3d9-232">System.Int32</span></span>

## <span data-ttu-id="ee3d9-233">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee3d9-233">OUTPUTS</span></span>

### <span data-ttu-id="ee3d9-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ee3d9-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ee3d9-235">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee3d9-235">NOTES</span></span>

## <span data-ttu-id="ee3d9-236">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee3d9-236">RELATED LINKS</span></span>
