---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390863"
---
# <span data-ttu-id="d989a-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d989a-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="d989a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d989a-102">SYNOPSIS</span></span>
<span data-ttu-id="d989a-103">Получает сведения о подписке на событие или список всех подписок на события в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="d989a-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="d989a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d989a-104">SYNTAX</span></span>

### <span data-ttu-id="d989a-105">EventSubscriptionTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d989a-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d989a-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d989a-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="d989a-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d989a-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d989a-113">DESCRIPTION</span></span>
<span data-ttu-id="d989a-114">Этот Get-AzEventGridSubscription возвращает сведения о указанной подписке на сетку событий или список всех подписок на сетку событий в текущей подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d989a-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="d989a-115">Если за предоставлено название подписки на событие, возвращаются сведения об отдельной подписке на сетку событий.</span><span class="sxs-lookup"><span data-stu-id="d989a-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="d989a-116">Если название подписки на событие не предоставлено, возвращается список всех подписок на события.</span><span class="sxs-lookup"><span data-stu-id="d989a-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="d989a-117">Количество элементов, возвращаемых в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="d989a-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="d989a-118">Если значение "Верхнее" не указано или $null, в списке будут указаны все элементы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d989a-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="d989a-119">В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.</span><span class="sxs-lookup"><span data-stu-id="d989a-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="d989a-120">Если по-прежнему доступны дополнительные подписки на события, значение в NextLink нужно использовать в следующем звонке, чтобы получить следующую страницу подписок на события.</span><span class="sxs-lookup"><span data-stu-id="d989a-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="d989a-121">Наконец, для фильтрации результатов поиска используется параметр ODataQuery.</span><span class="sxs-lookup"><span data-stu-id="d989a-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="d989a-122">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="d989a-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="d989a-123">Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="d989a-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="d989a-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d989a-124">EXAMPLES</span></span>

### <span data-ttu-id="d989a-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d989a-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d989a-126">Сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="d989a-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d989a-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d989a-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="d989a-128">Получает сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName, включая полный URL-адрес конечной точки, если это подписка на событие на основе \` webhook.</span><span class="sxs-lookup"><span data-stu-id="d989a-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="d989a-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d989a-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="d989a-130">Получите список всех подписок на события, созданные для темы "Тема1" в группе ресурсов \` \` \` MyResourceGroupName \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="d989a-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="d989a-131">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d989a-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-132">Со списком первых 10 подписок на события (если таковые есть), созданных для темы "Тема1", в группе ресурсов \` \` \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="d989a-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-133">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-134">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-135">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-136">Пример 5</span><span class="sxs-lookup"><span data-stu-id="d989a-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d989a-137">Получает сведения о подписке \` на событие EventSubscription1, созданной для группы \` ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="d989a-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d989a-138">Пример 6</span><span class="sxs-lookup"><span data-stu-id="d989a-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d989a-139">Получает сведения о подписке \` на событие EventSubscription1, \` созданной для выбранной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d989a-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="d989a-140">Пример 7</span><span class="sxs-lookup"><span data-stu-id="d989a-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="d989a-141">Список всех подписок на глобальные события, созданные в группе ресурсов \` MyResourceGroupName \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="d989a-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="d989a-142">Пример 8</span><span class="sxs-lookup"><span data-stu-id="d989a-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-143">Со списком первых 5 подписок на события (если таковые есть), созданных в группе ресурсов \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="d989a-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-144">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-145">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-146">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-147">Пример 9</span><span class="sxs-lookup"><span data-stu-id="d989a-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="d989a-148">Возвращает список всех подписок на глобальные события, созданные в выбранной подписке Azure без разрывления на них разрывений.</span><span class="sxs-lookup"><span data-stu-id="d989a-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="d989a-149">Пример 10</span><span class="sxs-lookup"><span data-stu-id="d989a-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-150">Список первых 15 подписок на глобальные события (если они есть), созданных в выбранной подписке Azure, которая удовлетворяет запросу $odataFilter событий.</span><span class="sxs-lookup"><span data-stu-id="d989a-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-151">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-152">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-153">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-154">Пример 11</span><span class="sxs-lookup"><span data-stu-id="d989a-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="d989a-155">Получает список всех подписок на региональные события, созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2 \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="d989a-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="d989a-156">Пример 12</span><span class="sxs-lookup"><span data-stu-id="d989a-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-157">Перечислите первые 15 подписок на региональные события (если таковые есть), созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2, удовлетворяющий $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="d989a-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-158">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-159">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-160">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-161">Пример 13</span><span class="sxs-lookup"><span data-stu-id="d989a-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="d989a-162">Возвращает список всех подписок на события, созданные для указанного пространства имен EventHub без разбиения на разбиение на нее.</span><span class="sxs-lookup"><span data-stu-id="d989a-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="d989a-163">Пример 14</span><span class="sxs-lookup"><span data-stu-id="d989a-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-164">Со списком первых 25 подписок на события (если они есть), созданных для указанного пространства имен EventHub, удовлетворяющий $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="d989a-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-165">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-166">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-167">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-168">Пример 15</span><span class="sxs-lookup"><span data-stu-id="d989a-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="d989a-169">Возвращает список всех подписок на события, созданные для определенного типа темы (пространства имен EventHub) в указанном расположении без разбиения на разделы.</span><span class="sxs-lookup"><span data-stu-id="d989a-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="d989a-170">Пример 16</span><span class="sxs-lookup"><span data-stu-id="d989a-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-171">Список первых 15 подписок на события (если они есть), созданные для указанного типа темы (пространства имен EventHub) в указанном расположении, которое удовлетворяет запросу $odataFilter событий.</span><span class="sxs-lookup"><span data-stu-id="d989a-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-172">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-173">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-174">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d989a-175">Пример 17</span><span class="sxs-lookup"><span data-stu-id="d989a-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="d989a-176">Возвращает список всех подписок на события, созданные для определенной группы ресурсов без разрывления на них.</span><span class="sxs-lookup"><span data-stu-id="d989a-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="d989a-177">Пример 18</span><span class="sxs-lookup"><span data-stu-id="d989a-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="d989a-178">Со списком первых 100 подписок на события (если они есть), созданных для определенной группы ресурсов, которая удовлетворяет $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="d989a-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d989a-179">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d989a-180">Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="d989a-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d989a-181">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="d989a-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="d989a-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d989a-182">PARAMETERS</span></span>

