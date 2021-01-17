---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403775"
---
# <span data-ttu-id="f28ea-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="f28ea-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="f28ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f28ea-103">Создание объекта типа PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="f28ea-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="f28ea-104">Его можно передать в качестве значения параметра set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="f28ea-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="f28ea-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f28ea-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f28ea-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28ea-106">DESCRIPTION</span></span>
<span data-ttu-id="f28ea-107">Объект, соответствующий API Гремлина IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="f28ea-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="f28ea-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f28ea-108">EXAMPLES</span></span>

### <span data-ttu-id="f28ea-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f28ea-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="f28ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f28ea-110">PARAMETERS</span></span>

### <span data-ttu-id="f28ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28ea-111">-DefaultProfile</span></span>
<span data-ttu-id="f28ea-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f28ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28ea-113">-Index</span><span class="sxs-lookup"><span data-stu-id="f28ea-113">-Index</span></span>
<span data-ttu-id="f28ea-114">Список индексов для этого пути</span><span class="sxs-lookup"><span data-stu-id="f28ea-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="f28ea-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f28ea-115">-Path</span></span>
<span data-ttu-id="f28ea-116">Путь, к которому относится индексация.</span><span class="sxs-lookup"><span data-stu-id="f28ea-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="f28ea-117">Путь индекса обычно начинается с корневого и заканчивается поддиками (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="f28ea-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="f28ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28ea-118">CommonParameters</span></span>
<span data-ttu-id="f28ea-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28ea-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f28ea-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28ea-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f28ea-121">INPUTS</span></span>

### <span data-ttu-id="f28ea-122">Нет</span><span class="sxs-lookup"><span data-stu-id="f28ea-122">None</span></span>

## <span data-ttu-id="f28ea-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f28ea-123">OUTPUTS</span></span>

### <span data-ttu-id="f28ea-124">Microsoft.Azure.Commands.ВацDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="f28ea-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="f28ea-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f28ea-125">NOTES</span></span>

## <span data-ttu-id="f28ea-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f28ea-126">RELATED LINKS</span></span>
