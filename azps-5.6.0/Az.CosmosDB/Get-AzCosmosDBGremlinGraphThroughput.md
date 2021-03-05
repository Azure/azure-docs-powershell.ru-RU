---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983619"
---
# <span data-ttu-id="0afb3-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="0afb3-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="0afb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afb3-102">SYNOPSIS</span></span>
<span data-ttu-id="0afb3-103">Получает пропускную способность Диаграммы Гремлина ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="0afb3-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0afb3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0afb3-104">SYNTAX</span></span>

### <span data-ttu-id="0afb3-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0afb3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afb3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0afb3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afb3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0afb3-107">DESCRIPTION</span></span>
<span data-ttu-id="0afb3-108">С **помощью cmdlet get-AzCosmosDBGremlinGraphThroughput** можно получить пропускную способность РегинаDb Гремлин Graph.</span><span class="sxs-lookup"><span data-stu-id="0afb3-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0afb3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0afb3-109">EXAMPLES</span></span>

### <span data-ttu-id="0afb3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0afb3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0afb3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afb3-111">PARAMETERS</span></span>

### <span data-ttu-id="0afb3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0afb3-112">-AccountName</span></span>
<span data-ttu-id="0afb3-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="0afb3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0afb3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afb3-114">-Confirm</span></span>
<span data-ttu-id="0afb3-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afb3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afb3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0afb3-116">-DatabaseName</span></span>
<span data-ttu-id="0afb3-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0afb3-117">Database name.</span></span>

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

### <span data-ttu-id="0afb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afb3-118">-DefaultProfile</span></span>
<span data-ttu-id="0afb3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0afb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afb3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afb3-120">-InputObject</span></span>
<span data-ttu-id="0afb3-121">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="0afb3-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="0afb3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0afb3-122">-Name</span></span>
<span data-ttu-id="0afb3-123">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="0afb3-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0afb3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afb3-124">-ResourceGroupName</span></span>
<span data-ttu-id="0afb3-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0afb3-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0afb3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afb3-126">-WhatIf</span></span>
<span data-ttu-id="0afb3-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afb3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afb3-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0afb3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afb3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afb3-129">CommonParameters</span></span>
<span data-ttu-id="0afb3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afb3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afb3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0afb3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afb3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0afb3-132">INPUTS</span></span>

### <span data-ttu-id="0afb3-133">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="0afb3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="0afb3-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0afb3-134">OUTPUTS</span></span>

### <span data-ttu-id="0afb3-135">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0afb3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0afb3-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0afb3-136">NOTES</span></span>

## <span data-ttu-id="0afb3-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0afb3-137">RELATED LINKS</span></span>
