---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314831"
---
# <span data-ttu-id="39586-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="39586-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="39586-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39586-102">SYNOPSIS</span></span>
<span data-ttu-id="39586-103">Создает новый объект CosmosDB IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="39586-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="39586-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39586-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39586-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39586-105">DESCRIPTION</span></span>
<span data-ttu-id="39586-106">Командлет **New-AzCosmosDBGremlinIndexingPolicy** создает новый объект типа PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="39586-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="39586-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39586-107">EXAMPLES</span></span>

### <span data-ttu-id="39586-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39586-108">Example 1</span></span>
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

<span data-ttu-id="39586-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="39586-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="39586-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39586-110">PARAMETERS</span></span>

### <span data-ttu-id="39586-111">-Автоматический</span><span class="sxs-lookup"><span data-stu-id="39586-111">-Automatic</span></span>
<span data-ttu-id="39586-112">Логическое значение, определяющее, является ли политика индексации автоматическим</span><span class="sxs-lookup"><span data-stu-id="39586-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="39586-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="39586-113">-CompositePath</span></span>
<span data-ttu-id="39586-114">Массив массив объектов типа Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="39586-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="39586-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39586-115">-DefaultProfile</span></span>
<span data-ttu-id="39586-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39586-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39586-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="39586-117">-ExcludedPath</span></span>
<span data-ttu-id="39586-118">Массив строк, содержащий excludedPath (указывает путь в документе JSON, который нужно исключить в службе Jet Cosmos DB.)  element.</span><span class="sxs-lookup"><span data-stu-id="39586-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="39586-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="39586-119">-IncludedPath</span></span>
<span data-ttu-id="39586-120">Массив строк, содержащих includedPath (указывает путь в документе JSON для включения в элементы службы Azure Cosmos DB.).</span><span class="sxs-lookup"><span data-stu-id="39586-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="39586-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="39586-121">-IndexingMode</span></span>
<span data-ttu-id="39586-122">Указывает режим индексирования.</span><span class="sxs-lookup"><span data-stu-id="39586-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="39586-123">Возможные значения: "неоднородный", "ленивый", "нет"</span><span class="sxs-lookup"><span data-stu-id="39586-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="39586-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="39586-124">-SpatialSpec</span></span>
<span data-ttu-id="39586-125">Массив объектов типа Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="39586-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="39586-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39586-126">CommonParameters</span></span>
<span data-ttu-id="39586-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39586-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39586-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39586-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39586-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39586-129">INPUTS</span></span>

### <span data-ttu-id="39586-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="39586-130">None</span></span>

## <span data-ttu-id="39586-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39586-131">OUTPUTS</span></span>

### <span data-ttu-id="39586-132">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="39586-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="39586-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="39586-133">NOTES</span></span>

## <span data-ttu-id="39586-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39586-134">RELATED LINKS</span></span>