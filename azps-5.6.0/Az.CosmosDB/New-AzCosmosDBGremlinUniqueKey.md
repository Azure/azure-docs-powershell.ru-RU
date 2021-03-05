---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998791"
---
# <span data-ttu-id="b6942-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b6942-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="b6942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6942-102">SYNOPSIS</span></span>
<span data-ttu-id="b6942-103">Создание нового объекта UniqueKeyPolicy вНося в Результате ДВ.</span><span class="sxs-lookup"><span data-stu-id="b6942-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="b6942-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6942-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6942-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6942-105">DESCRIPTION</span></span>
<span data-ttu-id="b6942-106">Для создания нового объекта psUniqueKeyPolicy будет создаваться новый объект psUniqueKeyPolicy, который является объектом **New-AzCosmosDBGremlinUniqueKeyPolicy.**</span><span class="sxs-lookup"><span data-stu-id="b6942-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="b6942-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6942-107">EXAMPLES</span></span>

### <span data-ttu-id="b6942-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6942-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="b6942-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6942-109">PARAMETERS</span></span>

### <span data-ttu-id="b6942-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6942-110">-DefaultProfile</span></span>
<span data-ttu-id="b6942-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6942-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6942-112">-Path</span><span class="sxs-lookup"><span data-stu-id="b6942-112">-Path</span></span>
<span data-ttu-id="b6942-113">Массив значений строки пути</span><span class="sxs-lookup"><span data-stu-id="b6942-113">Array of string of path values</span></span>

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

### <span data-ttu-id="b6942-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6942-114">CommonParameters</span></span>
<span data-ttu-id="b6942-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6942-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6942-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6942-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6942-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6942-117">INPUTS</span></span>

### <span data-ttu-id="b6942-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b6942-118">None</span></span>

## <span data-ttu-id="b6942-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6942-119">OUTPUTS</span></span>

### <span data-ttu-id="b6942-120">Microsoft.Azure.Commands.ВацыDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b6942-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="b6942-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6942-121">NOTES</span></span>

## <span data-ttu-id="b6942-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6942-122">RELATED LINKS</span></span>
