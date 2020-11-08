---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073645"
---
# <span data-ttu-id="e460a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e460a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="e460a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e460a-102">SYNOPSIS</span></span>
<span data-ttu-id="e460a-103">Создает новый объект CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e460a-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e460a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e460a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e460a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e460a-105">DESCRIPTION</span></span>
<span data-ttu-id="e460a-106">Командлет **New-AzCosmosDBGremlinUniqueKeyPolicy** создает новый объект типа PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e460a-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e460a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e460a-107">EXAMPLES</span></span>

### <span data-ttu-id="e460a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e460a-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="e460a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e460a-109">PARAMETERS</span></span>

### <span data-ttu-id="e460a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e460a-110">-DefaultProfile</span></span>
<span data-ttu-id="e460a-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e460a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e460a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="e460a-112">-UniqueKey</span></span>
<span data-ttu-id="e460a-113">Массив объектов типа PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="e460a-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e460a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e460a-114">CommonParameters</span></span>
<span data-ttu-id="e460a-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e460a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e460a-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e460a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e460a-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e460a-117">INPUTS</span></span>

### <span data-ttu-id="e460a-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="e460a-118">None</span></span>

## <span data-ttu-id="e460a-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e460a-119">OUTPUTS</span></span>

### <span data-ttu-id="e460a-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e460a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="e460a-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e460a-121">NOTES</span></span>

## <span data-ttu-id="e460a-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e460a-122">RELATED LINKS</span></span>
