---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519373"
---
# <span data-ttu-id="65b0c-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="65b0c-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="65b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="65b0c-103">Получает ключ "КрасаВ", Климова и Климова.</span><span class="sxs-lookup"><span data-stu-id="65b0c-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="65b0c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65b0c-104">SYNTAX</span></span>

### <span data-ttu-id="65b0c-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65b0c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65b0c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b0c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="65b0c-108">Для создания нового или обновления существующей клавишной области Вадима Кузьмина в **AzCosmosDBCassandraKeyspace.**</span><span class="sxs-lookup"><span data-stu-id="65b0c-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="65b0c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="65b0c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65b0c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="65b0c-111">Get-AzCosmosDBCassandraKeyspace получает свойства существующего пространства В.И.</span><span class="sxs-lookup"><span data-stu-id="65b0c-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="65b0c-112">Вы можете развернуть ресурс, чтобы получить _etag, _ts и _rid свойства.</span><span class="sxs-lookup"><span data-stu-id="65b0c-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="65b0c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65b0c-113">PARAMETERS</span></span>

### <span data-ttu-id="65b0c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65b0c-114">-AccountName</span></span>
<span data-ttu-id="65b0c-115">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="65b0c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65b0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b0c-116">-DefaultProfile</span></span>
<span data-ttu-id="65b0c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65b0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b0c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="65b0c-118">-Name</span></span>
<span data-ttu-id="65b0c-119">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="65b0c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="65b0c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="65b0c-120">-ParentObject</span></span>
<span data-ttu-id="65b0c-121">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="65b0c-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="65b0c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65b0c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="65b0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b0c-124">CommonParameters</span></span>
<span data-ttu-id="65b0c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b0c-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65b0c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b0c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65b0c-127">INPUTS</span></span>

### <span data-ttu-id="65b0c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="65b0c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="65b0c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65b0c-129">OUTPUTS</span></span>

### <span data-ttu-id="65b0c-130">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="65b0c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="65b0c-131">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="65b0c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="65b0c-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65b0c-132">NOTES</span></span>

## <span data-ttu-id="65b0c-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65b0c-133">RELATED LINKS</span></span>
