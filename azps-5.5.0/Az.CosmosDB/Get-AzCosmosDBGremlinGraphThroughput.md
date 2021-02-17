---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211388"
---
# <span data-ttu-id="0be95-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="0be95-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="0be95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be95-102">SYNOPSIS</span></span>
<span data-ttu-id="0be95-103">Получает пропускную способность Диаграммы Гремлина ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="0be95-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0be95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0be95-104">SYNTAX</span></span>

### <span data-ttu-id="0be95-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0be95-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0be95-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0be95-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be95-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0be95-107">DESCRIPTION</span></span>
<span data-ttu-id="0be95-108">С **помощью cmdlet Get-AzCosmosDBGremlinGraphThroughput** можно получить пропускную способность РегинаDb Гремлин Graph.</span><span class="sxs-lookup"><span data-stu-id="0be95-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0be95-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0be95-109">EXAMPLES</span></span>

### <span data-ttu-id="0be95-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0be95-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0be95-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0be95-111">PARAMETERS</span></span>

### <span data-ttu-id="0be95-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0be95-112">-AccountName</span></span>
<span data-ttu-id="0be95-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="0be95-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0be95-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0be95-114">-Confirm</span></span>
<span data-ttu-id="0be95-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0be95-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be95-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0be95-116">-DatabaseName</span></span>
<span data-ttu-id="0be95-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0be95-117">Database name.</span></span>

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

### <span data-ttu-id="0be95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be95-118">-DefaultProfile</span></span>
<span data-ttu-id="0be95-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0be95-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be95-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0be95-120">-InputObject</span></span>
<span data-ttu-id="0be95-121">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="0be95-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="0be95-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0be95-122">-Name</span></span>
<span data-ttu-id="0be95-123">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="0be95-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0be95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be95-124">-ResourceGroupName</span></span>
<span data-ttu-id="0be95-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0be95-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0be95-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be95-126">-WhatIf</span></span>
<span data-ttu-id="0be95-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0be95-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0be95-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0be95-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0be95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be95-129">CommonParameters</span></span>
<span data-ttu-id="0be95-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be95-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0be95-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be95-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0be95-132">INPUTS</span></span>

### <span data-ttu-id="0be95-133">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="0be95-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="0be95-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0be95-134">OUTPUTS</span></span>

### <span data-ttu-id="0be95-135">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0be95-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0be95-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0be95-136">NOTES</span></span>

## <span data-ttu-id="0be95-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0be95-137">RELATED LINKS</span></span>
