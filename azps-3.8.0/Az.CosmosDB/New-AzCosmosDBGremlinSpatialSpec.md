---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073648"
---
# <span data-ttu-id="1805e-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1805e-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="1805e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1805e-102">SYNOPSIS</span></span>
<span data-ttu-id="1805e-103">Создает новый объект типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="1805e-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="1805e-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1805e-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="1805e-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1805e-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1805e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1805e-106">DESCRIPTION</span></span>
<span data-ttu-id="1805e-107">Создает объект, соответствующий SpatialSpec API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1805e-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="1805e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1805e-108">EXAMPLES</span></span>

### <span data-ttu-id="1805e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1805e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="1805e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1805e-110">PARAMETERS</span></span>

### <span data-ttu-id="1805e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1805e-111">-DefaultProfile</span></span>
<span data-ttu-id="1805e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1805e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1805e-113">-Path</span><span class="sxs-lookup"><span data-stu-id="1805e-113">-Path</span></span>
<span data-ttu-id="1805e-114">Путь в документе JSON для индексирования.</span><span class="sxs-lookup"><span data-stu-id="1805e-114">Path in JSON document to index.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1805e-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="1805e-115">-Type</span></span>
<span data-ttu-id="1805e-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, многоугольный.</span><span class="sxs-lookup"><span data-stu-id="1805e-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="1805e-117">Пространственный тип путей представления.</span><span class="sxs-lookup"><span data-stu-id="1805e-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1805e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1805e-118">CommonParameters</span></span>
<span data-ttu-id="1805e-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1805e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1805e-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1805e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1805e-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1805e-121">INPUTS</span></span>

### <span data-ttu-id="1805e-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="1805e-122">None</span></span>

## <span data-ttu-id="1805e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1805e-123">OUTPUTS</span></span>

### <span data-ttu-id="1805e-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1805e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="1805e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1805e-125">NOTES</span></span>

## <span data-ttu-id="1805e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1805e-126">RELATED LINKS</span></span>
