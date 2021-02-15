---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215377"
---
# <span data-ttu-id="f1f1b-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="f1f1b-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="f1f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f1b-103">Создание объекта типа PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="f1f1b-104">Его можно передать в качестве значения параметра для Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="f1f1b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1f1b-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f1b-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1f1b-106">DESCRIPTION</span></span>
<span data-ttu-id="f1f1b-107">Объект, соответствующий Sql API CompositePath.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="f1f1b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1f1b-108">EXAMPLES</span></span>

### <span data-ttu-id="f1f1b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1f1b-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="f1f1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1f1b-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f1b-111">-DefaultProfile</span></span>
<span data-ttu-id="f1f1b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f1b-113">-Порядок</span><span class="sxs-lookup"><span data-stu-id="f1f1b-113">-Order</span></span>
<span data-ttu-id="f1f1b-114">Возвращает или задает порядок сортировки для составных путей.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="f1f1b-115">Возможные значения: "по возрастанию", "по убытию"</span><span class="sxs-lookup"><span data-stu-id="f1f1b-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="f1f1b-116">-Path</span><span class="sxs-lookup"><span data-stu-id="f1f1b-116">-Path</span></span>
<span data-ttu-id="f1f1b-117">Путь, к которому относится индексация.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="f1f1b-118">Путь индекса обычно начинается с корневого и заканчивается поддиками (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="f1f1b-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="f1f1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f1b-119">CommonParameters</span></span>
<span data-ttu-id="f1f1b-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f1b-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1f1b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f1b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1f1b-122">INPUTS</span></span>

### <span data-ttu-id="f1f1b-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f1f1b-123">None</span></span>

## <span data-ttu-id="f1f1b-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1f1b-124">OUTPUTS</span></span>

### <span data-ttu-id="f1f1b-125">Microsoft.Azure.Commands.АsDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="f1f1b-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="f1f1b-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1f1b-126">NOTES</span></span>

## <span data-ttu-id="f1f1b-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1f1b-127">RELATED LINKS</span></span>
