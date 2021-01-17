---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403727"
---
# <span data-ttu-id="2e064-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2e064-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="2e064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e064-102">SYNOPSIS</span></span>
<span data-ttu-id="2e064-103">Создание нового объекта UniqueKeyPolicy вНося в Результате ДВ.</span><span class="sxs-lookup"><span data-stu-id="2e064-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="2e064-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e064-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e064-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e064-105">DESCRIPTION</span></span>
<span data-ttu-id="2e064-106">Для создания объекта psUniqueKeyPolicy с новым объектом psUniqueKeyPolicy создается новый объект — **AzCosmosDBGremlinUniqueKeyPolicy.**</span><span class="sxs-lookup"><span data-stu-id="2e064-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="2e064-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e064-107">EXAMPLES</span></span>

### <span data-ttu-id="2e064-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e064-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="2e064-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e064-109">PARAMETERS</span></span>

### <span data-ttu-id="2e064-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e064-110">-DefaultProfile</span></span>
<span data-ttu-id="2e064-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e064-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e064-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="2e064-112">-UniqueKey</span></span>
<span data-ttu-id="2e064-113">Массив объектов типа PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="2e064-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="2e064-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e064-114">CommonParameters</span></span>
<span data-ttu-id="2e064-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e064-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e064-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e064-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e064-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e064-117">INPUTS</span></span>

### <span data-ttu-id="2e064-118">Нет</span><span class="sxs-lookup"><span data-stu-id="2e064-118">None</span></span>

## <span data-ttu-id="2e064-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e064-119">OUTPUTS</span></span>

### <span data-ttu-id="2e064-120">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2e064-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="2e064-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e064-121">NOTES</span></span>

## <span data-ttu-id="2e064-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e064-122">RELATED LINKS</span></span>
