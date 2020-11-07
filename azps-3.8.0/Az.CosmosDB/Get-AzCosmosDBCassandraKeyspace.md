---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912047"
---
# <span data-ttu-id="4d072-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="4d072-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="4d072-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d072-102">SYNOPSIS</span></span>
<span data-ttu-id="4d072-103">Возвращает CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="4d072-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4d072-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d072-104">SYNTAX</span></span>

### <span data-ttu-id="4d072-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d072-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d072-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d072-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d072-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d072-107">DESCRIPTION</span></span>
<span data-ttu-id="4d072-108">Командлет **Get-AzCosmosDBCassandraKeyspace** создает новый или обновляет существующий CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="4d072-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4d072-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d072-109">EXAMPLES</span></span>

### <span data-ttu-id="4d072-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d072-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4d072-111">Get-AzCosmosDBCassandraKeyspace получает свойства существующего CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="4d072-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4d072-112">Вы можете развернуть ресурс, чтобы получить _etag, _ts _rid свойств.</span><span class="sxs-lookup"><span data-stu-id="4d072-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="4d072-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d072-113">PARAMETERS</span></span>

### <span data-ttu-id="4d072-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4d072-114">-AccountName</span></span>
<span data-ttu-id="4d072-115">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4d072-115">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d072-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d072-116">-DefaultProfile</span></span>
<span data-ttu-id="4d072-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d072-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d072-118">-Подробно</span><span class="sxs-lookup"><span data-stu-id="4d072-118">-Detailed</span></span>
<span data-ttu-id="4d072-119">Если он указан, командлет возвращает keyspace с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="4d072-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d072-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d072-120">-InputObject</span></span>
<span data-ttu-id="4d072-121">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4d072-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d072-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d072-122">-Name</span></span>
<span data-ttu-id="4d072-123">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="4d072-123">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d072-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d072-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d072-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d072-125">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d072-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d072-126">CommonParameters</span></span>
<span data-ttu-id="4d072-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d072-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d072-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d072-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d072-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d072-129">INPUTS</span></span>

### <span data-ttu-id="4d072-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4d072-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4d072-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d072-131">OUTPUTS</span></span>

### <span data-ttu-id="4d072-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4d072-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="4d072-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4d072-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4d072-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d072-134">NOTES</span></span>

## <span data-ttu-id="4d072-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d072-135">RELATED LINKS</span></span>
