---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073644"
---
# <span data-ttu-id="74851-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="74851-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="74851-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74851-102">SYNOPSIS</span></span>
<span data-ttu-id="74851-103">Создает новый объект типа PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="74851-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="74851-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="74851-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="74851-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74851-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74851-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74851-106">DESCRIPTION</span></span>
<span data-ttu-id="74851-107">Объект, соответствующий CompositePath API SQL.</span><span class="sxs-lookup"><span data-stu-id="74851-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="74851-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74851-108">EXAMPLES</span></span>

### <span data-ttu-id="74851-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74851-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="74851-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74851-110">PARAMETERS</span></span>

### <span data-ttu-id="74851-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74851-111">-DefaultProfile</span></span>
<span data-ttu-id="74851-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74851-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74851-113">-Порядок</span><span class="sxs-lookup"><span data-stu-id="74851-113">-Order</span></span>
<span data-ttu-id="74851-114">Возвращает или задает порядок сортировки для составных путей.</span><span class="sxs-lookup"><span data-stu-id="74851-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="74851-115">Возможные значения: "по возрастанию", "по убыванию"</span><span class="sxs-lookup"><span data-stu-id="74851-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="74851-116">-Path</span><span class="sxs-lookup"><span data-stu-id="74851-116">-Path</span></span>
<span data-ttu-id="74851-117">Путь, к которому применяется поведение индексирования.</span><span class="sxs-lookup"><span data-stu-id="74851-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="74851-118">Пути индексов обычно начинаются с корневого элемента и заканчиваются подстановочными знаками (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="74851-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="74851-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74851-119">CommonParameters</span></span>
<span data-ttu-id="74851-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74851-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74851-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74851-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74851-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74851-122">INPUTS</span></span>

### <span data-ttu-id="74851-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="74851-123">None</span></span>

## <span data-ttu-id="74851-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74851-124">OUTPUTS</span></span>

### <span data-ttu-id="74851-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="74851-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="74851-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="74851-126">NOTES</span></span>

## <span data-ttu-id="74851-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74851-127">RELATED LINKS</span></span>
