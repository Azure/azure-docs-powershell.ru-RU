---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519301"
---
# <span data-ttu-id="57068-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="57068-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="57068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57068-102">SYNOPSIS</span></span>
<span data-ttu-id="57068-103">Создается новая клавишная область «МоментыDB».</span><span class="sxs-lookup"><span data-stu-id="57068-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="57068-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57068-104">SYNTAX</span></span>

### <span data-ttu-id="57068-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57068-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57068-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57068-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57068-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57068-107">DESCRIPTION</span></span>
<span data-ttu-id="57068-108">Создается новая клавишная область «МоментыDB».</span><span class="sxs-lookup"><span data-stu-id="57068-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="57068-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57068-109">EXAMPLES</span></span>

### <span data-ttu-id="57068-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57068-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="57068-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57068-111">PARAMETERS</span></span>

### <span data-ttu-id="57068-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57068-112">-AccountName</span></span>
<span data-ttu-id="57068-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="57068-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57068-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="57068-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="57068-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="57068-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="57068-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57068-116">-Confirm</span></span>
<span data-ttu-id="57068-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57068-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57068-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57068-118">-DefaultProfile</span></span>
<span data-ttu-id="57068-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57068-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57068-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57068-120">-Name</span></span>
<span data-ttu-id="57068-121">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="57068-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="57068-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57068-122">-ParentObject</span></span>
<span data-ttu-id="57068-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="57068-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="57068-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57068-124">-ResourceGroupName</span></span>
<span data-ttu-id="57068-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57068-125">Name of resource group.</span></span>

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

### <span data-ttu-id="57068-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="57068-126">-Throughput</span></span>
<span data-ttu-id="57068-127">Пропускная способность Клавиши Русланы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="57068-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="57068-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="57068-128">Default value is 400.</span></span>

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

### <span data-ttu-id="57068-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57068-129">-WhatIf</span></span>
<span data-ttu-id="57068-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57068-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57068-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57068-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57068-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57068-132">CommonParameters</span></span>
<span data-ttu-id="57068-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57068-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57068-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57068-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57068-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57068-135">INPUTS</span></span>

### <span data-ttu-id="57068-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="57068-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="57068-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57068-137">OUTPUTS</span></span>

### <span data-ttu-id="57068-138">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="57068-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="57068-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="57068-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="57068-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57068-140">NOTES</span></span>

## <span data-ttu-id="57068-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57068-141">RELATED LINKS</span></span>
