---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245074"
---
# <span data-ttu-id="9c368-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="9c368-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="9c368-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c368-102">SYNOPSIS</span></span>
<span data-ttu-id="9c368-103">Обновляет контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9c368-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="9c368-104">Выполняет операцию исправления на стороне клиента, считывая существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="9c368-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="9c368-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c368-105">SYNTAX</span></span>

### <span data-ttu-id="9c368-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c368-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c368-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c368-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c368-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c368-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c368-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c368-109">DESCRIPTION</span></span>
<span data-ttu-id="9c368-110">Обновляет контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9c368-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="9c368-111">Выполняет операцию исправления на стороне клиента, считывая существующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="9c368-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="9c368-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c368-112">EXAMPLES</span></span>

### <span data-ttu-id="9c368-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c368-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="9c368-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c368-114">PARAMETERS</span></span>

### <span data-ttu-id="9c368-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9c368-115">-AccountName</span></span>
<span data-ttu-id="9c368-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9c368-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c368-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9c368-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9c368-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="9c368-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9c368-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c368-119">-Confirm</span></span>
<span data-ttu-id="9c368-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c368-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c368-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="9c368-122">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="9c368-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="9c368-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="9c368-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="9c368-124">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="9c368-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="9c368-125">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9c368-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="9c368-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="9c368-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="9c368-127">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="9c368-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="9c368-128">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9c368-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="9c368-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="9c368-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="9c368-130">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="9c368-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="9c368-131">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9c368-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="9c368-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c368-132">-DatabaseName</span></span>
<span data-ttu-id="9c368-133">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c368-133">Database name.</span></span>

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

### <span data-ttu-id="9c368-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c368-134">-DefaultProfile</span></span>
<span data-ttu-id="9c368-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c368-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c368-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-136">-IndexingPolicy</span></span>
<span data-ttu-id="9c368-137">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9c368-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="9c368-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c368-138">-InputObject</span></span>
<span data-ttu-id="9c368-139">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="9c368-139">Sql Container object.</span></span>

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

### <span data-ttu-id="9c368-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c368-140">-Name</span></span>
<span data-ttu-id="9c368-141">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="9c368-141">Container name.</span></span>

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

### <span data-ttu-id="9c368-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c368-142">-ParentObject</span></span>
<span data-ttu-id="9c368-143">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9c368-143">Sql Database object.</span></span>

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

### <span data-ttu-id="9c368-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="9c368-144">-PartitionKeyKind</span></span>
<span data-ttu-id="9c368-145">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="9c368-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="9c368-146">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="9c368-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="9c368-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="9c368-147">-PartitionKeyPath</span></span>
<span data-ttu-id="9c368-148">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="9c368-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="9c368-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="9c368-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="9c368-150">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="9c368-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="9c368-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c368-151">-ResourceGroupName</span></span>
<span data-ttu-id="9c368-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c368-152">Name of resource group.</span></span>

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

### <span data-ttu-id="9c368-153">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="9c368-153">-Throughput</span></span>
<span data-ttu-id="9c368-154">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9c368-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="9c368-155">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9c368-155">Default value is 400.</span></span>

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

### <span data-ttu-id="9c368-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="9c368-156">-TtlInSeconds</span></span>
<span data-ttu-id="9c368-157">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="9c368-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="9c368-158">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="9c368-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="9c368-159">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="9c368-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="9c368-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="9c368-161">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="9c368-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="9c368-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c368-162">-WhatIf</span></span>
<span data-ttu-id="9c368-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c368-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c368-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c368-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c368-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c368-165">CommonParameters</span></span>
<span data-ttu-id="9c368-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c368-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c368-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c368-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c368-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c368-168">INPUTS</span></span>

### <span data-ttu-id="9c368-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="9c368-170">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="9c368-171">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c368-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="9c368-172">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9c368-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9c368-173">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="9c368-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="9c368-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c368-174">OUTPUTS</span></span>

### <span data-ttu-id="9c368-175">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9c368-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9c368-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9c368-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9c368-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c368-177">NOTES</span></span>

## <span data-ttu-id="9c368-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c368-178">RELATED LINKS</span></span>
