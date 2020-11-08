---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074437"
---
# <span data-ttu-id="9ef26-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="9ef26-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="9ef26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ef26-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef26-103">Задает коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9ef26-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9ef26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ef26-104">SYNTAX</span></span>

### <span data-ttu-id="9ef26-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ef26-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef26-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef26-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef26-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef26-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef26-108">Командлет **Set-AzCosmosDBMongoDBCollection** задает коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9ef26-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9ef26-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ef26-109">EXAMPLES</span></span>

### <span data-ttu-id="9ef26-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ef26-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="9ef26-111">Объект Resource включает в себя MongoIndexes, _rid _ts, _etag свойств.</span><span class="sxs-lookup"><span data-stu-id="9ef26-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="9ef26-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ef26-112">PARAMETERS</span></span>

### <span data-ttu-id="9ef26-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9ef26-113">-AccountName</span></span>
<span data-ttu-id="9ef26-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9ef26-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9ef26-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ef26-115">-Confirm</span></span>
<span data-ttu-id="9ef26-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ef26-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef26-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ef26-117">-DatabaseName</span></span>
<span data-ttu-id="9ef26-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ef26-118">Database name.</span></span>

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

### <span data-ttu-id="9ef26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef26-119">-DefaultProfile</span></span>
<span data-ttu-id="9ef26-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef26-121">-Index</span><span class="sxs-lookup"><span data-stu-id="9ef26-121">-Index</span></span>
<span data-ttu-id="9ef26-122">Массив объектов PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="9ef26-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="9ef26-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef26-123">-InputObject</span></span>
<span data-ttu-id="9ef26-124">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="9ef26-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="9ef26-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ef26-125">-Name</span></span>
<span data-ttu-id="9ef26-126">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="9ef26-126">Collection name.</span></span>

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

### <span data-ttu-id="9ef26-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef26-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ef26-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ef26-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9ef26-129">-Сегментов</span><span class="sxs-lookup"><span data-stu-id="9ef26-129">-Shard</span></span>
<span data-ttu-id="9ef26-130">Путь к ключу сегментирования.</span><span class="sxs-lookup"><span data-stu-id="9ef26-130">Sharding key path.</span></span>

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

### <span data-ttu-id="9ef26-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="9ef26-131">-Throughput</span></span>
<span data-ttu-id="9ef26-132">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9ef26-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="9ef26-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9ef26-133">Default value is 400.</span></span>

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

### <span data-ttu-id="9ef26-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef26-134">-WhatIf</span></span>
<span data-ttu-id="9ef26-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ef26-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef26-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ef26-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef26-137">CommonParameters</span></span>
<span data-ttu-id="9ef26-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ef26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef26-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ef26-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef26-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ef26-140">INPUTS</span></span>

### <span data-ttu-id="9ef26-141">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9ef26-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="9ef26-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef26-142">OUTPUTS</span></span>

### <span data-ttu-id="9ef26-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="9ef26-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="9ef26-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ef26-144">NOTES</span></span>

## <span data-ttu-id="9ef26-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ef26-145">RELATED LINKS</span></span>
