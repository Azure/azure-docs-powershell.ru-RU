---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417471"
---
# <span data-ttu-id="af93b-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="af93b-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="af93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af93b-102">SYNOPSIS</span></span>
<span data-ttu-id="af93b-103">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="af93b-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="af93b-104">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="af93b-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="af93b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af93b-105">SYNTAX</span></span>

### <span data-ttu-id="af93b-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af93b-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af93b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af93b-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af93b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af93b-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af93b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af93b-109">DESCRIPTION</span></span>
<span data-ttu-id="af93b-110">Обновляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="af93b-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="af93b-111">Выполняет обновление на стороне клиента, считыв существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="af93b-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="af93b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af93b-112">EXAMPLES</span></span>

### <span data-ttu-id="af93b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af93b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="af93b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af93b-114">PARAMETERS</span></span>

### <span data-ttu-id="af93b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af93b-115">-AccountName</span></span>
<span data-ttu-id="af93b-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="af93b-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af93b-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="af93b-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="af93b-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="af93b-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="af93b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af93b-119">-Confirm</span></span>
<span data-ttu-id="af93b-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af93b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af93b-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="af93b-122">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="af93b-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="af93b-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="af93b-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="af93b-124">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="af93b-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="af93b-125">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="af93b-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="af93b-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="af93b-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="af93b-127">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="af93b-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="af93b-128">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="af93b-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="af93b-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="af93b-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="af93b-130">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="af93b-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="af93b-131">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="af93b-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="af93b-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af93b-132">-DatabaseName</span></span>
<span data-ttu-id="af93b-133">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="af93b-133">Database name.</span></span>

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

### <span data-ttu-id="af93b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af93b-134">-DefaultProfile</span></span>
<span data-ttu-id="af93b-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af93b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af93b-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-136">-IndexingPolicy</span></span>
<span data-ttu-id="af93b-137">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="af93b-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="af93b-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af93b-138">-InputObject</span></span>
<span data-ttu-id="af93b-139">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="af93b-139">Sql Container object.</span></span>

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

### <span data-ttu-id="af93b-140">-Name</span><span class="sxs-lookup"><span data-stu-id="af93b-140">-Name</span></span>
<span data-ttu-id="af93b-141">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="af93b-141">Container name.</span></span>

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

### <span data-ttu-id="af93b-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af93b-142">-ParentObject</span></span>
<span data-ttu-id="af93b-143">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="af93b-143">Sql Database object.</span></span>

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

### <span data-ttu-id="af93b-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="af93b-144">-PartitionKeyKind</span></span>
<span data-ttu-id="af93b-145">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="af93b-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="af93b-146">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="af93b-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="af93b-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="af93b-147">-PartitionKeyPath</span></span>
<span data-ttu-id="af93b-148">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="af93b-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="af93b-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="af93b-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="af93b-150">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="af93b-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="af93b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af93b-151">-ResourceGroupName</span></span>
<span data-ttu-id="af93b-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af93b-152">Name of resource group.</span></span>

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

### <span data-ttu-id="af93b-153">-Throughput</span><span class="sxs-lookup"><span data-stu-id="af93b-153">-Throughput</span></span>
<span data-ttu-id="af93b-154">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="af93b-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="af93b-155">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="af93b-155">Default value is 400.</span></span>

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

### <span data-ttu-id="af93b-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="af93b-156">-TtlInSeconds</span></span>
<span data-ttu-id="af93b-157">Значение ttl по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="af93b-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="af93b-158">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="af93b-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="af93b-159">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="af93b-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="af93b-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="af93b-161">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="af93b-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="af93b-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af93b-162">-WhatIf</span></span>
<span data-ttu-id="af93b-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af93b-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af93b-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af93b-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af93b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af93b-165">CommonParameters</span></span>
<span data-ttu-id="af93b-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af93b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af93b-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af93b-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af93b-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af93b-168">INPUTS</span></span>

### <span data-ttu-id="af93b-169">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="af93b-170">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="af93b-171">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="af93b-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="af93b-172">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="af93b-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="af93b-173">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="af93b-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="af93b-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af93b-174">OUTPUTS</span></span>

### <span data-ttu-id="af93b-175">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="af93b-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="af93b-176">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="af93b-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="af93b-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af93b-177">NOTES</span></span>

## <span data-ttu-id="af93b-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af93b-178">RELATED LINKS</span></span>