### <span data-ttu-id="d989a-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d989a-183">-DefaultProfile</span></span>
<span data-ttu-id="d989a-184">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d989a-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d989a-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="d989a-185">-DomainInputObject</span></span>
<span data-ttu-id="d989a-186">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="d989a-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="d989a-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d989a-187">-DomainName</span></span>
<span data-ttu-id="d989a-188">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d989a-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="d989a-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="d989a-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="d989a-190">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="d989a-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="d989a-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="d989a-191">-DomainTopicName</span></span>
<span data-ttu-id="d989a-192">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d989a-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="d989a-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d989a-193">-EventSubscriptionName</span></span>
<span data-ttu-id="d989a-194">Название подписки на событие</span><span class="sxs-lookup"><span data-stu-id="d989a-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="d989a-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="d989a-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="d989a-196">Включив полный URL-адрес конечной точки назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="d989a-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="d989a-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d989a-197">-InputObject</span></span>
<span data-ttu-id="d989a-198">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="d989a-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d989a-199">-Location</span><span class="sxs-lookup"><span data-stu-id="d989a-199">-Location</span></span>
<span data-ttu-id="d989a-200">Расположение</span><span class="sxs-lookup"><span data-stu-id="d989a-200">Location</span></span>

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

### <span data-ttu-id="d989a-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="d989a-201">-NextLink</span></span>
<span data-ttu-id="d989a-202">Ссылка на следующую страницу ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d989a-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="d989a-203">Это значение получают при первом Get-AzEventGrid, когда для запроса по-прежнему доступно больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d989a-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="d989a-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d989a-204">-ODataQuery</span></span>
<span data-ttu-id="d989a-205">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="d989a-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d989a-206">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="d989a-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="d989a-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d989a-207">-ResourceGroupName</span></span>
<span data-ttu-id="d989a-208">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d989a-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="d989a-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d989a-209">-ResourceId</span></span>
<span data-ttu-id="d989a-210">Идентификатор ресурса, для которого созданы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d989a-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="d989a-211">-Top</span><span class="sxs-lookup"><span data-stu-id="d989a-211">-Top</span></span>
<span data-ttu-id="d989a-212">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="d989a-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d989a-213">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="d989a-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="d989a-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d989a-214">-TopicName</span></span>
<span data-ttu-id="d989a-215">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d989a-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="d989a-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="d989a-216">-TopicTypeName</span></span>
<span data-ttu-id="d989a-217">Имя TopicType</span><span class="sxs-lookup"><span data-stu-id="d989a-217">TopicType name</span></span>

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

### <span data-ttu-id="d989a-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d989a-218">CommonParameters</span></span>
<span data-ttu-id="d989a-219">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d989a-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d989a-220">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d989a-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d989a-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d989a-221">INPUTS</span></span>

### <span data-ttu-id="d989a-222">System.String</span><span class="sxs-lookup"><span data-stu-id="d989a-222">System.String</span></span>

### <span data-ttu-id="d989a-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="d989a-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="d989a-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d989a-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="d989a-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d989a-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="d989a-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d989a-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d989a-227">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d989a-227">OUTPUTS</span></span>

### <span data-ttu-id="d989a-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d989a-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d989a-229">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d989a-229">NOTES</span></span>

## <span data-ttu-id="d989a-230">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d989a-230">RELATED LINKS</span></span>
