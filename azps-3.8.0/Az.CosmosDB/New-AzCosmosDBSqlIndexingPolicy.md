---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073630"
---
# <span data-ttu-id="41e9c-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="41e9c-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="41e9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="41e9c-103">Создает новый объект CosmosDB SQL IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="41e9c-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="41e9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41e9c-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41e9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="41e9c-106">Командлет **New-AzCosmosDBSqlIndexingPolicy** создает новый объект типа PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="41e9c-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="41e9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="41e9c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41e9c-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="41e9c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41e9c-109">PARAMETERS</span></span>

### <span data-ttu-id="41e9c-110">-Автоматический</span><span class="sxs-lookup"><span data-stu-id="41e9c-110">-Automatic</span></span>
<span data-ttu-id="41e9c-111">Логическое значение, определяющее, является ли политика индексации автоматическим</span><span class="sxs-lookup"><span data-stu-id="41e9c-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="41e9c-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="41e9c-112">-CompositePath</span></span>
<span data-ttu-id="41e9c-113">Массив массив объектов типа Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="41e9c-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="41e9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e9c-114">-DefaultProfile</span></span>
<span data-ttu-id="41e9c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41e9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e9c-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="41e9c-116">-ExcludedPath</span></span>
<span data-ttu-id="41e9c-117">Массив строк, содержащий excludedPath (указывает путь в документе JSON, который нужно исключить в службе Jet Cosmos DB.)  element.</span><span class="sxs-lookup"><span data-stu-id="41e9c-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="41e9c-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="41e9c-118">-IncludedPath</span></span>
<span data-ttu-id="41e9c-119">Массив строк, содержащих includedPath (указывает путь в документе JSON для включения в элементы службы Azure Cosmos DB.).</span><span class="sxs-lookup"><span data-stu-id="41e9c-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="41e9c-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="41e9c-120">-IndexingMode</span></span>
<span data-ttu-id="41e9c-121">Указывает режим индексирования.</span><span class="sxs-lookup"><span data-stu-id="41e9c-121">indicates the indexing mode.</span></span>
<span data-ttu-id="41e9c-122">Возможные значения: "неоднородный", "ленивый", "нет"</span><span class="sxs-lookup"><span data-stu-id="41e9c-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="41e9c-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="41e9c-123">-SpatialSpec</span></span>
<span data-ttu-id="41e9c-124">Массив объектов типа Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="41e9c-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="41e9c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e9c-125">CommonParameters</span></span>
<span data-ttu-id="41e9c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41e9c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e9c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41e9c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e9c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41e9c-128">INPUTS</span></span>

### <span data-ttu-id="41e9c-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="41e9c-129">None</span></span>

## <span data-ttu-id="41e9c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41e9c-130">OUTPUTS</span></span>

### <span data-ttu-id="41e9c-131">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="41e9c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="41e9c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="41e9c-132">NOTES</span></span>

## <span data-ttu-id="41e9c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41e9c-133">RELATED LINKS</span></span>
