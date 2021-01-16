---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392668"
---
# <span data-ttu-id="c72f4-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="c72f4-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="c72f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c72f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c72f4-103">Создает новый столбец "Дискеты" Вадима Климова.</span><span class="sxs-lookup"><span data-stu-id="c72f4-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="c72f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c72f4-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c72f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c72f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c72f4-106">Новая **столбец AzCosmosDBCassandraColumn** создает новый столбец Вадима Кузьмина (Егоры).</span><span class="sxs-lookup"><span data-stu-id="c72f4-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="c72f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c72f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c72f4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c72f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="c72f4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c72f4-109">PARAMETERS</span></span>

### <span data-ttu-id="c72f4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72f4-110">-DefaultProfile</span></span>
<span data-ttu-id="c72f4-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c72f4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72f4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c72f4-112">-Name</span></span>
<span data-ttu-id="c72f4-113">Имя столбца "Александра".</span><span class="sxs-lookup"><span data-stu-id="c72f4-113">Name of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72f4-114">-Type</span><span class="sxs-lookup"><span data-stu-id="c72f4-114">-Type</span></span>
<span data-ttu-id="c72f4-115">Тип столбца "Александра".</span><span class="sxs-lookup"><span data-stu-id="c72f4-115">Type of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72f4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72f4-116">CommonParameters</span></span>
<span data-ttu-id="c72f4-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72f4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72f4-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c72f4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72f4-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c72f4-119">INPUTS</span></span>

### <span data-ttu-id="c72f4-120">Нет</span><span class="sxs-lookup"><span data-stu-id="c72f4-120">None</span></span>

## <span data-ttu-id="c72f4-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c72f4-121">OUTPUTS</span></span>

### <span data-ttu-id="c72f4-122">Microsoft.Azure.Commands.АsDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="c72f4-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="c72f4-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c72f4-123">NOTES</span></span>

## <span data-ttu-id="c72f4-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c72f4-124">RELATED LINKS</span></span>
