---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210417"
---
# <span data-ttu-id="f3716-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="f3716-101">Search-AzGraph</span></span>

## <span data-ttu-id="f3716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3716-102">SYNOPSIS</span></span>
<span data-ttu-id="f3716-103">Запросы ресурсов, управляемых Диспетчером ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f3716-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="f3716-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3716-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3716-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3716-105">DESCRIPTION</span></span>
<span data-ttu-id="f3716-106">Подробнее о синтаксисе запроса можно узнать здесь: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="f3716-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="f3716-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3716-107">EXAMPLES</span></span>

### <span data-ttu-id="f3716-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3716-108">Example 1</span></span>
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

<span data-ttu-id="f3716-109">Простой запрос ресурсов, запрашивающий подмножество полей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3716-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="f3716-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f3716-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="f3716-111">Сложный запрос к ресурсам с выделением полей, фильтрацией и обобщением данных.</span><span class="sxs-lookup"><span data-stu-id="f3716-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="f3716-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f3716-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="f3716-113">Запрос со всеми виртуальными машинами, которые не используют управляемые диски и содержат отображаемые имена подписок.</span><span class="sxs-lookup"><span data-stu-id="f3716-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="f3716-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f3716-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="f3716-115">Запрос, отображающий количество ресурсов по именам клиента и подписки.</span><span class="sxs-lookup"><span data-stu-id="f3716-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="f3716-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3716-116">PARAMETERS</span></span>

### <span data-ttu-id="f3716-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3716-117">-DefaultProfile</span></span>
<span data-ttu-id="f3716-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3716-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3716-119">-Query</span><span class="sxs-lookup"><span data-stu-id="f3716-119">-Query</span></span>
<span data-ttu-id="f3716-120">Запрос "График ресурсов".</span><span class="sxs-lookup"><span data-stu-id="f3716-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="f3716-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="f3716-121">-Subscription</span></span>
<span data-ttu-id="f3716-122">Подписки для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="f3716-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="f3716-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3716-123">-Skip</span></span>
<span data-ttu-id="f3716-124">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="f3716-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f3716-125">-First</span><span class="sxs-lookup"><span data-stu-id="f3716-125">-First</span></span>
<span data-ttu-id="f3716-126">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="f3716-126">The maximum number of objects to return.</span></span> <span data-ttu-id="f3716-127">Разрешенные значения: 1–5000.</span><span class="sxs-lookup"><span data-stu-id="f3716-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="f3716-128">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="f3716-128">Default value is 100.</span></span>

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

### <span data-ttu-id="f3716-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3716-129">CommonParameters</span></span>
<span data-ttu-id="f3716-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3716-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3716-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3716-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3716-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3716-132">INPUTS</span></span>

### <span data-ttu-id="f3716-133">Нет</span><span class="sxs-lookup"><span data-stu-id="f3716-133">None</span></span>

## <span data-ttu-id="f3716-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3716-134">OUTPUTS</span></span>

### <span data-ttu-id="f3716-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f3716-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f3716-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3716-136">NOTES</span></span>

## <span data-ttu-id="f3716-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3716-137">RELATED LINKS</span></span>
