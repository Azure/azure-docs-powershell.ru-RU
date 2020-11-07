---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911800"
---
# <span data-ttu-id="ad4a6-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="ad4a6-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="ad4a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4a6-103">Создает новый ключ кластера CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="ad4a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad4a6-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad4a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad4a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4a6-106">**New-AzCosmosDBCassandraClusterKey** создает новый ключ кластера CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="ad4a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad4a6-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4a6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad4a6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="ad4a6-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad4a6-109">PARAMETERS</span></span>

### <span data-ttu-id="ad4a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4a6-110">-DefaultProfile</span></span>
<span data-ttu-id="ad4a6-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad4a6-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad4a6-112">-Name</span></span>
<span data-ttu-id="ad4a6-113">Имя ключа кластера Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="ad4a6-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ad4a6-114">-OrderBy</span></span>
<span data-ttu-id="ad4a6-115">Упорядочение ключа кластера Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="ad4a6-116">Возможные значения: "ASC", "DESC"</span><span class="sxs-lookup"><span data-stu-id="ad4a6-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="ad4a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4a6-117">CommonParameters</span></span>
<span data-ttu-id="ad4a6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad4a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4a6-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad4a6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4a6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad4a6-120">INPUTS</span></span>

### <span data-ttu-id="ad4a6-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="ad4a6-121">None</span></span>

## <span data-ttu-id="ad4a6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad4a6-122">OUTPUTS</span></span>

### <span data-ttu-id="ad4a6-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="ad4a6-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="ad4a6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad4a6-124">NOTES</span></span>

## <span data-ttu-id="ad4a6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad4a6-125">RELATED LINKS</span></span>
