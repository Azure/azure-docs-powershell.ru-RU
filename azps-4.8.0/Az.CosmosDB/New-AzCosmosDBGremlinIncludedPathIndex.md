---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079740"
---
# <span data-ttu-id="af0d8-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="af0d8-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="af0d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="af0d8-103">Создает новый объект типа PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="af0d8-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="af0d8-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="af0d8-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="af0d8-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af0d8-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af0d8-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af0d8-106">DESCRIPTION</span></span>
<span data-ttu-id="af0d8-107">Объект, соответствующий индексам IncludedPath's API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="af0d8-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="af0d8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af0d8-108">EXAMPLES</span></span>

### <span data-ttu-id="af0d8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af0d8-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="af0d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af0d8-110">PARAMETERS</span></span>

### <span data-ttu-id="af0d8-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="af0d8-111">-DataType</span></span>
<span data-ttu-id="af0d8-112">Тип данных, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="af0d8-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="af0d8-113">Возможные значения: "строка", "число", "точечный", "Многоугольник", "LineString", "Многоугольный"</span><span class="sxs-lookup"><span data-stu-id="af0d8-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="af0d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0d8-114">-DefaultProfile</span></span>
<span data-ttu-id="af0d8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af0d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af0d8-116">-Видах</span><span class="sxs-lookup"><span data-stu-id="af0d8-116">-Kind</span></span>
<span data-ttu-id="af0d8-117">Указывает тип индекса.</span><span class="sxs-lookup"><span data-stu-id="af0d8-117">Indicates the type of index.</span></span>
<span data-ttu-id="af0d8-118">Возможные значения: "хэш", "диапазон", "пространственный"</span><span class="sxs-lookup"><span data-stu-id="af0d8-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="af0d8-119">-Точность</span><span class="sxs-lookup"><span data-stu-id="af0d8-119">-Precision</span></span>
<span data-ttu-id="af0d8-120">Точность индекса.</span><span class="sxs-lookup"><span data-stu-id="af0d8-120">The precision of the index.</span></span>
<span data-ttu-id="af0d8-121">-1 — максимальная точность.</span><span class="sxs-lookup"><span data-stu-id="af0d8-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="af0d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0d8-122">CommonParameters</span></span>
<span data-ttu-id="af0d8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af0d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0d8-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af0d8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0d8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af0d8-125">INPUTS</span></span>

### <span data-ttu-id="af0d8-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="af0d8-126">None</span></span>

## <span data-ttu-id="af0d8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af0d8-127">OUTPUTS</span></span>

### <span data-ttu-id="af0d8-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="af0d8-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="af0d8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="af0d8-129">NOTES</span></span>

## <span data-ttu-id="af0d8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af0d8-130">RELATED LINKS</span></span>
