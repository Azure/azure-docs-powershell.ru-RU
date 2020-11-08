---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244205"
---
# <span data-ttu-id="ab27a-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="ab27a-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="ab27a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab27a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab27a-103">Получает граф Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ab27a-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ab27a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab27a-104">SYNTAX</span></span>

### <span data-ttu-id="ab27a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab27a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="ab27a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab27a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab27a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab27a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab27a-108">Командлет **Get-AzCosmosDBGremlinGraph** получает свойства CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="ab27a-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="ab27a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab27a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab27a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab27a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="ab27a-111">Объект Resource включает в себя IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="ab27a-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="ab27a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab27a-112">PARAMETERS</span></span>

### <span data-ttu-id="ab27a-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ab27a-113">-AccountName</span></span>
<span data-ttu-id="ab27a-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ab27a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ab27a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab27a-115">-DatabaseName</span></span>
<span data-ttu-id="ab27a-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ab27a-116">Database name.</span></span>

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

### <span data-ttu-id="ab27a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab27a-117">-DefaultProfile</span></span>
<span data-ttu-id="ab27a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab27a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab27a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab27a-119">-Name</span></span>
<span data-ttu-id="ab27a-120">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ab27a-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="ab27a-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ab27a-121">-ParentObject</span></span>
<span data-ttu-id="ab27a-122">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ab27a-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ab27a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab27a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab27a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab27a-124">Name of resource group.</span></span>

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

### <span data-ttu-id="ab27a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab27a-125">CommonParameters</span></span>
<span data-ttu-id="ab27a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab27a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab27a-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab27a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab27a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab27a-128">INPUTS</span></span>

### <span data-ttu-id="ab27a-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ab27a-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="ab27a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab27a-130">OUTPUTS</span></span>

### <span data-ttu-id="ab27a-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="ab27a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="ab27a-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ab27a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ab27a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab27a-133">NOTES</span></span>

## <span data-ttu-id="ab27a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab27a-134">RELATED LINKS</span></span>
