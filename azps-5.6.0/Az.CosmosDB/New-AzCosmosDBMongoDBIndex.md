---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991444"
---
# <span data-ttu-id="15173-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="15173-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="15173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15173-102">SYNOPSIS</span></span>
<span data-ttu-id="15173-103">Создание нового индекса :'ДискоссDB MongoDB''</span><span class="sxs-lookup"><span data-stu-id="15173-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="15173-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="15173-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15173-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15173-105">DESCRIPTION</span></span>
<span data-ttu-id="15173-106">**New-AzCosmosDBMongoDBIndex** создает новый индекс Вадима Ермонова.</span><span class="sxs-lookup"><span data-stu-id="15173-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="15173-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="15173-107">EXAMPLES</span></span>

### <span data-ttu-id="15173-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15173-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="15173-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15173-109">PARAMETERS</span></span>

### <span data-ttu-id="15173-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15173-110">-DefaultProfile</span></span>
<span data-ttu-id="15173-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15173-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15173-112">-Key</span><span class="sxs-lookup"><span data-stu-id="15173-112">-Key</span></span>
<span data-ttu-id="15173-113">Массив значений ключей в качестве строк.</span><span class="sxs-lookup"><span data-stu-id="15173-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15173-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="15173-114">-TtlInSeconds</span></span>
<span data-ttu-id="15173-115">Количество секунд, после которого истекает срок действия индекса.</span><span class="sxs-lookup"><span data-stu-id="15173-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15173-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="15173-116">-Unique</span></span>
<span data-ttu-id="15173-117">Bool to indicate if the index is unique or not.</span><span class="sxs-lookup"><span data-stu-id="15173-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15173-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15173-118">CommonParameters</span></span>
<span data-ttu-id="15173-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15173-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15173-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15173-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15173-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15173-121">INPUTS</span></span>

### <span data-ttu-id="15173-122">Нет</span><span class="sxs-lookup"><span data-stu-id="15173-122">None</span></span>

## <span data-ttu-id="15173-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="15173-123">OUTPUTS</span></span>

### <span data-ttu-id="15173-124">Microsoft.Azure.Commands.ВацыDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="15173-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="15173-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="15173-125">NOTES</span></span>

## <span data-ttu-id="15173-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15173-126">RELATED LINKS</span></span>
