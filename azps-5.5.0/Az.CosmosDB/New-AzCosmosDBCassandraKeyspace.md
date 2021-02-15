---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215388"
---
# <span data-ttu-id="bbb56-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="bbb56-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="bbb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb56-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb56-103">Создается новая клавишная область «МоментыDB».</span><span class="sxs-lookup"><span data-stu-id="bbb56-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="bbb56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbb56-104">SYNTAX</span></span>

### <span data-ttu-id="bbb56-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbb56-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbb56-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbb56-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbb56-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbb56-107">DESCRIPTION</span></span>
<span data-ttu-id="bbb56-108">Создается новая клавишная область «МоментыDB».</span><span class="sxs-lookup"><span data-stu-id="bbb56-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="bbb56-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbb56-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb56-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbb56-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="bbb56-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbb56-111">PARAMETERS</span></span>

### <span data-ttu-id="bbb56-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bbb56-112">-AccountName</span></span>
<span data-ttu-id="bbb56-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="bbb56-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bbb56-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bbb56-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bbb56-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="bbb56-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bbb56-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbb56-116">-Confirm</span></span>
<span data-ttu-id="bbb56-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb56-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb56-118">-DefaultProfile</span></span>
<span data-ttu-id="bbb56-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb56-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bbb56-120">-Name</span></span>
<span data-ttu-id="bbb56-121">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="bbb56-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="bbb56-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bbb56-122">-ParentObject</span></span>
<span data-ttu-id="bbb56-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="bbb56-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="bbb56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb56-124">-ResourceGroupName</span></span>
<span data-ttu-id="bbb56-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbb56-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bbb56-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="bbb56-126">-Throughput</span></span>
<span data-ttu-id="bbb56-127">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="bbb56-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="bbb56-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="bbb56-128">Default value is 400.</span></span>

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

### <span data-ttu-id="bbb56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb56-129">-WhatIf</span></span>
<span data-ttu-id="bbb56-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb56-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bbb56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb56-132">CommonParameters</span></span>
<span data-ttu-id="bbb56-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb56-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbb56-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb56-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbb56-135">INPUTS</span></span>

### <span data-ttu-id="bbb56-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="bbb56-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="bbb56-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbb56-137">OUTPUTS</span></span>

### <span data-ttu-id="bbb56-138">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="bbb56-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="bbb56-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bbb56-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bbb56-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbb56-140">NOTES</span></span>

## <span data-ttu-id="bbb56-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbb56-141">RELATED LINKS</span></span>
