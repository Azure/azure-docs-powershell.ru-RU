---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519369"
---
# <span data-ttu-id="57e3e-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="57e3e-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="57e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="57e3e-103">Получает таблицу Климова Климова.</span><span class="sxs-lookup"><span data-stu-id="57e3e-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="57e3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57e3e-104">SYNTAX</span></span>

### <span data-ttu-id="57e3e-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57e3e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e3e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57e3e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e3e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="57e3e-108">Cmdlet **Get-AzCosmosDBCassandraTable** создает или обновляет существующую клавишную область Кузьмина Кузьмина Вадима.</span><span class="sxs-lookup"><span data-stu-id="57e3e-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="57e3e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57e3e-109">EXAMPLES</span></span>

### <span data-ttu-id="57e3e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57e3e-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="57e3e-111">{{ Get-AzCosmosDBCassandraTable получает свойства существующего пространства ДляРки.</span><span class="sxs-lookup"><span data-stu-id="57e3e-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="57e3e-112">Вы можете развернуть ресурс, чтобы получить свойства DefaultTtl, Schema, _etag, _ts, _rid.}}</span><span class="sxs-lookup"><span data-stu-id="57e3e-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="57e3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57e3e-113">PARAMETERS</span></span>

### <span data-ttu-id="57e3e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57e3e-114">-AccountName</span></span>
<span data-ttu-id="57e3e-115">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="57e3e-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57e3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e3e-116">-DefaultProfile</span></span>
<span data-ttu-id="57e3e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57e3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e3e-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="57e3e-118">-KeyspaceName</span></span>
<span data-ttu-id="57e3e-119">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="57e3e-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="57e3e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57e3e-120">-Name</span></span>
<span data-ttu-id="57e3e-121">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="57e3e-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="57e3e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57e3e-122">-ParentObject</span></span>
<span data-ttu-id="57e3e-123">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="57e3e-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="57e3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="57e3e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57e3e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="57e3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e3e-126">CommonParameters</span></span>
<span data-ttu-id="57e3e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e3e-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e3e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57e3e-129">INPUTS</span></span>

### <span data-ttu-id="57e3e-130">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="57e3e-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="57e3e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57e3e-131">OUTPUTS</span></span>

### <span data-ttu-id="57e3e-132">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="57e3e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="57e3e-133">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="57e3e-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="57e3e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57e3e-134">NOTES</span></span>

## <span data-ttu-id="57e3e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57e3e-135">RELATED LINKS</span></span>
