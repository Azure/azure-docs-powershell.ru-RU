---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399220"
---
# <span data-ttu-id="a8c57-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a8c57-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="a8c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8c57-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c57-103">Обновив свойства подписки на события сетки событий событий.</span><span class="sxs-lookup"><span data-stu-id="a8c57-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="a8c57-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8c57-104">SYNTAX</span></span>

### <span data-ttu-id="a8c57-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8c57-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c57-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8c57-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8c57-111">DESCRIPTION</span></span>
<span data-ttu-id="a8c57-112">Обновив свойства подписки на события сетки событий событий.</span><span class="sxs-lookup"><span data-stu-id="a8c57-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="a8c57-113">Его можно использовать для обновления фильтра, назначения или меток существующей подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="a8c57-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8c57-114">EXAMPLES</span></span>

### <span data-ttu-id="a8c57-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8c57-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="a8c57-116">Обновляет конечную точку подписки на событие ES1 для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName, \` чтобы \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="a8c57-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="a8c57-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a8c57-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="a8c57-118">Обновляет конечную точку подписки на событие ES1 для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName, \` чтобы \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="a8c57-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="a8c57-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a8c57-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="a8c57-120">Обновление свойств подписки на событие ES1 для пространства имен EventHub ContosoNamespace с новой конечной точкой в формате ' и нового фильтра \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith в \` формате JPG\`</span><span class="sxs-lookup"><span data-stu-id="a8c57-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="a8c57-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a8c57-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="a8c57-122">Обновляет свойства подписки на событие ES1 для группы ресурсов \` \` \` MyResourceGroupName с помощью новых \` $labels.</span><span class="sxs-lookup"><span data-stu-id="a8c57-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="a8c57-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8c57-123">PARAMETERS</span></span>

