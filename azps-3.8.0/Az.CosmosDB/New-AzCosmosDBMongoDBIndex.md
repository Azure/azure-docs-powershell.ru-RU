---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073647"
---
# <span data-ttu-id="815c2-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="815c2-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="815c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="815c2-102">SYNOPSIS</span></span>
<span data-ttu-id="815c2-103">Создает новый индекс CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="815c2-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="815c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="815c2-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="815c2-105">DESCRIPTION</span></span>
<span data-ttu-id="815c2-106">**New-AzCosmosDBMongoDBIndex** создает новый индекс CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="815c2-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="815c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="815c2-107">EXAMPLES</span></span>

### <span data-ttu-id="815c2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="815c2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="815c2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="815c2-109">PARAMETERS</span></span>

### <span data-ttu-id="815c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815c2-110">-DefaultProfile</span></span>
<span data-ttu-id="815c2-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="815c2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="815c2-112">Клавиша</span><span class="sxs-lookup"><span data-stu-id="815c2-112">-Key</span></span>
<span data-ttu-id="815c2-113">Массив значений ключа в виде строк.</span><span class="sxs-lookup"><span data-stu-id="815c2-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="815c2-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="815c2-114">-TtlInSeconds</span></span>
<span data-ttu-id="815c2-115">Количество секунд, после которого истекает срок действия индекса.</span><span class="sxs-lookup"><span data-stu-id="815c2-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="815c2-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="815c2-116">-Unique</span></span>
<span data-ttu-id="815c2-117">Логическое значение, определяющее, является ли индекс уникальным.</span><span class="sxs-lookup"><span data-stu-id="815c2-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="815c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815c2-118">CommonParameters</span></span>
<span data-ttu-id="815c2-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="815c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815c2-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="815c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815c2-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="815c2-121">INPUTS</span></span>

### <span data-ttu-id="815c2-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="815c2-122">None</span></span>

## <span data-ttu-id="815c2-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="815c2-123">OUTPUTS</span></span>

### <span data-ttu-id="815c2-124">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="815c2-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="815c2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="815c2-125">NOTES</span></span>

## <span data-ttu-id="815c2-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="815c2-126">RELATED LINKS</span></span>
