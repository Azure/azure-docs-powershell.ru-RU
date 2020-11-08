---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079742"
---
# <span data-ttu-id="14e12-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="14e12-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="14e12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14e12-102">SYNOPSIS</span></span>
<span data-ttu-id="14e12-103">Создает новый объект типа PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="14e12-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="14e12-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="14e12-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="14e12-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14e12-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e12-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14e12-106">DESCRIPTION</span></span>
<span data-ttu-id="14e12-107">Объект, соответствующий IncludedPath API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="14e12-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="14e12-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14e12-108">EXAMPLES</span></span>

### <span data-ttu-id="14e12-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14e12-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="14e12-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14e12-110">PARAMETERS</span></span>

### <span data-ttu-id="14e12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e12-111">-DefaultProfile</span></span>
<span data-ttu-id="14e12-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14e12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e12-113">-Index</span><span class="sxs-lookup"><span data-stu-id="14e12-113">-Index</span></span>
<span data-ttu-id="14e12-114">Список индексов для этого пути</span><span class="sxs-lookup"><span data-stu-id="14e12-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e12-115">-Path</span><span class="sxs-lookup"><span data-stu-id="14e12-115">-Path</span></span>
<span data-ttu-id="14e12-116">Путь, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="14e12-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="14e12-117">Пути индексов обычно начинаются с корневого элемента и заканчиваются подстановочными знаками (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="14e12-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="14e12-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e12-118">CommonParameters</span></span>
<span data-ttu-id="14e12-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14e12-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e12-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14e12-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e12-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14e12-121">INPUTS</span></span>

### <span data-ttu-id="14e12-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="14e12-122">None</span></span>

## <span data-ttu-id="14e12-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14e12-123">OUTPUTS</span></span>

### <span data-ttu-id="14e12-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="14e12-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="14e12-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="14e12-125">NOTES</span></span>

## <span data-ttu-id="14e12-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14e12-126">RELATED LINKS</span></span>