### <span data-ttu-id="a8c57-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="a8c57-124">-AdvancedFilter</span></span>
<span data-ttu-id="a8c57-125">Расширенный фильтр, задающий массив из нескольких hashtable значений, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a8c57-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="a8c57-126">Каждое значение в режиме hashtable имеет следующие сведения о значении ключа: operation, Key и Value или Values.</span><span class="sxs-lookup"><span data-stu-id="a8c57-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="a8c57-127">Оператор может быть одним из следующих значений: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith или StringContains.</span><span class="sxs-lookup"><span data-stu-id="a8c57-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="a8c57-128">Ключ представляет свойство полезной нагрузки, в котором применяются расширенные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a8c57-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="a8c57-129">Наконец, значения представляют собой совпадают со значением или набором значений.</span><span class="sxs-lookup"><span data-stu-id="a8c57-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="a8c57-130">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="a8c57-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="a8c57-131">Пример параметров расширенных фильтров: $AdvancedFilters=@($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="a8c57-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="a8c57-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="a8c57-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="a8c57-133">ИД приложения Azure Active Directory (AAD) или Uri для получения маркера доступа, который будет включен в запросы на доставку в качестве маркера. Применимо только к webhook в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="a8c57-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="a8c57-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="a8c57-135">ИД клиента Azure Active Directory (AAD) для получения маркера доступа, который будет включен в запросы на доставку в качестве маркера для получения. Применимо только к webhook в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="a8c57-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8c57-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="a8c57-137">Конечная точка, используемая для хранения неоставных событий.</span><span class="sxs-lookup"><span data-stu-id="a8c57-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="a8c57-138">Укажите ИД ресурсов Azure для контейнера BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="a8c57-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="a8c57-139">Например: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="a8c57-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="a8c57-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c57-140">-DefaultProfile</span></span>
<span data-ttu-id="a8c57-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c57-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c57-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a8c57-142">-DomainName</span></span>
<span data-ttu-id="a8c57-143">Имя домена, для которого должна быть создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-143">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a8c57-144">-DomainTopicName</span></span>
<span data-ttu-id="a8c57-145">Имя раздела домена, для которого нужно создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-145">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-146">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="a8c57-146">-Endpoint</span></span>
<span data-ttu-id="a8c57-147">Конечная точка назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="a8c57-148">Это может быть URL-адрес веб-приложения или ИД ресурса Azure из EventHub, очереди хранения, гибридного подключения или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="a8c57-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a8c57-149">Например, код ресурса для гибридного подключения имеет следующую форму: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="a8c57-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="a8c57-150">Предполагается, что конечная точка будет создана и доступна для использования перед выполнением любых cmdletов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="a8c57-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="a8c57-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a8c57-151">-EndpointType</span></span>
<span data-ttu-id="a8c57-152">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a8c57-152">Endpoint Type.</span></span>
<span data-ttu-id="a8c57-153">Это может быть webhook, eventhub, объем хранилища, гибридное подключение или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="a8c57-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a8c57-154">Значением по умолчанию является webhook.</span><span class="sxs-lookup"><span data-stu-id="a8c57-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a8c57-155">-EventSubscriptionName</span></span>
<span data-ttu-id="a8c57-156">Название подписки на событие</span><span class="sxs-lookup"><span data-stu-id="a8c57-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="a8c57-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="a8c57-157">-EventTtl</span></span>
<span data-ttu-id="a8c57-158">Время доставки события в минутах.</span><span class="sxs-lookup"><span data-stu-id="a8c57-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="a8c57-159">Это значение должно быть в возрасте от 1 до 1440.</span><span class="sxs-lookup"><span data-stu-id="a8c57-159">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="a8c57-160">-ExpirationDate</span></span>
<span data-ttu-id="a8c57-161">Определяет срок действия даты и времени окончания срока действия подписки на событие, после которого подписка на событие будет соединяема.</span><span class="sxs-lookup"><span data-stu-id="a8c57-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="a8c57-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="a8c57-162">-IncludedEventType</span></span>
<span data-ttu-id="a8c57-163">Фильтр, который определяет список типов событий, которые нужно включить. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="a8c57-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8c57-164">-InputObject</span></span>
<span data-ttu-id="a8c57-165">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a8c57-165">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-166">-Label</span><span class="sxs-lookup"><span data-stu-id="a8c57-166">-Label</span></span>
<span data-ttu-id="a8c57-167">Метки для подписки на событие</span><span class="sxs-lookup"><span data-stu-id="a8c57-167">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="a8c57-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="a8c57-169">Максимальное количество попыток проведения события.</span><span class="sxs-lookup"><span data-stu-id="a8c57-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="a8c57-170">Это значение должно быть в возрасте от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="a8c57-170">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="a8c57-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="a8c57-172">Максимальное количество событий в пакете.</span><span class="sxs-lookup"><span data-stu-id="a8c57-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="a8c57-173">Это значение должно быть в возрасте от 1 до 5000.</span><span class="sxs-lookup"><span data-stu-id="a8c57-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="a8c57-174">Этот параметр действителен, если типом конечных страниц является только веб-ook.</span><span class="sxs-lookup"><span data-stu-id="a8c57-174">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="a8c57-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="a8c57-176">Предпочитаемый размер пакета в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="a8c57-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="a8c57-177">Это значение должно быть в период от 1 до 1024.</span><span class="sxs-lookup"><span data-stu-id="a8c57-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="a8c57-178">Этот параметр действителен, если типом конечных страниц является только веб-ook.</span><span class="sxs-lookup"><span data-stu-id="a8c57-178">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c57-179">-ResourceGroupName</span></span>
<span data-ttu-id="a8c57-180">Группа ресурсов по теме.</span><span class="sxs-lookup"><span data-stu-id="a8c57-180">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c57-181">-ResourceId</span></span>
<span data-ttu-id="a8c57-182">Идентификатор ресурса, для которого создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="a8c57-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="a8c57-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="a8c57-184">Фильтр, который указывает, что будут включены только события, которые соответствуют указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="a8c57-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="a8c57-185">Если не указано, будут включены события со всеми префиксами темы.</span><span class="sxs-lookup"><span data-stu-id="a8c57-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="a8c57-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="a8c57-186">-SubjectEndsWith</span></span>
<span data-ttu-id="a8c57-187">Фильтр, который указывает, что будут включены только события, которые соответствуют указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="a8c57-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="a8c57-188">Если не указано, будут включены события со всеми суффиксами темы.</span><span class="sxs-lookup"><span data-stu-id="a8c57-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="a8c57-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a8c57-189">-TopicName</span></span>
<span data-ttu-id="a8c57-190">Название темы, для которой нужно создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="a8c57-190">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c57-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8c57-191">-Confirm</span></span>
<span data-ttu-id="a8c57-192">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c57-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8c57-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c57-193">-WhatIf</span></span>
<span data-ttu-id="a8c57-194">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c57-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8c57-195">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8c57-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8c57-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c57-196">CommonParameters</span></span>
<span data-ttu-id="a8c57-197">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c57-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c57-198">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8c57-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c57-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8c57-199">INPUTS</span></span>

### <span data-ttu-id="a8c57-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a8c57-200">System.String</span></span>

### <span data-ttu-id="a8c57-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a8c57-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a8c57-202">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8c57-202">OUTPUTS</span></span>

### <span data-ttu-id="a8c57-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a8c57-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a8c57-204">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8c57-204">NOTES</span></span>

## <span data-ttu-id="a8c57-205">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8c57-205">RELATED LINKS</span></span>
