---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314588"
---
# <span data-ttu-id="14813-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="14813-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="14813-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14813-102">SYNOPSIS</span></span>
<span data-ttu-id="14813-103">Обновляет значение пропускной способности CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="14813-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="14813-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14813-104">SYNTAX</span></span>

### <span data-ttu-id="14813-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14813-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14813-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14813-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14813-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14813-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14813-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14813-108">DESCRIPTION</span></span>
<span data-ttu-id="14813-109">Обновляет значение пропускной способности CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="14813-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="14813-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14813-110">EXAMPLES</span></span>

### <span data-ttu-id="14813-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14813-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="14813-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14813-112">PARAMETERS</span></span>

### <span data-ttu-id="14813-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="14813-113">-AccountName</span></span>
<span data-ttu-id="14813-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="14813-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="14813-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="14813-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="14813-116">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="14813-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="14813-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14813-117">-Confirm</span></span>
<span data-ttu-id="14813-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14813-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14813-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14813-119">-DefaultProfile</span></span>
<span data-ttu-id="14813-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14813-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14813-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14813-121">-InputObject</span></span>
<span data-ttu-id="14813-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="14813-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14813-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14813-123">-Name</span></span>
<span data-ttu-id="14813-124">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="14813-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="14813-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="14813-125">-ParentObject</span></span>
<span data-ttu-id="14813-126">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="14813-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14813-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14813-127">-ResourceGroupName</span></span>
<span data-ttu-id="14813-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14813-128">Name of resource group.</span></span>

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

### <span data-ttu-id="14813-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="14813-129">-Throughput</span></span>
<span data-ttu-id="14813-130">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="14813-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="14813-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="14813-131">Default value is 400.</span></span>

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

### <span data-ttu-id="14813-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14813-132">-WhatIf</span></span>
<span data-ttu-id="14813-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14813-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14813-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14813-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14813-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14813-135">CommonParameters</span></span>
<span data-ttu-id="14813-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14813-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14813-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14813-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14813-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14813-138">INPUTS</span></span>

### <span data-ttu-id="14813-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="14813-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="14813-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14813-140">OUTPUTS</span></span>

### <span data-ttu-id="14813-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="14813-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="14813-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="14813-142">NOTES</span></span>

## <span data-ttu-id="14813-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14813-143">RELATED LINKS</span></span>
