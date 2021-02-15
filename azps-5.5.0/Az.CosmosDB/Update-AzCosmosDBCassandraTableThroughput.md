---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215364"
---
# <span data-ttu-id="57022-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="57022-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="57022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57022-102">SYNOPSIS</span></span>
<span data-ttu-id="57022-103">Обновляет значение пропускной способности таблицы Климова Вадимова.</span><span class="sxs-lookup"><span data-stu-id="57022-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="57022-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57022-104">SYNTAX</span></span>

### <span data-ttu-id="57022-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57022-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57022-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57022-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57022-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57022-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57022-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57022-108">DESCRIPTION</span></span>
<span data-ttu-id="57022-109">Обновляет значение пропускной способности таблицы Сергея Климова.</span><span class="sxs-lookup"><span data-stu-id="57022-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="57022-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57022-110">EXAMPLES</span></span>

### <span data-ttu-id="57022-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57022-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="57022-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57022-112">PARAMETERS</span></span>

### <span data-ttu-id="57022-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57022-113">-AccountName</span></span>
<span data-ttu-id="57022-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="57022-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57022-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="57022-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="57022-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="57022-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="57022-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57022-117">-Confirm</span></span>
<span data-ttu-id="57022-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57022-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57022-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57022-119">-DefaultProfile</span></span>
<span data-ttu-id="57022-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57022-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57022-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57022-121">-InputObject</span></span>
<span data-ttu-id="57022-122">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="57022-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="57022-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="57022-123">-KeyspaceName</span></span>
<span data-ttu-id="57022-124">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="57022-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="57022-125">-Name</span><span class="sxs-lookup"><span data-stu-id="57022-125">-Name</span></span>
<span data-ttu-id="57022-126">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="57022-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="57022-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57022-127">-ParentObject</span></span>
<span data-ttu-id="57022-128">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="57022-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="57022-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57022-129">-ResourceGroupName</span></span>
<span data-ttu-id="57022-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57022-130">Name of resource group.</span></span>

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

### <span data-ttu-id="57022-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="57022-131">-Throughput</span></span>
<span data-ttu-id="57022-132">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="57022-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="57022-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="57022-133">Default value is 400.</span></span>

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

### <span data-ttu-id="57022-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57022-134">-WhatIf</span></span>
<span data-ttu-id="57022-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57022-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57022-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57022-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57022-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57022-137">CommonParameters</span></span>
<span data-ttu-id="57022-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57022-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57022-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57022-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57022-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57022-140">INPUTS</span></span>

### <span data-ttu-id="57022-141">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="57022-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="57022-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57022-142">OUTPUTS</span></span>

### <span data-ttu-id="57022-143">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="57022-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="57022-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57022-144">NOTES</span></span>

## <span data-ttu-id="57022-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57022-145">RELATED LINKS</span></span>
