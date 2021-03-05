---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986863"
---
# <span data-ttu-id="35745-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="35745-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="35745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35745-102">SYNOPSIS</span></span>
<span data-ttu-id="35745-103">Создает объект SqlUniqueKeyPolicy, который создается в Качестве объекта .</span><span class="sxs-lookup"><span data-stu-id="35745-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="35745-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35745-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35745-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35745-105">DESCRIPTION</span></span>
<span data-ttu-id="35745-106">Для создания нового объекта типа **PSSqlUniqueKeyPolicy** создается новый объект psSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="35745-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="35745-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35745-107">EXAMPLES</span></span>

### <span data-ttu-id="35745-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35745-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="35745-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35745-109">PARAMETERS</span></span>

### <span data-ttu-id="35745-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35745-110">-DefaultProfile</span></span>
<span data-ttu-id="35745-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35745-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35745-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="35745-112">-UniqueKey</span></span>
<span data-ttu-id="35745-113">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="35745-113">Database name.</span></span>

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

### <span data-ttu-id="35745-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35745-114">CommonParameters</span></span>
<span data-ttu-id="35745-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35745-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35745-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35745-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35745-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35745-117">INPUTS</span></span>

### <span data-ttu-id="35745-118">Нет</span><span class="sxs-lookup"><span data-stu-id="35745-118">None</span></span>

## <span data-ttu-id="35745-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35745-119">OUTPUTS</span></span>

### <span data-ttu-id="35745-120">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="35745-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="35745-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35745-121">NOTES</span></span>

## <span data-ttu-id="35745-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35745-122">RELATED LINKS</span></span>
