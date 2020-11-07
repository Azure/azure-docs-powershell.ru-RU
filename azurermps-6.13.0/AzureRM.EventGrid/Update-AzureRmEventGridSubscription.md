---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: d036ba2df289b0b2f84430f01000632a887ec20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734658"
---
# <span data-ttu-id="d7bb4-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d7bb4-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="d7bb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bb4-103">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7bb4-104">SYNTAX</span></span>

### <span data-ttu-id="d7bb4-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7bb4-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bb4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7bb4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bb4-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7bb4-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bb4-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7bb4-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bb4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7bb4-109">DESCRIPTION</span></span>
<span data-ttu-id="d7bb4-110">Обновите свойства подписки на события сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="d7bb4-111">Это можно использовать для обновления фильтра, назначения или меток существующей подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="d7bb4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7bb4-112">EXAMPLES</span></span>

### <span data-ttu-id="d7bb4-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7bb4-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="d7bb4-114">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="d7bb4-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="d7bb4-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d7bb4-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="d7bb4-116">Обновляет конечную точку подписки на событие \` ES1 \` для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="d7bb4-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="d7bb4-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d7bb4-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="d7bb4-118">Обновляет свойства подписки на события \` ES1 \` для пространства имен EventHub ContosoNamespace с новой конечной точкой AS, \` https://requestb.in/1kxxoui1\ а новый фильтр SubjectEndsWith — как \` JPG.\`</span><span class="sxs-lookup"><span data-stu-id="d7bb4-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="d7bb4-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d7bb4-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="d7bb4-120">Обновляет свойства подписок на события \` ES1 \` для группы ресурсов \` MyResourceGroupName \` с новыми метками $labels.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="d7bb4-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7bb4-121">PARAMETERS</span></span>

### <span data-ttu-id="d7bb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bb4-122">-DefaultProfile</span></span>
<span data-ttu-id="d7bb4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bb4-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d7bb4-124">-Endpoint</span></span>
<span data-ttu-id="d7bb4-125">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="d7bb4-126">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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

### <span data-ttu-id="d7bb4-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d7bb4-127">-EndpointType</span></span>
<span data-ttu-id="d7bb4-128">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-128">Endpoint Type.</span></span>
<span data-ttu-id="d7bb4-129">Это может быть веб-перехватчик или eventhub</span><span class="sxs-lookup"><span data-stu-id="d7bb4-129">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bb4-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d7bb4-130">-EventSubscriptionName</span></span>
<span data-ttu-id="d7bb4-131">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="d7bb4-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="d7bb4-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="d7bb4-132">-IncludedEventType</span></span>
<span data-ttu-id="d7bb4-133">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="d7bb4-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7bb4-134">-InputObject</span></span>
<span data-ttu-id="d7bb4-135">Объект EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-135">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bb4-136">-Label</span><span class="sxs-lookup"><span data-stu-id="d7bb4-136">-Label</span></span>
<span data-ttu-id="d7bb4-137">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="d7bb4-137">Labels for the event subscription</span></span>

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

### <span data-ttu-id="d7bb4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bb4-138">-ResourceGroupName</span></span>
<span data-ttu-id="d7bb4-139">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-139">The resource group of the topic.</span></span>

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

### <span data-ttu-id="d7bb4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bb4-140">-ResourceId</span></span>
<span data-ttu-id="d7bb4-141">Идентификатор ресурса, для которого была создана подписка на событие.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="d7bb4-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d7bb4-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="d7bb4-143">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="d7bb4-144">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-144">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="d7bb4-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="d7bb4-145">-SubjectEndsWith</span></span>
<span data-ttu-id="d7bb4-146">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="d7bb4-147">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-147">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="d7bb4-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d7bb4-148">-TopicName</span></span>
<span data-ttu-id="d7bb4-149">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-149">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d7bb4-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7bb4-150">-Confirm</span></span>
<span data-ttu-id="d7bb4-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bb4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bb4-152">-WhatIf</span></span>
<span data-ttu-id="d7bb4-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bb4-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bb4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bb4-155">CommonParameters</span></span>
<span data-ttu-id="d7bb4-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7bb4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bb4-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bb4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bb4-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7bb4-158">INPUTS</span></span>

### <span data-ttu-id="d7bb4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bb4-159">System.String</span></span>

### <span data-ttu-id="d7bb4-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d7bb4-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="d7bb4-161">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7bb4-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d7bb4-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7bb4-162">OUTPUTS</span></span>

### <span data-ttu-id="d7bb4-163">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d7bb4-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d7bb4-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7bb4-164">NOTES</span></span>

## <span data-ttu-id="d7bb4-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7bb4-165">RELATED LINKS</span></span>
