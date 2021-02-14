---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228497"
---
# <span data-ttu-id="09061-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="09061-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="09061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09061-102">SYNOPSIS</span></span>
<span data-ttu-id="09061-103">Возвращает сведения о теме сетки событий или список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="09061-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="09061-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="09061-104">SYNTAX</span></span>

### <span data-ttu-id="09061-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09061-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09061-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09061-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09061-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="09061-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09061-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="09061-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09061-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09061-109">DESCRIPTION</span></span>
<span data-ttu-id="09061-110">Этот Get-AzEventGridTopic возвращает сведения о указанном разделе сетки событий или список всех тем сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="09061-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="09061-111">Если за предоставлено название темы, возвращаются сведения об отдельной теме сетки событий.</span><span class="sxs-lookup"><span data-stu-id="09061-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="09061-112">Если название темы не заданной, возвращается список разделов.</span><span class="sxs-lookup"><span data-stu-id="09061-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="09061-113">Количество элементов, возвращаемых в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="09061-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="09061-114">Если значение не указано или $null, в списке будут указаны все элементы.</span><span class="sxs-lookup"><span data-stu-id="09061-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="09061-115">В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.</span><span class="sxs-lookup"><span data-stu-id="09061-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="09061-116">Если по-прежнему доступны другие темы, значение в NextLink нужно использовать в следующем звонке для получения следующей страницы тем.</span><span class="sxs-lookup"><span data-stu-id="09061-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="09061-117">Наконец, параметр ODataQuery используется для фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="09061-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="09061-118">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="09061-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="09061-119">Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="09061-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="09061-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="09061-120">EXAMPLES</span></span>

### <span data-ttu-id="09061-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09061-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="09061-122">Возвращает сведения о теме "Сетка событий" "Тема1" в группе ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="09061-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09061-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09061-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="09061-124">Возвращает сведения о теме "Сетка событий" "Тема1" в группе ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="09061-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09061-125">Пример 3</span><span class="sxs-lookup"><span data-stu-id="09061-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="09061-126">Перечислите все разделы сетки событий в группе ресурсов \` MyResourceGroupName \` без разрежения.</span><span class="sxs-lookup"><span data-stu-id="09061-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="09061-127">Пример 4</span><span class="sxs-lookup"><span data-stu-id="09061-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="09061-128">Перечислите первые 10 разделов сетки событий (если таковые есть) в группе ресурсов \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу.</span><span class="sxs-lookup"><span data-stu-id="09061-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="09061-129">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="09061-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="09061-130">Чтобы получить следующие страницы тем, пользователь должен переназвать Get-AzEventGridTopic использовать результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="09061-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="09061-131">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="09061-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="09061-132">Пример 5</span><span class="sxs-lookup"><span data-stu-id="09061-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="09061-133">Со списком всех разделов сетки событий в подписке без разгибов.</span><span class="sxs-lookup"><span data-stu-id="09061-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="09061-134">Пример 6</span><span class="sxs-lookup"><span data-stu-id="09061-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="09061-135">Со списком первых 10 разделов сетки событий (если они есть) в подписке, которая удовлетворяет $odataFilter запросу.</span><span class="sxs-lookup"><span data-stu-id="09061-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="09061-136">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="09061-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="09061-137">Чтобы получить следующие страницы тем, пользователь должен переназвать Get-AzEventGridTopic использовать результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="09061-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="09061-138">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="09061-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="09061-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09061-139">PARAMETERS</span></span>

### <span data-ttu-id="09061-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09061-140">-DefaultProfile</span></span>
<span data-ttu-id="09061-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="09061-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09061-142">-Name</span><span class="sxs-lookup"><span data-stu-id="09061-142">-Name</span></span>
<span data-ttu-id="09061-143">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="09061-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="09061-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="09061-144">-NextLink</span></span>
<span data-ttu-id="09061-145">Ссылка на следующую страницу ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="09061-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="09061-146">Это значение получается при первом Get-AzEventGrid, когда для запроса остается доступно больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09061-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="09061-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="09061-147">-ODataQuery</span></span>
<span data-ttu-id="09061-148">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="09061-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="09061-149">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="09061-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="09061-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09061-150">-ResourceGroupName</span></span>
<span data-ttu-id="09061-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09061-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="09061-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09061-152">-ResourceId</span></span>
<span data-ttu-id="09061-153">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="09061-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="09061-154">-Top</span><span class="sxs-lookup"><span data-stu-id="09061-154">-Top</span></span>
<span data-ttu-id="09061-155">Максимальное количество ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="09061-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="09061-156">Допустимым является значение от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="09061-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="09061-157">Если указано верхнее значение и другие результаты по-прежнему доступны, результат будет содержать ссылку на следующую страницу, которая будет запрашиваться в NextLink.</span><span class="sxs-lookup"><span data-stu-id="09061-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="09061-158">Если значение не указано, возвращается полный список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09061-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="09061-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09061-159">CommonParameters</span></span>
<span data-ttu-id="09061-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09061-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09061-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09061-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09061-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09061-162">INPUTS</span></span>

### <span data-ttu-id="09061-163">System.String</span><span class="sxs-lookup"><span data-stu-id="09061-163">System.String</span></span>

### <span data-ttu-id="09061-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09061-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09061-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09061-165">OUTPUTS</span></span>

### <span data-ttu-id="09061-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="09061-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="09061-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="09061-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="09061-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="09061-168">NOTES</span></span>

## <span data-ttu-id="09061-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09061-169">RELATED LINKS</span></span>
