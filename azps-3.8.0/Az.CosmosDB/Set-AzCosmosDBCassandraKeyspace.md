---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: d1b0dcee6c4337a572f98a51cb03c3fcdcd6c84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074440"
---
# <span data-ttu-id="9e081-101">Set-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9e081-101">Set-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9e081-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e081-102">SYNOPSIS</span></span>
<span data-ttu-id="9e081-103">Задает CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="9e081-103">Sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9e081-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e081-104">SYNTAX</span></span>

### <span data-ttu-id="9e081-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e081-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e081-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e081-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e081-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e081-107">DESCRIPTION</span></span>
<span data-ttu-id="9e081-108">Командлет **Set-AzCosmosDBCassandraKeyspace** задает CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="9e081-108">The **Set-AzCosmosDBCassandraKeyspace** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9e081-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e081-109">EXAMPLES</span></span>

### <span data-ttu-id="9e081-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e081-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraKeyspace -ResourceGroupName {rgName} -AccountName {accountName} -Name {keyspaceName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

<span data-ttu-id="9e081-111">Объект Resource (ресурс) включает значения свойств _rid, _ts и _etag.</span><span class="sxs-lookup"><span data-stu-id="9e081-111">Resource object contains the values of the _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="9e081-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e081-112">PARAMETERS</span></span>

### <span data-ttu-id="9e081-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9e081-113">-AccountName</span></span>
<span data-ttu-id="9e081-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9e081-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9e081-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e081-115">-Confirm</span></span>
<span data-ttu-id="9e081-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e081-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e081-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e081-117">-DefaultProfile</span></span>
<span data-ttu-id="9e081-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e081-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e081-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e081-119">-InputObject</span></span>
<span data-ttu-id="9e081-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9e081-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9e081-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e081-121">-Name</span></span>
<span data-ttu-id="9e081-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="9e081-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9e081-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e081-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e081-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e081-124">Name of resource group.</span></span>

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

### <span data-ttu-id="9e081-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="9e081-125">-Throughput</span></span>
<span data-ttu-id="9e081-126">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9e081-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9e081-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9e081-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e081-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e081-128">-WhatIf</span></span>
<span data-ttu-id="9e081-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e081-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e081-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e081-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e081-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e081-131">CommonParameters</span></span>
<span data-ttu-id="9e081-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e081-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e081-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e081-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e081-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e081-134">INPUTS</span></span>

### <span data-ttu-id="9e081-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9e081-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9e081-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e081-136">OUTPUTS</span></span>

### <span data-ttu-id="9e081-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9e081-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9e081-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e081-138">NOTES</span></span>

## <span data-ttu-id="9e081-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e081-139">RELATED LINKS</span></span>
