---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245077"
---
# <span data-ttu-id="487a5-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="487a5-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="487a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="487a5-102">SYNOPSIS</span></span>
<span data-ttu-id="487a5-103">Обновляет CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="487a5-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="487a5-104">Выполняет операцию исправления на стороне клиента, считывая существующий граф.</span><span class="sxs-lookup"><span data-stu-id="487a5-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="487a5-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="487a5-105">SYNTAX</span></span>

### <span data-ttu-id="487a5-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="487a5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="487a5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="487a5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="487a5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="487a5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="487a5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="487a5-109">DESCRIPTION</span></span>
<span data-ttu-id="487a5-110">Обновляет CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="487a5-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="487a5-111">Выполняет операцию исправления на стороне клиента, считывая существующий граф.</span><span class="sxs-lookup"><span data-stu-id="487a5-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="487a5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="487a5-112">EXAMPLES</span></span>

### <span data-ttu-id="487a5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="487a5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="487a5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="487a5-114">PARAMETERS</span></span>

### <span data-ttu-id="487a5-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="487a5-115">-AccountName</span></span>
<span data-ttu-id="487a5-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="487a5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="487a5-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="487a5-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="487a5-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="487a5-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="487a5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="487a5-119">-Confirm</span></span>
<span data-ttu-id="487a5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="487a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="487a5-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="487a5-122">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="487a5-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="487a5-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="487a5-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="487a5-124">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="487a5-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="487a5-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="487a5-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="487a5-126">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="487a5-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="487a5-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="487a5-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="487a5-128">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="487a5-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="487a5-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="487a5-129">-DatabaseName</span></span>
<span data-ttu-id="487a5-130">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="487a5-130">Database name.</span></span>

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

### <span data-ttu-id="487a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="487a5-131">-DefaultProfile</span></span>
<span data-ttu-id="487a5-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="487a5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="487a5-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-133">-IndexingPolicy</span></span>
<span data-ttu-id="487a5-134">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="487a5-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="487a5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="487a5-135">-InputObject</span></span>
<span data-ttu-id="487a5-136">Объект Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="487a5-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="487a5-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="487a5-137">-Name</span></span>
<span data-ttu-id="487a5-138">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="487a5-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="487a5-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="487a5-139">-ParentObject</span></span>
<span data-ttu-id="487a5-140">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="487a5-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="487a5-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="487a5-141">-PartitionKeyKind</span></span>
<span data-ttu-id="487a5-142">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="487a5-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="487a5-143">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="487a5-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="487a5-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="487a5-144">-PartitionKeyPath</span></span>
<span data-ttu-id="487a5-145">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="487a5-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="487a5-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="487a5-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="487a5-147">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="487a5-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="487a5-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="487a5-148">-ResourceGroupName</span></span>
<span data-ttu-id="487a5-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="487a5-149">Name of resource group.</span></span>

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

### <span data-ttu-id="487a5-150">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="487a5-150">-Throughput</span></span>
<span data-ttu-id="487a5-151">Пропускная способность Gremlin графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="487a5-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="487a5-152">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="487a5-152">Default value is 400.</span></span>

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

### <span data-ttu-id="487a5-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="487a5-153">-TtlInSeconds</span></span>
<span data-ttu-id="487a5-154">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="487a5-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="487a5-155">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="487a5-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="487a5-156">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="487a5-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="487a5-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="487a5-158">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="487a5-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="487a5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="487a5-159">-WhatIf</span></span>
<span data-ttu-id="487a5-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="487a5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="487a5-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="487a5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="487a5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487a5-162">CommonParameters</span></span>
<span data-ttu-id="487a5-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="487a5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487a5-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="487a5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487a5-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="487a5-165">INPUTS</span></span>

### <span data-ttu-id="487a5-166">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="487a5-167">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="487a5-168">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="487a5-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="487a5-169">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="487a5-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="487a5-170">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="487a5-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="487a5-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="487a5-171">OUTPUTS</span></span>

### <span data-ttu-id="487a5-172">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="487a5-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="487a5-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="487a5-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="487a5-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="487a5-174">NOTES</span></span>

## <span data-ttu-id="487a5-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="487a5-175">RELATED LINKS</span></span>
