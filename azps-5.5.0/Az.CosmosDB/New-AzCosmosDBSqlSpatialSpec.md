---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238516"
---
# <span data-ttu-id="32eab-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="32eab-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="32eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32eab-102">SYNOPSIS</span></span>
<span data-ttu-id="32eab-103">Создание объекта типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="32eab-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="32eab-104">Его можно передать в качестве значения параметра set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="32eab-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="32eab-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32eab-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32eab-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32eab-106">DESCRIPTION</span></span>
<span data-ttu-id="32eab-107">Создает объект, соответствующий Sql API Для пространственных данных.</span><span class="sxs-lookup"><span data-stu-id="32eab-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="32eab-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32eab-108">EXAMPLES</span></span>

### <span data-ttu-id="32eab-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32eab-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="32eab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32eab-110">PARAMETERS</span></span>

### <span data-ttu-id="32eab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eab-111">-DefaultProfile</span></span>
<span data-ttu-id="32eab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32eab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32eab-113">-Path</span><span class="sxs-lookup"><span data-stu-id="32eab-113">-Path</span></span>
<span data-ttu-id="32eab-114">Путь в документе JSON для индексации.</span><span class="sxs-lookup"><span data-stu-id="32eab-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="32eab-115">-Type</span><span class="sxs-lookup"><span data-stu-id="32eab-115">-Type</span></span>
<span data-ttu-id="32eab-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="32eab-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="32eab-117">Представляет пространственный тип путей.</span><span class="sxs-lookup"><span data-stu-id="32eab-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="32eab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eab-118">CommonParameters</span></span>
<span data-ttu-id="32eab-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32eab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eab-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32eab-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eab-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32eab-121">INPUTS</span></span>

### <span data-ttu-id="32eab-122">Нет</span><span class="sxs-lookup"><span data-stu-id="32eab-122">None</span></span>

## <span data-ttu-id="32eab-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32eab-123">OUTPUTS</span></span>

### <span data-ttu-id="32eab-124">Microsoft.Azure.Commands.АsDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="32eab-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="32eab-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32eab-125">NOTES</span></span>

## <span data-ttu-id="32eab-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32eab-126">RELATED LINKS</span></span>
