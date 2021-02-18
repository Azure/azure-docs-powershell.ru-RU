---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214804"
---
# <span data-ttu-id="4fc77-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc77-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="4fc77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc77-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc77-103">Получает сведения о подписке на событие или список всех подписок на события в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc77-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="4fc77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fc77-104">SYNTAX</span></span>

### <span data-ttu-id="4fc77-105">EventSubscriptionTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fc77-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc77-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc77-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc77-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fc77-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc77-113">DESCRIPTION</span></span>
<span data-ttu-id="4fc77-114">Этот Get-AzEventGridSubscription возвращает сведения о указанной подписке на сетку событий или список всех подписок на сетку событий в текущей подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc77-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="4fc77-115">Если за предоставлено название подписки на событие, возвращаются сведения об отдельной подписке на сетку событий.</span><span class="sxs-lookup"><span data-stu-id="4fc77-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="4fc77-116">Если название подписки на событие не предоставлено, возвращается список всех подписок на события.</span><span class="sxs-lookup"><span data-stu-id="4fc77-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="4fc77-117">Количество элементов, возвращаемых в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="4fc77-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="4fc77-118">Если значение "Верхнее" не указано или $null, в списке будут указаны все элементы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="4fc77-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="4fc77-119">В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="4fc77-120">Если по-прежнему доступны дополнительные подписки на события, значение в NextLink следует использовать в следующем звонке, чтобы получить следующую страницу подписок на события.</span><span class="sxs-lookup"><span data-stu-id="4fc77-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="4fc77-121">Наконец, параметр ODataQuery используется для фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="4fc77-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="4fc77-122">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="4fc77-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="4fc77-123">Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="4fc77-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="4fc77-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fc77-124">EXAMPLES</span></span>

### <span data-ttu-id="4fc77-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fc77-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4fc77-126">Сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="4fc77-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4fc77-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4fc77-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="4fc77-128">Получает сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName, включая полный URL-адрес конечной точки, если это подписка на событие на основе \` webhook.</span><span class="sxs-lookup"><span data-stu-id="4fc77-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="4fc77-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4fc77-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="4fc77-130">Получите список всех подписок на события, созданные для темы "Тема1", в группе ресурсов \` \` \` MyResourceGroupName \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="4fc77-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="4fc77-131">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4fc77-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-132">Со списком первых 10 подписок на события (если таковые есть), созданных для темы "Тема1", в группе ресурсов \` \` \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="4fc77-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-133">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-134">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-135">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-136">Пример 5</span><span class="sxs-lookup"><span data-stu-id="4fc77-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4fc77-137">Получает сведения о подписке \` на событие EventSubscription1, созданной для группы \` ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="4fc77-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4fc77-138">Пример 6</span><span class="sxs-lookup"><span data-stu-id="4fc77-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4fc77-139">Получает сведения о подписке \` на событие EventSubscription1, \` созданной для выбранной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc77-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="4fc77-140">Пример 7</span><span class="sxs-lookup"><span data-stu-id="4fc77-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="4fc77-141">Список всех подписок на глобальные события, созданные в группе ресурсов \` MyResourceGroupName \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="4fc77-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="4fc77-142">Пример 8</span><span class="sxs-lookup"><span data-stu-id="4fc77-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-143">Со списком первых 5 подписок на события (если таковые есть), созданных в группе ресурсов \` MyResourceGroupName, удовлетворяющий $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="4fc77-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-144">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-145">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-146">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-147">Пример 9</span><span class="sxs-lookup"><span data-stu-id="4fc77-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="4fc77-148">Возвращает список всех подписок на глобальные события, созданные в выбранной подписке Azure без разрывления на них разрывений.</span><span class="sxs-lookup"><span data-stu-id="4fc77-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="4fc77-149">Пример 10</span><span class="sxs-lookup"><span data-stu-id="4fc77-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-150">Список первых 15 подписок на глобальные события (если они есть), созданных в выбранной подписке Azure, которая удовлетворяет запросу $odataFilter событий.</span><span class="sxs-lookup"><span data-stu-id="4fc77-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-151">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-152">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-153">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-154">Пример 11</span><span class="sxs-lookup"><span data-stu-id="4fc77-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="4fc77-155">Получает список всех подписок на региональные события, созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2 \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="4fc77-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="4fc77-156">Пример 12</span><span class="sxs-lookup"><span data-stu-id="4fc77-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-157">Перечислите первые 15 подписок на региональные события (если таковые есть), созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2, удовлетворяющий $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="4fc77-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-158">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-159">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-160">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-161">Пример 13</span><span class="sxs-lookup"><span data-stu-id="4fc77-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="4fc77-162">Возвращает список всех подписок на события, созданные для указанного пространства имен EventHub без разбиения на разбиение на нее.</span><span class="sxs-lookup"><span data-stu-id="4fc77-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="4fc77-163">Пример 14</span><span class="sxs-lookup"><span data-stu-id="4fc77-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-164">Со списком первых 25 подписок на события (если они есть), созданных для указанного пространства имен EventHub, удовлетворяющий $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="4fc77-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-165">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-166">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-167">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-168">Пример 15</span><span class="sxs-lookup"><span data-stu-id="4fc77-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="4fc77-169">Возвращает список всех подписок на события, созданные для определенного типа темы (пространства имен EventHub) в указанном расположении без разбиения на разделы.</span><span class="sxs-lookup"><span data-stu-id="4fc77-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="4fc77-170">Пример 16</span><span class="sxs-lookup"><span data-stu-id="4fc77-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-171">Список первых 15 подписок на события (если они есть), созданные для указанного типа темы (пространства имен EventHub) в указанном расположении, которое удовлетворяет запросу $odataFilter событий.</span><span class="sxs-lookup"><span data-stu-id="4fc77-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-172">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-173">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-174">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="4fc77-175">Пример 17</span><span class="sxs-lookup"><span data-stu-id="4fc77-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="4fc77-176">Возвращает список всех подписок на события, созданные для определенной группы ресурсов без разрывления на них разрывений.</span><span class="sxs-lookup"><span data-stu-id="4fc77-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="4fc77-177">Пример 18</span><span class="sxs-lookup"><span data-stu-id="4fc77-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="4fc77-178">Со списком первых 100 подписок на события (если они есть), созданных для определенной группы ресурсов, которая удовлетворяет $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="4fc77-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="4fc77-179">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4fc77-180">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="4fc77-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4fc77-181">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="4fc77-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="4fc77-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fc77-182">PARAMETERS</span></span>

