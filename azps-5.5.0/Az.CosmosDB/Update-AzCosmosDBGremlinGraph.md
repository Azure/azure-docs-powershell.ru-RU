---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215332"
---
# <span data-ttu-id="1d83f-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1d83f-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1d83f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d83f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d83f-103">Обновляет Диаграмму Гремлин (Graph) ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="1d83f-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="1d83f-104">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="1d83f-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="1d83f-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d83f-105">SYNTAX</span></span>

### <span data-ttu-id="1d83f-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d83f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d83f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d83f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d83f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d83f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d83f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d83f-109">DESCRIPTION</span></span>
<span data-ttu-id="1d83f-110">Обновляет Диаграмму Гремлин (Graph) ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="1d83f-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="1d83f-111">Выполняет клиентскую операцию исправления на стороне клиента, читая существующий Graph.</span><span class="sxs-lookup"><span data-stu-id="1d83f-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="1d83f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d83f-112">EXAMPLES</span></span>

### <span data-ttu-id="1d83f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d83f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="1d83f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d83f-114">PARAMETERS</span></span>

### <span data-ttu-id="1d83f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d83f-115">-AccountName</span></span>
<span data-ttu-id="1d83f-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="1d83f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d83f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1d83f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1d83f-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="1d83f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1d83f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d83f-119">-Confirm</span></span>
<span data-ttu-id="1d83f-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d83f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d83f-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="1d83f-122">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="1d83f-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="1d83f-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="1d83f-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="1d83f-124">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="1d83f-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1d83f-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="1d83f-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="1d83f-126">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="1d83f-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1d83f-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="1d83f-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="1d83f-128">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="1d83f-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1d83f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d83f-129">-DatabaseName</span></span>
<span data-ttu-id="1d83f-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1d83f-130">Database name.</span></span>

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

### <span data-ttu-id="1d83f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d83f-131">-DefaultProfile</span></span>
<span data-ttu-id="1d83f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d83f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d83f-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-133">-IndexingPolicy</span></span>
<span data-ttu-id="1d83f-134">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1d83f-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="1d83f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d83f-135">-InputObject</span></span>
<span data-ttu-id="1d83f-136">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="1d83f-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1d83f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="1d83f-137">-Name</span></span>
<span data-ttu-id="1d83f-138">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="1d83f-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1d83f-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d83f-139">-ParentObject</span></span>
<span data-ttu-id="1d83f-140">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="1d83f-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="1d83f-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="1d83f-141">-PartitionKeyKind</span></span>
<span data-ttu-id="1d83f-142">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="1d83f-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="1d83f-143">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="1d83f-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="1d83f-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="1d83f-144">-PartitionKeyPath</span></span>
<span data-ttu-id="1d83f-145">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="1d83f-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="1d83f-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1d83f-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="1d83f-147">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="1d83f-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="1d83f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d83f-148">-ResourceGroupName</span></span>
<span data-ttu-id="1d83f-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d83f-149">Name of resource group.</span></span>

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

### <span data-ttu-id="1d83f-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1d83f-150">-Throughput</span></span>
<span data-ttu-id="1d83f-151">Пропускная способность Гремлин Графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1d83f-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="1d83f-152">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="1d83f-152">Default value is 400.</span></span>

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

### <span data-ttu-id="1d83f-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d83f-153">-TtlInSeconds</span></span>
<span data-ttu-id="1d83f-154">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1d83f-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="1d83f-155">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="1d83f-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="1d83f-156">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="1d83f-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="1d83f-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="1d83f-158">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВапсDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="1d83f-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="1d83f-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d83f-159">-WhatIf</span></span>
<span data-ttu-id="1d83f-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d83f-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d83f-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d83f-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d83f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d83f-162">CommonParameters</span></span>
<span data-ttu-id="1d83f-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d83f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d83f-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d83f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d83f-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d83f-165">INPUTS</span></span>

### <span data-ttu-id="1d83f-166">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="1d83f-167">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="1d83f-168">Microsoft.Azure.Commands.АsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d83f-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="1d83f-169">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1d83f-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="1d83f-170">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d83f-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1d83f-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d83f-171">OUTPUTS</span></span>

### <span data-ttu-id="1d83f-172">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d83f-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="1d83f-173">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1d83f-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1d83f-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d83f-174">NOTES</span></span>

## <span data-ttu-id="1d83f-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d83f-175">RELATED LINKS</span></span>
