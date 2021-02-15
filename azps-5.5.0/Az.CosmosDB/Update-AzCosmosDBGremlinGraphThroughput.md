---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215321"
---
# <span data-ttu-id="bd310-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="bd310-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="bd310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd310-102">SYNOPSIS</span></span>
<span data-ttu-id="bd310-103">Обновляет значение пропускной способности Для Диаграммы Гремлина вбокDB.</span><span class="sxs-lookup"><span data-stu-id="bd310-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="bd310-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd310-104">SYNTAX</span></span>

### <span data-ttu-id="bd310-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd310-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd310-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd310-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd310-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd310-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd310-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd310-108">DESCRIPTION</span></span>
<span data-ttu-id="bd310-109">Обновляет значение пропускной способности Для Диаграммы Гремлина вбокDB.</span><span class="sxs-lookup"><span data-stu-id="bd310-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="bd310-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd310-110">EXAMPLES</span></span>

### <span data-ttu-id="bd310-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd310-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="bd310-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd310-112">PARAMETERS</span></span>

### <span data-ttu-id="bd310-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd310-113">-AccountName</span></span>
<span data-ttu-id="bd310-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="bd310-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd310-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bd310-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bd310-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="bd310-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bd310-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd310-117">-Confirm</span></span>
<span data-ttu-id="bd310-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd310-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd310-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd310-119">-DatabaseName</span></span>
<span data-ttu-id="bd310-120">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd310-120">Database name.</span></span>

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

### <span data-ttu-id="bd310-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd310-121">-DefaultProfile</span></span>
<span data-ttu-id="bd310-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd310-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd310-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd310-123">-InputObject</span></span>
<span data-ttu-id="bd310-124">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="bd310-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="bd310-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd310-125">-Name</span></span>
<span data-ttu-id="bd310-126">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="bd310-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="bd310-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd310-127">-ParentObject</span></span>
<span data-ttu-id="bd310-128">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="bd310-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="bd310-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd310-129">-ResourceGroupName</span></span>
<span data-ttu-id="bd310-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd310-130">Name of resource group.</span></span>

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

### <span data-ttu-id="bd310-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="bd310-131">-Throughput</span></span>
<span data-ttu-id="bd310-132">Пропускная способность Гремлин Графа (RU/s).</span><span class="sxs-lookup"><span data-stu-id="bd310-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="bd310-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="bd310-133">Default value is 400.</span></span>

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

### <span data-ttu-id="bd310-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd310-134">-WhatIf</span></span>
<span data-ttu-id="bd310-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd310-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd310-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd310-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd310-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd310-137">CommonParameters</span></span>
<span data-ttu-id="bd310-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd310-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd310-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd310-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd310-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd310-140">INPUTS</span></span>

### <span data-ttu-id="bd310-141">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd310-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="bd310-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd310-142">OUTPUTS</span></span>

### <span data-ttu-id="bd310-143">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bd310-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bd310-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd310-144">NOTES</span></span>

## <span data-ttu-id="bd310-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd310-145">RELATED LINKS</span></span>
