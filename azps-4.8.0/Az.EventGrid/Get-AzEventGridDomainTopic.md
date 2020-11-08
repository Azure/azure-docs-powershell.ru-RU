---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243603"
---
# <span data-ttu-id="ab160-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ab160-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ab160-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab160-102">SYNOPSIS</span></span>
<span data-ttu-id="ab160-103">Получает подробные сведения о домене событий, а также список всех разделов с доменами, в которых указана область сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ab160-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="ab160-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab160-104">SYNTAX</span></span>

### <span data-ttu-id="ab160-105">DomainTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab160-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab160-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab160-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab160-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab160-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab160-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab160-108">DESCRIPTION</span></span>
<span data-ttu-id="ab160-109">Командлет Get-AzEventGridDomainTopic получает либо сведения о заданной теме сетки событий, либо список всех разделов, посвященных сетке событий, в рамках определенного домена в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ab160-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="ab160-110">Если указано доменное имя домена, возвращается информация об одном из данных, указанных в области сетки событий.</span><span class="sxs-lookup"><span data-stu-id="ab160-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="ab160-111">Если имя раздела домена не указано, возвращается список разделов домена под указанным именем домена.</span><span class="sxs-lookup"><span data-stu-id="ab160-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="ab160-112">Количество элементов, возвращенных в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="ab160-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ab160-113">Если значение Top не задано или $null, список будет содержать все элементы в разделе "подразделы домена".</span><span class="sxs-lookup"><span data-stu-id="ab160-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="ab160-114">В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="ab160-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ab160-115">Если по-прежнему доступны другие разделы домена, значение в NextLink следует использовать при следующем звонке, чтобы получить следующую страницу разделов домена.</span><span class="sxs-lookup"><span data-stu-id="ab160-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="ab160-116">Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="ab160-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ab160-117">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="ab160-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ab160-118">Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ab160-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ab160-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab160-119">EXAMPLES</span></span>

### <span data-ttu-id="ab160-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab160-120">Example 1</span></span>

<span data-ttu-id="ab160-121">Получает подробные сведения о домене событий DomainTopic1 в \` разделе \` Domain1 домена на сетку событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ab160-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ab160-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ab160-122">Example 2</span></span>

<span data-ttu-id="ab160-123">Получает подробные сведения о домене событий DomainTopic1 в \` разделе \` Domain1 домена на сетку событий \` \` в группе ресурсов \` MyResourceGroupName \` с помощью параметра ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ab160-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ab160-124">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ab160-124">Example 3</span></span>

<span data-ttu-id="ab160-125">Список всех разделов, посвященных сетке событий, в разделе Сетка событий \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы (все результаты возвращаются в одном снимке).</span><span class="sxs-lookup"><span data-stu-id="ab160-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="ab160-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ab160-126">Example 4</span></span>

<span data-ttu-id="ab160-127">Список всех разделов, посвященных сетке событий, в разделе Сетка событий \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы (все результаты возвращаются одним снимком) с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab160-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="ab160-128">Пример 5</span><span class="sxs-lookup"><span data-stu-id="ab160-128">Example 5</span></span>

<span data-ttu-id="ab160-129">Перечислите доменные темы сетки событий (если таковые имеются) в разделе Domain \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` , которые удовлетворяют $odataFilter для домена запросов 10.</span><span class="sxs-lookup"><span data-stu-id="ab160-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="ab160-130">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="ab160-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ab160-131">Чтобы получить следующие страницы разделов домена, пользователь должен повторно вызвать Get-AzEventGridDomainTopic и использовать результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="ab160-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ab160-132">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="ab160-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="ab160-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab160-133">PARAMETERS</span></span>

### <span data-ttu-id="ab160-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab160-134">-DefaultProfile</span></span>
<span data-ttu-id="ab160-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab160-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab160-136">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="ab160-136">-DomainName</span></span>
<span data-ttu-id="ab160-137">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="ab160-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ab160-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab160-138">-Name</span></span>
<span data-ttu-id="ab160-139">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ab160-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ab160-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ab160-140">-NextLink</span></span>
<span data-ttu-id="ab160-141">Ссылка на следующую страницу ресурсов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="ab160-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ab160-142">Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.</span><span class="sxs-lookup"><span data-stu-id="ab160-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ab160-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ab160-143">-ODataQuery</span></span>
<span data-ttu-id="ab160-144">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="ab160-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ab160-145">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ab160-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ab160-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab160-146">-ResourceGroupName</span></span>
<span data-ttu-id="ab160-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab160-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab160-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab160-148">-ResourceId</span></span>
<span data-ttu-id="ab160-149">Идентификатор ресурса, представляющий собой доменную область сетки событий или доменную область сетки.</span><span class="sxs-lookup"><span data-stu-id="ab160-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="ab160-150">-Top</span><span class="sxs-lookup"><span data-stu-id="ab160-150">-Top</span></span>
<span data-ttu-id="ab160-151">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="ab160-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ab160-152">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="ab160-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ab160-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab160-153">CommonParameters</span></span>
<span data-ttu-id="ab160-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab160-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab160-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab160-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab160-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab160-156">INPUTS</span></span>

### <span data-ttu-id="ab160-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ab160-157">System.String</span></span>

### <span data-ttu-id="ab160-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ab160-158">System.Int32</span></span>

## <span data-ttu-id="ab160-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab160-159">OUTPUTS</span></span>

### <span data-ttu-id="ab160-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ab160-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ab160-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="ab160-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="ab160-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab160-162">NOTES</span></span>

## <span data-ttu-id="ab160-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab160-163">RELATED LINKS</span></span>
