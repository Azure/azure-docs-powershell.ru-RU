---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904121"
---
# <span data-ttu-id="5e2f9-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="5e2f9-101">Search-AzGraph</span></span>

## <span data-ttu-id="5e2f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2f9-103">Запрашивает ресурсы, управляемые диспетчером ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="5e2f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e2f9-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e2f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="5e2f9-106">Дополнительные сведения о синтаксисе запроса: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="5e2f9-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="5e2f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e2f9-107">EXAMPLES</span></span>

### <span data-ttu-id="5e2f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e2f9-108">Example 1</span></span>
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

<span data-ttu-id="5e2f9-109">Простой запрос Resources, запрашивающий подмножество полей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="5e2f9-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5e2f9-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="5e2f9-111">Сложный запрос ресурсов с выбором полей, фильтрацией и обобщением.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="5e2f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e2f9-112">PARAMETERS</span></span>

### <span data-ttu-id="5e2f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2f9-113">-DefaultProfile</span></span>
<span data-ttu-id="5e2f9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e2f9-115">-Query</span><span class="sxs-lookup"><span data-stu-id="5e2f9-115">-Query</span></span>
<span data-ttu-id="5e2f9-116">Запрос графика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-116">Resource Graph query.</span></span>

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

### <span data-ttu-id="5e2f9-117">-Подписка</span><span class="sxs-lookup"><span data-stu-id="5e2f9-117">-Subscription</span></span>
<span data-ttu-id="5e2f9-118">Подписок для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-118">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="5e2f9-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="5e2f9-119">-Skip</span></span>
<span data-ttu-id="5e2f9-120">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-120">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5e2f9-121">-First</span><span class="sxs-lookup"><span data-stu-id="5e2f9-121">-First</span></span>
<span data-ttu-id="5e2f9-122">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-122">The maximum number of objects to return.</span></span> <span data-ttu-id="5e2f9-123">Допустимые значения: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="5e2f9-124">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-124">Default value is 100.</span></span>

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

### <span data-ttu-id="5e2f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2f9-125">CommonParameters</span></span>
<span data-ttu-id="5e2f9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e2f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2f9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2f9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e2f9-128">INPUTS</span></span>

### <span data-ttu-id="5e2f9-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e2f9-129">None</span></span>

## <span data-ttu-id="5e2f9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e2f9-130">OUTPUTS</span></span>

### <span data-ttu-id="5e2f9-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5e2f9-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5e2f9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e2f9-132">NOTES</span></span>

## <span data-ttu-id="5e2f9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e2f9-133">RELATED LINKS</span></span>
