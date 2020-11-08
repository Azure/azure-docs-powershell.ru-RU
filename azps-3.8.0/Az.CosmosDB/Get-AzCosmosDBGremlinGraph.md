---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074122"
---
# <span data-ttu-id="6603b-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="6603b-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="6603b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6603b-102">SYNOPSIS</span></span>
<span data-ttu-id="6603b-103">Получает граф Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6603b-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6603b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6603b-104">SYNTAX</span></span>

### <span data-ttu-id="6603b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6603b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="6603b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6603b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6603b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6603b-107">DESCRIPTION</span></span>
<span data-ttu-id="6603b-108">Командлет **Get-AzCosmosDBGremlinGraph** получает свойства CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="6603b-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="6603b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6603b-109">EXAMPLES</span></span>

### <span data-ttu-id="6603b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6603b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="6603b-111">Объект Resource включает в себя IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="6603b-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="6603b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6603b-112">PARAMETERS</span></span>

### <span data-ttu-id="6603b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6603b-113">-AccountName</span></span>
<span data-ttu-id="6603b-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6603b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6603b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6603b-115">-DatabaseName</span></span>
<span data-ttu-id="6603b-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6603b-116">Database name.</span></span>

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

### <span data-ttu-id="6603b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6603b-117">-DefaultProfile</span></span>
<span data-ttu-id="6603b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6603b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6603b-119">-Подробно</span><span class="sxs-lookup"><span data-stu-id="6603b-119">-Detailed</span></span>
<span data-ttu-id="6603b-120">Если он указан, командлет возвращает граф Gremlin с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="6603b-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="6603b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6603b-121">-InputObject</span></span>
<span data-ttu-id="6603b-122">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6603b-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6603b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6603b-123">-Name</span></span>
<span data-ttu-id="6603b-124">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6603b-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6603b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6603b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6603b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6603b-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6603b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6603b-127">CommonParameters</span></span>
<span data-ttu-id="6603b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6603b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6603b-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6603b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6603b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6603b-130">INPUTS</span></span>

### <span data-ttu-id="6603b-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6603b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="6603b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6603b-132">OUTPUTS</span></span>

### <span data-ttu-id="6603b-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6603b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="6603b-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6603b-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6603b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6603b-135">NOTES</span></span>

## <span data-ttu-id="6603b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6603b-136">RELATED LINKS</span></span>
