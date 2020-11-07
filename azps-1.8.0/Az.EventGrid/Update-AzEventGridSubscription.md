---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730862"
---
# <span data-ttu-id="d13a3-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d13a3-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="d13a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d13a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d13a3-103">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d13a3-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="d13a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d13a3-104">SYNTAX</span></span>

### <span data-ttu-id="d13a3-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d13a3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d13a3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d13a3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d13a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d13a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13a3-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d13a3-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13a3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13a3-109">DESCRIPTION</span></span>
<span data-ttu-id="d13a3-110">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d13a3-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="d13a3-111">Это можно использовать для обновления фильтра, назначения или меток существующей подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d13a3-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="d13a3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d13a3-112">EXAMPLES</span></span>

### <span data-ttu-id="d13a3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d13a3-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="d13a3-114">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="d13a3-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="d13a3-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d13a3-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="d13a3-116">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="d13a3-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="d13a3-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d13a3-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="d13a3-118">Обновляет свойства подписки на события \` ES1 \` для пространства имен EventHub ContosoNamespace с новой конечной точкой AS, \` https://requestb.in/1kxxoui1\ а новый фильтр SubjectEndsWith — как \` JPG.\`</span><span class="sxs-lookup"><span data-stu-id="d13a3-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="d13a3-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d13a3-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="d13a3-120">Обновляет свойства подписок на события \` ES1 \` для группы ресурсов \` MyResourceGroupName \` с новыми метками $labels.</span><span class="sxs-lookup"><span data-stu-id="d13a3-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="d13a3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d13a3-121">PARAMETERS</span></span>

### <span data-ttu-id="d13a3-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="d13a3-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="d13a3-123">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="d13a3-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="d13a3-124">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="d13a3-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="d13a3-125">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="d13a3-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="d13a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13a3-126">-DefaultProfile</span></span>
<span data-ttu-id="d13a3-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d13a3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d13a3-128">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d13a3-128">-Endpoint</span></span>
<span data-ttu-id="d13a3-129">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d13a3-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="d13a3-130">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure для EventHub, очереди хранения или hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="d13a3-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="d13a3-131">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="d13a3-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="d13a3-132">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d13a3-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="d13a3-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d13a3-133">-EndpointType</span></span>
<span data-ttu-id="d13a3-134">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d13a3-134">Endpoint Type.</span></span>
<span data-ttu-id="d13a3-135">Это может быть веб-перехватчик, eventhub, storagequeue или hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="d13a3-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="d13a3-136">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="d13a3-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13a3-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d13a3-137">-EventSubscriptionName</span></span>
<span data-ttu-id="d13a3-138">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="d13a3-138">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13a3-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="d13a3-139">-EventTtl</span></span>
<span data-ttu-id="d13a3-140">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="d13a3-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="d13a3-141">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="d13a3-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="d13a3-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="d13a3-142">-IncludedEventType</span></span>
<span data-ttu-id="d13a3-143">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="d13a3-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="d13a3-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d13a3-144">-InputObject</span></span>
<span data-ttu-id="d13a3-145">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d13a3-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="d13a3-146">-Label</span><span class="sxs-lookup"><span data-stu-id="d13a3-146">-Label</span></span>
<span data-ttu-id="d13a3-147">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="d13a3-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="d13a3-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="d13a3-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="d13a3-149">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="d13a3-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="d13a3-150">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="d13a3-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="d13a3-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13a3-151">-ResourceGroupName</span></span>
<span data-ttu-id="d13a3-152">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="d13a3-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13a3-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d13a3-153">-ResourceId</span></span>
<span data-ttu-id="d13a3-154">Идентификатор ресурса, для которого была создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="d13a3-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="d13a3-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d13a3-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="d13a3-156">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="d13a3-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="d13a3-157">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="d13a3-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="d13a3-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="d13a3-158">-SubjectEndsWith</span></span>
<span data-ttu-id="d13a3-159">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="d13a3-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="d13a3-160">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="d13a3-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="d13a3-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d13a3-161">-TopicName</span></span>
<span data-ttu-id="d13a3-162">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="d13a3-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d13a3-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d13a3-163">-Confirm</span></span>
<span data-ttu-id="d13a3-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d13a3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13a3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13a3-165">-WhatIf</span></span>
<span data-ttu-id="d13a3-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d13a3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d13a3-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d13a3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13a3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13a3-168">CommonParameters</span></span>
<span data-ttu-id="d13a3-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d13a3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13a3-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13a3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13a3-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d13a3-171">INPUTS</span></span>

### <span data-ttu-id="d13a3-172">System. String</span><span class="sxs-lookup"><span data-stu-id="d13a3-172">System.String</span></span>

### <span data-ttu-id="d13a3-173">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d13a3-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d13a3-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13a3-174">OUTPUTS</span></span>

### <span data-ttu-id="d13a3-175">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d13a3-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d13a3-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="d13a3-176">NOTES</span></span>

## <span data-ttu-id="d13a3-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d13a3-177">RELATED LINKS</span></span>
