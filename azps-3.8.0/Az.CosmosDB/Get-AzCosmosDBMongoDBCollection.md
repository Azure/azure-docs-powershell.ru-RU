---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074120"
---
# <span data-ttu-id="718f3-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="718f3-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="718f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="718f3-102">SYNOPSIS</span></span>
<span data-ttu-id="718f3-103">Возвращает коллекцию MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="718f3-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="718f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="718f3-104">SYNTAX</span></span>

### <span data-ttu-id="718f3-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="718f3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="718f3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="718f3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="718f3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="718f3-107">DESCRIPTION</span></span>
<span data-ttu-id="718f3-108">Командлет **Get-AzCosmosDBMongoDBCollection** получает коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="718f3-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="718f3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="718f3-109">EXAMPLES</span></span>

### <span data-ttu-id="718f3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="718f3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="718f3-111">Объект Resource включает в себя MongoIndexes, _rid _ts, _etag свойств.</span><span class="sxs-lookup"><span data-stu-id="718f3-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="718f3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="718f3-112">PARAMETERS</span></span>

### <span data-ttu-id="718f3-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="718f3-113">-AccountName</span></span>
<span data-ttu-id="718f3-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="718f3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="718f3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="718f3-115">-DatabaseName</span></span>
<span data-ttu-id="718f3-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="718f3-116">Database name.</span></span>

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

### <span data-ttu-id="718f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718f3-117">-DefaultProfile</span></span>
<span data-ttu-id="718f3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="718f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718f3-119">-Подробно</span><span class="sxs-lookup"><span data-stu-id="718f3-119">-Detailed</span></span>
<span data-ttu-id="718f3-120">Если он указан, командлет возвращает коллекцию с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="718f3-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="718f3-121">-InputObject</span></span>
<span data-ttu-id="718f3-122">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="718f3-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="718f3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="718f3-123">-Name</span></span>
<span data-ttu-id="718f3-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="718f3-124">Collection name.</span></span>

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

### <span data-ttu-id="718f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="718f3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="718f3-126">Name of resource group.</span></span>

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

### <span data-ttu-id="718f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718f3-127">CommonParameters</span></span>
<span data-ttu-id="718f3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="718f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718f3-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="718f3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718f3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="718f3-130">INPUTS</span></span>

### <span data-ttu-id="718f3-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="718f3-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="718f3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="718f3-132">OUTPUTS</span></span>

### <span data-ttu-id="718f3-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="718f3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="718f3-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="718f3-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="718f3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="718f3-135">NOTES</span></span>

## <span data-ttu-id="718f3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="718f3-136">RELATED LINKS</span></span>
