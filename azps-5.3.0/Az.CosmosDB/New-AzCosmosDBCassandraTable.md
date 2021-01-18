---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519298"
---
# <span data-ttu-id="f8148-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="f8148-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="f8148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8148-102">SYNOPSIS</span></span>
<span data-ttu-id="f8148-103">Создает таблицу "Сергей Петров" в "О-ве".</span><span class="sxs-lookup"><span data-stu-id="f8148-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f8148-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8148-104">SYNTAX</span></span>

### <span data-ttu-id="f8148-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8148-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8148-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8148-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8148-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8148-107">DESCRIPTION</span></span>
<span data-ttu-id="f8148-108">Создает таблицу "Сергей Петров" в "О-ве".</span><span class="sxs-lookup"><span data-stu-id="f8148-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f8148-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8148-109">EXAMPLES</span></span>

### <span data-ttu-id="f8148-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8148-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="f8148-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8148-111">PARAMETERS</span></span>

### <span data-ttu-id="f8148-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f8148-112">-AccountName</span></span>
<span data-ttu-id="f8148-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="f8148-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f8148-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f8148-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f8148-115">TTL для аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="f8148-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="f8148-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f8148-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f8148-117">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="f8148-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f8148-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8148-118">-Confirm</span></span>
<span data-ttu-id="f8148-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8148-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8148-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8148-120">-DefaultProfile</span></span>
<span data-ttu-id="f8148-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8148-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8148-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="f8148-122">-KeyspaceName</span></span>
<span data-ttu-id="f8148-123">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="f8148-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f8148-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f8148-124">-Name</span></span>
<span data-ttu-id="f8148-125">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="f8148-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="f8148-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f8148-126">-ParentObject</span></span>
<span data-ttu-id="f8148-127">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="f8148-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f8148-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8148-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8148-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8148-129">Name of resource group.</span></span>

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

### <span data-ttu-id="f8148-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="f8148-130">-Schema</span></span>
<span data-ttu-id="f8148-131">Объект PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="f8148-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="f8148-132">Используйте New-AzCosmosDBCassandraSchema для создания этого объекта.</span><span class="sxs-lookup"><span data-stu-id="f8148-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="f8148-133">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f8148-133">-Throughput</span></span>
<span data-ttu-id="f8148-134">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f8148-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f8148-135">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="f8148-135">Default value is 400.</span></span>

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

### <span data-ttu-id="f8148-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f8148-136">-TtlInSeconds</span></span>
<span data-ttu-id="f8148-137">Значение TTL по умолчанию (в секундах).</span><span class="sxs-lookup"><span data-stu-id="f8148-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="f8148-138">Если значение отсутствует или установлено значение -1, срок действия элементов не истекает.</span><span class="sxs-lookup"><span data-stu-id="f8148-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f8148-139">Если для этого значения установлено значение n, срок действия элементов истекает через n секунд после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="f8148-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f8148-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8148-140">-WhatIf</span></span>
<span data-ttu-id="f8148-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8148-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8148-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8148-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8148-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8148-143">CommonParameters</span></span>
<span data-ttu-id="f8148-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8148-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8148-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8148-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8148-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8148-146">INPUTS</span></span>

### <span data-ttu-id="f8148-147">Microsoft.Azure.Commands.АsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f8148-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="f8148-148">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f8148-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f8148-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8148-149">OUTPUTS</span></span>

### <span data-ttu-id="f8148-150">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f8148-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="f8148-151">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f8148-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f8148-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8148-152">NOTES</span></span>

## <span data-ttu-id="f8148-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8148-153">RELATED LINKS</span></span>
