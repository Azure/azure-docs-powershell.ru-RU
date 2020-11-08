---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074423"
---
# <span data-ttu-id="9f34c-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="9f34c-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="9f34c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f34c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f34c-103">Обновляет значение пропускной способности таблицы CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9f34c-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="9f34c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f34c-104">SYNTAX</span></span>

### <span data-ttu-id="9f34c-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f34c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f34c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f34c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f34c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f34c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f34c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f34c-108">EXAMPLES</span></span>

### <span data-ttu-id="9f34c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f34c-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9f34c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f34c-110">PARAMETERS</span></span>

### <span data-ttu-id="9f34c-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9f34c-111">-AccountName</span></span>
<span data-ttu-id="9f34c-112">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9f34c-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f34c-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f34c-113">-Confirm</span></span>
<span data-ttu-id="9f34c-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f34c-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f34c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f34c-115">-DefaultProfile</span></span>
<span data-ttu-id="9f34c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f34c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f34c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f34c-117">-InputObject</span></span>
<span data-ttu-id="9f34c-118">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="9f34c-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f34c-119">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="9f34c-119">-KeyspaceName</span></span>
<span data-ttu-id="9f34c-120">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="9f34c-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9f34c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f34c-121">-Name</span></span>
<span data-ttu-id="9f34c-122">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9f34c-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="9f34c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f34c-123">-ParentObject</span></span>
<span data-ttu-id="9f34c-124">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="9f34c-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9f34c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f34c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f34c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f34c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9f34c-127">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="9f34c-127">-Throughput</span></span>
<span data-ttu-id="9f34c-128">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9f34c-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9f34c-129">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9f34c-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f34c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f34c-130">-WhatIf</span></span>
<span data-ttu-id="9f34c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f34c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f34c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f34c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f34c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f34c-133">CommonParameters</span></span>
<span data-ttu-id="9f34c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f34c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f34c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f34c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f34c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f34c-136">INPUTS</span></span>

### <span data-ttu-id="9f34c-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9f34c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9f34c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f34c-138">OUTPUTS</span></span>

### <span data-ttu-id="9f34c-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f34c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f34c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f34c-140">NOTES</span></span>

## <span data-ttu-id="9f34c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f34c-141">RELATED LINKS</span></span>
