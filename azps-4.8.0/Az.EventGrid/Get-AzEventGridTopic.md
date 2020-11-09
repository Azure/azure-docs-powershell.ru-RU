---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243594"
---
# <span data-ttu-id="c0720-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c0720-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="c0720-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0720-102">SYNOPSIS</span></span>
<span data-ttu-id="c0720-103">Получает сведения о сетке событий или получает список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c0720-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="c0720-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0720-104">SYNTAX</span></span>

### <span data-ttu-id="c0720-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0720-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0720-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0720-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0720-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0720-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0720-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0720-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0720-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0720-109">DESCRIPTION</span></span>
<span data-ttu-id="c0720-110">Командлет Get-AzEventGridTopic получает либо сведения о заданной теме сетки событий, либо список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c0720-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="c0720-111">Если указано название раздела, возвращается информация об одной статье.</span><span class="sxs-lookup"><span data-stu-id="c0720-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="c0720-112">Если название темы не указано, возвращается список тем.</span><span class="sxs-lookup"><span data-stu-id="c0720-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="c0720-113">Количество элементов, возвращенных в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="c0720-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="c0720-114">Если значение Top не задано или $null, список будет содержать все элементы тем.</span><span class="sxs-lookup"><span data-stu-id="c0720-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="c0720-115">В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="c0720-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="c0720-116">Если по-прежнему доступны другие темы, значение в NextLink следует использовать при следующем звонке для перехода к следующей странице разделов.</span><span class="sxs-lookup"><span data-stu-id="c0720-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="c0720-117">Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="c0720-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="c0720-118">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="c0720-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="c0720-119">Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="c0720-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="c0720-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0720-120">EXAMPLES</span></span>

### <span data-ttu-id="c0720-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0720-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c0720-122">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c0720-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c0720-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0720-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="c0720-124">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c0720-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c0720-125">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c0720-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="c0720-126">Перечислите все разделы сетки событий в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="c0720-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="c0720-127">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c0720-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="c0720-128">Список первых 10 разделов сетки событий (если таковые имеются) в группе ресурсов \` MyResourceGroupName \` , удовлетворяющих запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c0720-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c0720-129">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="c0720-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c0720-130">Чтобы получить следующие страницы тем, ожидается повторный вызов Get-AzEventGridTopic и использование функции результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="c0720-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c0720-131">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="c0720-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c0720-132">Пример 5</span><span class="sxs-lookup"><span data-stu-id="c0720-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="c0720-133">Перечислите все разделы сетки событий в подписке без разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="c0720-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="c0720-134">Пример 6</span><span class="sxs-lookup"><span data-stu-id="c0720-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="c0720-135">Список первых 10 разделов сетки событий (если таковые имеются) в подписке, удовлетворяющей запросу $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c0720-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c0720-136">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="c0720-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c0720-137">Чтобы получить следующие страницы тем, ожидается повторный вызов Get-AzEventGridTopic и использование функции результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="c0720-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c0720-138">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="c0720-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="c0720-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0720-139">PARAMETERS</span></span>

### <span data-ttu-id="c0720-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0720-140">-DefaultProfile</span></span>
<span data-ttu-id="c0720-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0720-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0720-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0720-142">-Name</span></span>
<span data-ttu-id="c0720-143">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c0720-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0720-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="c0720-144">-NextLink</span></span>
<span data-ttu-id="c0720-145">Ссылка на следующую страницу ресурсов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="c0720-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="c0720-146">Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.</span><span class="sxs-lookup"><span data-stu-id="c0720-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="c0720-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c0720-147">-ODataQuery</span></span>
<span data-ttu-id="c0720-148">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="c0720-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="c0720-149">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="c0720-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0720-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0720-150">-ResourceGroupName</span></span>
<span data-ttu-id="c0720-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0720-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0720-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0720-152">-ResourceId</span></span>
<span data-ttu-id="c0720-153">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="c0720-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c0720-154">-Top</span><span class="sxs-lookup"><span data-stu-id="c0720-154">-Top</span></span>
<span data-ttu-id="c0720-155">Максимальное количество получаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0720-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="c0720-156">Допустимые значения: от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="c0720-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="c0720-157">Если указано значение Top и другие результаты по-прежнему доступны, результат будет содержать ссылку на следующую страницу для запроса в NextLink.</span><span class="sxs-lookup"><span data-stu-id="c0720-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="c0720-158">Если значение Top не задано, будет возвращен весь список ресурсов за один раз.</span><span class="sxs-lookup"><span data-stu-id="c0720-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0720-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0720-159">CommonParameters</span></span>
<span data-ttu-id="c0720-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0720-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0720-161">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0720-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0720-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0720-162">INPUTS</span></span>

### <span data-ttu-id="c0720-163">System. String</span><span class="sxs-lookup"><span data-stu-id="c0720-163">System.String</span></span>

### <span data-ttu-id="c0720-164">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0720-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c0720-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0720-165">OUTPUTS</span></span>

### <span data-ttu-id="c0720-166">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c0720-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c0720-167">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="c0720-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="c0720-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0720-168">NOTES</span></span>

## <span data-ttu-id="c0720-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0720-169">RELATED LINKS</span></span>