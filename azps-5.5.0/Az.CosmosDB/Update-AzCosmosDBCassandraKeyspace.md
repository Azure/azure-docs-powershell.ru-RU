---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211289"
---
# <span data-ttu-id="9a7b5-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9a7b5-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9a7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7b5-103">Обновляет клавишную область Климова Вадима Вадимова.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="9a7b5-104">Выполняет обновление на стороне клиента с помощью существующей области ключей.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="9a7b5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a7b5-105">SYNTAX</span></span>

### <span data-ttu-id="9a7b5-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a7b5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7b5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7b5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a7b5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7b5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a7b5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a7b5-109">DESCRIPTION</span></span>
<span data-ttu-id="9a7b5-110">Обновляет клавишную область Климова Вадима Вадимова.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="9a7b5-111">Выполняет обновление на стороне клиента с помощью существующей области ключей.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="9a7b5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a7b5-112">EXAMPLES</span></span>

### <span data-ttu-id="9a7b5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a7b5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="9a7b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a7b5-114">PARAMETERS</span></span>

### <span data-ttu-id="9a7b5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a7b5-115">-AccountName</span></span>
<span data-ttu-id="9a7b5-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9a7b5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9a7b5-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9a7b5-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9a7b5-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9a7b5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a7b5-119">-Confirm</span></span>
<span data-ttu-id="9a7b5-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7b5-121">-DefaultProfile</span></span>
<span data-ttu-id="9a7b5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a7b5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7b5-123">-InputObject</span></span>
<span data-ttu-id="9a7b5-124">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9a7b5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9a7b5-125">-Name</span></span>
<span data-ttu-id="9a7b5-126">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9a7b5-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a7b5-127">-ParentObject</span></span>
<span data-ttu-id="9a7b5-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9a7b5-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9a7b5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7b5-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a7b5-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-130">Name of resource group.</span></span>

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

### <span data-ttu-id="9a7b5-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="9a7b5-131">-Throughput</span></span>
<span data-ttu-id="9a7b5-132">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9a7b5-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9a7b5-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-133">Default value is 400.</span></span>

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

### <span data-ttu-id="9a7b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7b5-134">-WhatIf</span></span>
<span data-ttu-id="9a7b5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7b5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7b5-137">CommonParameters</span></span>
<span data-ttu-id="9a7b5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7b5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a7b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7b5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a7b5-140">INPUTS</span></span>

### <span data-ttu-id="9a7b5-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9a7b5-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="9a7b5-142">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9a7b5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9a7b5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a7b5-143">OUTPUTS</span></span>

### <span data-ttu-id="9a7b5-144">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9a7b5-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9a7b5-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9a7b5-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9a7b5-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a7b5-146">NOTES</span></span>

## <span data-ttu-id="9a7b5-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a7b5-147">RELATED LINKS</span></span>
