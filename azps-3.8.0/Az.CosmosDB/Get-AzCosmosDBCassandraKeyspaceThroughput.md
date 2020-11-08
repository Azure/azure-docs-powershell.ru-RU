---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074130"
---
# <span data-ttu-id="e71ab-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="e71ab-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="e71ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e71ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e71ab-103">Возвращает значение пропускной способности Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="e71ab-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="e71ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e71ab-104">SYNTAX</span></span>

### <span data-ttu-id="e71ab-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e71ab-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e71ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e71ab-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e71ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71ab-107">DESCRIPTION</span></span>
<span data-ttu-id="e71ab-108">Командлет **Get-AzCosmosDBCassandraKeyspaceThroughput** получает объект пропускной способности, соответствующий заданному keyspace.</span><span class="sxs-lookup"><span data-stu-id="e71ab-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="e71ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e71ab-109">EXAMPLES</span></span>

### <span data-ttu-id="e71ab-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e71ab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="e71ab-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e71ab-111">PARAMETERS</span></span>

### <span data-ttu-id="e71ab-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e71ab-112">-AccountName</span></span>
<span data-ttu-id="e71ab-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e71ab-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e71ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71ab-114">-DefaultProfile</span></span>
<span data-ttu-id="e71ab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e71ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e71ab-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e71ab-116">-InputObject</span></span>
<span data-ttu-id="e71ab-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e71ab-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e71ab-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e71ab-118">-Name</span></span>
<span data-ttu-id="e71ab-119">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="e71ab-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="e71ab-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e71ab-121">Name of resource group.</span></span>

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

### <span data-ttu-id="e71ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71ab-122">CommonParameters</span></span>
<span data-ttu-id="e71ab-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e71ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71ab-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71ab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71ab-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e71ab-125">INPUTS</span></span>

### <span data-ttu-id="e71ab-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e71ab-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e71ab-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71ab-127">OUTPUTS</span></span>

### <span data-ttu-id="e71ab-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e71ab-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e71ab-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e71ab-129">NOTES</span></span>

## <span data-ttu-id="e71ab-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e71ab-130">RELATED LINKS</span></span>
