---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247453"
---
# <span data-ttu-id="4159a-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4159a-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="4159a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4159a-102">SYNOPSIS</span></span>
<span data-ttu-id="4159a-103">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="4159a-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="4159a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4159a-104">SYNTAX</span></span>

### <span data-ttu-id="4159a-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4159a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4159a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4159a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4159a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4159a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4159a-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4159a-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4159a-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4159a-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4159a-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4159a-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4159a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4159a-111">DESCRIPTION</span></span>
<span data-ttu-id="4159a-112">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="4159a-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="4159a-113">Это можно использовать для обновления фильтра, назначения или меток существующей подписки на события.</span><span class="sxs-lookup"><span data-stu-id="4159a-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="4159a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4159a-114">EXAMPLES</span></span>

### <span data-ttu-id="4159a-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4159a-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="4159a-116">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="4159a-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="4159a-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4159a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="4159a-118">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="4159a-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="4159a-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4159a-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="4159a-120">Обновляет свойства подписки на события \` ES1 \` для пространства имен EventHub ContosoNamespace с новой конечной точкой AS, \` https://requestb.in/1kxxoui1\ а новый фильтр SubjectEndsWith — как \` JPG.\`</span><span class="sxs-lookup"><span data-stu-id="4159a-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="4159a-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4159a-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="4159a-122">Обновляет свойства подписок на события \` ES1 \` для группы ресурсов \` MyResourceGroupName \` с новыми метками $labels.</span><span class="sxs-lookup"><span data-stu-id="4159a-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="4159a-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4159a-123">PARAMETERS</span></span>

