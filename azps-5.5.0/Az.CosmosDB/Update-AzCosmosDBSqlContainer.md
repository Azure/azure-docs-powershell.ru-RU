---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 60bbe085aaaa65c65ba33839db5f02ae5198e155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215308"
---
# <span data-ttu-id="c2620-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c2620-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c2620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2620-102">SYNOPSIS</span></span>
<span data-ttu-id="c2620-103">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="c2620-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c2620-104">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="c2620-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c2620-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2620-105">SYNTAX</span></span>

### <span data-ttu-id="c2620-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2620-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2620-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2620-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2620-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2620-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2620-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2620-109">DESCRIPTION</span></span>
<span data-ttu-id="c2620-110">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="c2620-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c2620-111">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="c2620-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c2620-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2620-112">EXAMPLES</span></span>

### <span data-ttu-id="c2620-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2620-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="c2620-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2620-114">PARAMETERS</span></span>

### <span data-ttu-id="c2620-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2620-115">-AccountName</span></span>
<span data-ttu-id="c2620-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="c2620-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2620-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="c2620-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="c2620-118">TTL для аналитического хранилища (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c2620-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="c2620-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c2620-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c2620-120">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="c2620-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c2620-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2620-121">-Confirm</span></span>
<span data-ttu-id="c2620-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2620-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2620-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c2620-124">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="c2620-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2620-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c2620-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c2620-126">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="c2620-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="c2620-127">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2620-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2620-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c2620-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c2620-129">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="c2620-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="c2620-130">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2620-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2620-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c2620-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c2620-132">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="c2620-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="c2620-133">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2620-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2620-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2620-134">-DatabaseName</span></span>
<span data-ttu-id="c2620-135">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2620-135">Database name.</span></span>

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

### <span data-ttu-id="c2620-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2620-136">-DefaultProfile</span></span>
<span data-ttu-id="c2620-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2620-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2620-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-138">-IndexingPolicy</span></span>
<span data-ttu-id="c2620-139">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2620-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2620-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2620-140">-InputObject</span></span>
<span data-ttu-id="c2620-141">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="c2620-141">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2620-142">-Name</span><span class="sxs-lookup"><span data-stu-id="c2620-142">-Name</span></span>
<span data-ttu-id="c2620-143">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c2620-143">Container name.</span></span>

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

### <span data-ttu-id="c2620-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2620-144">-ParentObject</span></span>
<span data-ttu-id="c2620-145">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="c2620-145">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2620-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c2620-146">-PartitionKeyKind</span></span>
<span data-ttu-id="c2620-147">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="c2620-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c2620-148">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="c2620-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c2620-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c2620-149">-PartitionKeyPath</span></span>
<span data-ttu-id="c2620-150">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="c2620-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c2620-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c2620-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="c2620-152">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="c2620-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c2620-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2620-153">-ResourceGroupName</span></span>
<span data-ttu-id="c2620-154">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2620-154">Name of resource group.</span></span>

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

### <span data-ttu-id="c2620-155">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="c2620-155">-Throughput</span></span>
<span data-ttu-id="c2620-156">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c2620-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c2620-157">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="c2620-157">Default value is 400.</span></span>

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

### <span data-ttu-id="c2620-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c2620-158">-TtlInSeconds</span></span>
<span data-ttu-id="c2620-159">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c2620-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="c2620-160">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="c2620-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c2620-161">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c2620-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c2620-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c2620-163">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2620-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2620-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2620-164">-WhatIf</span></span>
<span data-ttu-id="c2620-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2620-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2620-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2620-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2620-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2620-167">CommonParameters</span></span>
<span data-ttu-id="c2620-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2620-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2620-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2620-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2620-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2620-170">INPUTS</span></span>

### <span data-ttu-id="c2620-171">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="c2620-172">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="c2620-173">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2620-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="c2620-174">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2620-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2620-175">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="c2620-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="c2620-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2620-176">OUTPUTS</span></span>

### <span data-ttu-id="c2620-177">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2620-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2620-178">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c2620-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c2620-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2620-179">NOTES</span></span>

## <span data-ttu-id="c2620-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2620-180">RELATED LINKS</span></span>
