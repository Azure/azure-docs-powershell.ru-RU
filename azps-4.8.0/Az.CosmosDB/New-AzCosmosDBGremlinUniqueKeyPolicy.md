---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078379"
---
# <span data-ttu-id="d2157-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d2157-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="d2157-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2157-102">SYNOPSIS</span></span>
<span data-ttu-id="d2157-103">Создает новый объект CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d2157-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="d2157-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2157-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2157-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2157-105">DESCRIPTION</span></span>
<span data-ttu-id="d2157-106">Командлет **New-AzCosmosDBGremlinUniqueKeyPolicy** создает новый объект типа PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d2157-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="d2157-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2157-107">EXAMPLES</span></span>

### <span data-ttu-id="d2157-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2157-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="d2157-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2157-109">PARAMETERS</span></span>

### <span data-ttu-id="d2157-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2157-110">-DefaultProfile</span></span>
<span data-ttu-id="d2157-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2157-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2157-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="d2157-112">-UniqueKey</span></span>
<span data-ttu-id="d2157-113">Массив объектов типа PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="d2157-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="d2157-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2157-114">CommonParameters</span></span>
<span data-ttu-id="d2157-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2157-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2157-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2157-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2157-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2157-117">INPUTS</span></span>

### <span data-ttu-id="d2157-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="d2157-118">None</span></span>

## <span data-ttu-id="d2157-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2157-119">OUTPUTS</span></span>

### <span data-ttu-id="d2157-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d2157-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="d2157-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2157-121">NOTES</span></span>

## <span data-ttu-id="d2157-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2157-122">RELATED LINKS</span></span>
