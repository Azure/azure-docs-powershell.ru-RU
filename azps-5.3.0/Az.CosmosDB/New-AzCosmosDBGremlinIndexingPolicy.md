---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508818"
---
# <span data-ttu-id="e3242-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e3242-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="e3242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3242-102">SYNOPSIS</span></span>
<span data-ttu-id="e3242-103">Создает объект IndexsDB IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3242-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="e3242-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3242-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3242-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3242-105">DESCRIPTION</span></span>
<span data-ttu-id="e3242-106">Cmdlet **New-AzCosmosDBGremlinIndexingPolicy** создает объект типа PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3242-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="e3242-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3242-107">EXAMPLES</span></span>

### <span data-ttu-id="e3242-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3242-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="e3242-109">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="e3242-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e3242-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3242-110">PARAMETERS</span></span>

### <span data-ttu-id="e3242-111">-Automatic</span><span class="sxs-lookup"><span data-stu-id="e3242-111">-Automatic</span></span>
<span data-ttu-id="e3242-112">Bool to indicate if the indexing policy is automatic</span><span class="sxs-lookup"><span data-stu-id="e3242-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="e3242-113">-CompositePath</span></span>
<span data-ttu-id="e3242-114">Массив объектов типа Microsoft.Azure.Commands.ВацыDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="e3242-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3242-115">-DefaultProfile</span></span>
<span data-ttu-id="e3242-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3242-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="e3242-117">-ExcludedPath</span></span>
<span data-ttu-id="e3242-118">Массив строк, содержащих excludedPath(указывает путь в документе JSON, который следует исключить в службе Azure Azure DB.)  .</span><span class="sxs-lookup"><span data-stu-id="e3242-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="e3242-119">-IncludedPath</span></span>
<span data-ttu-id="e3242-120">Массив строк, содержащих includedPath (указывает путь в документе JSON, который будет включен в службу Azure Azure Azure DB).)</span><span class="sxs-lookup"><span data-stu-id="e3242-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="e3242-121">-IndexingMode</span></span>
<span data-ttu-id="e3242-122">Указывает на режим индексации.</span><span class="sxs-lookup"><span data-stu-id="e3242-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="e3242-123">Возможные значения: "Последователь", "Высвея" и "Нет".</span><span class="sxs-lookup"><span data-stu-id="e3242-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e3242-124">-SpatialSpec</span></span>
<span data-ttu-id="e3242-125">Массив объектов типа Microsoft.Azure.Commands.ВацDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e3242-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3242-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3242-126">CommonParameters</span></span>
<span data-ttu-id="e3242-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3242-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3242-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3242-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3242-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3242-129">INPUTS</span></span>

### <span data-ttu-id="e3242-130">Нет</span><span class="sxs-lookup"><span data-stu-id="e3242-130">None</span></span>

## <span data-ttu-id="e3242-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3242-131">OUTPUTS</span></span>

### <span data-ttu-id="e3242-132">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e3242-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="e3242-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3242-133">NOTES</span></span>

## <span data-ttu-id="e3242-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3242-134">RELATED LINKS</span></span>
