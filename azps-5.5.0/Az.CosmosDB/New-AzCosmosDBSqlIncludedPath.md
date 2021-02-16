---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243917"
---
# <span data-ttu-id="5e948-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="5e948-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="5e948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e948-102">SYNOPSIS</span></span>
<span data-ttu-id="5e948-103">Создание объекта типа PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="5e948-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="5e948-104">Его можно передать в качестве значения параметра для Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="5e948-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="5e948-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e948-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e948-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e948-106">DESCRIPTION</span></span>
<span data-ttu-id="5e948-107">Объект, соответствующий Sql API IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="5e948-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="5e948-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e948-108">EXAMPLES</span></span>

### <span data-ttu-id="5e948-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e948-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="5e948-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e948-110">PARAMETERS</span></span>

### <span data-ttu-id="5e948-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e948-111">-DefaultProfile</span></span>
<span data-ttu-id="5e948-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e948-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e948-113">-Index</span><span class="sxs-lookup"><span data-stu-id="5e948-113">-Index</span></span>
<span data-ttu-id="5e948-114">Список индексов для этого пути</span><span class="sxs-lookup"><span data-stu-id="5e948-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="5e948-115">-Path</span><span class="sxs-lookup"><span data-stu-id="5e948-115">-Path</span></span>
<span data-ttu-id="5e948-116">Путь, к которому относится индексация.</span><span class="sxs-lookup"><span data-stu-id="5e948-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="5e948-117">Путь индекса обычно начинается с корневого и заканчивается поддиками (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="5e948-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="5e948-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e948-118">CommonParameters</span></span>
<span data-ttu-id="5e948-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e948-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e948-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e948-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e948-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e948-121">INPUTS</span></span>

### <span data-ttu-id="5e948-122">Нет</span><span class="sxs-lookup"><span data-stu-id="5e948-122">None</span></span>

## <span data-ttu-id="5e948-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e948-123">OUTPUTS</span></span>

### <span data-ttu-id="5e948-124">Microsoft.Azure.Commands.ВацDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="5e948-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="5e948-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e948-125">NOTES</span></span>

## <span data-ttu-id="5e948-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e948-126">RELATED LINKS</span></span>
