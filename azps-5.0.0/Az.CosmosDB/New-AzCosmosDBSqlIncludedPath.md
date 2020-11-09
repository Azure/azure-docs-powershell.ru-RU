---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314759"
---
# <span data-ttu-id="096f5-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="096f5-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="096f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="096f5-102">SYNOPSIS</span></span>
<span data-ttu-id="096f5-103">Создает новый объект типа PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="096f5-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="096f5-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="096f5-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="096f5-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="096f5-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096f5-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="096f5-106">DESCRIPTION</span></span>
<span data-ttu-id="096f5-107">Объект, соответствующий IncludedPath API SQL.</span><span class="sxs-lookup"><span data-stu-id="096f5-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="096f5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="096f5-108">EXAMPLES</span></span>

### <span data-ttu-id="096f5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="096f5-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="096f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="096f5-110">PARAMETERS</span></span>

### <span data-ttu-id="096f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096f5-111">-DefaultProfile</span></span>
<span data-ttu-id="096f5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="096f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="096f5-113">-Index</span><span class="sxs-lookup"><span data-stu-id="096f5-113">-Index</span></span>
<span data-ttu-id="096f5-114">Список индексов для этого пути</span><span class="sxs-lookup"><span data-stu-id="096f5-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="096f5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="096f5-115">-Path</span></span>
<span data-ttu-id="096f5-116">Путь, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="096f5-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="096f5-117">Пути индексов обычно начинаются с корневого элемента и заканчиваются подстановочными знаками (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="096f5-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="096f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096f5-118">CommonParameters</span></span>
<span data-ttu-id="096f5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="096f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096f5-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="096f5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096f5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="096f5-121">INPUTS</span></span>

### <span data-ttu-id="096f5-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="096f5-122">None</span></span>

## <span data-ttu-id="096f5-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="096f5-123">OUTPUTS</span></span>

### <span data-ttu-id="096f5-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="096f5-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="096f5-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="096f5-125">NOTES</span></span>

## <span data-ttu-id="096f5-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="096f5-126">RELATED LINKS</span></span>