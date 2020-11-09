---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315038"
---
# <span data-ttu-id="3bb79-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="3bb79-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="3bb79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bb79-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb79-103">Возвращает коллекцию MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3bb79-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3bb79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bb79-104">SYNTAX</span></span>

### <span data-ttu-id="3bb79-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bb79-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="3bb79-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb79-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb79-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb79-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb79-108">Командлет **Get-AzCosmosDBMongoDBCollection** получает коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="3bb79-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3bb79-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bb79-109">EXAMPLES</span></span>

### <span data-ttu-id="3bb79-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3bb79-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="3bb79-111">Объект Resource включает в себя MongoIndexes, _rid _ts, _etag свойств.</span><span class="sxs-lookup"><span data-stu-id="3bb79-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="3bb79-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3bb79-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="3bb79-113">В этом примере получается ShardKey извлеченной коллекции.</span><span class="sxs-lookup"><span data-stu-id="3bb79-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="3bb79-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bb79-114">PARAMETERS</span></span>

### <span data-ttu-id="3bb79-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3bb79-115">-AccountName</span></span>
<span data-ttu-id="3bb79-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3bb79-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3bb79-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bb79-117">-DatabaseName</span></span>
<span data-ttu-id="3bb79-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3bb79-118">Database name.</span></span>

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

### <span data-ttu-id="3bb79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb79-119">-DefaultProfile</span></span>
<span data-ttu-id="3bb79-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb79-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bb79-121">-Name</span></span>
<span data-ttu-id="3bb79-122">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="3bb79-122">Collection name.</span></span>

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

### <span data-ttu-id="3bb79-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3bb79-123">-ParentObject</span></span>
<span data-ttu-id="3bb79-124">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="3bb79-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="3bb79-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb79-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bb79-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bb79-126">Name of resource group.</span></span>

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

### <span data-ttu-id="3bb79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb79-127">CommonParameters</span></span>
<span data-ttu-id="3bb79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bb79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb79-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb79-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bb79-130">INPUTS</span></span>

### <span data-ttu-id="3bb79-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3bb79-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3bb79-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb79-132">OUTPUTS</span></span>

### <span data-ttu-id="3bb79-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="3bb79-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="3bb79-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3bb79-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3bb79-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bb79-135">NOTES</span></span>

## <span data-ttu-id="3bb79-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bb79-136">RELATED LINKS</span></span>