---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244629"
---
# <span data-ttu-id="ebd4d-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="ebd4d-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="ebd4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd4d-103">Создает новую коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ebd4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebd4d-104">SYNTAX</span></span>

### <span data-ttu-id="ebd4d-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebd4d-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebd4d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebd4d-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebd4d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebd4d-107">DESCRIPTION</span></span>
<span data-ttu-id="ebd4d-108">Создает новую коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ebd4d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebd4d-109">EXAMPLES</span></span>

### <span data-ttu-id="ebd4d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebd4d-110">Example 1</span></span>
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

## <span data-ttu-id="ebd4d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebd4d-111">PARAMETERS</span></span>

### <span data-ttu-id="ebd4d-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ebd4d-112">-AccountName</span></span>
<span data-ttu-id="ebd4d-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ebd4d-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ebd4d-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ebd4d-115">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="ebd4d-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ebd4d-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ebd4d-117">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ebd4d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebd4d-118">-Confirm</span></span>
<span data-ttu-id="ebd4d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebd4d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebd4d-120">-DatabaseName</span></span>
<span data-ttu-id="ebd4d-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-121">Database name.</span></span>

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

### <span data-ttu-id="ebd4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd4d-122">-DefaultProfile</span></span>
<span data-ttu-id="ebd4d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd4d-124">-Index</span><span class="sxs-lookup"><span data-stu-id="ebd4d-124">-Index</span></span>
<span data-ttu-id="ebd4d-125">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="ebd4d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebd4d-126">-Name</span></span>
<span data-ttu-id="ebd4d-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-127">Collection name.</span></span>

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

### <span data-ttu-id="ebd4d-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ebd4d-128">-ParentObject</span></span>
<span data-ttu-id="ebd4d-129">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="ebd4d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd4d-130">-ResourceGroupName</span></span>
<span data-ttu-id="ebd4d-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-131">Name of resource group.</span></span>

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

### <span data-ttu-id="ebd4d-132">-Сегментов</span><span class="sxs-lookup"><span data-stu-id="ebd4d-132">-Shard</span></span>
<span data-ttu-id="ebd4d-133">Путь к ключу сегментирования.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-133">Sharding key path.</span></span>

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

### <span data-ttu-id="ebd4d-134">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="ebd4d-134">-Throughput</span></span>
<span data-ttu-id="ebd4d-135">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ebd4d-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="ebd4d-136">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-136">Default value is 400.</span></span>

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

### <span data-ttu-id="ebd4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebd4d-137">-WhatIf</span></span>
<span data-ttu-id="ebd4d-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebd4d-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebd4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd4d-140">CommonParameters</span></span>
<span data-ttu-id="ebd4d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd4d-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebd4d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd4d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebd4d-143">INPUTS</span></span>

### <span data-ttu-id="ebd4d-144">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ebd4d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="ebd4d-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebd4d-145">OUTPUTS</span></span>

### <span data-ttu-id="ebd4d-146">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="ebd4d-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="ebd4d-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ebd4d-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ebd4d-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebd4d-148">NOTES</span></span>

## <span data-ttu-id="ebd4d-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebd4d-149">RELATED LINKS</span></span>
