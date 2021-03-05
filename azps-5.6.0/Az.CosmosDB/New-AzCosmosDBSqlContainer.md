---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 4fc4bd816511132d5a4fd5d317069e3baf9d9225
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966691"
---
# <span data-ttu-id="62114-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="62114-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="62114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62114-102">SYNOPSIS</span></span>
<span data-ttu-id="62114-103">Создает новый контейнер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="62114-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="62114-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62114-104">SYNTAX</span></span>

### <span data-ttu-id="62114-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62114-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62114-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62114-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62114-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62114-107">DESCRIPTION</span></span>
<span data-ttu-id="62114-108">Создает новый контейнер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="62114-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="62114-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62114-109">EXAMPLES</span></span>

### <span data-ttu-id="62114-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62114-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="62114-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62114-111">PARAMETERS</span></span>

### <span data-ttu-id="62114-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62114-112">-AccountName</span></span>
<span data-ttu-id="62114-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="62114-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="62114-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="62114-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="62114-115">TTL для аналитического хранилища (в секундах).</span><span class="sxs-lookup"><span data-stu-id="62114-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="62114-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="62114-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="62114-117">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="62114-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="62114-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62114-118">-Confirm</span></span>
<span data-ttu-id="62114-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62114-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62114-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="62114-121">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="62114-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="62114-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="62114-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="62114-123">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="62114-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="62114-124">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="62114-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="62114-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="62114-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="62114-126">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="62114-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="62114-127">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="62114-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="62114-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="62114-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="62114-129">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="62114-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="62114-130">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="62114-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="62114-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="62114-131">-DatabaseName</span></span>
<span data-ttu-id="62114-132">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="62114-132">Database name.</span></span>

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

### <span data-ttu-id="62114-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62114-133">-DefaultProfile</span></span>
<span data-ttu-id="62114-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62114-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62114-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-135">-IndexingPolicy</span></span>
<span data-ttu-id="62114-136">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="62114-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="62114-137">-Name</span><span class="sxs-lookup"><span data-stu-id="62114-137">-Name</span></span>
<span data-ttu-id="62114-138">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="62114-138">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62114-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="62114-139">-ParentObject</span></span>
<span data-ttu-id="62114-140">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="62114-140">Sql Database object.</span></span>

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

### <span data-ttu-id="62114-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="62114-141">-PartitionKeyKind</span></span>
<span data-ttu-id="62114-142">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="62114-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="62114-143">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="62114-143">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62114-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="62114-144">-PartitionKeyPath</span></span>
<span data-ttu-id="62114-145">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="62114-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62114-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="62114-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="62114-147">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="62114-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="62114-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62114-148">-ResourceGroupName</span></span>
<span data-ttu-id="62114-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62114-149">Name of resource group.</span></span>

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

### <span data-ttu-id="62114-150">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="62114-150">-Throughput</span></span>
<span data-ttu-id="62114-151">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="62114-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="62114-152">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="62114-152">Default value is 400.</span></span>

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

### <span data-ttu-id="62114-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="62114-153">-TtlInSeconds</span></span>
<span data-ttu-id="62114-154">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="62114-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="62114-155">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="62114-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="62114-156">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="62114-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="62114-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="62114-158">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="62114-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="62114-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62114-159">-WhatIf</span></span>
<span data-ttu-id="62114-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62114-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62114-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62114-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62114-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62114-162">CommonParameters</span></span>
<span data-ttu-id="62114-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62114-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62114-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62114-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62114-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62114-165">INPUTS</span></span>

### <span data-ttu-id="62114-166">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="62114-167">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="62114-168">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="62114-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="62114-169">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="62114-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="62114-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62114-170">OUTPUTS</span></span>

### <span data-ttu-id="62114-171">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="62114-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="62114-172">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="62114-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="62114-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62114-173">NOTES</span></span>

## <span data-ttu-id="62114-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62114-174">RELATED LINKS</span></span>
