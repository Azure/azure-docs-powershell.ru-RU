---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233052"
---
# <span data-ttu-id="048cb-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="048cb-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="048cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="048cb-102">SYNOPSIS</span></span>
<span data-ttu-id="048cb-103">Создает новый столбец "Дискеты" Вадима Климова.</span><span class="sxs-lookup"><span data-stu-id="048cb-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="048cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="048cb-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="048cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="048cb-105">DESCRIPTION</span></span>
<span data-ttu-id="048cb-106">Новая **столбец AzCosmosDBCassandraColumn** создает новый столбец Вадима Кузьмина (Егоры).</span><span class="sxs-lookup"><span data-stu-id="048cb-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="048cb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="048cb-107">EXAMPLES</span></span>

### <span data-ttu-id="048cb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="048cb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="048cb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="048cb-109">PARAMETERS</span></span>

### <span data-ttu-id="048cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048cb-110">-DefaultProfile</span></span>
<span data-ttu-id="048cb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="048cb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="048cb-112">-Name</span><span class="sxs-lookup"><span data-stu-id="048cb-112">-Name</span></span>
<span data-ttu-id="048cb-113">Имя столбца "Александра".</span><span class="sxs-lookup"><span data-stu-id="048cb-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="048cb-114">-Type</span><span class="sxs-lookup"><span data-stu-id="048cb-114">-Type</span></span>
<span data-ttu-id="048cb-115">Тип столбца "Александра".</span><span class="sxs-lookup"><span data-stu-id="048cb-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="048cb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048cb-116">CommonParameters</span></span>
<span data-ttu-id="048cb-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048cb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048cb-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="048cb-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048cb-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="048cb-119">INPUTS</span></span>

### <span data-ttu-id="048cb-120">Нет</span><span class="sxs-lookup"><span data-stu-id="048cb-120">None</span></span>

## <span data-ttu-id="048cb-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="048cb-121">OUTPUTS</span></span>

### <span data-ttu-id="048cb-122">Microsoft.Azure.Commands.ВацыDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="048cb-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="048cb-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="048cb-123">NOTES</span></span>

## <span data-ttu-id="048cb-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="048cb-124">RELATED LINKS</span></span>
