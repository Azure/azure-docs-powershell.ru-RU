---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314579"
---
# <span data-ttu-id="17bd9-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="17bd9-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="17bd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="17bd9-103">Обновляет таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="17bd9-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="17bd9-104">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="17bd9-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="17bd9-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17bd9-105">SYNTAX</span></span>

### <span data-ttu-id="17bd9-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17bd9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17bd9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17bd9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17bd9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17bd9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17bd9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bd9-109">DESCRIPTION</span></span>
<span data-ttu-id="17bd9-110">Обновляет таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="17bd9-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="17bd9-111">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="17bd9-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="17bd9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17bd9-112">EXAMPLES</span></span>

### <span data-ttu-id="17bd9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17bd9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="17bd9-114">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="17bd9-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="17bd9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17bd9-115">PARAMETERS</span></span>

### <span data-ttu-id="17bd9-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="17bd9-116">-AccountName</span></span>
<span data-ttu-id="17bd9-117">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="17bd9-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="17bd9-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="17bd9-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="17bd9-119">Аналитическое хранилище: срок жизни.</span><span class="sxs-lookup"><span data-stu-id="17bd9-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="17bd9-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="17bd9-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="17bd9-121">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="17bd9-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="17bd9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17bd9-122">-Confirm</span></span>
<span data-ttu-id="17bd9-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17bd9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bd9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bd9-124">-DefaultProfile</span></span>
<span data-ttu-id="17bd9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17bd9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bd9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17bd9-126">-InputObject</span></span>
<span data-ttu-id="17bd9-127">Объект таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="17bd9-127">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17bd9-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="17bd9-128">-KeyspaceName</span></span>
<span data-ttu-id="17bd9-129">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="17bd9-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="17bd9-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17bd9-130">-Name</span></span>
<span data-ttu-id="17bd9-131">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="17bd9-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="17bd9-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="17bd9-132">-ParentObject</span></span>
<span data-ttu-id="17bd9-133">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="17bd9-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="17bd9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bd9-134">-ResourceGroupName</span></span>
<span data-ttu-id="17bd9-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17bd9-135">Name of resource group.</span></span>

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

### <span data-ttu-id="17bd9-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="17bd9-136">-Schema</span></span>
<span data-ttu-id="17bd9-137">Объект PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="17bd9-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="17bd9-138">Для создания объекта используйте New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="17bd9-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17bd9-139">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="17bd9-139">-Throughput</span></span>
<span data-ttu-id="17bd9-140">Пропускная способность Cassandra keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="17bd9-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="17bd9-141">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="17bd9-141">Default value is 400.</span></span>

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

### <span data-ttu-id="17bd9-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="17bd9-142">-TtlInSeconds</span></span>
<span data-ttu-id="17bd9-143">Срок жизни по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="17bd9-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="17bd9-144">Если значение отсутствует или равно-1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="17bd9-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="17bd9-145">Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="17bd9-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="17bd9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bd9-146">-WhatIf</span></span>
<span data-ttu-id="17bd9-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17bd9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bd9-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17bd9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bd9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bd9-149">CommonParameters</span></span>
<span data-ttu-id="17bd9-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17bd9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bd9-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17bd9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bd9-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17bd9-152">INPUTS</span></span>

### <span data-ttu-id="17bd9-153">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="17bd9-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="17bd9-154">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="17bd9-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="17bd9-155">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="17bd9-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="17bd9-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bd9-156">OUTPUTS</span></span>

### <span data-ttu-id="17bd9-157">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="17bd9-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="17bd9-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="17bd9-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="17bd9-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="17bd9-159">NOTES</span></span>

## <span data-ttu-id="17bd9-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17bd9-160">RELATED LINKS</span></span>
