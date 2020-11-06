---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565448"
---
# <span data-ttu-id="54f3c-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="54f3c-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="54f3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="54f3c-103">Получает сведения о подписке на события или возвращает список всех подписок на события в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="54f3c-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54f3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54f3c-104">SYNTAX</span></span>

### <span data-ttu-id="54f3c-105">EventSubscriptionTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54f3c-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54f3c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f3c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54f3c-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f3c-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54f3c-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54f3c-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54f3c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f3c-109">DESCRIPTION</span></span>
<span data-ttu-id="54f3c-110">Командлет Get-AzureRmEventGridSubscription получает либо сведения о заданной подписке на сетку событий, либо список всех подписок на сетку событий в текущей подписке или группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="54f3c-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="54f3c-111">Если задано имя подписки на событие, возвращается информация об одной подписке на сетку событий.</span><span class="sxs-lookup"><span data-stu-id="54f3c-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="54f3c-112">Если имя подписки на событие не указано, возвращается список всех подписок на события.</span><span class="sxs-lookup"><span data-stu-id="54f3c-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="54f3c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54f3c-113">EXAMPLES</span></span>

### <span data-ttu-id="54f3c-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54f3c-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54f3c-115">Получает сведения о подписке \` на события EventSubscription1, \` созданной для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="54f3c-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54f3c-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="54f3c-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="54f3c-117">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , включая полный URL-адрес конечной точки, если он является подпиской на события на основе веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="54f3c-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="54f3c-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="54f3c-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="54f3c-119">Получите список всех подписок на события, созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="54f3c-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54f3c-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="54f3c-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54f3c-121">Получает подробные сведения о подписке на события \` EventSubscription1 \` , созданные для группы ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="54f3c-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54f3c-122">Пример 5</span><span class="sxs-lookup"><span data-stu-id="54f3c-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54f3c-123">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для выбранной в данный момент подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="54f3c-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="54f3c-124">Пример 6</span><span class="sxs-lookup"><span data-stu-id="54f3c-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="54f3c-125">Получает список всех глобальных подписок на события, созданных в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="54f3c-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54f3c-126">Пример 7</span><span class="sxs-lookup"><span data-stu-id="54f3c-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="54f3c-127">Получает список всех глобальных подписок на события, созданных в текущей выбранной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="54f3c-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="54f3c-128">Пример 8</span><span class="sxs-lookup"><span data-stu-id="54f3c-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="54f3c-129">Получает список всех региональных подписок на мероприятия, созданных в группе ресурсов \` MyResourceGroupName \` в указанном расположении \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="54f3c-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="54f3c-130">Пример 9</span><span class="sxs-lookup"><span data-stu-id="54f3c-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="54f3c-131">Получает список всех подписок на события, созданных для указанного пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="54f3c-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="54f3c-132">Пример 10</span><span class="sxs-lookup"><span data-stu-id="54f3c-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="54f3c-133">Получает список всех подписок на события, созданных для указанного типа темы (пространства имен EventHub) в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="54f3c-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="54f3c-134">Пример 11</span><span class="sxs-lookup"><span data-stu-id="54f3c-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="54f3c-135">Возвращает список всех подписок на события, созданных для определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54f3c-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="54f3c-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54f3c-136">PARAMETERS</span></span>

### <span data-ttu-id="54f3c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f3c-137">-DefaultProfile</span></span>
<span data-ttu-id="54f3c-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54f3c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54f3c-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="54f3c-139">-EventSubscriptionName</span></span>
<span data-ttu-id="54f3c-140">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="54f3c-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="54f3c-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="54f3c-142">Включите полный URL-адрес конечной точки для назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="54f3c-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54f3c-143">-InputObject</span></span>
<span data-ttu-id="54f3c-144">Объект подписки на события EventGrid.</span><span class="sxs-lookup"><span data-stu-id="54f3c-144">EventGrid Event Subscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-145">-Location</span><span class="sxs-lookup"><span data-stu-id="54f3c-145">-Location</span></span>
<span data-ttu-id="54f3c-146">Поиска</span><span class="sxs-lookup"><span data-stu-id="54f3c-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f3c-147">-ResourceGroupName</span></span>
<span data-ttu-id="54f3c-148">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54f3c-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f3c-149">-ResourceId</span></span>
<span data-ttu-id="54f3c-150">Идентификатор ресурса, для которого созданы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="54f3c-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="54f3c-151">-TopicName</span></span>
<span data-ttu-id="54f3c-152">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="54f3c-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="54f3c-153">-TopicTypeName</span></span>
<span data-ttu-id="54f3c-154">Имя TopicType</span><span class="sxs-lookup"><span data-stu-id="54f3c-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f3c-155">CommonParameters</span></span>
<span data-ttu-id="54f3c-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54f3c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f3c-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f3c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f3c-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54f3c-158">INPUTS</span></span>

### <span data-ttu-id="54f3c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="54f3c-159">System.String</span></span>

### <span data-ttu-id="54f3c-160">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="54f3c-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="54f3c-161">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="54f3c-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="54f3c-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f3c-162">OUTPUTS</span></span>

### <span data-ttu-id="54f3c-163">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="54f3c-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="54f3c-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="54f3c-164">NOTES</span></span>

## <span data-ttu-id="54f3c-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54f3c-165">RELATED LINKS</span></span>
