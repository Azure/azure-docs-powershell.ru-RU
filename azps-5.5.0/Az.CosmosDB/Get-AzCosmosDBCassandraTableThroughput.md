---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233113"
---
# <span data-ttu-id="e8135-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="e8135-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="e8135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8135-102">SYNOPSIS</span></span>
<span data-ttu-id="e8135-103">Возвращает значение пропускной способности таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="e8135-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="e8135-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8135-104">SYNTAX</span></span>

### <span data-ttu-id="e8135-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8135-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8135-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8135-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8135-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8135-107">DESCRIPTION</span></span>
<span data-ttu-id="e8135-108">С **помощью cmdlet get-AzCosmosDBCassandraTableThroughput** можно получить объект пропускной способности, соответствующий заданной области клавиш.</span><span class="sxs-lookup"><span data-stu-id="e8135-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="e8135-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8135-109">EXAMPLES</span></span>

### <span data-ttu-id="e8135-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8135-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="e8135-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8135-111">PARAMETERS</span></span>

### <span data-ttu-id="e8135-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8135-112">-AccountName</span></span>
<span data-ttu-id="e8135-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="e8135-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8135-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8135-114">-Confirm</span></span>
<span data-ttu-id="e8135-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e8135-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8135-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8135-116">-DefaultProfile</span></span>
<span data-ttu-id="e8135-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8135-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8135-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8135-118">-InputObject</span></span>
<span data-ttu-id="e8135-119">Объект "Таблица", "Александра".</span><span class="sxs-lookup"><span data-stu-id="e8135-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="e8135-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="e8135-120">-KeyspaceName</span></span>
<span data-ttu-id="e8135-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e8135-121">Database name.</span></span>

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

### <span data-ttu-id="e8135-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8135-122">-Name</span></span>
<span data-ttu-id="e8135-123">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="e8135-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="e8135-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8135-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8135-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8135-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e8135-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8135-126">-WhatIf</span></span>
<span data-ttu-id="e8135-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8135-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8135-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e8135-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8135-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8135-129">CommonParameters</span></span>
<span data-ttu-id="e8135-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8135-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8135-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8135-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8135-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8135-132">INPUTS</span></span>

### <span data-ttu-id="e8135-133">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e8135-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e8135-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8135-134">OUTPUTS</span></span>

### <span data-ttu-id="e8135-135">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e8135-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e8135-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8135-136">NOTES</span></span>

## <span data-ttu-id="e8135-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8135-137">RELATED LINKS</span></span>
