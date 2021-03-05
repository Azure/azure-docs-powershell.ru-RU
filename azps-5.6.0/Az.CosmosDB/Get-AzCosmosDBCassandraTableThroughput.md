---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 7693d507874dc5ebc4aa7b9c720c3efbe2963c05
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983683"
---
# <span data-ttu-id="2a77b-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="2a77b-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="2a77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a77b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a77b-103">Возвращает значение пропускной способности таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="2a77b-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="2a77b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a77b-104">SYNTAX</span></span>

### <span data-ttu-id="2a77b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a77b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a77b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a77b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a77b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a77b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a77b-108">С **помощью cmdlet get-AzCosmosDBCassandraTableThroughput** можно получить объект пропускной способности, соответствующий заданной области клавиш.</span><span class="sxs-lookup"><span data-stu-id="2a77b-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="2a77b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a77b-109">EXAMPLES</span></span>

### <span data-ttu-id="2a77b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a77b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="2a77b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a77b-111">PARAMETERS</span></span>

### <span data-ttu-id="2a77b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a77b-112">-AccountName</span></span>
<span data-ttu-id="2a77b-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="2a77b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2a77b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a77b-114">-Confirm</span></span>
<span data-ttu-id="2a77b-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a77b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a77b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a77b-116">-DefaultProfile</span></span>
<span data-ttu-id="2a77b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a77b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a77b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a77b-118">-InputObject</span></span>
<span data-ttu-id="2a77b-119">Объект "Таблица" Вадима.</span><span class="sxs-lookup"><span data-stu-id="2a77b-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="2a77b-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="2a77b-120">-KeyspaceName</span></span>
<span data-ttu-id="2a77b-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2a77b-121">Database name.</span></span>

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

### <span data-ttu-id="2a77b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2a77b-122">-Name</span></span>
<span data-ttu-id="2a77b-123">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="2a77b-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2a77b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a77b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a77b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a77b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2a77b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a77b-126">-WhatIf</span></span>
<span data-ttu-id="2a77b-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a77b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a77b-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a77b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a77b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a77b-129">CommonParameters</span></span>
<span data-ttu-id="2a77b-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a77b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a77b-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a77b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a77b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a77b-132">INPUTS</span></span>

### <span data-ttu-id="2a77b-133">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2a77b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2a77b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a77b-134">OUTPUTS</span></span>

### <span data-ttu-id="2a77b-135">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2a77b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2a77b-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a77b-136">NOTES</span></span>

## <span data-ttu-id="2a77b-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a77b-137">RELATED LINKS</span></span>
