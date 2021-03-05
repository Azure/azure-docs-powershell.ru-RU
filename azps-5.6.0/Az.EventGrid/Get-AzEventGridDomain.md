---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 919d8d0557fd6bb57cc826da8ac18bc71b911c62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984682"
---
# <span data-ttu-id="108a7-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="108a7-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="108a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108a7-102">SYNOPSIS</span></span>
<span data-ttu-id="108a7-103">Возвращает сведения о домене "Сетка событий" или список всех доменов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="108a7-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="108a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="108a7-104">SYNTAX</span></span>

### <span data-ttu-id="108a7-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="108a7-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="108a7-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="108a7-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="108a7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="108a7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="108a7-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="108a7-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108a7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="108a7-109">DESCRIPTION</span></span>
<span data-ttu-id="108a7-110">Этот Get-AzEventGridDomain возвращает сведения о указанном домене сетки событий или список всех доменов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="108a7-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="108a7-111">Если за предоставлено доменное имя, возвращаются сведения об одном домене Event Grid.</span><span class="sxs-lookup"><span data-stu-id="108a7-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="108a7-112">Если имя домена не предоставлено, возвращается список доменов.</span><span class="sxs-lookup"><span data-stu-id="108a7-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="108a7-113">Количество элементов, возвращаемых в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="108a7-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="108a7-114">Если значение "Верхнее" не указано или $null, список будет содержать все элементы доменов, возвращаемые одновременно.</span><span class="sxs-lookup"><span data-stu-id="108a7-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="108a7-115">В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.</span><span class="sxs-lookup"><span data-stu-id="108a7-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="108a7-116">Если по-прежнему доступны другие домены, значение NextLink следует использовать во время следующего вызова, чтобы получить следующую страницу доменов.</span><span class="sxs-lookup"><span data-stu-id="108a7-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="108a7-117">Наконец, для фильтрации результатов поиска используется параметр ODataQuery.</span><span class="sxs-lookup"><span data-stu-id="108a7-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="108a7-118">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="108a7-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="108a7-119">Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="108a7-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="108a7-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="108a7-120">EXAMPLES</span></span>

### <span data-ttu-id="108a7-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="108a7-121">Example 1</span></span>

<span data-ttu-id="108a7-122">Сведения о домене Event Grid \` Domain1 \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="108a7-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="108a7-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="108a7-123">Example 2</span></span>

<span data-ttu-id="108a7-124">Получает сведения о домене Event Grid \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` с помощью параметра ResourceId.</span><span class="sxs-lookup"><span data-stu-id="108a7-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="108a7-125">Пример 3</span><span class="sxs-lookup"><span data-stu-id="108a7-125">Example 3</span></span>

<span data-ttu-id="108a7-126">Перечислите все домены сетки событий в группе ресурсов MyResourceGroupName без разбиения на нее (все домены возвращаются \` \` одним кадром)</span><span class="sxs-lookup"><span data-stu-id="108a7-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="108a7-127">Пример 4</span><span class="sxs-lookup"><span data-stu-id="108a7-127">Example 4</span></span>

<span data-ttu-id="108a7-128">Перечислите домены сетки событий (если таковые есть) в группе ресурсов \` MyResourceGroupName, которая удовлетворяет запросу $odataFilter 10 доменов \` одновременно.</span><span class="sxs-lookup"><span data-stu-id="108a7-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="108a7-129">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="108a7-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="108a7-130">Чтобы получить доступ к следующим страницам доменов, пользователь должен повторно позвонить в Get-AzEventGridDomain и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="108a7-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="108a7-131">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="108a7-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="108a7-132">Пример 5</span><span class="sxs-lookup"><span data-stu-id="108a7-132">Example 5</span></span>

<span data-ttu-id="108a7-133">Перечислить все домены сетки событий в подписке Azure без разбиения на разбиение на нее (все домены возвращаются одним кадром)</span><span class="sxs-lookup"><span data-stu-id="108a7-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="108a7-134">Пример 6</span><span class="sxs-lookup"><span data-stu-id="108a7-134">Example 6</span></span>

<span data-ttu-id="108a7-135">Укаймь домены сетки событий (если есть) в подписке Azure, $odataFilter запроса 20 доменов одновременно.</span><span class="sxs-lookup"><span data-stu-id="108a7-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="108a7-136">Если доступно больше результатов, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="108a7-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="108a7-137">Чтобы получить доступ к следующим страницам доменов, пользователь должен повторно позвонить в Get-AzEventGridDomain и использует результат. NextLink, полученные в предыдущем звонке.</span><span class="sxs-lookup"><span data-stu-id="108a7-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="108a7-138">Звонок должен остановиться в результатах. NextLink становится $null.</span><span class="sxs-lookup"><span data-stu-id="108a7-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="108a7-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108a7-139">PARAMETERS</span></span>

### <span data-ttu-id="108a7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108a7-140">-DefaultProfile</span></span>
<span data-ttu-id="108a7-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="108a7-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="108a7-142">-Name</span><span class="sxs-lookup"><span data-stu-id="108a7-142">-Name</span></span>
<span data-ttu-id="108a7-143">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="108a7-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108a7-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="108a7-144">-NextLink</span></span>
<span data-ttu-id="108a7-145">Ссылка на следующую страницу ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="108a7-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="108a7-146">Это значение получают при первом Get-AzEventGrid, когда для запроса по-прежнему доступно больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="108a7-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="108a7-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="108a7-147">-ODataQuery</span></span>
<span data-ttu-id="108a7-148">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="108a7-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="108a7-149">Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.</span><span class="sxs-lookup"><span data-stu-id="108a7-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108a7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="108a7-150">-ResourceGroupName</span></span>
<span data-ttu-id="108a7-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="108a7-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108a7-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="108a7-152">-ResourceId</span></span>
<span data-ttu-id="108a7-153">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="108a7-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="108a7-154">-Top</span><span class="sxs-lookup"><span data-stu-id="108a7-154">-Top</span></span>
<span data-ttu-id="108a7-155">Максимальное количество ресурсов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="108a7-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="108a7-156">Допустимым является значение от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="108a7-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="108a7-157">Если указано верхнее значение и другие результаты по-прежнему доступны, результат будет содержать ссылку на следующую страницу, которая будет запрашиваться в NextLink.</span><span class="sxs-lookup"><span data-stu-id="108a7-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="108a7-158">Если значение не указано, возвращается полный список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="108a7-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108a7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108a7-159">CommonParameters</span></span>
<span data-ttu-id="108a7-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108a7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108a7-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="108a7-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108a7-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="108a7-162">INPUTS</span></span>

### <span data-ttu-id="108a7-163">System.String</span><span class="sxs-lookup"><span data-stu-id="108a7-163">System.String</span></span>

## <span data-ttu-id="108a7-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="108a7-164">OUTPUTS</span></span>

### <span data-ttu-id="108a7-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="108a7-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="108a7-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="108a7-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="108a7-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="108a7-167">NOTES</span></span>

## <span data-ttu-id="108a7-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="108a7-168">RELATED LINKS</span></span>
