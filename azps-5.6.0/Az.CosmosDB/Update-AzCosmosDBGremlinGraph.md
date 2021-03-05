---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 500bd1203f7f70b5749986a6b4ff1ab8d5978185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977331"
---
# <span data-ttu-id="783f9-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="783f9-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="783f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783f9-102">SYNOPSIS</span></span>
<span data-ttu-id="783f9-103">Обновляет График Гремлина вНося изменения в СхемуDb.</span><span class="sxs-lookup"><span data-stu-id="783f9-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="783f9-104">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="783f9-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="783f9-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="783f9-105">SYNTAX</span></span>

### <span data-ttu-id="783f9-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="783f9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="783f9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="783f9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783f9-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="783f9-109">DESCRIPTION</span></span>
<span data-ttu-id="783f9-110">Обновляет График Гремлина вНося изменения в СхемуDb.</span><span class="sxs-lookup"><span data-stu-id="783f9-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="783f9-111">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="783f9-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="783f9-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="783f9-112">EXAMPLES</span></span>

### <span data-ttu-id="783f9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="783f9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="783f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="783f9-114">PARAMETERS</span></span>

### <span data-ttu-id="783f9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="783f9-115">-AccountName</span></span>
<span data-ttu-id="783f9-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="783f9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="783f9-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="783f9-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="783f9-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="783f9-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="783f9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="783f9-119">-Confirm</span></span>
<span data-ttu-id="783f9-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="783f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783f9-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="783f9-122">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="783f9-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="783f9-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="783f9-124">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="783f9-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="783f9-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="783f9-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="783f9-126">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="783f9-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="783f9-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="783f9-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="783f9-128">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="783f9-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="783f9-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="783f9-129">-DatabaseName</span></span>
<span data-ttu-id="783f9-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="783f9-130">Database name.</span></span>

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

### <span data-ttu-id="783f9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783f9-131">-DefaultProfile</span></span>
<span data-ttu-id="783f9-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="783f9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="783f9-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-133">-IndexingPolicy</span></span>
<span data-ttu-id="783f9-134">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="783f9-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="783f9-135">-InputObject</span></span>
<span data-ttu-id="783f9-136">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="783f9-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-137">-Name</span><span class="sxs-lookup"><span data-stu-id="783f9-137">-Name</span></span>
<span data-ttu-id="783f9-138">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="783f9-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="783f9-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="783f9-139">-ParentObject</span></span>
<span data-ttu-id="783f9-140">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="783f9-140">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="783f9-141">-PartitionKeyKind</span></span>
<span data-ttu-id="783f9-142">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="783f9-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="783f9-143">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="783f9-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="783f9-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="783f9-144">-PartitionKeyPath</span></span>
<span data-ttu-id="783f9-145">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="783f9-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="783f9-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="783f9-147">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="783f9-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="783f9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="783f9-148">-ResourceGroupName</span></span>
<span data-ttu-id="783f9-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="783f9-149">Name of resource group.</span></span>

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

### <span data-ttu-id="783f9-150">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="783f9-150">-Throughput</span></span>
<span data-ttu-id="783f9-151">Пропускная способность Гремлин Графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="783f9-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="783f9-152">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="783f9-152">Default value is 400.</span></span>

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

### <span data-ttu-id="783f9-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="783f9-153">-TtlInSeconds</span></span>
<span data-ttu-id="783f9-154">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="783f9-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="783f9-155">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="783f9-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="783f9-156">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="783f9-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="783f9-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="783f9-158">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="783f9-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783f9-159">-WhatIf</span></span>
<span data-ttu-id="783f9-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="783f9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783f9-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="783f9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783f9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783f9-162">CommonParameters</span></span>
<span data-ttu-id="783f9-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783f9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783f9-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="783f9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783f9-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="783f9-165">INPUTS</span></span>

### <span data-ttu-id="783f9-166">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="783f9-167">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="783f9-168">Microsoft.Azure.Commands.ВацDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="783f9-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="783f9-169">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="783f9-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="783f9-170">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="783f9-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="783f9-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="783f9-171">OUTPUTS</span></span>

### <span data-ttu-id="783f9-172">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="783f9-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="783f9-173">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="783f9-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="783f9-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="783f9-174">NOTES</span></span>

## <span data-ttu-id="783f9-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="783f9-175">RELATED LINKS</span></span>
