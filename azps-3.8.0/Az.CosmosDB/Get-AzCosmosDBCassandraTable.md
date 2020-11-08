---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074127"
---
# <span data-ttu-id="74da9-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="74da9-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="74da9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74da9-102">SYNOPSIS</span></span>
<span data-ttu-id="74da9-103">Возвращает таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="74da9-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="74da9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74da9-104">SYNTAX</span></span>

### <span data-ttu-id="74da9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74da9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74da9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74da9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74da9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74da9-107">DESCRIPTION</span></span>
<span data-ttu-id="74da9-108">Командлет **Get-AzCosmosDBCassandraTable** создает новый или обновляет существующий CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="74da9-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="74da9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74da9-109">EXAMPLES</span></span>

### <span data-ttu-id="74da9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74da9-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="74da9-111">{{Get-AzCosmosDBCassandraTable получает свойства существующего CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="74da9-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="74da9-112">Вы можете развернуть ресурс, чтобы получить DefaultTtl, схему, _etag, _ts, _rid свойства.}}</span><span class="sxs-lookup"><span data-stu-id="74da9-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="74da9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74da9-113">PARAMETERS</span></span>

### <span data-ttu-id="74da9-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="74da9-114">-AccountName</span></span>
<span data-ttu-id="74da9-115">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="74da9-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74da9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74da9-116">-DefaultProfile</span></span>
<span data-ttu-id="74da9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74da9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74da9-118">-Подробно</span><span class="sxs-lookup"><span data-stu-id="74da9-118">-Detailed</span></span>
<span data-ttu-id="74da9-119">Если он указан, командлет возвращает таблицу Cassandra с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="74da9-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="74da9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74da9-120">-InputObject</span></span>
<span data-ttu-id="74da9-121">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="74da9-121">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74da9-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="74da9-122">-KeyspaceName</span></span>
<span data-ttu-id="74da9-123">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="74da9-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="74da9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74da9-124">-Name</span></span>
<span data-ttu-id="74da9-125">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="74da9-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="74da9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74da9-126">-ResourceGroupName</span></span>
<span data-ttu-id="74da9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74da9-127">Name of resource group.</span></span>

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

### <span data-ttu-id="74da9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74da9-128">CommonParameters</span></span>
<span data-ttu-id="74da9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74da9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74da9-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74da9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74da9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74da9-131">INPUTS</span></span>

### <span data-ttu-id="74da9-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="74da9-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="74da9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74da9-133">OUTPUTS</span></span>

### <span data-ttu-id="74da9-134">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="74da9-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="74da9-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="74da9-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="74da9-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="74da9-136">NOTES</span></span>

## <span data-ttu-id="74da9-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74da9-137">RELATED LINKS</span></span>
