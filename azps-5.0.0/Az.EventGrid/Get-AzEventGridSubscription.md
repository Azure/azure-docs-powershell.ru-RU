---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245472"
---
# <span data-ttu-id="ba9b1-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ba9b1-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="ba9b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9b1-103">Получает сведения о подписке на события или возвращает список всех подписок на события в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="ba9b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba9b1-104">SYNTAX</span></span>

### <span data-ttu-id="ba9b1-105">EventSubscriptionTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba9b1-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b1-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b1-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba9b1-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba9b1-113">DESCRIPTION</span></span>
<span data-ttu-id="ba9b1-114">Командлет Get-AzEventGridSubscription получает либо сведения о заданной подписке на сетку событий, либо список всех подписок на сетку событий в текущей подписке или группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="ba9b1-115">Если задано имя подписки на событие, возвращается информация об одной подписке на сетку событий.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="ba9b1-116">Если имя подписки на событие не указано, возвращается список всех подписок на события.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="ba9b1-117">Количество элементов, возвращенных в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ba9b1-118">Если значение Top не указано или $null, список будет содержать все элементы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="ba9b1-119">В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ba9b1-120">Если по-прежнему доступны дополнительные подписки на события, значение в NextLink следует использовать при следующем вызове для получения следующей страницы подписок на события.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="ba9b1-121">Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ba9b1-122">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ba9b1-123">Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ba9b1-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba9b1-124">EXAMPLES</span></span>

### <span data-ttu-id="ba9b1-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba9b1-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba9b1-126">Получает сведения о подписке \` на события EventSubscription1, \` созданной для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ba9b1-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ba9b1-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ba9b1-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="ba9b1-128">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , включая полный URL-адрес конечной точки, если он является подпиской на события на основе веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="ba9b1-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ba9b1-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="ba9b1-130">Получение списка всех подписок на события, созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ba9b1-131">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ba9b1-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-132">Список первых 10 подписок на события (если таковые имеются), созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , которые удовлетворяют $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-133">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-134">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-135">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-136">Пример 5</span><span class="sxs-lookup"><span data-stu-id="ba9b1-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba9b1-137">Получает подробные сведения о подписке на события \` EventSubscription1 \` , созданные для группы ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ba9b1-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ba9b1-138">Пример 6</span><span class="sxs-lookup"><span data-stu-id="ba9b1-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba9b1-139">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для выбранной в данный момент подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="ba9b1-140">Пример 7</span><span class="sxs-lookup"><span data-stu-id="ba9b1-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ba9b1-141">Получает список всех глобальных подписок на события, созданных в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ba9b1-142">Пример 8</span><span class="sxs-lookup"><span data-stu-id="ba9b1-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-143">Список первых пяти подписок на события (при их наличии), созданных в группе ресурсов \` MyResourceGroupName \` , которая удовлетворяет запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-144">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-145">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-146">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-147">Пример 9</span><span class="sxs-lookup"><span data-stu-id="ba9b1-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="ba9b1-148">Получает список всех глобальных подписок на события, созданных в текущей выбранной подписке Azure без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="ba9b1-149">Пример 10</span><span class="sxs-lookup"><span data-stu-id="ba9b1-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-150">Список первых 15 глобальных подписок на события (если таковые имеются), созданных в текущей выбранной подписке Azure, соответствующей $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-151">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-152">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-153">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-154">Пример 11</span><span class="sxs-lookup"><span data-stu-id="ba9b1-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="ba9b1-155">Получает список всех региональных подписок на мероприятия, созданных в группе ресурсов \` MyResourceGroupName \` в указанном расположении \` westus2 \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="ba9b1-156">Пример 12</span><span class="sxs-lookup"><span data-stu-id="ba9b1-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-157">Перечислите первые 15 региональных подписок на события (если таковые имеются), созданные в группе ресурсов \` MyResourceGroupName \` в указанном местоположении \` westus2 \` , которые удовлетворяют $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-158">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-159">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-160">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-161">Пример 13</span><span class="sxs-lookup"><span data-stu-id="ba9b1-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="ba9b1-162">Получает список всех подписок на события, созданных для указанного пространства имен EventHub без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="ba9b1-163">Пример 14</span><span class="sxs-lookup"><span data-stu-id="ba9b1-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-164">Список первых 25 подписок на события (если таковые имеются), созданных для указанного пространства имен EventHub, удовлетворяющего запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-165">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-166">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-167">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-168">Пример 15</span><span class="sxs-lookup"><span data-stu-id="ba9b1-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="ba9b1-169">Получает список всех подписок на события, созданных для указанного типа темы (пространства имен EventHub) в указанном месте без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="ba9b1-170">Пример 16</span><span class="sxs-lookup"><span data-stu-id="ba9b1-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-171">Список первых 15 подписок на события (если таковые имеются), созданных для указанного типа темы (пространства имен EventHub) в указанном расположении, удовлетворяющем запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-172">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-173">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-174">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba9b1-175">Пример 17</span><span class="sxs-lookup"><span data-stu-id="ba9b1-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ba9b1-176">Возвращает список всех подписок на события, созданных для определенной группы ресурсов без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="ba9b1-177">Пример 18</span><span class="sxs-lookup"><span data-stu-id="ba9b1-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba9b1-178">Список первых 100 подписок на события (если таковые имеются), созданных для конкретной группы ресурсов, которая удовлетворяет запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba9b1-179">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba9b1-180">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba9b1-181">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="ba9b1-182">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba9b1-182">PARAMETERS</span></span>

