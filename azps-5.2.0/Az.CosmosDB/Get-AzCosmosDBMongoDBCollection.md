---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392908"
---
# <span data-ttu-id="533e0-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="533e0-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="533e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="533e0-102">SYNOPSIS</span></span>
<span data-ttu-id="533e0-103">Получает коллекцию "ГрадыDB " MongoDB".</span><span class="sxs-lookup"><span data-stu-id="533e0-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="533e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="533e0-104">SYNTAX</span></span>

### <span data-ttu-id="533e0-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="533e0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="533e0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="533e0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="533e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="533e0-107">DESCRIPTION</span></span>
<span data-ttu-id="533e0-108">Cmdlet **Get-AzCosmosDBMongoDBCollection** получает коллекцию "ЕгоsDB MongoDB".</span><span class="sxs-lookup"><span data-stu-id="533e0-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="533e0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="533e0-109">EXAMPLES</span></span>

### <span data-ttu-id="533e0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="533e0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="533e0-111">Объект ресурса содержит свойства MongoIndexes, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="533e0-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="533e0-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="533e0-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="533e0-113">В этом примере возвращается ShardKey из извлеченной коллекции.</span><span class="sxs-lookup"><span data-stu-id="533e0-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="533e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="533e0-114">PARAMETERS</span></span>

### <span data-ttu-id="533e0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="533e0-115">-AccountName</span></span>
<span data-ttu-id="533e0-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="533e0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="533e0-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="533e0-117">-DatabaseName</span></span>
<span data-ttu-id="533e0-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="533e0-118">Database name.</span></span>

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

### <span data-ttu-id="533e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533e0-119">-DefaultProfile</span></span>
<span data-ttu-id="533e0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="533e0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="533e0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="533e0-121">-Name</span></span>
<span data-ttu-id="533e0-122">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="533e0-122">Collection name.</span></span>

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

### <span data-ttu-id="533e0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="533e0-123">-ParentObject</span></span>
<span data-ttu-id="533e0-124">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="533e0-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="533e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="533e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="533e0-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="533e0-126">Name of resource group.</span></span>

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

### <span data-ttu-id="533e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533e0-127">CommonParameters</span></span>
<span data-ttu-id="533e0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="533e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533e0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="533e0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533e0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="533e0-130">INPUTS</span></span>

### <span data-ttu-id="533e0-131">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="533e0-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="533e0-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="533e0-132">OUTPUTS</span></span>

### <span data-ttu-id="533e0-133">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="533e0-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="533e0-134">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="533e0-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="533e0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="533e0-135">NOTES</span></span>

## <span data-ttu-id="533e0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="533e0-136">RELATED LINKS</span></span>
