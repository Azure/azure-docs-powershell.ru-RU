---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074438"
---
# <span data-ttu-id="5aafa-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="5aafa-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="5aafa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5aafa-102">SYNOPSIS</span></span>
<span data-ttu-id="5aafa-103">Задает граф CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5aafa-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5aafa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5aafa-104">SYNTAX</span></span>

### <span data-ttu-id="5aafa-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5aafa-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aafa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aafa-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aafa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aafa-107">DESCRIPTION</span></span>
<span data-ttu-id="5aafa-108">Командлет **Set-AzCosmosDBGremlinGraph** задает CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="5aafa-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5aafa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5aafa-109">EXAMPLES</span></span>

### <span data-ttu-id="5aafa-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5aafa-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="5aafa-111">Объект Resource включает в себя IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="5aafa-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="5aafa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5aafa-112">PARAMETERS</span></span>

### <span data-ttu-id="5aafa-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5aafa-113">-AccountName</span></span>
<span data-ttu-id="5aafa-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5aafa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5aafa-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aafa-115">-Confirm</span></span>
<span data-ttu-id="5aafa-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5aafa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aafa-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5aafa-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="5aafa-118">Объект ConflictResolutionPolicy типа PSConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="5aafa-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="5aafa-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="5aafa-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="5aafa-120">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="5aafa-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="5aafa-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="5aafa-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="5aafa-122">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="5aafa-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="5aafa-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="5aafa-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="5aafa-124">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="5aafa-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="5aafa-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5aafa-125">-DatabaseName</span></span>
<span data-ttu-id="5aafa-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5aafa-126">Database name.</span></span>

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

### <span data-ttu-id="5aafa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aafa-127">-DefaultProfile</span></span>
<span data-ttu-id="5aafa-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5aafa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aafa-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5aafa-129">-IndexingPolicy</span></span>
<span data-ttu-id="5aafa-130">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="5aafa-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="5aafa-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aafa-131">-InputObject</span></span>
<span data-ttu-id="5aafa-132">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5aafa-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5aafa-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5aafa-133">-Name</span></span>
<span data-ttu-id="5aafa-134">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5aafa-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5aafa-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="5aafa-135">-PartitionKeyKind</span></span>
<span data-ttu-id="5aafa-136">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="5aafa-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="5aafa-137">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="5aafa-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="5aafa-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="5aafa-138">-PartitionKeyPath</span></span>
<span data-ttu-id="5aafa-139">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="5aafa-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="5aafa-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5aafa-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="5aafa-141">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="5aafa-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="5aafa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aafa-142">-ResourceGroupName</span></span>
<span data-ttu-id="5aafa-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5aafa-143">Name of resource group.</span></span>

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

### <span data-ttu-id="5aafa-144">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="5aafa-144">-Throughput</span></span>
<span data-ttu-id="5aafa-145">Пропускная способность Gremlin графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5aafa-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5aafa-146">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="5aafa-146">Default value is 400.</span></span>

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

### <span data-ttu-id="5aafa-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5aafa-147">-TtlInSeconds</span></span>
<span data-ttu-id="5aafa-148">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5aafa-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="5aafa-149">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="5aafa-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5aafa-150">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="5aafa-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5aafa-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5aafa-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="5aafa-152">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="5aafa-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="5aafa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aafa-153">-WhatIf</span></span>
<span data-ttu-id="5aafa-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5aafa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aafa-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5aafa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aafa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aafa-156">CommonParameters</span></span>
<span data-ttu-id="5aafa-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5aafa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aafa-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aafa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aafa-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5aafa-159">INPUTS</span></span>

### <span data-ttu-id="5aafa-160">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5aafa-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="5aafa-161">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5aafa-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="5aafa-162">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5aafa-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5aafa-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aafa-163">OUTPUTS</span></span>

### <span data-ttu-id="5aafa-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="5aafa-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="5aafa-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="5aafa-165">NOTES</span></span>

## <span data-ttu-id="5aafa-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5aafa-166">RELATED LINKS</span></span>
