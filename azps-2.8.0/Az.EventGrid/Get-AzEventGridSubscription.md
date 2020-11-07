---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721006"
---
# <span data-ttu-id="a81ac-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a81ac-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="a81ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a81ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a81ac-103">Получает сведения о подписке на события или возвращает список всех подписок на события в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="a81ac-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="a81ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a81ac-104">SYNTAX</span></span>

### <span data-ttu-id="a81ac-105">EventSubscriptionTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a81ac-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81ac-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a81ac-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81ac-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a81ac-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81ac-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81ac-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81ac-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81ac-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a81ac-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a81ac-113">DESCRIPTION</span></span>
<span data-ttu-id="a81ac-114">Командлет Get-AzEventGridSubscription получает либо сведения о заданной подписке на сетку событий, либо список всех подписок на сетку событий в текущей подписке или группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a81ac-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a81ac-115">Если задано имя подписки на событие, возвращается информация об одной подписке на сетку событий.</span><span class="sxs-lookup"><span data-stu-id="a81ac-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a81ac-116">Если имя подписки на событие не указано, возвращается список всех подписок на события.</span><span class="sxs-lookup"><span data-stu-id="a81ac-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="a81ac-117">Количество элементов, возвращенных в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="a81ac-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="a81ac-118">Если значение Top не указано или $null, список будет содержать все элементы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="a81ac-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="a81ac-119">В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="a81ac-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="a81ac-120">Если по-прежнему доступны дополнительные подписки на события, значение в NextLink следует использовать при следующем вызове для получения следующей страницы подписок на события.</span><span class="sxs-lookup"><span data-stu-id="a81ac-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="a81ac-121">Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="a81ac-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="a81ac-122">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="a81ac-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="a81ac-123">Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="a81ac-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="a81ac-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a81ac-124">EXAMPLES</span></span>

### <span data-ttu-id="a81ac-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a81ac-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a81ac-126">Получает сведения о подписке \` на события EventSubscription1, \` созданной для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a81ac-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a81ac-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a81ac-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a81ac-128">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , включая полный URL-адрес конечной точки, если он является подпиской на события на основе веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="a81ac-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a81ac-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a81ac-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a81ac-130">Получение списка всех подписок на события, созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a81ac-131">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a81ac-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-132">Список первых 10 подписок на события (если таковые имеются), созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , которые удовлетворяют $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="a81ac-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-133">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-134">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-135">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-136">Пример 5</span><span class="sxs-lookup"><span data-stu-id="a81ac-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a81ac-137">Получает подробные сведения о подписке на события \` EventSubscription1 \` , созданные для группы ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a81ac-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a81ac-138">Пример 6</span><span class="sxs-lookup"><span data-stu-id="a81ac-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a81ac-139">Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для выбранной в данный момент подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a81ac-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a81ac-140">Пример 7</span><span class="sxs-lookup"><span data-stu-id="a81ac-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a81ac-141">Получает список всех глобальных подписок на события, созданных в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a81ac-142">Пример 8</span><span class="sxs-lookup"><span data-stu-id="a81ac-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-143">Список первых пяти подписок на события (при их наличии), созданных в группе ресурсов \` MyResourceGroupName \` , которая удовлетворяет запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a81ac-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-144">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-145">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-146">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-147">Пример 9</span><span class="sxs-lookup"><span data-stu-id="a81ac-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="a81ac-148">Получает список всех глобальных подписок на события, созданных в текущей выбранной подписке Azure без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="a81ac-149">Пример 10</span><span class="sxs-lookup"><span data-stu-id="a81ac-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-150">Список первых 15 глобальных подписок на события (если таковые имеются), созданных в текущей выбранной подписке Azure, соответствующей $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="a81ac-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-151">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-152">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-153">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-154">Пример 11</span><span class="sxs-lookup"><span data-stu-id="a81ac-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a81ac-155">Получает список всех региональных подписок на мероприятия, созданных в группе ресурсов \` MyResourceGroupName \` в указанном расположении \` westus2 \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="a81ac-156">Пример 12</span><span class="sxs-lookup"><span data-stu-id="a81ac-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-157">Перечислите первые 15 региональных подписок на события (если таковые имеются), созданные в группе ресурсов \` MyResourceGroupName \` в указанном местоположении \` westus2 \` , которые удовлетворяют $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="a81ac-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-158">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-159">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-160">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-161">Пример 13</span><span class="sxs-lookup"><span data-stu-id="a81ac-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a81ac-162">Получает список всех подписок на события, созданных для указанного пространства имен EventHub без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="a81ac-163">Пример 14</span><span class="sxs-lookup"><span data-stu-id="a81ac-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-164">Список первых 25 подписок на события (если таковые имеются), созданных для указанного пространства имен EventHub, удовлетворяющего запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a81ac-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-165">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-166">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-167">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-168">Пример 15</span><span class="sxs-lookup"><span data-stu-id="a81ac-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a81ac-169">Получает список всех подписок на события, созданных для указанного типа темы (пространства имен EventHub) в указанном месте без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="a81ac-170">Пример 16</span><span class="sxs-lookup"><span data-stu-id="a81ac-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-171">Список первых 15 подписок на события (если таковые имеются), созданных для указанного типа темы (пространства имен EventHub) в указанном расположении, удовлетворяющем запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a81ac-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-172">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-173">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-174">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a81ac-175">Пример 17</span><span class="sxs-lookup"><span data-stu-id="a81ac-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a81ac-176">Возвращает список всех подписок на события, созданных для определенной группы ресурсов без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="a81ac-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="a81ac-177">Пример 18</span><span class="sxs-lookup"><span data-stu-id="a81ac-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a81ac-178">Список первых 100 подписок на события (если таковые имеются), созданных для конкретной группы ресурсов, которая удовлетворяет запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a81ac-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a81ac-179">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="a81ac-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a81ac-180">Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a81ac-181">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="a81ac-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="a81ac-182">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a81ac-182">PARAMETERS</span></span>

