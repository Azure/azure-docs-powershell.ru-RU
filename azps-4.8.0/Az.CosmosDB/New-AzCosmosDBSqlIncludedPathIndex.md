---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244625"
---
# <span data-ttu-id="e3ca6-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="e3ca6-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="e3ca6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ca6-103">Создает новый объект типа PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="e3ca6-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="e3ca6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3ca6-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ca6-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3ca6-106">DESCRIPTION</span></span>
<span data-ttu-id="e3ca6-107">Объект, соответствующий индексам IncludedPath's API SQL.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="e3ca6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3ca6-108">EXAMPLES</span></span>

### <span data-ttu-id="e3ca6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3ca6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="e3ca6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3ca6-110">PARAMETERS</span></span>

### <span data-ttu-id="e3ca6-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e3ca6-111">-DataType</span></span>
<span data-ttu-id="e3ca6-112">Тип данных, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="e3ca6-113">Возможные значения: "строка", "число", "точечный", "Многоугольник", "LineString", "Многоугольный"</span><span class="sxs-lookup"><span data-stu-id="e3ca6-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="e3ca6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ca6-114">-DefaultProfile</span></span>
<span data-ttu-id="e3ca6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ca6-116">-Видах</span><span class="sxs-lookup"><span data-stu-id="e3ca6-116">-Kind</span></span>
<span data-ttu-id="e3ca6-117">Указывает тип индекса.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-117">Indicates the type of index.</span></span>
<span data-ttu-id="e3ca6-118">Возможные значения: "хэш", "диапазон", "пространственный"</span><span class="sxs-lookup"><span data-stu-id="e3ca6-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="e3ca6-119">-Точность</span><span class="sxs-lookup"><span data-stu-id="e3ca6-119">-Precision</span></span>
<span data-ttu-id="e3ca6-120">Точность индекса.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-120">The precision of the index.</span></span>
<span data-ttu-id="e3ca6-121">-1 — максимальная точность.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="e3ca6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ca6-122">CommonParameters</span></span>
<span data-ttu-id="e3ca6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ca6-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3ca6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ca6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3ca6-125">INPUTS</span></span>

### <span data-ttu-id="e3ca6-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3ca6-126">None</span></span>

## <span data-ttu-id="e3ca6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3ca6-127">OUTPUTS</span></span>

### <span data-ttu-id="e3ca6-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="e3ca6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="e3ca6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3ca6-129">NOTES</span></span>

## <span data-ttu-id="e3ca6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3ca6-130">RELATED LINKS</span></span>
