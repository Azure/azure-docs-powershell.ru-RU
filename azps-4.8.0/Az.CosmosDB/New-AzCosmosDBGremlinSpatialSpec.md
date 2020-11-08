---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079736"
---
# <span data-ttu-id="f5249-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f5249-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="f5249-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5249-102">SYNOPSIS</span></span>
<span data-ttu-id="f5249-103">Создает новый объект типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="f5249-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="f5249-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f5249-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="f5249-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5249-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5249-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5249-106">DESCRIPTION</span></span>
<span data-ttu-id="f5249-107">Создает объект, соответствующий SpatialSpec API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f5249-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="f5249-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5249-108">EXAMPLES</span></span>

### <span data-ttu-id="f5249-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5249-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="f5249-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5249-110">PARAMETERS</span></span>

### <span data-ttu-id="f5249-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5249-111">-DefaultProfile</span></span>
<span data-ttu-id="f5249-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5249-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5249-113">-Path</span><span class="sxs-lookup"><span data-stu-id="f5249-113">-Path</span></span>
<span data-ttu-id="f5249-114">Путь в документе JSON для индексирования.</span><span class="sxs-lookup"><span data-stu-id="f5249-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="f5249-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f5249-115">-Type</span></span>
<span data-ttu-id="f5249-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, многоугольный.</span><span class="sxs-lookup"><span data-stu-id="f5249-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="f5249-117">Пространственный тип путей представления.</span><span class="sxs-lookup"><span data-stu-id="f5249-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="f5249-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5249-118">CommonParameters</span></span>
<span data-ttu-id="f5249-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5249-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5249-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5249-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5249-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5249-121">INPUTS</span></span>

### <span data-ttu-id="f5249-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5249-122">None</span></span>

## <span data-ttu-id="f5249-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5249-123">OUTPUTS</span></span>

### <span data-ttu-id="f5249-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f5249-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="f5249-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5249-125">NOTES</span></span>

## <span data-ttu-id="f5249-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5249-126">RELATED LINKS</span></span>
