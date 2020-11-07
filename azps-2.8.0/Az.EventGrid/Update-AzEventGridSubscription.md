---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720975"
---
# <span data-ttu-id="3c977-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3c977-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="3c977-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c977-102">SYNOPSIS</span></span>
<span data-ttu-id="3c977-103">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="3c977-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="3c977-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c977-104">SYNTAX</span></span>

### <span data-ttu-id="3c977-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c977-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c977-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c977-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c977-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c977-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c977-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c977-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c977-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c977-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c977-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c977-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c977-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c977-111">DESCRIPTION</span></span>
<span data-ttu-id="3c977-112">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="3c977-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="3c977-113">Это можно использовать для обновления фильтра, назначения или меток существующей подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3c977-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="3c977-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c977-114">EXAMPLES</span></span>

### <span data-ttu-id="3c977-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c977-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3c977-116">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3c977-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3c977-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c977-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3c977-118">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3c977-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3c977-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3c977-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="3c977-120">Обновляет свойства подписки на события \` ES1 \` для пространства имен EventHub ContosoNamespace с новой конечной точкой AS, \` https://requestb.in/1kxxoui1\ а новый фильтр SubjectEndsWith — как \` JPG.\`</span><span class="sxs-lookup"><span data-stu-id="3c977-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="3c977-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3c977-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="3c977-122">Обновляет свойства подписок на события \` ES1 \` для группы ресурсов \` MyResourceGroupName \` с новыми метками $labels.</span><span class="sxs-lookup"><span data-stu-id="3c977-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="3c977-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c977-123">PARAMETERS</span></span>

### <span data-ttu-id="3c977-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="3c977-124">-AdvancedFilter</span></span>
<span data-ttu-id="3c977-125">Расширенный фильтр, указывающий массив из нескольких значений Hashtable, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="3c977-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="3c977-126">У каждого значения Hashtable есть следующие ключи: сведения об операции, ключе, значении или значениях.</span><span class="sxs-lookup"><span data-stu-id="3c977-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="3c977-127">Может принимать одно из следующих значений: Number in, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringNotIn, StringBeginsWith или StringEndsWith.</span><span class="sxs-lookup"><span data-stu-id="3c977-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="3c977-128">Key представляет свойство полезных данных, к которому применяются дополнительные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3c977-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="3c977-129">Наконец, значение или значения представляют значение или набор значений, которые должны быть сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="3c977-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="3c977-130">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="3c977-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="3c977-131">В качестве примера параметров расширенного фильтра: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1 = @ {operator = "Number in"; Key = "Data. key1"; Значения = @ (1; 2)} и $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Тема"; Значения = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="3c977-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="3c977-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c977-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="3c977-133">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="3c977-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="3c977-134">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c977-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="3c977-135">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="3c977-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="3c977-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c977-136">-DefaultProfile</span></span>
<span data-ttu-id="3c977-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c977-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c977-138">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="3c977-138">-DomainName</span></span>
<span data-ttu-id="3c977-139">Имя домена, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="3c977-139">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3c977-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="3c977-140">-DomainTopicName</span></span>
<span data-ttu-id="3c977-141">Имя домена, для которого требуется создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="3c977-141">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3c977-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="3c977-142">-Endpoint</span></span>
<span data-ttu-id="3c977-143">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3c977-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="3c977-144">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub, очередь хранилища, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="3c977-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3c977-145">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="3c977-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="3c977-146">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="3c977-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="3c977-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3c977-147">-EndpointType</span></span>
<span data-ttu-id="3c977-148">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3c977-148">Endpoint Type.</span></span>
<span data-ttu-id="3c977-149">Это может быть веб-перехватчик, eventhub, storagequeue, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="3c977-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3c977-150">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="3c977-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c977-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3c977-151">-EventSubscriptionName</span></span>
<span data-ttu-id="3c977-152">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="3c977-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="3c977-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="3c977-153">-EventTtl</span></span>
<span data-ttu-id="3c977-154">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="3c977-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="3c977-155">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="3c977-155">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="3c977-156">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="3c977-156">-ExpirationDate</span></span>
<span data-ttu-id="3c977-157">Определяет дату и время окончания срока действия для подписки на события, после которого подписку на события будут аннулированы.</span><span class="sxs-lookup"><span data-stu-id="3c977-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="3c977-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="3c977-158">-IncludedEventType</span></span>
<span data-ttu-id="3c977-159">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="3c977-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="3c977-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c977-160">-InputObject</span></span>
<span data-ttu-id="3c977-161">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3c977-161">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="3c977-162">-Label</span><span class="sxs-lookup"><span data-stu-id="3c977-162">-Label</span></span>
<span data-ttu-id="3c977-163">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="3c977-163">Labels for the event subscription</span></span>

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

### <span data-ttu-id="3c977-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="3c977-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="3c977-165">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="3c977-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="3c977-166">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="3c977-166">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="3c977-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c977-167">-ResourceGroupName</span></span>
<span data-ttu-id="3c977-168">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="3c977-168">The resource group of the topic.</span></span>

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

### <span data-ttu-id="3c977-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c977-169">-ResourceId</span></span>
<span data-ttu-id="3c977-170">Идентификатор ресурса, для которого была создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="3c977-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="3c977-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="3c977-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="3c977-172">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="3c977-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="3c977-173">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="3c977-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="3c977-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="3c977-174">-SubjectEndsWith</span></span>
<span data-ttu-id="3c977-175">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="3c977-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="3c977-176">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="3c977-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="3c977-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3c977-177">-TopicName</span></span>
<span data-ttu-id="3c977-178">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="3c977-178">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3c977-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c977-179">-Confirm</span></span>
<span data-ttu-id="3c977-180">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c977-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c977-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c977-181">-WhatIf</span></span>
<span data-ttu-id="3c977-182">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c977-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c977-183">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c977-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c977-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c977-184">CommonParameters</span></span>
<span data-ttu-id="3c977-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c977-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c977-186">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c977-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c977-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c977-187">INPUTS</span></span>

### <span data-ttu-id="3c977-188">System. String</span><span class="sxs-lookup"><span data-stu-id="3c977-188">System.String</span></span>

### <span data-ttu-id="3c977-189">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3c977-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3c977-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c977-190">OUTPUTS</span></span>

### <span data-ttu-id="3c977-191">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3c977-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3c977-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c977-192">NOTES</span></span>

## <span data-ttu-id="3c977-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c977-193">RELATED LINKS</span></span>
