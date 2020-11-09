---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315071"
---
# <span data-ttu-id="a5836-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="a5836-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="a5836-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5836-102">SYNOPSIS</span></span>
<span data-ttu-id="a5836-103">Возвращает таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a5836-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a5836-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5836-104">SYNTAX</span></span>

### <span data-ttu-id="a5836-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5836-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5836-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5836-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5836-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5836-107">DESCRIPTION</span></span>
<span data-ttu-id="a5836-108">Командлет **Get-AzCosmosDBCassandraTable** создает новый или обновляет существующий CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="a5836-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a5836-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5836-109">EXAMPLES</span></span>

### <span data-ttu-id="a5836-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5836-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="a5836-111">{{Get-AzCosmosDBCassandraTable получает свойства существующего CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="a5836-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="a5836-112">Вы можете развернуть ресурс, чтобы получить DefaultTtl, схему, _etag, _ts, _rid свойства.}}</span><span class="sxs-lookup"><span data-stu-id="a5836-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="a5836-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5836-113">PARAMETERS</span></span>

### <span data-ttu-id="a5836-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a5836-114">-AccountName</span></span>
<span data-ttu-id="a5836-115">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a5836-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5836-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5836-116">-DefaultProfile</span></span>
<span data-ttu-id="a5836-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5836-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5836-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="a5836-118">-KeyspaceName</span></span>
<span data-ttu-id="a5836-119">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="a5836-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a5836-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5836-120">-Name</span></span>
<span data-ttu-id="a5836-121">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a5836-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="a5836-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5836-122">-ParentObject</span></span>
<span data-ttu-id="a5836-123">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="a5836-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="a5836-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5836-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5836-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5836-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a5836-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5836-126">CommonParameters</span></span>
<span data-ttu-id="a5836-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5836-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5836-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5836-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5836-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5836-129">INPUTS</span></span>

### <span data-ttu-id="a5836-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="a5836-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="a5836-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5836-131">OUTPUTS</span></span>

### <span data-ttu-id="a5836-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a5836-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="a5836-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a5836-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a5836-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5836-134">NOTES</span></span>

## <span data-ttu-id="a5836-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5836-135">RELATED LINKS</span></span>
