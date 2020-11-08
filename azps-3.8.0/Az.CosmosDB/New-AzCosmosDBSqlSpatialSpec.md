---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073634"
---
# <span data-ttu-id="9dfbb-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9dfbb-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="9dfbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfbb-103">Создает новый объект типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="9dfbb-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="9dfbb-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dfbb-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dfbb-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfbb-106">DESCRIPTION</span></span>
<span data-ttu-id="9dfbb-107">Создает объект, соответствующий SpatialSpec API SQL.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="9dfbb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dfbb-108">EXAMPLES</span></span>

### <span data-ttu-id="9dfbb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dfbb-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="9dfbb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dfbb-110">PARAMETERS</span></span>

### <span data-ttu-id="9dfbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfbb-111">-DefaultProfile</span></span>
<span data-ttu-id="9dfbb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dfbb-113">-Path</span><span class="sxs-lookup"><span data-stu-id="9dfbb-113">-Path</span></span>
<span data-ttu-id="9dfbb-114">Путь в документе JSON для индексирования.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="9dfbb-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9dfbb-115">-Type</span></span>
<span data-ttu-id="9dfbb-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, многоугольный.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="9dfbb-117">Пространственный тип путей представления.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="9dfbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfbb-118">CommonParameters</span></span>
<span data-ttu-id="9dfbb-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dfbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfbb-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dfbb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfbb-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dfbb-121">INPUTS</span></span>

### <span data-ttu-id="9dfbb-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="9dfbb-122">None</span></span>

## <span data-ttu-id="9dfbb-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfbb-123">OUTPUTS</span></span>

### <span data-ttu-id="9dfbb-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9dfbb-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="9dfbb-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dfbb-125">NOTES</span></span>

## <span data-ttu-id="9dfbb-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dfbb-126">RELATED LINKS</span></span>
