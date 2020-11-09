---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314582"
---
# <span data-ttu-id="e6b98-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="e6b98-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="e6b98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6b98-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b98-103">Обновляет значение пропускной способности таблицы CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e6b98-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e6b98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6b98-104">SYNTAX</span></span>

### <span data-ttu-id="e6b98-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6b98-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b98-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b98-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b98-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b98-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6b98-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b98-108">DESCRIPTION</span></span>
<span data-ttu-id="e6b98-109">Обновляет значение пропускной способности таблицы CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e6b98-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e6b98-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6b98-110">EXAMPLES</span></span>

### <span data-ttu-id="e6b98-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6b98-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e6b98-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6b98-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b98-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e6b98-113">-AccountName</span></span>
<span data-ttu-id="e6b98-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e6b98-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e6b98-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e6b98-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e6b98-116">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="e6b98-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6b98-117">-Confirm</span></span>
<span data-ttu-id="e6b98-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6b98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6b98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b98-119">-DefaultProfile</span></span>
<span data-ttu-id="e6b98-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b98-121">-InputObject</span></span>
<span data-ttu-id="e6b98-122">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="e6b98-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e6b98-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="e6b98-123">-KeyspaceName</span></span>
<span data-ttu-id="e6b98-124">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="e6b98-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e6b98-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6b98-125">-Name</span></span>
<span data-ttu-id="e6b98-126">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e6b98-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="e6b98-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e6b98-127">-ParentObject</span></span>
<span data-ttu-id="e6b98-128">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="e6b98-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e6b98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b98-129">-ResourceGroupName</span></span>
<span data-ttu-id="e6b98-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6b98-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e6b98-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="e6b98-131">-Throughput</span></span>
<span data-ttu-id="e6b98-132">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e6b98-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e6b98-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="e6b98-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6b98-134">-WhatIf</span></span>
<span data-ttu-id="e6b98-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6b98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6b98-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6b98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6b98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b98-137">CommonParameters</span></span>
<span data-ttu-id="e6b98-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6b98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b98-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b98-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b98-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6b98-140">INPUTS</span></span>

### <span data-ttu-id="e6b98-141">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e6b98-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e6b98-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b98-142">OUTPUTS</span></span>

### <span data-ttu-id="e6b98-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e6b98-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e6b98-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6b98-144">NOTES</span></span>

## <span data-ttu-id="e6b98-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6b98-145">RELATED LINKS</span></span>
