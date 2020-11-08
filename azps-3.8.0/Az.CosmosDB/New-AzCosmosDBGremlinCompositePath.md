---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065382"
---
# <span data-ttu-id="21cf2-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="21cf2-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="21cf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="21cf2-103">Создает новый объект типа PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="21cf2-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="21cf2-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="21cf2-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="21cf2-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21cf2-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21cf2-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21cf2-106">DESCRIPTION</span></span>
<span data-ttu-id="21cf2-107">Объект, соответствующий CompositePath API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="21cf2-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="21cf2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="21cf2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21cf2-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="21cf2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="21cf2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21cf2-111">-DefaultProfile</span></span>
<span data-ttu-id="21cf2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21cf2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21cf2-113">-Порядок</span><span class="sxs-lookup"><span data-stu-id="21cf2-113">-Order</span></span>
<span data-ttu-id="21cf2-114">Возвращает или задает порядок сортировки для составных путей.</span><span class="sxs-lookup"><span data-stu-id="21cf2-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="21cf2-115">Возможные значения: "по возрастанию", "по убыванию"</span><span class="sxs-lookup"><span data-stu-id="21cf2-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="21cf2-116">-Path</span><span class="sxs-lookup"><span data-stu-id="21cf2-116">-Path</span></span>
<span data-ttu-id="21cf2-117">Путь, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="21cf2-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="21cf2-118">Пути индексов обычно начинаются с корневого элемента и заканчиваются подстановочными знаками (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="21cf2-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="21cf2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21cf2-119">CommonParameters</span></span>
<span data-ttu-id="21cf2-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21cf2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21cf2-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21cf2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21cf2-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21cf2-122">INPUTS</span></span>

### <span data-ttu-id="21cf2-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="21cf2-123">None</span></span>

## <span data-ttu-id="21cf2-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21cf2-124">OUTPUTS</span></span>

### <span data-ttu-id="21cf2-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="21cf2-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="21cf2-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="21cf2-126">NOTES</span></span>

## <span data-ttu-id="21cf2-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21cf2-127">RELATED LINKS</span></span>
