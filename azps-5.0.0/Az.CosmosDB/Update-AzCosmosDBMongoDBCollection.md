---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314537"
---
# <span data-ttu-id="f1244-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="f1244-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="f1244-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1244-102">SYNOPSIS</span></span>
<span data-ttu-id="f1244-103">Обновляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f1244-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f1244-104">Выполняет операцию исправления на стороне клиента, считывая существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f1244-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f1244-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1244-105">SYNTAX</span></span>

### <span data-ttu-id="f1244-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1244-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1244-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1244-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1244-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1244-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1244-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1244-109">DESCRIPTION</span></span>
<span data-ttu-id="f1244-110">Обновляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f1244-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f1244-111">Выполняет операцию исправления на стороне клиента, считывая существующую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f1244-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f1244-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1244-112">EXAMPLES</span></span>

### <span data-ttu-id="f1244-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1244-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="f1244-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1244-114">PARAMETERS</span></span>

### <span data-ttu-id="f1244-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f1244-115">-AccountName</span></span>
<span data-ttu-id="f1244-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f1244-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f1244-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f1244-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f1244-118">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="f1244-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="f1244-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f1244-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f1244-120">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="f1244-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f1244-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1244-121">-Confirm</span></span>
<span data-ttu-id="f1244-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1244-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1244-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1244-123">-DatabaseName</span></span>
<span data-ttu-id="f1244-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f1244-124">Database name.</span></span>

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

### <span data-ttu-id="f1244-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1244-125">-DefaultProfile</span></span>
<span data-ttu-id="f1244-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1244-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1244-127">-Index</span><span class="sxs-lookup"><span data-stu-id="f1244-127">-Index</span></span>
<span data-ttu-id="f1244-128">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="f1244-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="f1244-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1244-129">-InputObject</span></span>
<span data-ttu-id="f1244-130">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="f1244-130">Sql Container object.</span></span>

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

### <span data-ttu-id="f1244-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1244-131">-Name</span></span>
<span data-ttu-id="f1244-132">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="f1244-132">Collection name.</span></span>

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

### <span data-ttu-id="f1244-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f1244-133">-ParentObject</span></span>
<span data-ttu-id="f1244-134">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="f1244-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="f1244-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1244-135">-ResourceGroupName</span></span>
<span data-ttu-id="f1244-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1244-136">Name of resource group.</span></span>

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

### <span data-ttu-id="f1244-137">-Сегментов</span><span class="sxs-lookup"><span data-stu-id="f1244-137">-Shard</span></span>
<span data-ttu-id="f1244-138">Путь к ключу сегментирования.</span><span class="sxs-lookup"><span data-stu-id="f1244-138">Sharding key path.</span></span>

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

### <span data-ttu-id="f1244-139">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="f1244-139">-Throughput</span></span>
<span data-ttu-id="f1244-140">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f1244-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f1244-141">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="f1244-141">Default value is 400.</span></span>

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

### <span data-ttu-id="f1244-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1244-142">-WhatIf</span></span>
<span data-ttu-id="f1244-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1244-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1244-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1244-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1244-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1244-145">CommonParameters</span></span>
<span data-ttu-id="f1244-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1244-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1244-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1244-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1244-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1244-148">INPUTS</span></span>

### <span data-ttu-id="f1244-149">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f1244-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="f1244-150">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f1244-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="f1244-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1244-151">OUTPUTS</span></span>

### <span data-ttu-id="f1244-152">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f1244-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="f1244-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f1244-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f1244-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1244-154">NOTES</span></span>

## <span data-ttu-id="f1244-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1244-155">RELATED LINKS</span></span>
