---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236842"
---
# <span data-ttu-id="34a2e-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="34a2e-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="34a2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="34a2e-103">Обновляет CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="34a2e-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="34a2e-104">Выполняет операцию исправления на стороне клиента, считывая существующий keyspace.</span><span class="sxs-lookup"><span data-stu-id="34a2e-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="34a2e-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34a2e-105">SYNTAX</span></span>

### <span data-ttu-id="34a2e-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34a2e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a2e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a2e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34a2e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a2e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34a2e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34a2e-109">DESCRIPTION</span></span>
<span data-ttu-id="34a2e-110">Обновляет CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="34a2e-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="34a2e-111">Выполняет операцию исправления на стороне клиента, считывая существующий keyspace.</span><span class="sxs-lookup"><span data-stu-id="34a2e-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="34a2e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34a2e-112">EXAMPLES</span></span>

### <span data-ttu-id="34a2e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34a2e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="34a2e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34a2e-114">PARAMETERS</span></span>

### <span data-ttu-id="34a2e-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="34a2e-115">-AccountName</span></span>
<span data-ttu-id="34a2e-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="34a2e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34a2e-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="34a2e-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="34a2e-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="34a2e-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="34a2e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34a2e-119">-Confirm</span></span>
<span data-ttu-id="34a2e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34a2e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a2e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a2e-121">-DefaultProfile</span></span>
<span data-ttu-id="34a2e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34a2e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a2e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34a2e-123">-InputObject</span></span>
<span data-ttu-id="34a2e-124">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="34a2e-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="34a2e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34a2e-125">-Name</span></span>
<span data-ttu-id="34a2e-126">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="34a2e-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="34a2e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34a2e-127">-ParentObject</span></span>
<span data-ttu-id="34a2e-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="34a2e-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="34a2e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a2e-129">-ResourceGroupName</span></span>
<span data-ttu-id="34a2e-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34a2e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="34a2e-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="34a2e-131">-Throughput</span></span>
<span data-ttu-id="34a2e-132">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="34a2e-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="34a2e-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="34a2e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="34a2e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a2e-134">-WhatIf</span></span>
<span data-ttu-id="34a2e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34a2e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a2e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34a2e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a2e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a2e-137">CommonParameters</span></span>
<span data-ttu-id="34a2e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34a2e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a2e-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34a2e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a2e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34a2e-140">INPUTS</span></span>

### <span data-ttu-id="34a2e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="34a2e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="34a2e-142">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="34a2e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="34a2e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34a2e-143">OUTPUTS</span></span>

### <span data-ttu-id="34a2e-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="34a2e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="34a2e-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="34a2e-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="34a2e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="34a2e-146">NOTES</span></span>

## <span data-ttu-id="34a2e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34a2e-147">RELATED LINKS</span></span>
