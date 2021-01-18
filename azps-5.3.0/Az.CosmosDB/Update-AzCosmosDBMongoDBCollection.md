---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519186"
---
# <span data-ttu-id="35079-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="35079-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="35079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35079-102">SYNOPSIS</span></span>
<span data-ttu-id="35079-103">Обновляет коллекцию "ГрадыDB" в MongoDB.</span><span class="sxs-lookup"><span data-stu-id="35079-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="35079-104">Выполняет обновление на стороне клиента, считыв существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="35079-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="35079-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35079-105">SYNTAX</span></span>

### <span data-ttu-id="35079-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35079-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35079-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35079-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35079-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35079-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35079-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35079-109">DESCRIPTION</span></span>
<span data-ttu-id="35079-110">Обновляет коллекцию "ГрадыDB" в MongoDB.</span><span class="sxs-lookup"><span data-stu-id="35079-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="35079-111">Выполняет обновление на стороне клиента, считыв существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="35079-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="35079-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35079-112">EXAMPLES</span></span>

### <span data-ttu-id="35079-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35079-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="35079-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35079-114">PARAMETERS</span></span>

### <span data-ttu-id="35079-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35079-115">-AccountName</span></span>
<span data-ttu-id="35079-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="35079-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="35079-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="35079-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="35079-118">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="35079-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="35079-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="35079-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="35079-120">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="35079-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="35079-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35079-121">-Confirm</span></span>
<span data-ttu-id="35079-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="35079-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35079-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35079-123">-DatabaseName</span></span>
<span data-ttu-id="35079-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="35079-124">Database name.</span></span>

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

### <span data-ttu-id="35079-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35079-125">-DefaultProfile</span></span>
<span data-ttu-id="35079-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35079-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35079-127">-Index</span><span class="sxs-lookup"><span data-stu-id="35079-127">-Index</span></span>
<span data-ttu-id="35079-128">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="35079-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="35079-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35079-129">-InputObject</span></span>
<span data-ttu-id="35079-130">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="35079-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35079-131">-Name</span><span class="sxs-lookup"><span data-stu-id="35079-131">-Name</span></span>
<span data-ttu-id="35079-132">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="35079-132">Collection name.</span></span>

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

### <span data-ttu-id="35079-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="35079-133">-ParentObject</span></span>
<span data-ttu-id="35079-134">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="35079-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="35079-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35079-135">-ResourceGroupName</span></span>
<span data-ttu-id="35079-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35079-136">Name of resource group.</span></span>

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

### <span data-ttu-id="35079-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="35079-137">-Shard</span></span>
<span data-ttu-id="35079-138">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="35079-138">Sharding key path.</span></span>

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

### <span data-ttu-id="35079-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="35079-139">-Throughput</span></span>
<span data-ttu-id="35079-140">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="35079-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="35079-141">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="35079-141">Default value is 400.</span></span>

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

### <span data-ttu-id="35079-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35079-142">-WhatIf</span></span>
<span data-ttu-id="35079-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35079-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35079-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35079-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35079-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35079-145">CommonParameters</span></span>
<span data-ttu-id="35079-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35079-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35079-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35079-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35079-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35079-148">INPUTS</span></span>

### <span data-ttu-id="35079-149">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="35079-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="35079-150">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="35079-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="35079-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35079-151">OUTPUTS</span></span>

### <span data-ttu-id="35079-152">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="35079-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="35079-153">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="35079-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="35079-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35079-154">NOTES</span></span>

## <span data-ttu-id="35079-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35079-155">RELATED LINKS</span></span>
