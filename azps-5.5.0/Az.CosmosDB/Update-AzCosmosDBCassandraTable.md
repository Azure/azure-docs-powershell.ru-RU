---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233001"
---
# <span data-ttu-id="92e85-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="92e85-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="92e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e85-102">SYNOPSIS</span></span>
<span data-ttu-id="92e85-103">Обновляет таблицу Климова Вадимова.</span><span class="sxs-lookup"><span data-stu-id="92e85-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="92e85-104">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="92e85-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="92e85-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92e85-105">SYNTAX</span></span>

### <span data-ttu-id="92e85-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92e85-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92e85-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e85-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92e85-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e85-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92e85-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e85-109">DESCRIPTION</span></span>
<span data-ttu-id="92e85-110">Обновляет таблицу Климова Вадимова.</span><span class="sxs-lookup"><span data-stu-id="92e85-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="92e85-111">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="92e85-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="92e85-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92e85-112">EXAMPLES</span></span>

### <span data-ttu-id="92e85-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92e85-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="92e85-114">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="92e85-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="92e85-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e85-115">PARAMETERS</span></span>

### <span data-ttu-id="92e85-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92e85-116">-AccountName</span></span>
<span data-ttu-id="92e85-117">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="92e85-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="92e85-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="92e85-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="92e85-119">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="92e85-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="92e85-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="92e85-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="92e85-121">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="92e85-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="92e85-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92e85-122">-Confirm</span></span>
<span data-ttu-id="92e85-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92e85-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e85-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e85-124">-DefaultProfile</span></span>
<span data-ttu-id="92e85-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92e85-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e85-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92e85-126">-InputObject</span></span>
<span data-ttu-id="92e85-127">Объект "Таблица" Вадима.</span><span class="sxs-lookup"><span data-stu-id="92e85-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="92e85-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="92e85-128">-KeyspaceName</span></span>
<span data-ttu-id="92e85-129">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="92e85-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="92e85-130">-Name</span><span class="sxs-lookup"><span data-stu-id="92e85-130">-Name</span></span>
<span data-ttu-id="92e85-131">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="92e85-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="92e85-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="92e85-132">-ParentObject</span></span>
<span data-ttu-id="92e85-133">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="92e85-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="92e85-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e85-134">-ResourceGroupName</span></span>
<span data-ttu-id="92e85-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92e85-135">Name of resource group.</span></span>

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

### <span data-ttu-id="92e85-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="92e85-136">-Schema</span></span>
<span data-ttu-id="92e85-137">Объект PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="92e85-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="92e85-138">Используйте New-AzCosmosDBCassandraSchema для создания этого объекта.</span><span class="sxs-lookup"><span data-stu-id="92e85-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="92e85-139">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="92e85-139">-Throughput</span></span>
<span data-ttu-id="92e85-140">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="92e85-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="92e85-141">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="92e85-141">Default value is 400.</span></span>

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

### <span data-ttu-id="92e85-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="92e85-142">-TtlInSeconds</span></span>
<span data-ttu-id="92e85-143">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="92e85-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="92e85-144">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="92e85-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="92e85-145">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="92e85-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="92e85-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e85-146">-WhatIf</span></span>
<span data-ttu-id="92e85-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e85-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e85-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92e85-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e85-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e85-149">CommonParameters</span></span>
<span data-ttu-id="92e85-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e85-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e85-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e85-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e85-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92e85-152">INPUTS</span></span>

### <span data-ttu-id="92e85-153">Microsoft.Azure.Commands.АsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="92e85-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="92e85-154">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="92e85-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="92e85-155">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="92e85-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="92e85-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92e85-156">OUTPUTS</span></span>

### <span data-ttu-id="92e85-157">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="92e85-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="92e85-158">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="92e85-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="92e85-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92e85-159">NOTES</span></span>

## <span data-ttu-id="92e85-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92e85-160">RELATED LINKS</span></span>
