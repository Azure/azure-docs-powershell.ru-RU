---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402303"
---
# <span data-ttu-id="6d89d-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6d89d-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="6d89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d89d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d89d-103">Возвращает сведения о теме домена "Сетка событий" или список всех тем домена "Сетка событий" в определенном домене "Сетка событий" в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="6d89d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d89d-104">SYNTAX</span></span>

### <span data-ttu-id="6d89d-105">DomainTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d89d-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d89d-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d89d-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d89d-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d89d-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d89d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d89d-108">DESCRIPTION</span></span>
<span data-ttu-id="6d89d-109">Этот Get-AzEventGridDomainTopic получает сведения об определенном разделе домена сетки событий или список всех тем домена "Сетка событий" в определенном домене в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="6d89d-110">Если за предоставлено имя темы домена, возвращаются сведения об отдельной теме сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6d89d-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="6d89d-111">Если имя темы домена не указано, возвращается список тем домена под указанным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="6d89d-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="6d89d-112">Количество элементов, возвращаемых в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="6d89d-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="6d89d-113">Если значение "Верхнее" не указано или $null, список будет содержать все элементы, связанные с доменами.</span><span class="sxs-lookup"><span data-stu-id="6d89d-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="6d89d-114">В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.</span><span class="sxs-lookup"><span data-stu-id="6d89d-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="6d89d-115">Если другие темы домена по-прежнему доступны, значение в NextLink нужно использовать в следующем звонке, чтобы получить следующую страницу тем домена.</span><span class="sxs-lookup"><span data-stu-id="6d89d-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="6d89d-116">Наконец, для фильтрации результатов поиска используется параметр ODataQuery.</span><span class="sxs-lookup"><span data-stu-id="6d89d-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="6d89d-117">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="6d89d-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="6d89d-118">Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="6d89d-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="6d89d-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d89d-119">EXAMPLES</span></span>

### <span data-ttu-id="6d89d-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d89d-120">Example 1</span></span>

<span data-ttu-id="6d89d-121">Gets the details of Event Grid domain topic \` DomainTopic1 \` under Event Grid domain \` Domain1 in resource group \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6d89d-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6d89d-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6d89d-122">Example 2</span></span>

<span data-ttu-id="6d89d-123">Получает сведения о теме domain DomainTopic1 сетки событий в домене Event Grid Domain1 в группе ресурсов \` \` \` \` \` MyResourceGroupName с помощью \` параметра ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6d89d-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6d89d-124">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6d89d-124">Example 3</span></span>

<span data-ttu-id="6d89d-125">Перечислите все темы домена "Сетка мероприятий" в домене Event Grid Domain1 в группе ресурсов \` \` \` MyResourceGroupName без разбиения на разделы (все результаты возвращаются \` одним кадром).</span><span class="sxs-lookup"><span data-stu-id="6d89d-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6d89d-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6d89d-126">Example 4</span></span>

<span data-ttu-id="6d89d-127">Перечислите все темы домена "Сетка событий" в домене Event Grid Domain1 в группе ресурсов \` \` \` MyResourceGroupName без разбиения на разделы (все результаты возвращаются в одном кадре) с помощью параметра \` ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d89d-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6d89d-128">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6d89d-128">Example 5</span></span>

<span data-ttu-id="6d89d-129">Уделяйте группе ресурсов MyResourceGroupName темы домена "Сетка событий" (если таковые есть) в группе \` \` ресурсов \` MyResourceGroupName, которая удовлетворяет $odataFilter запросов по 10 темам доменов \` одновременно.</span><span class="sxs-lookup"><span data-stu-id="6d89d-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="6d89d-130">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="6d89d-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6d89d-131">Чтобы получить доступ к следующим страницам тем о доменах, пользователь должен будет повторно позвонить в Get-AzEventGridDomainTopic и будет использовать результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="6d89d-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6d89d-132">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="6d89d-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="6d89d-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d89d-133">PARAMETERS</span></span>

### <span data-ttu-id="6d89d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d89d-134">-DefaultProfile</span></span>
<span data-ttu-id="6d89d-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d89d-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="6d89d-136">-DomainName</span></span>
<span data-ttu-id="6d89d-137">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6d89d-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="6d89d-138">-Name</span></span>
<span data-ttu-id="6d89d-139">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6d89d-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="6d89d-140">-NextLink</span></span>
<span data-ttu-id="6d89d-141">Ссылка на следующую страницу ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="6d89d-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="6d89d-142">Это значение получают при первом Get-AzEventGrid, когда для запроса по-прежнему доступно больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d89d-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="6d89d-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6d89d-143">-ODataQuery</span></span>
<span data-ttu-id="6d89d-144">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="6d89d-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6d89d-145">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="6d89d-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d89d-146">-ResourceGroupName</span></span>
<span data-ttu-id="6d89d-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d89d-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d89d-148">-ResourceId</span></span>
<span data-ttu-id="6d89d-149">Идентификатор ресурса, представляющий домен или раздел домена сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6d89d-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-150">-Top</span><span class="sxs-lookup"><span data-stu-id="6d89d-150">-Top</span></span>
<span data-ttu-id="6d89d-151">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="6d89d-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6d89d-152">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="6d89d-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d89d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d89d-153">CommonParameters</span></span>
<span data-ttu-id="6d89d-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d89d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d89d-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d89d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d89d-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d89d-156">INPUTS</span></span>

### <span data-ttu-id="6d89d-157">System.String</span><span class="sxs-lookup"><span data-stu-id="6d89d-157">System.String</span></span>

### <span data-ttu-id="6d89d-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6d89d-158">System.Int32</span></span>

## <span data-ttu-id="6d89d-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d89d-159">OUTPUTS</span></span>

### <span data-ttu-id="6d89d-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6d89d-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="6d89d-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="6d89d-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="6d89d-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d89d-162">NOTES</span></span>

## <span data-ttu-id="6d89d-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d89d-163">RELATED LINKS</span></span>
