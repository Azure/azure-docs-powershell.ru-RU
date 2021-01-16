---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508829"
---
# <span data-ttu-id="58635-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="58635-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="58635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58635-102">SYNOPSIS</span></span>
<span data-ttu-id="58635-103">Создание объекта типа PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="58635-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="58635-104">Его можно передать в качестве значения параметра set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="58635-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="58635-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58635-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58635-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58635-106">DESCRIPTION</span></span>
<span data-ttu-id="58635-107">Объект, соответствующий API Гремлина CompositePath.</span><span class="sxs-lookup"><span data-stu-id="58635-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="58635-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58635-108">EXAMPLES</span></span>

### <span data-ttu-id="58635-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58635-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="58635-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58635-110">PARAMETERS</span></span>

### <span data-ttu-id="58635-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58635-111">-DefaultProfile</span></span>
<span data-ttu-id="58635-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58635-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58635-113">-Порядок</span><span class="sxs-lookup"><span data-stu-id="58635-113">-Order</span></span>
<span data-ttu-id="58635-114">Возвращает или задает порядок сортировки для составных путей.</span><span class="sxs-lookup"><span data-stu-id="58635-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="58635-115">Возможные значения: "по возрастанию", "по убытию"</span><span class="sxs-lookup"><span data-stu-id="58635-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="58635-116">-Path</span><span class="sxs-lookup"><span data-stu-id="58635-116">-Path</span></span>
<span data-ttu-id="58635-117">Путь, к которому относится индексация.</span><span class="sxs-lookup"><span data-stu-id="58635-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="58635-118">Путь индекса обычно начинается с корневого и заканчивается поддиками (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="58635-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="58635-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58635-119">CommonParameters</span></span>
<span data-ttu-id="58635-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58635-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58635-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58635-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58635-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58635-122">INPUTS</span></span>

### <span data-ttu-id="58635-123">Нет</span><span class="sxs-lookup"><span data-stu-id="58635-123">None</span></span>

## <span data-ttu-id="58635-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58635-124">OUTPUTS</span></span>

### <span data-ttu-id="58635-125">Microsoft.Azure.Commands.АsDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="58635-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="58635-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58635-126">NOTES</span></span>

## <span data-ttu-id="58635-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58635-127">RELATED LINKS</span></span>
