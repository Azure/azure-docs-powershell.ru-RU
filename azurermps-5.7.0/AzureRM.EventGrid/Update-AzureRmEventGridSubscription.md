---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563536"
---
# <span data-ttu-id="b1c99-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b1c99-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="b1c99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1c99-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c99-103">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="b1c99-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1c99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1c99-104">SYNTAX</span></span>

### <span data-ttu-id="b1c99-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1c99-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c99-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c99-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c99-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1c99-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c99-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c99-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c99-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1c99-109">DESCRIPTION</span></span>
<span data-ttu-id="b1c99-110">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="b1c99-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="b1c99-111">Это можно использовать для обновления фильтра, назначения или меток существующей подписки на события.</span><span class="sxs-lookup"><span data-stu-id="b1c99-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="b1c99-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1c99-112">EXAMPLES</span></span>

### <span data-ttu-id="b1c99-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1c99-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="b1c99-114">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="b1c99-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="b1c99-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1c99-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="b1c99-116">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="b1c99-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="b1c99-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b1c99-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="b1c99-118">Обновляет свойства подписки на события \` ES1 \` для пространства имен EventHub ContosoNamespace с новой конечной точкой AS, \` https://requestb.in/1kxxoui1\ а новый фильтр SubjectEndsWith — как \` JPG.\`</span><span class="sxs-lookup"><span data-stu-id="b1c99-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="b1c99-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b1c99-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="b1c99-120">Обновляет свойства подписок на события \` ES1 \` для группы ресурсов \` MyResourceGroupName \` с новыми метками $labels.</span><span class="sxs-lookup"><span data-stu-id="b1c99-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="b1c99-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1c99-121">PARAMETERS</span></span>

### <span data-ttu-id="b1c99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c99-122">-DefaultProfile</span></span>
<span data-ttu-id="b1c99-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c99-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="b1c99-124">-Endpoint</span></span>
<span data-ttu-id="b1c99-125">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="b1c99-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="b1c99-126">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub.</span><span class="sxs-lookup"><span data-stu-id="b1c99-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b1c99-127">-EndpointType</span></span>
<span data-ttu-id="b1c99-128">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b1c99-128">Endpoint Type.</span></span>
<span data-ttu-id="b1c99-129">Это может быть веб-перехватчик или eventhub</span><span class="sxs-lookup"><span data-stu-id="b1c99-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b1c99-130">-EventSubscriptionName</span></span>
<span data-ttu-id="b1c99-131">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="b1c99-131">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="b1c99-132">-IncludedEventType</span></span>
<span data-ttu-id="b1c99-133">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="b1c99-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c99-134">-InputObject</span></span>
<span data-ttu-id="b1c99-135">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b1c99-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-136">-Label</span><span class="sxs-lookup"><span data-stu-id="b1c99-136">-Label</span></span>
<span data-ttu-id="b1c99-137">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="b1c99-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c99-138">-ResourceGroupName</span></span>
<span data-ttu-id="b1c99-139">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="b1c99-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1c99-140">-ResourceId</span></span>
<span data-ttu-id="b1c99-141">Идентификатор ресурса, для которого была создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="b1c99-141">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="b1c99-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="b1c99-143">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="b1c99-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="b1c99-144">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="b1c99-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="b1c99-145">-SubjectEndsWith</span></span>
<span data-ttu-id="b1c99-146">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="b1c99-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="b1c99-147">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="b1c99-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b1c99-148">-TopicName</span></span>
<span data-ttu-id="b1c99-149">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="b1c99-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1c99-150">-Confirm</span></span>
<span data-ttu-id="b1c99-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1c99-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c99-152">-WhatIf</span></span>
<span data-ttu-id="b1c99-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1c99-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c99-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1c99-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c99-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c99-155">CommonParameters</span></span>
<span data-ttu-id="b1c99-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1c99-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c99-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c99-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1c99-158">INPUTS</span></span>

### <span data-ttu-id="b1c99-159">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c99-159">System.String</span></span>
<span data-ttu-id="b1c99-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. String []</span><span class="sxs-lookup"><span data-stu-id="b1c99-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="b1c99-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1c99-161">OUTPUTS</span></span>

### <span data-ttu-id="b1c99-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="b1c99-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="b1c99-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1c99-163">NOTES</span></span>

## <span data-ttu-id="b1c99-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1c99-164">RELATED LINKS</span></span>

