---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314594"
---
# <span data-ttu-id="5f2ba-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5f2ba-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5f2ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2ba-103">Обновляет CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="5f2ba-104">Выполняет операцию исправления на стороне клиента, считывая существующий keyspace.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="5f2ba-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f2ba-105">SYNTAX</span></span>

### <span data-ttu-id="5f2ba-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f2ba-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2ba-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f2ba-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f2ba-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f2ba-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f2ba-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f2ba-109">DESCRIPTION</span></span>
<span data-ttu-id="5f2ba-110">Обновляет CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="5f2ba-111">Выполняет операцию исправления на стороне клиента, считывая существующий keyspace.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="5f2ba-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f2ba-112">EXAMPLES</span></span>

### <span data-ttu-id="5f2ba-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f2ba-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="5f2ba-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f2ba-114">PARAMETERS</span></span>

### <span data-ttu-id="5f2ba-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5f2ba-115">-AccountName</span></span>
<span data-ttu-id="5f2ba-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5f2ba-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5f2ba-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5f2ba-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5f2ba-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f2ba-119">-Confirm</span></span>
<span data-ttu-id="5f2ba-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f2ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2ba-121">-DefaultProfile</span></span>
<span data-ttu-id="5f2ba-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f2ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f2ba-123">-InputObject</span></span>
<span data-ttu-id="5f2ba-124">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="5f2ba-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f2ba-125">-Name</span></span>
<span data-ttu-id="5f2ba-126">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5f2ba-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5f2ba-127">-ParentObject</span></span>
<span data-ttu-id="5f2ba-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5f2ba-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5f2ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f2ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="5f2ba-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5f2ba-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="5f2ba-131">-Throughput</span></span>
<span data-ttu-id="5f2ba-132">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5f2ba-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5f2ba-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5f2ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f2ba-134">-WhatIf</span></span>
<span data-ttu-id="5f2ba-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f2ba-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f2ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2ba-137">CommonParameters</span></span>
<span data-ttu-id="5f2ba-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f2ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2ba-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f2ba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2ba-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f2ba-140">INPUTS</span></span>

### <span data-ttu-id="5f2ba-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5f2ba-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="5f2ba-142">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5f2ba-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5f2ba-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f2ba-143">OUTPUTS</span></span>

### <span data-ttu-id="5f2ba-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5f2ba-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5f2ba-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5f2ba-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5f2ba-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f2ba-146">NOTES</span></span>

## <span data-ttu-id="5f2ba-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f2ba-147">RELATED LINKS</span></span>
