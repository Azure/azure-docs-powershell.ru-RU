---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508737"
---
# <span data-ttu-id="b26df-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="b26df-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="b26df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26df-102">SYNOPSIS</span></span>
<span data-ttu-id="b26df-103">Обновляет значение пропускной способности для Вадима Климова( ВадимОва).</span><span class="sxs-lookup"><span data-stu-id="b26df-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="b26df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b26df-104">SYNTAX</span></span>

### <span data-ttu-id="b26df-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b26df-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26df-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b26df-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26df-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b26df-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26df-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b26df-108">DESCRIPTION</span></span>
<span data-ttu-id="b26df-109">Обновляет значение пропускной способности Вадима Климова( Вадим Вадимов).</span><span class="sxs-lookup"><span data-stu-id="b26df-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="b26df-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b26df-110">EXAMPLES</span></span>

### <span data-ttu-id="b26df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b26df-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="b26df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b26df-112">PARAMETERS</span></span>

### <span data-ttu-id="b26df-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b26df-113">-AccountName</span></span>
<span data-ttu-id="b26df-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="b26df-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b26df-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b26df-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b26df-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="b26df-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b26df-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b26df-117">-Confirm</span></span>
<span data-ttu-id="b26df-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26df-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26df-119">-DefaultProfile</span></span>
<span data-ttu-id="b26df-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b26df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b26df-121">-InputObject</span></span>
<span data-ttu-id="b26df-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="b26df-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b26df-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b26df-123">-Name</span></span>
<span data-ttu-id="b26df-124">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="b26df-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b26df-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b26df-125">-ParentObject</span></span>
<span data-ttu-id="b26df-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="b26df-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b26df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26df-127">-ResourceGroupName</span></span>
<span data-ttu-id="b26df-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b26df-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b26df-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="b26df-129">-Throughput</span></span>
<span data-ttu-id="b26df-130">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b26df-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="b26df-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="b26df-131">Default value is 400.</span></span>

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

### <span data-ttu-id="b26df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26df-132">-WhatIf</span></span>
<span data-ttu-id="b26df-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26df-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b26df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26df-135">CommonParameters</span></span>
<span data-ttu-id="b26df-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26df-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b26df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26df-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b26df-138">INPUTS</span></span>

### <span data-ttu-id="b26df-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b26df-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b26df-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b26df-140">OUTPUTS</span></span>

### <span data-ttu-id="b26df-141">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b26df-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b26df-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b26df-142">NOTES</span></span>

## <span data-ttu-id="b26df-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b26df-143">RELATED LINKS</span></span>
