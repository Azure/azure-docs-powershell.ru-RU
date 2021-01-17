---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403759"
---
# <span data-ttu-id="a2219-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a2219-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="a2219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2219-102">SYNOPSIS</span></span>
<span data-ttu-id="a2219-103">Создание объекта типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="a2219-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="a2219-104">Его можно передать в качестве значения параметра set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a2219-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="a2219-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2219-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2219-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2219-106">DESCRIPTION</span></span>
<span data-ttu-id="a2219-107">Создает объект, соответствующий пространственным данным API Гремлина.</span><span class="sxs-lookup"><span data-stu-id="a2219-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="a2219-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2219-108">EXAMPLES</span></span>

### <span data-ttu-id="a2219-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2219-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="a2219-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2219-110">PARAMETERS</span></span>

### <span data-ttu-id="a2219-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2219-111">-DefaultProfile</span></span>
<span data-ttu-id="a2219-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2219-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2219-113">-Path</span><span class="sxs-lookup"><span data-stu-id="a2219-113">-Path</span></span>
<span data-ttu-id="a2219-114">Путь в документе JSON для индексации.</span><span class="sxs-lookup"><span data-stu-id="a2219-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="a2219-115">-Type</span><span class="sxs-lookup"><span data-stu-id="a2219-115">-Type</span></span>
<span data-ttu-id="a2219-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="a2219-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="a2219-117">Представляет пространственный тип путей.</span><span class="sxs-lookup"><span data-stu-id="a2219-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="a2219-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2219-118">CommonParameters</span></span>
<span data-ttu-id="a2219-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2219-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2219-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2219-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2219-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2219-121">INPUTS</span></span>

### <span data-ttu-id="a2219-122">Нет</span><span class="sxs-lookup"><span data-stu-id="a2219-122">None</span></span>

## <span data-ttu-id="a2219-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2219-123">OUTPUTS</span></span>

### <span data-ttu-id="a2219-124">Microsoft.Azure.Commands.АsDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a2219-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="a2219-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2219-125">NOTES</span></span>

## <span data-ttu-id="a2219-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2219-126">RELATED LINKS</span></span>
