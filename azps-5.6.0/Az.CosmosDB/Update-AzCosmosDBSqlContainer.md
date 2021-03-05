---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977267"
---
# <span data-ttu-id="c2f91-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c2f91-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c2f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f91-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f91-103">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="c2f91-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c2f91-104">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="c2f91-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c2f91-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2f91-105">SYNTAX</span></span>

### <span data-ttu-id="c2f91-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2f91-106">ByNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="c2f91-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f91-107">ByParentObjectParameterSet</span></span>
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

### <span data-ttu-id="c2f91-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f91-108">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="c2f91-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2f91-109">DESCRIPTION</span></span>
<span data-ttu-id="c2f91-110">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="c2f91-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c2f91-111">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="c2f91-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c2f91-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2f91-112">EXAMPLES</span></span>

### <span data-ttu-id="c2f91-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2f91-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="c2f91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2f91-114">PARAMETERS</span></span>

### <span data-ttu-id="c2f91-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2f91-115">-AccountName</span></span>
<span data-ttu-id="c2f91-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="c2f91-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2f91-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="c2f91-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="c2f91-118">TTL для аналитического хранилища (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c2f91-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="c2f91-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c2f91-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c2f91-120">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="c2f91-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c2f91-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2f91-121">-Confirm</span></span>
<span data-ttu-id="c2f91-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2f91-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f91-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c2f91-124">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="c2f91-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="c2f91-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c2f91-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c2f91-126">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="c2f91-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="c2f91-127">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2f91-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2f91-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c2f91-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c2f91-129">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="c2f91-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="c2f91-130">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2f91-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2f91-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c2f91-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c2f91-132">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="c2f91-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="c2f91-133">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2f91-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2f91-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2f91-134">-DatabaseName</span></span>
<span data-ttu-id="c2f91-135">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2f91-135">Database name.</span></span>

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

### <span data-ttu-id="c2f91-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f91-136">-DefaultProfile</span></span>
<span data-ttu-id="c2f91-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f91-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f91-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-138">-IndexingPolicy</span></span>
<span data-ttu-id="c2f91-139">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2f91-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="c2f91-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f91-140">-InputObject</span></span>
<span data-ttu-id="c2f91-141">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="c2f91-141">Sql Container object.</span></span>

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

### <span data-ttu-id="c2f91-142">-Name</span><span class="sxs-lookup"><span data-stu-id="c2f91-142">-Name</span></span>
<span data-ttu-id="c2f91-143">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c2f91-143">Container name.</span></span>

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

### <span data-ttu-id="c2f91-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2f91-144">-ParentObject</span></span>
<span data-ttu-id="c2f91-145">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="c2f91-145">Sql Database object.</span></span>

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

### <span data-ttu-id="c2f91-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c2f91-146">-PartitionKeyKind</span></span>
<span data-ttu-id="c2f91-147">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="c2f91-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c2f91-148">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="c2f91-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c2f91-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c2f91-149">-PartitionKeyPath</span></span>
<span data-ttu-id="c2f91-150">Путь к разделу, например"/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="c2f91-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c2f91-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c2f91-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="c2f91-152">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="c2f91-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c2f91-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f91-153">-ResourceGroupName</span></span>
<span data-ttu-id="c2f91-154">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2f91-154">Name of resource group.</span></span>

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

### <span data-ttu-id="c2f91-155">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c2f91-155">-Throughput</span></span>
<span data-ttu-id="c2f91-156">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c2f91-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c2f91-157">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="c2f91-157">Default value is 400.</span></span>

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

### <span data-ttu-id="c2f91-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c2f91-158">-TtlInSeconds</span></span>
<span data-ttu-id="c2f91-159">Значение ttl по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c2f91-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="c2f91-160">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="c2f91-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c2f91-161">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c2f91-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c2f91-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c2f91-163">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2f91-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="c2f91-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f91-164">-WhatIf</span></span>
<span data-ttu-id="c2f91-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f91-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f91-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2f91-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f91-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f91-167">CommonParameters</span></span>
<span data-ttu-id="c2f91-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f91-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f91-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2f91-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f91-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2f91-170">INPUTS</span></span>

### <span data-ttu-id="c2f91-171">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="c2f91-172">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="c2f91-173">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2f91-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="c2f91-174">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2f91-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2f91-175">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="c2f91-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="c2f91-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2f91-176">OUTPUTS</span></span>

### <span data-ttu-id="c2f91-177">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2f91-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2f91-178">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c2f91-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c2f91-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2f91-179">NOTES</span></span>

## <span data-ttu-id="c2f91-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2f91-180">RELATED LINKS</span></span>
