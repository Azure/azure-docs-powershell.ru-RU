---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078373"
---
# <span data-ttu-id="141c4-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="141c4-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="141c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="141c4-102">SYNOPSIS</span></span>
<span data-ttu-id="141c4-103">Создает новый контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="141c4-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="141c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="141c4-104">SYNTAX</span></span>

### <span data-ttu-id="141c4-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="141c4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141c4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="141c4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="141c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="141c4-107">DESCRIPTION</span></span>
<span data-ttu-id="141c4-108">Создает новый контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="141c4-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="141c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="141c4-109">EXAMPLES</span></span>

### <span data-ttu-id="141c4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="141c4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="141c4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="141c4-111">PARAMETERS</span></span>

### <span data-ttu-id="141c4-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="141c4-112">-AccountName</span></span>
<span data-ttu-id="141c4-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="141c4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="141c4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="141c4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="141c4-115">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="141c4-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="141c4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="141c4-116">-Confirm</span></span>
<span data-ttu-id="141c4-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="141c4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="141c4-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="141c4-119">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="141c4-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="141c4-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="141c4-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="141c4-121">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="141c4-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="141c4-122">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="141c4-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="141c4-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="141c4-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="141c4-124">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="141c4-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="141c4-125">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="141c4-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="141c4-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="141c4-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="141c4-127">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="141c4-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="141c4-128">Если он указан вместе с параметром ConflictResolutionPolicy, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="141c4-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="141c4-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="141c4-129">-DatabaseName</span></span>
<span data-ttu-id="141c4-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="141c4-130">Database name.</span></span>

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

### <span data-ttu-id="141c4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141c4-131">-DefaultProfile</span></span>
<span data-ttu-id="141c4-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="141c4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141c4-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-133">-IndexingPolicy</span></span>
<span data-ttu-id="141c4-134">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="141c4-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="141c4-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="141c4-135">-Name</span></span>
<span data-ttu-id="141c4-136">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="141c4-136">Container name.</span></span>

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

### <span data-ttu-id="141c4-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="141c4-137">-ParentObject</span></span>
<span data-ttu-id="141c4-138">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="141c4-138">Sql Database object.</span></span>

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

### <span data-ttu-id="141c4-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="141c4-139">-PartitionKeyKind</span></span>
<span data-ttu-id="141c4-140">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="141c4-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="141c4-141">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="141c4-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="141c4-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="141c4-142">-PartitionKeyPath</span></span>
<span data-ttu-id="141c4-143">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="141c4-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="141c4-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="141c4-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="141c4-145">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="141c4-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="141c4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141c4-146">-ResourceGroupName</span></span>
<span data-ttu-id="141c4-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="141c4-147">Name of resource group.</span></span>

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

### <span data-ttu-id="141c4-148">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="141c4-148">-Throughput</span></span>
<span data-ttu-id="141c4-149">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="141c4-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="141c4-150">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="141c4-150">Default value is 400.</span></span>

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

### <span data-ttu-id="141c4-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="141c4-151">-TtlInSeconds</span></span>
<span data-ttu-id="141c4-152">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="141c4-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="141c4-153">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="141c4-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="141c4-154">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="141c4-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="141c4-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="141c4-156">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="141c4-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="141c4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141c4-157">-WhatIf</span></span>
<span data-ttu-id="141c4-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="141c4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141c4-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="141c4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="141c4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141c4-160">CommonParameters</span></span>
<span data-ttu-id="141c4-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="141c4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141c4-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="141c4-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141c4-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="141c4-163">INPUTS</span></span>

### <span data-ttu-id="141c4-164">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="141c4-165">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="141c4-166">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="141c4-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="141c4-167">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="141c4-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="141c4-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="141c4-168">OUTPUTS</span></span>

### <span data-ttu-id="141c4-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="141c4-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="141c4-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="141c4-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="141c4-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="141c4-171">NOTES</span></span>

## <span data-ttu-id="141c4-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="141c4-172">RELATED LINKS</span></span>