### <span data-ttu-id="4159a-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="4159a-124">-AdvancedFilter</span></span>
<span data-ttu-id="4159a-125">Расширенный фильтр, указывающий массив из нескольких значений Hashtable, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4159a-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="4159a-126">У каждого значения Hashtable есть следующие ключи: сведения об операции, ключе, значении или значениях.</span><span class="sxs-lookup"><span data-stu-id="4159a-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="4159a-127">Может принимать одно из следующих значений: Number in, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringNotIn, StringBeginsWith или StringEndsWith.</span><span class="sxs-lookup"><span data-stu-id="4159a-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="4159a-128">Key представляет свойство полезных данных, к которому применяются дополнительные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4159a-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="4159a-129">Наконец, значение или значения представляют значение или набор значений, которые должны быть сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="4159a-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="4159a-130">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="4159a-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="4159a-131">В качестве примера параметров расширенного фильтра: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1 = @ {operator = "Number in"; Key = "Data. key1"; Значения = @ (1; 2)} и $AdvFilter 2 = @ {operator = "StringBeginsWith"; Key = "Тема"; Значения = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="4159a-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="4159a-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="4159a-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="4159a-133">Идентификатор приложения Azure Active Directory (AAD) или URI для получения маркера доступа, который будет включен в качестве маркера носителя в запросах на доставку. Применимо только для веб-перехватчика в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="4159a-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="4159a-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="4159a-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="4159a-135">Идентификатор клиента Azure Active Directory (AAD) для получения маркера доступа, который будет включен в качестве маркера носителя в запросах на доставку. Применимо только для веб-перехватчика в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="4159a-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="4159a-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="4159a-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="4159a-137">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="4159a-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="4159a-138">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="4159a-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="4159a-139">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="4159a-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="4159a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4159a-140">-DefaultProfile</span></span>
<span data-ttu-id="4159a-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4159a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4159a-142">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="4159a-142">-DomainName</span></span>
<span data-ttu-id="4159a-143">Имя домена, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="4159a-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="4159a-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="4159a-144">-DomainTopicName</span></span>
<span data-ttu-id="4159a-145">Имя домена, для которого требуется создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="4159a-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="4159a-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="4159a-146">-Endpoint</span></span>
<span data-ttu-id="4159a-147">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="4159a-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="4159a-148">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub, очередь хранилища, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="4159a-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="4159a-149">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="4159a-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="4159a-150">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="4159a-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="4159a-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4159a-151">-EndpointType</span></span>
<span data-ttu-id="4159a-152">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4159a-152">Endpoint Type.</span></span>
<span data-ttu-id="4159a-153">Это может быть веб-перехватчик, eventhub, storagequeue, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="4159a-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="4159a-154">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="4159a-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="4159a-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4159a-155">-EventSubscriptionName</span></span>
<span data-ttu-id="4159a-156">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="4159a-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="4159a-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="4159a-157">-EventTtl</span></span>
<span data-ttu-id="4159a-158">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="4159a-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="4159a-159">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="4159a-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="4159a-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="4159a-160">-ExpirationDate</span></span>
<span data-ttu-id="4159a-161">Определяет дату и время окончания срока действия для подписки на события, после которого подписку на события будут аннулированы.</span><span class="sxs-lookup"><span data-stu-id="4159a-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="4159a-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="4159a-162">-IncludedEventType</span></span>
<span data-ttu-id="4159a-163">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="4159a-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="4159a-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4159a-164">-InputObject</span></span>
<span data-ttu-id="4159a-165">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4159a-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="4159a-166">-Label</span><span class="sxs-lookup"><span data-stu-id="4159a-166">-Label</span></span>
<span data-ttu-id="4159a-167">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="4159a-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="4159a-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="4159a-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="4159a-169">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="4159a-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="4159a-170">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="4159a-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="4159a-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="4159a-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="4159a-172">Максимальное количество событий в пакете.</span><span class="sxs-lookup"><span data-stu-id="4159a-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="4159a-173">Это значение должно находиться в диапазоне от 1 до 5000.</span><span class="sxs-lookup"><span data-stu-id="4159a-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="4159a-174">Этот параметр является допустимым только в том случае, если тип Endpint — только веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="4159a-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="4159a-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="4159a-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="4159a-176">Предпочтительный размер пакета в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="4159a-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="4159a-177">Это значение должно находиться в диапазоне от 1 до 1024.</span><span class="sxs-lookup"><span data-stu-id="4159a-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="4159a-178">Этот параметр является допустимым только в том случае, если тип Endpint — только веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="4159a-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="4159a-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4159a-179">-ResourceGroupName</span></span>
<span data-ttu-id="4159a-180">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="4159a-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="4159a-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4159a-181">-ResourceId</span></span>
<span data-ttu-id="4159a-182">Идентификатор ресурса, для которого была создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="4159a-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="4159a-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="4159a-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="4159a-184">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="4159a-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="4159a-185">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="4159a-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="4159a-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="4159a-186">-SubjectEndsWith</span></span>
<span data-ttu-id="4159a-187">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="4159a-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="4159a-188">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="4159a-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="4159a-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4159a-189">-TopicName</span></span>
<span data-ttu-id="4159a-190">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="4159a-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="4159a-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4159a-191">-Confirm</span></span>
<span data-ttu-id="4159a-192">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4159a-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4159a-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4159a-193">-WhatIf</span></span>
<span data-ttu-id="4159a-194">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4159a-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4159a-195">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4159a-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4159a-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4159a-196">CommonParameters</span></span>
<span data-ttu-id="4159a-197">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4159a-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4159a-198">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4159a-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4159a-199">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4159a-199">INPUTS</span></span>

### <span data-ttu-id="4159a-200">System. String</span><span class="sxs-lookup"><span data-stu-id="4159a-200">System.String</span></span>

### <span data-ttu-id="4159a-201">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="4159a-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="4159a-202">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4159a-202">OUTPUTS</span></span>

### <span data-ttu-id="4159a-203">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="4159a-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="4159a-204">Пуск</span><span class="sxs-lookup"><span data-stu-id="4159a-204">NOTES</span></span>

## <span data-ttu-id="4159a-205">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4159a-205">RELATED LINKS</span></span>
