---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236869"
---
# <span data-ttu-id="4a780-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="4a780-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="4a780-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a780-102">SYNOPSIS</span></span>
<span data-ttu-id="4a780-103">Возвращает CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="4a780-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4a780-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a780-104">SYNTAX</span></span>

### <span data-ttu-id="4a780-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a780-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a780-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a780-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a780-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a780-107">DESCRIPTION</span></span>
<span data-ttu-id="4a780-108">Командлет **Get-AzCosmosDBCassandraKeyspace** создает новый или обновляет существующий CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="4a780-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4a780-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a780-109">EXAMPLES</span></span>

### <span data-ttu-id="4a780-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a780-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4a780-111">Get-AzCosmosDBCassandraKeyspace получает свойства существующего CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="4a780-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4a780-112">Вы можете развернуть ресурс, чтобы получить _etag, _ts _rid свойств.</span><span class="sxs-lookup"><span data-stu-id="4a780-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="4a780-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a780-113">PARAMETERS</span></span>

### <span data-ttu-id="4a780-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4a780-114">-AccountName</span></span>
<span data-ttu-id="4a780-115">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4a780-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4a780-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a780-116">-DefaultProfile</span></span>
<span data-ttu-id="4a780-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a780-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a780-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a780-118">-Name</span></span>
<span data-ttu-id="4a780-119">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="4a780-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4a780-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a780-120">-ParentObject</span></span>
<span data-ttu-id="4a780-121">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4a780-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4a780-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a780-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a780-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a780-123">Name of resource group.</span></span>

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

### <span data-ttu-id="4a780-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a780-124">CommonParameters</span></span>
<span data-ttu-id="4a780-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a780-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a780-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a780-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a780-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a780-127">INPUTS</span></span>

### <span data-ttu-id="4a780-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4a780-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4a780-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a780-129">OUTPUTS</span></span>

### <span data-ttu-id="4a780-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4a780-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="4a780-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4a780-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4a780-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a780-132">NOTES</span></span>

## <span data-ttu-id="4a780-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a780-133">RELATED LINKS</span></span>
