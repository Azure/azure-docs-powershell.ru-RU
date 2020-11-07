---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: cde1a3274c8fe8372c8b45a729d33d9dce04e998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721013"
---
# <span data-ttu-id="9f2a4-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9f2a4-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="9f2a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2a4-103">Возвращает данные домена сетки событий или получает список всех доменов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="9f2a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f2a4-104">SYNTAX</span></span>

### <span data-ttu-id="9f2a4-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f2a4-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f2a4-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f2a4-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f2a4-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f2a4-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f2a4-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f2a4-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f2a4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2a4-109">DESCRIPTION</span></span>
<span data-ttu-id="9f2a4-110">Командлет Get-AzEventGridDomain получает либо сведения о заданном домене сетки событий, либо список всех доменов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="9f2a4-111">Если указано доменное имя, возвращается информация об одном домене с сеткой событий.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="9f2a4-112">Если имя домена не указано, возвращается список доменов.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="9f2a4-113">Количество элементов, возвращенных в этом списке, управляется параметром Top.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="9f2a4-114">Если значение Top не указано или $null, список будет содержать все возвращенные элементы домена.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="9f2a4-115">В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="9f2a4-116">Если другие домены по-прежнему доступны, значение в NextLink следует использовать при следующем звонке для получения следующей страницы доменов.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="9f2a4-117">Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="9f2a4-118">Запрос фильтрации следует за синтаксисом OData, используя только свойство Name.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="9f2a4-119">Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="9f2a4-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f2a4-120">EXAMPLES</span></span>

### <span data-ttu-id="9f2a4-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f2a4-121">Example 1</span></span>

<span data-ttu-id="9f2a4-122">Получает сведения о Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9f2a4-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="9f2a4-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f2a4-123">Example 2</span></span>

<span data-ttu-id="9f2a4-124">Получает сведения о Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` с использованием параметра ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="9f2a4-125">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9f2a4-125">Example 3</span></span>

<span data-ttu-id="9f2a4-126">Список всех доменов сетки событий в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы (все домены возвращаются в одном снимке)</span><span class="sxs-lookup"><span data-stu-id="9f2a4-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="9f2a4-127">Пример 4</span><span class="sxs-lookup"><span data-stu-id="9f2a4-127">Example 4</span></span>

<span data-ttu-id="9f2a4-128">Перечислите домены с таблицами событий (если таковые имеются) в группе ресурсов \` MyResourceGroupName \` , которые удовлетворяют домены $odataFilter запросов 10 за один раз.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="9f2a4-129">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="9f2a4-130">Чтобы получить следующие страницы доменов, пользователь должен повторно вызвать Get-AzEventGridDomain и использовать результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="9f2a4-131">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="9f2a4-132">Пример 5</span><span class="sxs-lookup"><span data-stu-id="9f2a4-132">Example 5</span></span>

<span data-ttu-id="9f2a4-133">Список всех доменов сетки событий в подписке Azure без разбивки на страницы (все домены возвращаются в одном снимке)</span><span class="sxs-lookup"><span data-stu-id="9f2a4-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="9f2a4-134">Пример 6</span><span class="sxs-lookup"><span data-stu-id="9f2a4-134">Example 6</span></span>

<span data-ttu-id="9f2a4-135">Перечислите домены для событий (если таковые имеются) в подписке Azure, которые удовлетворяют домену $odataFilter запросов 20 за один раз.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="9f2a4-136">Если доступны дополнительные результаты, $result. NextLink не будет $null.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="9f2a4-137">Чтобы получить следующие страницы доменов, пользователь должен повторно вызвать Get-AzEventGridDomain и использовать результат. NextLink, полученный в результате предыдущего звонка.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="9f2a4-138">Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="9f2a4-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f2a4-139">PARAMETERS</span></span>

### <span data-ttu-id="9f2a4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2a4-140">-DefaultProfile</span></span>
<span data-ttu-id="9f2a4-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f2a4-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f2a4-142">-Name</span></span>
<span data-ttu-id="9f2a4-143">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="9f2a4-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2a4-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="9f2a4-144">-NextLink</span></span>
<span data-ttu-id="9f2a4-145">Ссылка на следующую страницу ресурсов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="9f2a4-146">Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2a4-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9f2a4-147">-ODataQuery</span></span>
<span data-ttu-id="9f2a4-148">Запрос OData, используемый для фильтрации результатов списка.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="9f2a4-149">В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2a4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2a4-150">-ResourceGroupName</span></span>
<span data-ttu-id="9f2a4-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2a4-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2a4-152">-ResourceId</span></span>
<span data-ttu-id="9f2a4-153">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="9f2a4-154">-Top</span><span class="sxs-lookup"><span data-stu-id="9f2a4-154">-Top</span></span>
<span data-ttu-id="9f2a4-155">Максимальное количество получаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="9f2a4-156">Допустимые значения: от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="9f2a4-157">Если указано значение Top и другие результаты по-прежнему доступны, результат будет содержать ссылку на следующую страницу для запроса в NextLink.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="9f2a4-158">Если значение Top не задано, будет возвращен весь список ресурсов за один раз.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2a4-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2a4-159">CommonParameters</span></span>
<span data-ttu-id="9f2a4-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f2a4-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2a4-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2a4-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2a4-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f2a4-162">INPUTS</span></span>

### <span data-ttu-id="9f2a4-163">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2a4-163">System.String</span></span>

## <span data-ttu-id="9f2a4-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2a4-164">OUTPUTS</span></span>

### <span data-ttu-id="9f2a4-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="9f2a4-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="9f2a4-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="9f2a4-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="9f2a4-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f2a4-167">NOTES</span></span>

## <span data-ttu-id="9f2a4-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f2a4-168">RELATED LINKS</span></span>
