---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314840"
---
# <span data-ttu-id="1f978-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1f978-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1f978-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f978-102">SYNOPSIS</span></span>
<span data-ttu-id="1f978-103">Создание нового графа CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1f978-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1f978-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f978-104">SYNTAX</span></span>

### <span data-ttu-id="1f978-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f978-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f978-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f978-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f978-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f978-107">DESCRIPTION</span></span>
<span data-ttu-id="1f978-108">Создание нового графа CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1f978-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1f978-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f978-109">EXAMPLES</span></span>

### <span data-ttu-id="1f978-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f978-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="1f978-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f978-111">PARAMETERS</span></span>

### <span data-ttu-id="1f978-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="1f978-112">-AccountName</span></span>
<span data-ttu-id="1f978-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1f978-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1f978-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1f978-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1f978-115">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="1f978-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1f978-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f978-116">-Confirm</span></span>
<span data-ttu-id="1f978-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f978-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f978-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="1f978-119">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="1f978-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="1f978-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="1f978-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="1f978-121">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="1f978-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1f978-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="1f978-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="1f978-123">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="1f978-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1f978-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="1f978-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="1f978-125">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="1f978-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1f978-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f978-126">-DatabaseName</span></span>
<span data-ttu-id="1f978-127">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1f978-127">Database name.</span></span>

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

### <span data-ttu-id="1f978-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f978-128">-DefaultProfile</span></span>
<span data-ttu-id="1f978-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f978-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f978-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-130">-IndexingPolicy</span></span>
<span data-ttu-id="1f978-131">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1f978-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="1f978-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f978-132">-Name</span></span>
<span data-ttu-id="1f978-133">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1f978-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1f978-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1f978-134">-ParentObject</span></span>
<span data-ttu-id="1f978-135">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1f978-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="1f978-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="1f978-136">-PartitionKeyKind</span></span>
<span data-ttu-id="1f978-137">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="1f978-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="1f978-138">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="1f978-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="1f978-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="1f978-139">-PartitionKeyPath</span></span>
<span data-ttu-id="1f978-140">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="1f978-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="1f978-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1f978-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="1f978-142">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="1f978-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="1f978-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f978-143">-ResourceGroupName</span></span>
<span data-ttu-id="1f978-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f978-144">Name of resource group.</span></span>

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

### <span data-ttu-id="1f978-145">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="1f978-145">-Throughput</span></span>
<span data-ttu-id="1f978-146">Пропускная способность Gremlin графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1f978-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="1f978-147">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="1f978-147">Default value is 400.</span></span>

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

### <span data-ttu-id="1f978-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="1f978-148">-TtlInSeconds</span></span>
<span data-ttu-id="1f978-149">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1f978-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="1f978-150">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="1f978-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="1f978-151">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="1f978-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="1f978-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="1f978-153">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="1f978-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="1f978-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f978-154">-WhatIf</span></span>
<span data-ttu-id="1f978-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f978-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f978-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f978-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f978-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f978-157">CommonParameters</span></span>
<span data-ttu-id="1f978-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f978-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f978-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f978-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f978-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f978-160">INPUTS</span></span>

### <span data-ttu-id="1f978-161">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="1f978-162">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="1f978-163">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f978-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="1f978-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1f978-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="1f978-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f978-165">OUTPUTS</span></span>

### <span data-ttu-id="1f978-166">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1f978-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="1f978-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1f978-167">System.Exception</span></span>

## <span data-ttu-id="1f978-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f978-168">NOTES</span></span>

## <span data-ttu-id="1f978-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f978-169">RELATED LINKS</span></span>
