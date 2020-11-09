---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248475"
---
# <span data-ttu-id="0fd5a-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="0fd5a-101">Search-AzGraph</span></span>

## <span data-ttu-id="0fd5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd5a-103">Запрашивает ресурсы, управляемые диспетчером ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="0fd5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fd5a-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fd5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fd5a-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd5a-106">Дополнительные сведения о синтаксисе запроса: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="0fd5a-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="0fd5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fd5a-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fd5a-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="0fd5a-109">Простой запрос Resources, запрашивающий подмножество полей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="0fd5a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0fd5a-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="0fd5a-111">Сложный запрос ресурсов с выбором полей, фильтрацией и обобщением.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="0fd5a-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0fd5a-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="0fd5a-113">Запрос, содержащий все виртуальные машины, на которых не используются управляемые диски и отображаются отображаемые имена подписок.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="0fd5a-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0fd5a-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="0fd5a-115">Запрос, отображающий количество ресурсов по отображаемым именам клиентов и подписок.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="0fd5a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fd5a-116">PARAMETERS</span></span>

### <span data-ttu-id="0fd5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd5a-117">-DefaultProfile</span></span>
<span data-ttu-id="0fd5a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd5a-119">-Query</span><span class="sxs-lookup"><span data-stu-id="0fd5a-119">-Query</span></span>
<span data-ttu-id="0fd5a-120">Запрос графика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-120">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5a-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="0fd5a-121">-Subscription</span></span>
<span data-ttu-id="0fd5a-122">Подписок для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-122">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5a-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="0fd5a-123">-Skip</span></span>
<span data-ttu-id="0fd5a-124">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-124">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5a-125">-First</span><span class="sxs-lookup"><span data-stu-id="0fd5a-125">-First</span></span>
<span data-ttu-id="0fd5a-126">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-126">The maximum number of objects to return.</span></span> <span data-ttu-id="0fd5a-127">Допустимые значения: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="0fd5a-128">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-128">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd5a-129">CommonParameters</span></span>
<span data-ttu-id="0fd5a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fd5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd5a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd5a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd5a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fd5a-132">INPUTS</span></span>

### <span data-ttu-id="0fd5a-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="0fd5a-133">None</span></span>

## <span data-ttu-id="0fd5a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fd5a-134">OUTPUTS</span></span>

### <span data-ttu-id="0fd5a-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0fd5a-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0fd5a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fd5a-136">NOTES</span></span>

## <span data-ttu-id="0fd5a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fd5a-137">RELATED LINKS</span></span>