### <span data-ttu-id="4fc77-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc77-183">-DefaultProfile</span></span>
<span data-ttu-id="4fc77-184">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4fc77-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fc77-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="4fc77-185">-DomainInputObject</span></span>
<span data-ttu-id="4fc77-186">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="4fc77-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="4fc77-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="4fc77-187">-DomainName</span></span>
<span data-ttu-id="4fc77-188">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4fc77-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="4fc77-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="4fc77-190">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="4fc77-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="4fc77-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="4fc77-191">-DomainTopicName</span></span>
<span data-ttu-id="4fc77-192">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4fc77-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4fc77-193">-EventSubscriptionName</span></span>
<span data-ttu-id="4fc77-194">Название подписки на событие</span><span class="sxs-lookup"><span data-stu-id="4fc77-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4fc77-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="4fc77-196">Включив полный URL-адрес конечной точки назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="4fc77-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc77-197">-InputObject</span></span>
<span data-ttu-id="4fc77-198">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="4fc77-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="4fc77-199">-Location</span><span class="sxs-lookup"><span data-stu-id="4fc77-199">-Location</span></span>
<span data-ttu-id="4fc77-200">Расположение</span><span class="sxs-lookup"><span data-stu-id="4fc77-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="4fc77-201">-NextLink</span></span>
<span data-ttu-id="4fc77-202">Ссылка на следующую страницу ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="4fc77-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="4fc77-203">Это значение получается при первом Get-AzEventGrid, когда для запроса остается доступно больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc77-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4fc77-204">-ODataQuery</span></span>
<span data-ttu-id="4fc77-205">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="4fc77-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="4fc77-206">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="4fc77-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc77-207">-ResourceGroupName</span></span>
<span data-ttu-id="4fc77-208">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc77-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc77-209">-ResourceId</span></span>
<span data-ttu-id="4fc77-210">Идентификатор ресурса, для которого созданы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="4fc77-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="4fc77-211">-Top</span><span class="sxs-lookup"><span data-stu-id="4fc77-211">-Top</span></span>
<span data-ttu-id="4fc77-212">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="4fc77-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="4fc77-213">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="4fc77-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4fc77-214">-TopicName</span></span>
<span data-ttu-id="4fc77-215">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4fc77-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="4fc77-216">-TopicTypeName</span></span>
<span data-ttu-id="4fc77-217">Имя TopicType</span><span class="sxs-lookup"><span data-stu-id="4fc77-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc77-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc77-218">CommonParameters</span></span>
<span data-ttu-id="4fc77-219">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc77-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc77-220">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc77-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc77-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc77-221">INPUTS</span></span>

### <span data-ttu-id="4fc77-222">System.String</span><span class="sxs-lookup"><span data-stu-id="4fc77-222">System.String</span></span>

### <span data-ttu-id="4fc77-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="4fc77-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="4fc77-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="4fc77-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="4fc77-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4fc77-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="4fc77-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4fc77-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4fc77-227">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc77-227">OUTPUTS</span></span>

### <span data-ttu-id="4fc77-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc77-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="4fc77-229">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fc77-229">NOTES</span></span>

## <span data-ttu-id="4fc77-230">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fc77-230">RELATED LINKS</span></span>
