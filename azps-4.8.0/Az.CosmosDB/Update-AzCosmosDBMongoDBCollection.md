---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242862"
---
# <span data-ttu-id="aac02-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="aac02-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="aac02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aac02-102">SYNOPSIS</span></span>
<span data-ttu-id="aac02-103">Обновляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="aac02-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="aac02-104">Выполняет операцию исправления на стороне клиента, считывая существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="aac02-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="aac02-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aac02-105">SYNTAX</span></span>

### <span data-ttu-id="aac02-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aac02-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aac02-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aac02-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aac02-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aac02-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aac02-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aac02-109">DESCRIPTION</span></span>
<span data-ttu-id="aac02-110">Обновляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="aac02-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="aac02-111">Выполняет операцию исправления на стороне клиента, считывая существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="aac02-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="aac02-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aac02-112">EXAMPLES</span></span>

### <span data-ttu-id="aac02-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aac02-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="aac02-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aac02-114">PARAMETERS</span></span>

### <span data-ttu-id="aac02-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="aac02-115">-AccountName</span></span>
<span data-ttu-id="aac02-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="aac02-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aac02-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="aac02-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="aac02-118">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="aac02-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="aac02-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="aac02-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="aac02-120">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="aac02-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="aac02-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aac02-121">-Confirm</span></span>
<span data-ttu-id="aac02-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aac02-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac02-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aac02-123">-DatabaseName</span></span>
<span data-ttu-id="aac02-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="aac02-124">Database name.</span></span>

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

### <span data-ttu-id="aac02-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac02-125">-DefaultProfile</span></span>
<span data-ttu-id="aac02-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aac02-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac02-127">-Index</span><span class="sxs-lookup"><span data-stu-id="aac02-127">-Index</span></span>
<span data-ttu-id="aac02-128">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="aac02-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="aac02-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aac02-129">-InputObject</span></span>
<span data-ttu-id="aac02-130">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="aac02-130">Sql Container object.</span></span>

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

### <span data-ttu-id="aac02-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aac02-131">-Name</span></span>
<span data-ttu-id="aac02-132">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="aac02-132">Collection name.</span></span>

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

### <span data-ttu-id="aac02-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aac02-133">-ParentObject</span></span>
<span data-ttu-id="aac02-134">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="aac02-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="aac02-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac02-135">-ResourceGroupName</span></span>
<span data-ttu-id="aac02-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aac02-136">Name of resource group.</span></span>

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

### <span data-ttu-id="aac02-137">-Сегментов</span><span class="sxs-lookup"><span data-stu-id="aac02-137">-Shard</span></span>
<span data-ttu-id="aac02-138">Путь к ключу сегментирования.</span><span class="sxs-lookup"><span data-stu-id="aac02-138">Sharding key path.</span></span>

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

### <span data-ttu-id="aac02-139">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="aac02-139">-Throughput</span></span>
<span data-ttu-id="aac02-140">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="aac02-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="aac02-141">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="aac02-141">Default value is 400.</span></span>

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

### <span data-ttu-id="aac02-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac02-142">-WhatIf</span></span>
<span data-ttu-id="aac02-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aac02-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac02-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aac02-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac02-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac02-145">CommonParameters</span></span>
<span data-ttu-id="aac02-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aac02-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac02-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aac02-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac02-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aac02-148">INPUTS</span></span>

### <span data-ttu-id="aac02-149">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="aac02-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="aac02-150">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="aac02-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="aac02-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aac02-151">OUTPUTS</span></span>

### <span data-ttu-id="aac02-152">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="aac02-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="aac02-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="aac02-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="aac02-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="aac02-154">NOTES</span></span>

## <span data-ttu-id="aac02-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aac02-155">RELATED LINKS</span></span>
