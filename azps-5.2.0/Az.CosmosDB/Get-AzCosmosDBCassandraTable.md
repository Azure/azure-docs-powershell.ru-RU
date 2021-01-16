---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396412"
---
# <span data-ttu-id="eb659-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="eb659-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="eb659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb659-102">SYNOPSIS</span></span>
<span data-ttu-id="eb659-103">Получает таблицу Климова " Васильева".</span><span class="sxs-lookup"><span data-stu-id="eb659-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="eb659-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb659-104">SYNTAX</span></span>

### <span data-ttu-id="eb659-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb659-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb659-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb659-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb659-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb659-107">DESCRIPTION</span></span>
<span data-ttu-id="eb659-108">Cmdlet **Get-AzCosmosDBCassandraTable** создает или обновляет существующую клавишную область Кузьмина Кузьмина Вадима.</span><span class="sxs-lookup"><span data-stu-id="eb659-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="eb659-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb659-109">EXAMPLES</span></span>

### <span data-ttu-id="eb659-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb659-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="eb659-111">{{ Get-AzCosmosDBCassandraTable получает свойства существующего пространства ДляРки.</span><span class="sxs-lookup"><span data-stu-id="eb659-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="eb659-112">Вы можете развернуть ресурс, чтобы получить свойства DefaultTtl, Schema, _etag, _ts, _rid.}}</span><span class="sxs-lookup"><span data-stu-id="eb659-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="eb659-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb659-113">PARAMETERS</span></span>

### <span data-ttu-id="eb659-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb659-114">-AccountName</span></span>
<span data-ttu-id="eb659-115">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="eb659-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eb659-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb659-116">-DefaultProfile</span></span>
<span data-ttu-id="eb659-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb659-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb659-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="eb659-118">-KeyspaceName</span></span>
<span data-ttu-id="eb659-119">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="eb659-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="eb659-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eb659-120">-Name</span></span>
<span data-ttu-id="eb659-121">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="eb659-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="eb659-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb659-122">-ParentObject</span></span>
<span data-ttu-id="eb659-123">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="eb659-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb659-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb659-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb659-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb659-125">Name of resource group.</span></span>

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

### <span data-ttu-id="eb659-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb659-126">CommonParameters</span></span>
<span data-ttu-id="eb659-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb659-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb659-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb659-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb659-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb659-129">INPUTS</span></span>

### <span data-ttu-id="eb659-130">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="eb659-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="eb659-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb659-131">OUTPUTS</span></span>

### <span data-ttu-id="eb659-132">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="eb659-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="eb659-133">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="eb659-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="eb659-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb659-134">NOTES</span></span>

## <span data-ttu-id="eb659-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb659-135">RELATED LINKS</span></span>
