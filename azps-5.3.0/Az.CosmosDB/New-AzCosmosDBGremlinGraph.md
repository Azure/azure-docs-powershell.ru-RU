---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519293"
---
# <span data-ttu-id="a7548-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="a7548-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="a7548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7548-102">SYNOPSIS</span></span>
<span data-ttu-id="a7548-103">Создает новый Диаграмма Гремлин (Graph) с помощью функции "ПеретаблицыDB".</span><span class="sxs-lookup"><span data-stu-id="a7548-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="a7548-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7548-104">SYNTAX</span></span>

### <span data-ttu-id="a7548-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7548-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7548-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7548-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7548-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7548-107">DESCRIPTION</span></span>
<span data-ttu-id="a7548-108">Создает новый Диаграмма Гремлин (Graph) с помощью функции "ПеретаблицыDB".</span><span class="sxs-lookup"><span data-stu-id="a7548-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="a7548-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7548-109">EXAMPLES</span></span>

### <span data-ttu-id="a7548-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7548-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="a7548-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7548-111">PARAMETERS</span></span>

### <span data-ttu-id="a7548-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7548-112">-AccountName</span></span>
<span data-ttu-id="a7548-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="a7548-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a7548-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a7548-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a7548-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="a7548-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a7548-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7548-116">-Confirm</span></span>
<span data-ttu-id="a7548-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7548-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7548-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a7548-119">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, если этот объект имеет тип ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="a7548-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="a7548-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="a7548-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="a7548-121">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="a7548-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="a7548-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="a7548-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="a7548-123">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="a7548-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="a7548-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="a7548-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="a7548-125">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="a7548-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="a7548-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7548-126">-DatabaseName</span></span>
<span data-ttu-id="a7548-127">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7548-127">Database name.</span></span>

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

### <span data-ttu-id="a7548-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7548-128">-DefaultProfile</span></span>
<span data-ttu-id="a7548-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7548-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7548-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-130">-IndexingPolicy</span></span>
<span data-ttu-id="a7548-131">Объект политики индексации типа Microsoft.Azure.Commands.JonessDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a7548-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="a7548-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a7548-132">-Name</span></span>
<span data-ttu-id="a7548-133">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="a7548-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="a7548-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7548-134">-ParentObject</span></span>
<span data-ttu-id="a7548-135">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="a7548-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="a7548-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="a7548-136">-PartitionKeyKind</span></span>
<span data-ttu-id="a7548-137">Тип алгоритма, используемого для разных разделов.</span><span class="sxs-lookup"><span data-stu-id="a7548-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="a7548-138">Возможные значения: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="a7548-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="a7548-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="a7548-139">-PartitionKeyPath</span></span>
<span data-ttu-id="a7548-140">Путь к разделу, например"/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="a7548-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="a7548-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="a7548-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="a7548-142">Версия определения ключа раздела раздела</span><span class="sxs-lookup"><span data-stu-id="a7548-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="a7548-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7548-143">-ResourceGroupName</span></span>
<span data-ttu-id="a7548-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7548-144">Name of resource group.</span></span>

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

### <span data-ttu-id="a7548-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="a7548-145">-Throughput</span></span>
<span data-ttu-id="a7548-146">Пропускная способность Гремлин Графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a7548-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="a7548-147">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="a7548-147">Default value is 400.</span></span>

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

### <span data-ttu-id="a7548-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a7548-148">-TtlInSeconds</span></span>
<span data-ttu-id="a7548-149">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a7548-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="a7548-150">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="a7548-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="a7548-151">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="a7548-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="a7548-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="a7548-153">Объект UniqueKeyPolicy типа Microsoft.Azure.Commands.ВацыDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a7548-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="a7548-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7548-154">-WhatIf</span></span>
<span data-ttu-id="a7548-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7548-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7548-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7548-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7548-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7548-157">CommonParameters</span></span>
<span data-ttu-id="a7548-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7548-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7548-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7548-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7548-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7548-160">INPUTS</span></span>

### <span data-ttu-id="a7548-161">Microsoft.Azure.Commands.ВацыDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="a7548-162">Microsoft.Azure.Commands.АsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="a7548-163">Microsoft.Azure.Commands.ВацDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7548-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="a7548-164">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a7548-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="a7548-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7548-165">OUTPUTS</span></span>

### <span data-ttu-id="a7548-166">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="a7548-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="a7548-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a7548-167">System.Exception</span></span>

## <span data-ttu-id="a7548-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7548-168">NOTES</span></span>

## <span data-ttu-id="a7548-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7548-169">RELATED LINKS</span></span>
