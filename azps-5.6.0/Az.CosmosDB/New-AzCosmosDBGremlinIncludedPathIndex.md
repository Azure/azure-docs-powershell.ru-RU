---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 6c84004ffb267a5bc429bb242d3bc7245775d69b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998822"
---
# <span data-ttu-id="2ee52-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="2ee52-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="2ee52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee52-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee52-103">Создает объект PSIndexes нового типа.</span><span class="sxs-lookup"><span data-stu-id="2ee52-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="2ee52-104">Его можно передать в качестве значения параметра для Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="2ee52-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="2ee52-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ee52-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee52-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ee52-106">DESCRIPTION</span></span>
<span data-ttu-id="2ee52-107">Объект, соответствующий индексам IncludedPath в API Гремлина.</span><span class="sxs-lookup"><span data-stu-id="2ee52-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="2ee52-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ee52-108">EXAMPLES</span></span>

### <span data-ttu-id="2ee52-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ee52-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="2ee52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ee52-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee52-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="2ee52-111">-DataType</span></span>
<span data-ttu-id="2ee52-112">Тип данных, к которому применяется индексация.</span><span class="sxs-lookup"><span data-stu-id="2ee52-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="2ee52-113">Возможные значения: String, 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="2ee52-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="2ee52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee52-114">-DefaultProfile</span></span>
<span data-ttu-id="2ee52-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee52-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="2ee52-116">-Kind</span></span>
<span data-ttu-id="2ee52-117">Указывает на тип индекса.</span><span class="sxs-lookup"><span data-stu-id="2ee52-117">Indicates the type of index.</span></span>
<span data-ttu-id="2ee52-118">Возможные значения: 'Hash', 'Range', 'Spatial'</span><span class="sxs-lookup"><span data-stu-id="2ee52-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="2ee52-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="2ee52-119">-Precision</span></span>
<span data-ttu-id="2ee52-120">Точность индекса.</span><span class="sxs-lookup"><span data-stu-id="2ee52-120">The precision of the index.</span></span>
<span data-ttu-id="2ee52-121">-1 — максимальная точность.</span><span class="sxs-lookup"><span data-stu-id="2ee52-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee52-122">CommonParameters</span></span>
<span data-ttu-id="2ee52-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee52-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee52-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ee52-125">INPUTS</span></span>

### <span data-ttu-id="2ee52-126">Нет</span><span class="sxs-lookup"><span data-stu-id="2ee52-126">None</span></span>

## <span data-ttu-id="2ee52-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ee52-127">OUTPUTS</span></span>

### <span data-ttu-id="2ee52-128">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="2ee52-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="2ee52-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ee52-129">NOTES</span></span>

## <span data-ttu-id="2ee52-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ee52-130">RELATED LINKS</span></span>
