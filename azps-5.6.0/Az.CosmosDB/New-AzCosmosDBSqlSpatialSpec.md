---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: e22c8931cf70fba970e71b7a2d099cda725287d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004323"
---
# <span data-ttu-id="54ca7-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="54ca7-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="54ca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="54ca7-103">Создание объекта типа PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="54ca7-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="54ca7-104">Его можно передать в качестве значения параметра set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="54ca7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="54ca7-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54ca7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54ca7-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54ca7-106">DESCRIPTION</span></span>
<span data-ttu-id="54ca7-107">Создает объект, соответствующий Sql API Из ПространственныхSpec.</span><span class="sxs-lookup"><span data-stu-id="54ca7-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="54ca7-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54ca7-108">EXAMPLES</span></span>

### <span data-ttu-id="54ca7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54ca7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="54ca7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="54ca7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ca7-111">-DefaultProfile</span></span>
<span data-ttu-id="54ca7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54ca7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ca7-113">-Path</span><span class="sxs-lookup"><span data-stu-id="54ca7-113">-Path</span></span>
<span data-ttu-id="54ca7-114">Путь в документе JSON для индексации.</span><span class="sxs-lookup"><span data-stu-id="54ca7-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="54ca7-115">-Type</span><span class="sxs-lookup"><span data-stu-id="54ca7-115">-Type</span></span>
<span data-ttu-id="54ca7-116">Массив строк с допустимыми значениями: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="54ca7-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="54ca7-117">Представляет пространственный тип путей.</span><span class="sxs-lookup"><span data-stu-id="54ca7-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="54ca7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ca7-118">CommonParameters</span></span>
<span data-ttu-id="54ca7-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ca7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ca7-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54ca7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ca7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54ca7-121">INPUTS</span></span>

### <span data-ttu-id="54ca7-122">Нет</span><span class="sxs-lookup"><span data-stu-id="54ca7-122">None</span></span>

## <span data-ttu-id="54ca7-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54ca7-123">OUTPUTS</span></span>

### <span data-ttu-id="54ca7-124">Microsoft.Azure.Commands.АsDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="54ca7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="54ca7-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54ca7-125">NOTES</span></span>

## <span data-ttu-id="54ca7-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54ca7-126">RELATED LINKS</span></span>
