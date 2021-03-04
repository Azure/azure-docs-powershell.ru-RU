---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957443"
---
# <span data-ttu-id="cf0d2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cf0d2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="cf0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0d2-103">Создание нового объекта UniqueKeyPolicy вНося в Результате ДВ.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="cf0d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf0d2-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf0d2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf0d2-105">DESCRIPTION</span></span>
<span data-ttu-id="cf0d2-106">Для создания нового объекта psUniqueKeyPolicy будет создаваться новый объект psUniqueKeyPolicy, который является объектом **New-AzCosmosDBGremlinUniqueKeyPolicy.**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="cf0d2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf0d2-107">EXAMPLES</span></span>

### <span data-ttu-id="cf0d2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf0d2-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="cf0d2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf0d2-109">PARAMETERS</span></span>

### <span data-ttu-id="cf0d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0d2-110">-DefaultProfile</span></span>
<span data-ttu-id="cf0d2-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf0d2-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="cf0d2-112">-UniqueKey</span></span>
<span data-ttu-id="cf0d2-113">Массив объектов типа PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0d2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0d2-114">CommonParameters</span></span>
<span data-ttu-id="cf0d2-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0d2-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf0d2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0d2-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf0d2-117">INPUTS</span></span>

### <span data-ttu-id="cf0d2-118">Нет</span><span class="sxs-lookup"><span data-stu-id="cf0d2-118">None</span></span>

## <span data-ttu-id="cf0d2-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf0d2-119">OUTPUTS</span></span>

### <span data-ttu-id="cf0d2-120">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cf0d2-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="cf0d2-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf0d2-121">NOTES</span></span>

## <span data-ttu-id="cf0d2-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf0d2-122">RELATED LINKS</span></span>
