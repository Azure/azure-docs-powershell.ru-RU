---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314891"
---
# <span data-ttu-id="5ba8f-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="5ba8f-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="5ba8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ba8f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba8f-103">Создает новый ключ кластера CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="5ba8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ba8f-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba8f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba8f-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba8f-106">**New-AzCosmosDBCassandraClusterKey** создает новый ключ кластера CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="5ba8f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ba8f-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba8f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ba8f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="5ba8f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ba8f-109">PARAMETERS</span></span>

### <span data-ttu-id="5ba8f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba8f-110">-DefaultProfile</span></span>
<span data-ttu-id="5ba8f-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba8f-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-112">-Name</span></span>
<span data-ttu-id="5ba8f-113">Имя ключа кластера Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="5ba8f-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5ba8f-114">-OrderBy</span></span>
<span data-ttu-id="5ba8f-115">Упорядочение ключа кластера Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="5ba8f-116">Возможные значения: "ASC", "DESC"</span><span class="sxs-lookup"><span data-stu-id="5ba8f-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="5ba8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba8f-117">CommonParameters</span></span>
<span data-ttu-id="5ba8f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba8f-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba8f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ba8f-120">INPUTS</span></span>

### <span data-ttu-id="5ba8f-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ba8f-121">None</span></span>

## <span data-ttu-id="5ba8f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba8f-122">OUTPUTS</span></span>

### <span data-ttu-id="5ba8f-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="5ba8f-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="5ba8f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ba8f-124">NOTES</span></span>

## <span data-ttu-id="5ba8f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ba8f-125">RELATED LINKS</span></span>