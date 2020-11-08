---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074439"
---
# <span data-ttu-id="a329b-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="a329b-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="a329b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a329b-102">SYNOPSIS</span></span>
<span data-ttu-id="a329b-103">Задает таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a329b-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a329b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a329b-104">SYNTAX</span></span>

### <span data-ttu-id="a329b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a329b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a329b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a329b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a329b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a329b-107">DESCRIPTION</span></span>
<span data-ttu-id="a329b-108">Командлет **Set-AzCosmosDBCassandraTable** задает CosmosDB Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="a329b-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a329b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a329b-109">EXAMPLES</span></span>

### <span data-ttu-id="a329b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a329b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="a329b-111">Объект Resource включает значения свойств _rid, _ts, _etag, DefaultTtl и Schema.</span><span class="sxs-lookup"><span data-stu-id="a329b-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="a329b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a329b-112">PARAMETERS</span></span>

### <span data-ttu-id="a329b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a329b-113">-AccountName</span></span>
<span data-ttu-id="a329b-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a329b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a329b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a329b-115">-Confirm</span></span>
<span data-ttu-id="a329b-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a329b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a329b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a329b-117">-DefaultProfile</span></span>
<span data-ttu-id="a329b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a329b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a329b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a329b-119">-InputObject</span></span>
<span data-ttu-id="a329b-120">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="a329b-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="a329b-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="a329b-121">-KeyspaceName</span></span>
<span data-ttu-id="a329b-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="a329b-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a329b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a329b-123">-Name</span></span>
<span data-ttu-id="a329b-124">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a329b-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="a329b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a329b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a329b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a329b-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a329b-127">-Schema</span><span class="sxs-lookup"><span data-stu-id="a329b-127">-Schema</span></span>
<span data-ttu-id="a329b-128">Объект PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="a329b-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="a329b-129">Для создания объекта используйте New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="a329b-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a329b-130">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="a329b-130">-Throughput</span></span>
<span data-ttu-id="a329b-131">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a329b-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="a329b-132">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="a329b-132">Default value is 400.</span></span>

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

### <span data-ttu-id="a329b-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a329b-133">-TtlInSeconds</span></span>
<span data-ttu-id="a329b-134">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a329b-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="a329b-135">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="a329b-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="a329b-136">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="a329b-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="a329b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a329b-137">-WhatIf</span></span>
<span data-ttu-id="a329b-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a329b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a329b-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a329b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a329b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a329b-140">CommonParameters</span></span>
<span data-ttu-id="a329b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a329b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a329b-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a329b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a329b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a329b-143">INPUTS</span></span>

### <span data-ttu-id="a329b-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="a329b-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="a329b-145">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="a329b-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="a329b-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a329b-146">OUTPUTS</span></span>

### <span data-ttu-id="a329b-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a329b-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="a329b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a329b-148">NOTES</span></span>

## <span data-ttu-id="a329b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a329b-149">RELATED LINKS</span></span>
