---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073641"
---
# <span data-ttu-id="e0cd6-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="e0cd6-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="e0cd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cd6-103">Создает новый объект типа PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="e0cd6-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="e0cd6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0cd6-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0cd6-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0cd6-106">DESCRIPTION</span></span>
<span data-ttu-id="e0cd6-107">Объект, соответствующий IncludedPath API SQL.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="e0cd6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0cd6-108">EXAMPLES</span></span>

### <span data-ttu-id="e0cd6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0cd6-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="e0cd6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0cd6-110">PARAMETERS</span></span>

### <span data-ttu-id="e0cd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cd6-111">-DefaultProfile</span></span>
<span data-ttu-id="e0cd6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0cd6-113">-Index</span><span class="sxs-lookup"><span data-stu-id="e0cd6-113">-Index</span></span>
<span data-ttu-id="e0cd6-114">Список индексов для этого пути</span><span class="sxs-lookup"><span data-stu-id="e0cd6-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="e0cd6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e0cd6-115">-Path</span></span>
<span data-ttu-id="e0cd6-116">Путь, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="e0cd6-117">Пути индексов обычно начинаются с корневого элемента и заканчиваются подстановочными знаками (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="e0cd6-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="e0cd6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cd6-118">CommonParameters</span></span>
<span data-ttu-id="e0cd6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0cd6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cd6-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0cd6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cd6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0cd6-121">INPUTS</span></span>

### <span data-ttu-id="e0cd6-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0cd6-122">None</span></span>

## <span data-ttu-id="e0cd6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0cd6-123">OUTPUTS</span></span>

### <span data-ttu-id="e0cd6-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="e0cd6-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="e0cd6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0cd6-125">NOTES</span></span>

## <span data-ttu-id="e0cd6-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0cd6-126">RELATED LINKS</span></span>
