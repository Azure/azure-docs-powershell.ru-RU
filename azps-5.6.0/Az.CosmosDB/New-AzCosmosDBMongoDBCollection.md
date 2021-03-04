---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954771"
---
# <span data-ttu-id="55233-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="55233-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="55233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55233-102">SYNOPSIS</span></span>
<span data-ttu-id="55233-103">Создает коллекцию "ДискиDB " MongoDB".</span><span class="sxs-lookup"><span data-stu-id="55233-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="55233-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55233-104">SYNTAX</span></span>

### <span data-ttu-id="55233-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55233-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55233-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55233-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55233-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55233-107">DESCRIPTION</span></span>
<span data-ttu-id="55233-108">Создает коллекцию "ДискиDB " MongoDB".</span><span class="sxs-lookup"><span data-stu-id="55233-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="55233-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55233-109">EXAMPLES</span></span>

### <span data-ttu-id="55233-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55233-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="55233-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55233-111">PARAMETERS</span></span>

### <span data-ttu-id="55233-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55233-112">-AccountName</span></span>
<span data-ttu-id="55233-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="55233-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55233-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="55233-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="55233-115">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="55233-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="55233-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="55233-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="55233-117">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="55233-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="55233-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55233-118">-Confirm</span></span>
<span data-ttu-id="55233-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55233-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55233-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55233-120">-DatabaseName</span></span>
<span data-ttu-id="55233-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="55233-121">Database name.</span></span>

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

### <span data-ttu-id="55233-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55233-122">-DefaultProfile</span></span>
<span data-ttu-id="55233-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55233-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55233-124">-Index</span><span class="sxs-lookup"><span data-stu-id="55233-124">-Index</span></span>
<span data-ttu-id="55233-125">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="55233-125">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55233-126">-Name</span><span class="sxs-lookup"><span data-stu-id="55233-126">-Name</span></span>
<span data-ttu-id="55233-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="55233-127">Collection name.</span></span>

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

### <span data-ttu-id="55233-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55233-128">-ParentObject</span></span>
<span data-ttu-id="55233-129">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="55233-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55233-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55233-130">-ResourceGroupName</span></span>
<span data-ttu-id="55233-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55233-131">Name of resource group.</span></span>

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

### <span data-ttu-id="55233-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="55233-132">-Shard</span></span>
<span data-ttu-id="55233-133">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="55233-133">Sharding key path.</span></span>

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

### <span data-ttu-id="55233-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="55233-134">-Throughput</span></span>
<span data-ttu-id="55233-135">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="55233-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="55233-136">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="55233-136">Default value is 400.</span></span>

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

### <span data-ttu-id="55233-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55233-137">-WhatIf</span></span>
<span data-ttu-id="55233-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55233-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55233-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="55233-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55233-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55233-140">CommonParameters</span></span>
<span data-ttu-id="55233-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55233-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55233-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55233-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55233-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55233-143">INPUTS</span></span>

### <span data-ttu-id="55233-144">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="55233-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="55233-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55233-145">OUTPUTS</span></span>

### <span data-ttu-id="55233-146">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="55233-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="55233-147">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="55233-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="55233-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55233-148">NOTES</span></span>

## <span data-ttu-id="55233-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55233-149">RELATED LINKS</span></span>
