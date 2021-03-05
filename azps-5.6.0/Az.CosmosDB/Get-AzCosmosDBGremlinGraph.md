---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983624"
---
# <span data-ttu-id="61527-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="61527-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="61527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61527-102">SYNOPSIS</span></span>
<span data-ttu-id="61527-103">Получает Диаграмму Гремлин (ЕФСDB Гремлин График).</span><span class="sxs-lookup"><span data-stu-id="61527-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="61527-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61527-104">SYNTAX</span></span>

### <span data-ttu-id="61527-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61527-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="61527-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61527-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61527-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61527-107">DESCRIPTION</span></span>
<span data-ttu-id="61527-108">Для этого с помощью **cmdlet Get-AzCosmosDBGremlinGraph** свойства "РегинаDb Гремлин Граф".</span><span class="sxs-lookup"><span data-stu-id="61527-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="61527-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61527-109">EXAMPLES</span></span>

### <span data-ttu-id="61527-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61527-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="61527-111">Объект ресурса содержит поля IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts и _etag.</span><span class="sxs-lookup"><span data-stu-id="61527-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="61527-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61527-112">PARAMETERS</span></span>

### <span data-ttu-id="61527-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61527-113">-AccountName</span></span>
<span data-ttu-id="61527-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="61527-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61527-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61527-115">-DatabaseName</span></span>
<span data-ttu-id="61527-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="61527-116">Database name.</span></span>

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

### <span data-ttu-id="61527-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61527-117">-DefaultProfile</span></span>
<span data-ttu-id="61527-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61527-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61527-119">-Name</span><span class="sxs-lookup"><span data-stu-id="61527-119">-Name</span></span>
<span data-ttu-id="61527-120">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="61527-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="61527-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61527-121">-ParentObject</span></span>
<span data-ttu-id="61527-122">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="61527-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="61527-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61527-123">-ResourceGroupName</span></span>
<span data-ttu-id="61527-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61527-124">Name of resource group.</span></span>

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

### <span data-ttu-id="61527-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61527-125">CommonParameters</span></span>
<span data-ttu-id="61527-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61527-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61527-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61527-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61527-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61527-128">INPUTS</span></span>

### <span data-ttu-id="61527-129">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="61527-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="61527-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61527-130">OUTPUTS</span></span>

### <span data-ttu-id="61527-131">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="61527-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="61527-132">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="61527-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="61527-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61527-133">NOTES</span></span>

## <span data-ttu-id="61527-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61527-134">RELATED LINKS</span></span>