### <span data-ttu-id="ba9b1-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9b1-183">-DefaultProfile</span></span>
<span data-ttu-id="ba9b1-184">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba9b1-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba9b1-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ba9b1-185">-DomainInputObject</span></span>
<span data-ttu-id="ba9b1-186">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ba9b1-187">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="ba9b1-187">-DomainName</span></span>
<span data-ttu-id="ba9b1-188">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="ba9b1-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ba9b1-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ba9b1-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="ba9b1-190">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="ba9b1-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ba9b1-191">-DomainTopicName</span></span>
<span data-ttu-id="ba9b1-192">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ba9b1-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ba9b1-193">-EventSubscriptionName</span></span>
<span data-ttu-id="ba9b1-194">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="ba9b1-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="ba9b1-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ba9b1-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="ba9b1-196">Включите полный URL-адрес конечной точки для назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="ba9b1-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba9b1-197">-InputObject</span></span>
<span data-ttu-id="ba9b1-198">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ba9b1-199">-Location</span><span class="sxs-lookup"><span data-stu-id="ba9b1-199">-Location</span></span>
<span data-ttu-id="ba9b1-200">Поиска</span><span class="sxs-lookup"><span data-stu-id="ba9b1-200">Location</span></span>

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

### <span data-ttu-id="ba9b1-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ba9b1-201">-NextLink</span></span>
<span data-ttu-id="ba9b1-202">Ссылка на следующую страницу ресурсов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ba9b1-203">Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ba9b1-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ba9b1-204">-ODataQuery</span></span>
<span data-ttu-id="ba9b1-205">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ba9b1-206">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ba9b1-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9b1-207">-ResourceGroupName</span></span>
<span data-ttu-id="ba9b1-208">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba9b1-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9b1-209">-ResourceId</span></span>
<span data-ttu-id="ba9b1-210">Идентификатор ресурса, для которого созданы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="ba9b1-211">-Top</span><span class="sxs-lookup"><span data-stu-id="ba9b1-211">-Top</span></span>
<span data-ttu-id="ba9b1-212">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ba9b1-213">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ba9b1-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ba9b1-214">-TopicName</span></span>
<span data-ttu-id="ba9b1-215">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ba9b1-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="ba9b1-216">-TopicTypeName</span></span>
<span data-ttu-id="ba9b1-217">Имя TopicType</span><span class="sxs-lookup"><span data-stu-id="ba9b1-217">TopicType name</span></span>

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

### <span data-ttu-id="ba9b1-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9b1-218">CommonParameters</span></span>
<span data-ttu-id="ba9b1-219">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9b1-220">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba9b1-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9b1-221">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba9b1-221">INPUTS</span></span>

### <span data-ttu-id="ba9b1-222">System. String</span><span class="sxs-lookup"><span data-stu-id="ba9b1-222">System.String</span></span>

### <span data-ttu-id="ba9b1-223">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ba9b1-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ba9b1-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ba9b1-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ba9b1-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ba9b1-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ba9b1-226">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ba9b1-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ba9b1-227">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba9b1-227">OUTPUTS</span></span>

### <span data-ttu-id="ba9b1-228">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ba9b1-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ba9b1-229">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba9b1-229">NOTES</span></span>

## <span data-ttu-id="ba9b1-230">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba9b1-230">RELATED LINKS</span></span>
