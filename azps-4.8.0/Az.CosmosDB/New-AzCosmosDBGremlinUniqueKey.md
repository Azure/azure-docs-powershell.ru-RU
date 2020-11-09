---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245090"
---
# <span data-ttu-id="30773-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="30773-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="30773-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30773-102">SYNOPSIS</span></span>
<span data-ttu-id="30773-103">Создает новый объект CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="30773-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="30773-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30773-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30773-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30773-105">DESCRIPTION</span></span>
<span data-ttu-id="30773-106">Командлет **New-AzCosmosDBGremlinUniqueKeyPolicy** создает новый объект типа PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="30773-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="30773-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30773-107">EXAMPLES</span></span>

### <span data-ttu-id="30773-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30773-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="30773-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30773-109">PARAMETERS</span></span>

### <span data-ttu-id="30773-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30773-110">-DefaultProfile</span></span>
<span data-ttu-id="30773-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30773-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30773-112">-Path</span><span class="sxs-lookup"><span data-stu-id="30773-112">-Path</span></span>
<span data-ttu-id="30773-113">Массив строк со значениями пути</span><span class="sxs-lookup"><span data-stu-id="30773-113">Array of string of path values</span></span>

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

### <span data-ttu-id="30773-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30773-114">CommonParameters</span></span>
<span data-ttu-id="30773-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30773-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30773-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30773-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30773-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30773-117">INPUTS</span></span>

### <span data-ttu-id="30773-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="30773-118">None</span></span>

## <span data-ttu-id="30773-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30773-119">OUTPUTS</span></span>

### <span data-ttu-id="30773-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="30773-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="30773-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="30773-121">NOTES</span></span>

## <span data-ttu-id="30773-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30773-122">RELATED LINKS</span></span>