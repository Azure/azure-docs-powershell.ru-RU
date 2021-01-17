---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398580"
---
# <span data-ttu-id="aa95f-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="aa95f-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="aa95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa95f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa95f-103">Возвращает значение пропускной способности таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="aa95f-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="aa95f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa95f-104">SYNTAX</span></span>

### <span data-ttu-id="aa95f-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa95f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa95f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa95f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa95f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa95f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa95f-108">С **помощью cmdlet get-AzCosmosDBCassandraTableThroughput** можно получить объект пропускной способности, соответствующий заданной области клавиш.</span><span class="sxs-lookup"><span data-stu-id="aa95f-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="aa95f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa95f-109">EXAMPLES</span></span>

### <span data-ttu-id="aa95f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa95f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="aa95f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa95f-111">PARAMETERS</span></span>

### <span data-ttu-id="aa95f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa95f-112">-AccountName</span></span>
<span data-ttu-id="aa95f-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="aa95f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aa95f-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa95f-114">-Confirm</span></span>
<span data-ttu-id="aa95f-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa95f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa95f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa95f-116">-DefaultProfile</span></span>
<span data-ttu-id="aa95f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa95f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa95f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa95f-118">-InputObject</span></span>
<span data-ttu-id="aa95f-119">Объект "Таблица" Вадима.</span><span class="sxs-lookup"><span data-stu-id="aa95f-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="aa95f-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="aa95f-120">-KeyspaceName</span></span>
<span data-ttu-id="aa95f-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="aa95f-121">Database name.</span></span>

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

### <span data-ttu-id="aa95f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aa95f-122">-Name</span></span>
<span data-ttu-id="aa95f-123">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="aa95f-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="aa95f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa95f-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa95f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa95f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="aa95f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa95f-126">-WhatIf</span></span>
<span data-ttu-id="aa95f-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa95f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa95f-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa95f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa95f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa95f-129">CommonParameters</span></span>
<span data-ttu-id="aa95f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa95f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa95f-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa95f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa95f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa95f-132">INPUTS</span></span>

### <span data-ttu-id="aa95f-133">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="aa95f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="aa95f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa95f-134">OUTPUTS</span></span>

### <span data-ttu-id="aa95f-135">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="aa95f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="aa95f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa95f-136">NOTES</span></span>

## <span data-ttu-id="aa95f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa95f-137">RELATED LINKS</span></span>
