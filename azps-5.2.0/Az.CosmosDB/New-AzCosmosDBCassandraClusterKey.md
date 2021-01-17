---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402548"
---
# <span data-ttu-id="c0bb1-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="c0bb1-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="c0bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0bb1-103">Создает новый ключ кластера Климова (Сергей Климов).</span><span class="sxs-lookup"><span data-stu-id="c0bb1-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c0bb1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0bb1-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0bb1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="c0bb1-106">**New-AzCosmosDBCassandraClusterKey** создает новый ключ кластера Кузьмина.</span><span class="sxs-lookup"><span data-stu-id="c0bb1-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c0bb1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="c0bb1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0bb1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="c0bb1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0bb1-109">PARAMETERS</span></span>

### <span data-ttu-id="c0bb1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0bb1-110">-DefaultProfile</span></span>
<span data-ttu-id="c0bb1-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bb1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0bb1-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c0bb1-112">-Name</span></span>
<span data-ttu-id="c0bb1-113">Имя ключа кластера "Александра".</span><span class="sxs-lookup"><span data-stu-id="c0bb1-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="c0bb1-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c0bb1-114">-OrderBy</span></span>
<span data-ttu-id="c0bb1-115">Порядок клавиши "Блок".</span><span class="sxs-lookup"><span data-stu-id="c0bb1-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="c0bb1-116">Возможные значения: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="c0bb1-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="c0bb1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0bb1-117">CommonParameters</span></span>
<span data-ttu-id="c0bb1-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0bb1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0bb1-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0bb1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0bb1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0bb1-120">INPUTS</span></span>

### <span data-ttu-id="c0bb1-121">Нет</span><span class="sxs-lookup"><span data-stu-id="c0bb1-121">None</span></span>

## <span data-ttu-id="c0bb1-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0bb1-122">OUTPUTS</span></span>

### <span data-ttu-id="c0bb1-123">Microsoft.Azure.Commands.ВацDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="c0bb1-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="c0bb1-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0bb1-124">NOTES</span></span>

## <span data-ttu-id="c0bb1-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0bb1-125">RELATED LINKS</span></span>
