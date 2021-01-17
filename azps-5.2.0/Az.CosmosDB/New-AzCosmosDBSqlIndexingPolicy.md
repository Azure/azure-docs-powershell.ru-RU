---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401095"
---
# <span data-ttu-id="56c45-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="56c45-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="56c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c45-102">SYNOPSIS</span></span>
<span data-ttu-id="56c45-103">Создание объекта Sql IndexingPolicy в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="56c45-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="56c45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56c45-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c45-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56c45-105">DESCRIPTION</span></span>
<span data-ttu-id="56c45-106">Для создания нового объекта типа **PSSqlIndexingPolicy** будет создаваться новый объект PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="56c45-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="56c45-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56c45-107">EXAMPLES</span></span>

### <span data-ttu-id="56c45-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56c45-108">Example 1</span></span>
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

## <span data-ttu-id="56c45-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56c45-109">PARAMETERS</span></span>

### <span data-ttu-id="56c45-110">-Automatic</span><span class="sxs-lookup"><span data-stu-id="56c45-110">-Automatic</span></span>
<span data-ttu-id="56c45-111">Bool to indicate if the indexing policy is automatic</span><span class="sxs-lookup"><span data-stu-id="56c45-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="56c45-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="56c45-112">-CompositePath</span></span>
<span data-ttu-id="56c45-113">Массив объектов типа Microsoft.Azure.Commands.ВацыDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="56c45-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="56c45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c45-114">-DefaultProfile</span></span>
<span data-ttu-id="56c45-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56c45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c45-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="56c45-116">-ExcludedPath</span></span>
<span data-ttu-id="56c45-117">Массив строк, содержащих excludedPath(указывает путь в документе JSON, который следует исключить в службе Azure Azure DB.)  .</span><span class="sxs-lookup"><span data-stu-id="56c45-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="56c45-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="56c45-118">-IncludedPath</span></span>
<span data-ttu-id="56c45-119">Массив строк, содержащих includedPath (указывает путь в документе JSON, который будет включен в службу Azure Azure Azure DB).)</span><span class="sxs-lookup"><span data-stu-id="56c45-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="56c45-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="56c45-120">-IndexingMode</span></span>
<span data-ttu-id="56c45-121">указывает на режим индексации.</span><span class="sxs-lookup"><span data-stu-id="56c45-121">indicates the indexing mode.</span></span>
<span data-ttu-id="56c45-122">Возможные значения: "Последователь", "Высвея" и "Нет".</span><span class="sxs-lookup"><span data-stu-id="56c45-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="56c45-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="56c45-123">-SpatialSpec</span></span>
<span data-ttu-id="56c45-124">Массив объектов типа Microsoft.Azure.Commands.ВацDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="56c45-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="56c45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c45-125">CommonParameters</span></span>
<span data-ttu-id="56c45-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c45-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56c45-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c45-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56c45-128">INPUTS</span></span>

### <span data-ttu-id="56c45-129">Нет</span><span class="sxs-lookup"><span data-stu-id="56c45-129">None</span></span>

## <span data-ttu-id="56c45-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56c45-130">OUTPUTS</span></span>

### <span data-ttu-id="56c45-131">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="56c45-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="56c45-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56c45-132">NOTES</span></span>

## <span data-ttu-id="56c45-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56c45-133">RELATED LINKS</span></span>
