---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519190"
---
# <span data-ttu-id="2269c-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="2269c-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="2269c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2269c-102">SYNOPSIS</span></span>
<span data-ttu-id="2269c-103">Обновляет График Гремлина вНося изменения в СхемуDb.</span><span class="sxs-lookup"><span data-stu-id="2269c-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="2269c-104">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="2269c-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="2269c-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2269c-105">SYNTAX</span></span>

### <span data-ttu-id="2269c-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2269c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2269c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2269c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2269c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2269c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2269c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2269c-109">DESCRIPTION</span></span>
<span data-ttu-id="2269c-110">Обновляет График Гремлина вНося изменения в СхемуDb.</span><span class="sxs-lookup"><span data-stu-id="2269c-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="2269c-111">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="2269c-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="2269c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2269c-112">EXAMPLES</span></span>

### <span data-ttu-id="2269c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2269c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="2269c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2269c-114">PARAMETERS</span></span>

### <span data-ttu-id="2269c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2269c-115">-AccountName</span></span>
<span data-ttu-id="2269c-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="2269c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2269c-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2269c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2269c-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="2269c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2269c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2269c-119">-Confirm</span></span>
<span data-ttu-id="2269c-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2269c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2269c-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="2269c-122">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="2269c-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="2269c-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="2269c-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="2269c-124">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="2269c-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="2269c-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="2269c-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="2269c-126">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="2269c-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="2269c-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="2269c-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="2269c-128">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="2269c-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="2269c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2269c-129">-DatabaseName</span></span>
<span data-ttu-id="2269c-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2269c-130">Database name.</span></span>

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

### <span data-ttu-id="2269c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2269c-131">-DefaultProfile</span></span>
<span data-ttu-id="2269c-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2269c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2269c-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-133">-IndexingPolicy</span></span>
<span data-ttu-id="2269c-134">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="2269c-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="2269c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2269c-135">-InputObject</span></span>
<span data-ttu-id="2269c-136">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="2269c-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="2269c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2269c-137">-Name</span></span>
<span data-ttu-id="2269c-138">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="2269c-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="2269c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2269c-139">-ParentObject</span></span>
<span data-ttu-id="2269c-140">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="2269c-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2269c-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="2269c-141">-PartitionKeyKind</span></span>
<span data-ttu-id="2269c-142">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="2269c-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="2269c-143">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="2269c-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="2269c-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="2269c-144">-PartitionKeyPath</span></span>
<span data-ttu-id="2269c-145">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="2269c-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="2269c-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2269c-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="2269c-147">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="2269c-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="2269c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2269c-148">-ResourceGroupName</span></span>
<span data-ttu-id="2269c-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2269c-149">Name of resource group.</span></span>

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

### <span data-ttu-id="2269c-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="2269c-150">-Throughput</span></span>
<span data-ttu-id="2269c-151">Пропускная способность Гремлин Графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2269c-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="2269c-152">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="2269c-152">Default value is 400.</span></span>

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

### <span data-ttu-id="2269c-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2269c-153">-TtlInSeconds</span></span>
<span data-ttu-id="2269c-154">Значение ttl по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="2269c-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="2269c-155">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="2269c-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2269c-156">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="2269c-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2269c-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="2269c-158">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВапсDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="2269c-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="2269c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2269c-159">-WhatIf</span></span>
<span data-ttu-id="2269c-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2269c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2269c-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2269c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2269c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2269c-162">CommonParameters</span></span>
<span data-ttu-id="2269c-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2269c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2269c-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2269c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2269c-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2269c-165">INPUTS</span></span>

### <span data-ttu-id="2269c-166">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="2269c-167">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="2269c-168">Microsoft.Azure.Commands.ВацDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2269c-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="2269c-169">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2269c-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2269c-170">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="2269c-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="2269c-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2269c-171">OUTPUTS</span></span>

### <span data-ttu-id="2269c-172">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="2269c-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="2269c-173">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2269c-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2269c-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2269c-174">NOTES</span></span>

## <span data-ttu-id="2269c-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2269c-175">RELATED LINKS</span></span>
