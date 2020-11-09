---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315074"
---
# <span data-ttu-id="81068-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="81068-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="81068-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81068-102">SYNOPSIS</span></span>
<span data-ttu-id="81068-103">Возвращает значение пропускной способности таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="81068-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="81068-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81068-104">SYNTAX</span></span>

### <span data-ttu-id="81068-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81068-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81068-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81068-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81068-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81068-107">DESCRIPTION</span></span>
<span data-ttu-id="81068-108">Командлет **Get-AzCosmosDBCassandraTableThroughput** получает объект пропускной способности, соответствующий заданному keyspace.</span><span class="sxs-lookup"><span data-stu-id="81068-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="81068-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81068-109">EXAMPLES</span></span>

### <span data-ttu-id="81068-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81068-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="81068-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81068-111">PARAMETERS</span></span>

### <span data-ttu-id="81068-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="81068-112">-AccountName</span></span>
<span data-ttu-id="81068-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="81068-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81068-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81068-114">-Confirm</span></span>
<span data-ttu-id="81068-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81068-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81068-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81068-116">-DefaultProfile</span></span>
<span data-ttu-id="81068-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81068-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81068-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81068-118">-InputObject</span></span>
<span data-ttu-id="81068-119">Объект таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="81068-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="81068-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="81068-120">-KeyspaceName</span></span>
<span data-ttu-id="81068-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="81068-121">Database name.</span></span>

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

### <span data-ttu-id="81068-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81068-122">-Name</span></span>
<span data-ttu-id="81068-123">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="81068-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="81068-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81068-124">-ResourceGroupName</span></span>
<span data-ttu-id="81068-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81068-125">Name of resource group.</span></span>

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

### <span data-ttu-id="81068-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81068-126">-WhatIf</span></span>
<span data-ttu-id="81068-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81068-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81068-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81068-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81068-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81068-129">CommonParameters</span></span>
<span data-ttu-id="81068-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81068-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81068-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81068-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81068-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81068-132">INPUTS</span></span>

### <span data-ttu-id="81068-133">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="81068-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="81068-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81068-134">OUTPUTS</span></span>

### <span data-ttu-id="81068-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="81068-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="81068-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="81068-136">NOTES</span></span>

## <span data-ttu-id="81068-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81068-137">RELATED LINKS</span></span>
