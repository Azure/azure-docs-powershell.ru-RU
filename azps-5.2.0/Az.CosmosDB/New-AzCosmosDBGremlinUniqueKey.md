---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403751"
---
# <span data-ttu-id="e338e-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e338e-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="e338e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e338e-102">SYNOPSIS</span></span>
<span data-ttu-id="e338e-103">Создание нового объекта UniqueKeyPolicy вНося в Результате ДВ.</span><span class="sxs-lookup"><span data-stu-id="e338e-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e338e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e338e-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e338e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e338e-105">DESCRIPTION</span></span>
<span data-ttu-id="e338e-106">Для создания объекта psUniqueKeyPolicy с новым объектом psUniqueKeyPolicy создается новый объект — **AzCosmosDBGremlinUniqueKeyPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e338e-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e338e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e338e-107">EXAMPLES</span></span>

### <span data-ttu-id="e338e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e338e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="e338e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e338e-109">PARAMETERS</span></span>

### <span data-ttu-id="e338e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e338e-110">-DefaultProfile</span></span>
<span data-ttu-id="e338e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e338e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e338e-112">-Path</span><span class="sxs-lookup"><span data-stu-id="e338e-112">-Path</span></span>
<span data-ttu-id="e338e-113">Массив значений строки пути</span><span class="sxs-lookup"><span data-stu-id="e338e-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e338e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e338e-114">CommonParameters</span></span>
<span data-ttu-id="e338e-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e338e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e338e-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e338e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e338e-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e338e-117">INPUTS</span></span>

### <span data-ttu-id="e338e-118">Нет</span><span class="sxs-lookup"><span data-stu-id="e338e-118">None</span></span>

## <span data-ttu-id="e338e-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e338e-119">OUTPUTS</span></span>

### <span data-ttu-id="e338e-120">Microsoft.Azure.Commands.ВацыDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e338e-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="e338e-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e338e-121">NOTES</span></span>

## <span data-ttu-id="e338e-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e338e-122">RELATED LINKS</span></span>
