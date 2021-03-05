---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000104"
---
# <span data-ttu-id="cc627-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="cc627-101">Search-AzGraph</span></span>

## <span data-ttu-id="cc627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc627-102">SYNOPSIS</span></span>
<span data-ttu-id="cc627-103">Запрос ресурсов, управляемых Диспетчером ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cc627-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="cc627-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc627-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc627-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc627-105">DESCRIPTION</span></span>
<span data-ttu-id="cc627-106">Подробнее о синтаксисе запроса можно узнать здесь: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="cc627-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="cc627-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc627-107">EXAMPLES</span></span>

### <span data-ttu-id="cc627-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc627-108">Example 1</span></span>
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

<span data-ttu-id="cc627-109">Простой запрос ресурсов, запрашивающий подмножество полей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc627-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="cc627-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc627-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="cc627-111">Сложный запрос к ресурсам с выделением полей, фильтрацией и обобщением данных.</span><span class="sxs-lookup"><span data-stu-id="cc627-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="cc627-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cc627-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="cc627-113">Запрос со всеми виртуальными компьютерами, которые не используют управляемые диски и содержит отображаемые имена подписок.</span><span class="sxs-lookup"><span data-stu-id="cc627-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="cc627-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="cc627-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="cc627-115">Запрос, отображающий количество ресурсов по именам клиента и подписки.</span><span class="sxs-lookup"><span data-stu-id="cc627-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="cc627-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc627-116">PARAMETERS</span></span>

### <span data-ttu-id="cc627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc627-117">-DefaultProfile</span></span>
<span data-ttu-id="cc627-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc627-119">-Query</span><span class="sxs-lookup"><span data-stu-id="cc627-119">-Query</span></span>
<span data-ttu-id="cc627-120">Запрос "График ресурсов".</span><span class="sxs-lookup"><span data-stu-id="cc627-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="cc627-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="cc627-121">-Subscription</span></span>
<span data-ttu-id="cc627-122">Подписки для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="cc627-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="cc627-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="cc627-123">-Skip</span></span>
<span data-ttu-id="cc627-124">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="cc627-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cc627-125">-First</span><span class="sxs-lookup"><span data-stu-id="cc627-125">-First</span></span>
<span data-ttu-id="cc627-126">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="cc627-126">The maximum number of objects to return.</span></span> <span data-ttu-id="cc627-127">Разрешенные значения: 1–5000.</span><span class="sxs-lookup"><span data-stu-id="cc627-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="cc627-128">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="cc627-128">Default value is 100.</span></span>

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

### <span data-ttu-id="cc627-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc627-129">CommonParameters</span></span>
<span data-ttu-id="cc627-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc627-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc627-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc627-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc627-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc627-132">INPUTS</span></span>

### <span data-ttu-id="cc627-133">Нет</span><span class="sxs-lookup"><span data-stu-id="cc627-133">None</span></span>

## <span data-ttu-id="cc627-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc627-134">OUTPUTS</span></span>

### <span data-ttu-id="cc627-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="cc627-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cc627-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc627-136">NOTES</span></span>

## <span data-ttu-id="cc627-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc627-137">RELATED LINKS</span></span>