### <span data-ttu-id="a81ac-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81ac-183">-DefaultProfile</span></span>
<span data-ttu-id="a81ac-184">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a81ac-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a81ac-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a81ac-185">-DomainInputObject</span></span>
<span data-ttu-id="a81ac-186">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a81ac-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a81ac-187">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="a81ac-187">-DomainName</span></span>
<span data-ttu-id="a81ac-188">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="a81ac-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="a81ac-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a81ac-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="a81ac-190">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a81ac-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="a81ac-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a81ac-191">-DomainTopicName</span></span>
<span data-ttu-id="a81ac-192">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a81ac-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="a81ac-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a81ac-193">-EventSubscriptionName</span></span>
<span data-ttu-id="a81ac-194">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="a81ac-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a81ac-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a81ac-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a81ac-196">Включите полный URL-адрес конечной точки для назначения подписки на событие.</span><span class="sxs-lookup"><span data-stu-id="a81ac-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="a81ac-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a81ac-197">-InputObject</span></span>
<span data-ttu-id="a81ac-198">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a81ac-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a81ac-199">-Location</span><span class="sxs-lookup"><span data-stu-id="a81ac-199">-Location</span></span>
<span data-ttu-id="a81ac-200">Поиска</span><span class="sxs-lookup"><span data-stu-id="a81ac-200">Location</span></span>

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

### <span data-ttu-id="a81ac-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a81ac-201">-NextLink</span></span>
<span data-ttu-id="a81ac-202">Ссылка на следующую страницу ресурсов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="a81ac-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="a81ac-203">Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.</span><span class="sxs-lookup"><span data-stu-id="a81ac-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="a81ac-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a81ac-204">-ODataQuery</span></span>
<span data-ttu-id="a81ac-205">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a81ac-206">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="a81ac-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="a81ac-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81ac-207">-ResourceGroupName</span></span>
<span data-ttu-id="a81ac-208">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a81ac-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a81ac-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a81ac-209">-ResourceId</span></span>
<span data-ttu-id="a81ac-210">Идентификатор ресурса, для которого созданы подписки на события.</span><span class="sxs-lookup"><span data-stu-id="a81ac-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="a81ac-211">-Top</span><span class="sxs-lookup"><span data-stu-id="a81ac-211">-Top</span></span>
<span data-ttu-id="a81ac-212">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="a81ac-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a81ac-213">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="a81ac-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="a81ac-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a81ac-214">-TopicName</span></span>
<span data-ttu-id="a81ac-215">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a81ac-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a81ac-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a81ac-216">-TopicTypeName</span></span>
<span data-ttu-id="a81ac-217">Имя TopicType</span><span class="sxs-lookup"><span data-stu-id="a81ac-217">TopicType name</span></span>

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

### <span data-ttu-id="a81ac-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81ac-218">CommonParameters</span></span>
<span data-ttu-id="a81ac-219">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a81ac-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81ac-220">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81ac-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81ac-221">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a81ac-221">INPUTS</span></span>

### <span data-ttu-id="a81ac-222">System. String</span><span class="sxs-lookup"><span data-stu-id="a81ac-222">System.String</span></span>

### <span data-ttu-id="a81ac-223">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a81ac-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a81ac-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a81ac-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a81ac-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a81ac-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="a81ac-226">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a81ac-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a81ac-227">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a81ac-227">OUTPUTS</span></span>

### <span data-ttu-id="a81ac-228">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a81ac-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a81ac-229">Пуск</span><span class="sxs-lookup"><span data-stu-id="a81ac-229">NOTES</span></span>

## <span data-ttu-id="a81ac-230">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a81ac-230">RELATED LINKS</span></span>
