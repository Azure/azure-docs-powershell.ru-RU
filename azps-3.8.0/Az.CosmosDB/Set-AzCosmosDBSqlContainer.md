---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074425"
---
# <span data-ttu-id="c8351-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c8351-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c8351-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8351-102">SYNOPSIS</span></span>
<span data-ttu-id="c8351-103">Создает новый или обновляет существующий контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c8351-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c8351-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8351-104">SYNTAX</span></span>

### <span data-ttu-id="c8351-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8351-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8351-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8351-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8351-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8351-107">DESCRIPTION</span></span>
<span data-ttu-id="c8351-108">Командлет **Set-AzCosmosDBSqlContainer** создает новый или обновляет существующий контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c8351-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c8351-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8351-109">EXAMPLES</span></span>

### <span data-ttu-id="c8351-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8351-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="c8351-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8351-111">PARAMETERS</span></span>

### <span data-ttu-id="c8351-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="c8351-112">-AccountName</span></span>
<span data-ttu-id="c8351-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c8351-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c8351-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8351-114">-Confirm</span></span>
<span data-ttu-id="c8351-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8351-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8351-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8351-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c8351-117">Объект ConflictResolutionPolicy типа PSSqlConflictResolutionPolicy, когда он указан, задается в качестве ConflictResolutionPolicy контейнера.</span><span class="sxs-lookup"><span data-stu-id="c8351-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="c8351-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c8351-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c8351-119">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="c8351-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="c8351-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c8351-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c8351-121">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="c8351-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="c8351-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c8351-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c8351-123">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="c8351-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="c8351-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8351-124">-DatabaseName</span></span>
<span data-ttu-id="c8351-125">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c8351-125">Database name.</span></span>

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

### <span data-ttu-id="c8351-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8351-126">-DefaultProfile</span></span>
<span data-ttu-id="c8351-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8351-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8351-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c8351-128">-IndexingPolicy</span></span>
<span data-ttu-id="c8351-129">Объект политики индексирования типа Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c8351-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="c8351-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8351-130">-InputObject</span></span>
<span data-ttu-id="c8351-131">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="c8351-131">Sql Database object.</span></span>

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

### <span data-ttu-id="c8351-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8351-132">-Name</span></span>
<span data-ttu-id="c8351-133">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c8351-133">Container name.</span></span>

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

### <span data-ttu-id="c8351-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c8351-134">-PartitionKeyKind</span></span>
<span data-ttu-id="c8351-135">Алгоритм, используемый для секционирования.</span><span class="sxs-lookup"><span data-stu-id="c8351-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c8351-136">Возможные значения: "хэш", "диапазон"</span><span class="sxs-lookup"><span data-stu-id="c8351-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c8351-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c8351-137">-PartitionKeyPath</span></span>
<span data-ttu-id="c8351-138">Путь к ключу раздела, например "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="c8351-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c8351-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c8351-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="c8351-140">Версия определения ключа раздела.</span><span class="sxs-lookup"><span data-stu-id="c8351-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c8351-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8351-141">-ResourceGroupName</span></span>
<span data-ttu-id="c8351-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8351-142">Name of resource group.</span></span>

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

### <span data-ttu-id="c8351-143">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="c8351-143">-Throughput</span></span>
<span data-ttu-id="c8351-144">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c8351-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c8351-145">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="c8351-145">Default value is 400.</span></span>

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

### <span data-ttu-id="c8351-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c8351-146">-TtlInSeconds</span></span>
<span data-ttu-id="c8351-147">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c8351-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="c8351-148">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="c8351-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c8351-149">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c8351-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c8351-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c8351-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c8351-151">Объект UniqueKeyPolicy типа Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c8351-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="c8351-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8351-152">-WhatIf</span></span>
<span data-ttu-id="c8351-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8351-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8351-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8351-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8351-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8351-155">CommonParameters</span></span>
<span data-ttu-id="c8351-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8351-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8351-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8351-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8351-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8351-158">INPUTS</span></span>

### <span data-ttu-id="c8351-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8351-159">None</span></span>

## <span data-ttu-id="c8351-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8351-160">OUTPUTS</span></span>

### <span data-ttu-id="c8351-161">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c8351-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="c8351-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8351-162">NOTES</span></span>

## <span data-ttu-id="c8351-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8351-163">RELATED LINKS</span></span>
