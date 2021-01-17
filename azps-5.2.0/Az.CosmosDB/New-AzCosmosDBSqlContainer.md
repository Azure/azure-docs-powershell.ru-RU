---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407988"
---
# <span data-ttu-id="7c364-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="7c364-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="7c364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c364-102">SYNOPSIS</span></span>
<span data-ttu-id="7c364-103">Создает новый контейнер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="7c364-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="7c364-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7c364-104">SYNTAX</span></span>

### <span data-ttu-id="7c364-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c364-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c364-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c364-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c364-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c364-107">DESCRIPTION</span></span>
<span data-ttu-id="7c364-108">Создает новый контейнер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="7c364-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="7c364-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7c364-109">EXAMPLES</span></span>

### <span data-ttu-id="7c364-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c364-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="7c364-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c364-111">PARAMETERS</span></span>

### <span data-ttu-id="7c364-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c364-112">-AccountName</span></span>
<span data-ttu-id="7c364-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="7c364-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7c364-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7c364-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7c364-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="7c364-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7c364-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c364-116">-Confirm</span></span>
<span data-ttu-id="7c364-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c364-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c364-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="7c364-119">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c364-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="7c364-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="7c364-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="7c364-121">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="7c364-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="7c364-122">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7c364-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="7c364-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="7c364-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="7c364-124">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="7c364-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="7c364-125">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7c364-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="7c364-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="7c364-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="7c364-127">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="7c364-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="7c364-128">Если они предоставляются вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7c364-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="7c364-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c364-129">-DatabaseName</span></span>
<span data-ttu-id="7c364-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c364-130">Database name.</span></span>

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

### <span data-ttu-id="7c364-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c364-131">-DefaultProfile</span></span>
<span data-ttu-id="7c364-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c364-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c364-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-133">-IndexingPolicy</span></span>
<span data-ttu-id="7c364-134">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="7c364-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="7c364-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7c364-135">-Name</span></span>
<span data-ttu-id="7c364-136">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c364-136">Container name.</span></span>

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

### <span data-ttu-id="7c364-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c364-137">-ParentObject</span></span>
<span data-ttu-id="7c364-138">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="7c364-138">Sql Database object.</span></span>

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

### <span data-ttu-id="7c364-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="7c364-139">-PartitionKeyKind</span></span>
<span data-ttu-id="7c364-140">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="7c364-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="7c364-141">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="7c364-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="7c364-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="7c364-142">-PartitionKeyPath</span></span>
<span data-ttu-id="7c364-143">Путь к разделу, например "/адрес/почтовый индекс".</span><span class="sxs-lookup"><span data-stu-id="7c364-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="7c364-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="7c364-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="7c364-145">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="7c364-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="7c364-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c364-146">-ResourceGroupName</span></span>
<span data-ttu-id="7c364-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c364-147">Name of resource group.</span></span>

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

### <span data-ttu-id="7c364-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7c364-148">-Throughput</span></span>
<span data-ttu-id="7c364-149">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7c364-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7c364-150">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="7c364-150">Default value is 400.</span></span>

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

### <span data-ttu-id="7c364-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c364-151">-TtlInSeconds</span></span>
<span data-ttu-id="7c364-152">Значение ttl по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="7c364-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="7c364-153">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="7c364-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="7c364-154">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="7c364-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="7c364-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="7c364-156">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="7c364-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="7c364-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c364-157">-WhatIf</span></span>
<span data-ttu-id="7c364-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c364-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c364-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7c364-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c364-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c364-160">CommonParameters</span></span>
<span data-ttu-id="7c364-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c364-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c364-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c364-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c364-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c364-163">INPUTS</span></span>

### <span data-ttu-id="7c364-164">Microsoft.Azure.Commands.ВацыDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="7c364-165">Microsoft.Azure.Commands.АsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="7c364-166">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c364-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="7c364-167">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7c364-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="7c364-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c364-168">OUTPUTS</span></span>

### <span data-ttu-id="7c364-169">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7c364-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="7c364-170">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7c364-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7c364-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7c364-171">NOTES</span></span>

## <span data-ttu-id="7c364-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c364-172">RELATED LINKS</span></span>
