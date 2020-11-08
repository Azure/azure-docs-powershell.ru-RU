---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066653"
---
# <span data-ttu-id="d7d06-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="d7d06-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="d7d06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7d06-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d06-103">Обновляет значение пропускной способности графа CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d7d06-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d7d06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7d06-104">SYNTAX</span></span>

### <span data-ttu-id="d7d06-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7d06-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d06-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7d06-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d06-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7d06-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7d06-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7d06-108">EXAMPLES</span></span>

### <span data-ttu-id="d7d06-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7d06-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d7d06-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7d06-110">PARAMETERS</span></span>

### <span data-ttu-id="d7d06-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="d7d06-111">-AccountName</span></span>
<span data-ttu-id="d7d06-112">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d7d06-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7d06-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d06-113">-Confirm</span></span>
<span data-ttu-id="d7d06-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d06-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d06-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7d06-115">-DatabaseName</span></span>
<span data-ttu-id="d7d06-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7d06-116">Database name.</span></span>

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

### <span data-ttu-id="d7d06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d06-117">-DefaultProfile</span></span>
<span data-ttu-id="d7d06-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d06-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7d06-119">-InputObject</span></span>
<span data-ttu-id="d7d06-120">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d7d06-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d06-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7d06-121">-Name</span></span>
<span data-ttu-id="d7d06-122">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d7d06-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d7d06-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7d06-123">-ParentObject</span></span>
<span data-ttu-id="d7d06-124">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d7d06-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d06-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7d06-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7d06-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d7d06-127">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="d7d06-127">-Throughput</span></span>
<span data-ttu-id="d7d06-128">Пропускная способность Gremlin графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d7d06-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d7d06-129">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="d7d06-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d06-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d06-130">-WhatIf</span></span>
<span data-ttu-id="d7d06-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d06-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d06-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7d06-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d06-133">CommonParameters</span></span>
<span data-ttu-id="d7d06-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7d06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d06-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7d06-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d06-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7d06-136">INPUTS</span></span>

### <span data-ttu-id="d7d06-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d7d06-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d7d06-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d06-138">OUTPUTS</span></span>

### <span data-ttu-id="d7d06-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d7d06-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d7d06-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7d06-140">NOTES</span></span>

## <span data-ttu-id="d7d06-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7d06-141">RELATED LINKS</span></span>
