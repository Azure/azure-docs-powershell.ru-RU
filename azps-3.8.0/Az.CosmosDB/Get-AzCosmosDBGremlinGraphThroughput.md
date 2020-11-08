---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074121"
---
# <span data-ttu-id="415c5-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="415c5-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="415c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="415c5-102">SYNOPSIS</span></span>
<span data-ttu-id="415c5-103">Возвращает пропускную способность графа CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="415c5-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="415c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="415c5-104">SYNTAX</span></span>

### <span data-ttu-id="415c5-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="415c5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="415c5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="415c5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415c5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="415c5-107">DESCRIPTION</span></span>
<span data-ttu-id="415c5-108">Командлет **Get-AzCosmosDBGremlinGraphThroughput** возвращает пропускную способность для CosmosDB Gremlin графа.</span><span class="sxs-lookup"><span data-stu-id="415c5-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="415c5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="415c5-109">EXAMPLES</span></span>

### <span data-ttu-id="415c5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="415c5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="415c5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="415c5-111">PARAMETERS</span></span>

### <span data-ttu-id="415c5-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="415c5-112">-AccountName</span></span>
<span data-ttu-id="415c5-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="415c5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="415c5-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="415c5-114">-Confirm</span></span>
<span data-ttu-id="415c5-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="415c5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415c5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="415c5-116">-DatabaseName</span></span>
<span data-ttu-id="415c5-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="415c5-117">Database name.</span></span>

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

### <span data-ttu-id="415c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415c5-118">-DefaultProfile</span></span>
<span data-ttu-id="415c5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="415c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="415c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="415c5-120">-InputObject</span></span>
<span data-ttu-id="415c5-121">Объект Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="415c5-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="415c5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="415c5-122">-Name</span></span>
<span data-ttu-id="415c5-123">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="415c5-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="415c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="415c5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415c5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="415c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415c5-126">-WhatIf</span></span>
<span data-ttu-id="415c5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="415c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415c5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="415c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415c5-129">CommonParameters</span></span>
<span data-ttu-id="415c5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="415c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415c5-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="415c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415c5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="415c5-132">INPUTS</span></span>

### <span data-ttu-id="415c5-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="415c5-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="415c5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="415c5-134">OUTPUTS</span></span>

### <span data-ttu-id="415c5-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="415c5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="415c5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="415c5-136">NOTES</span></span>

## <span data-ttu-id="415c5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="415c5-137">RELATED LINKS</span></span>
