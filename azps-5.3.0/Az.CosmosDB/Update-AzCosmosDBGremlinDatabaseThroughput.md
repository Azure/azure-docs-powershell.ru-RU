---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508730"
---
# <span data-ttu-id="57773-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="57773-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="57773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57773-102">SYNOPSIS</span></span>
<span data-ttu-id="57773-103">Обновляет значение пропускной способности базы данных ВайсDB Гремлин.</span><span class="sxs-lookup"><span data-stu-id="57773-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="57773-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57773-104">SYNTAX</span></span>

### <span data-ttu-id="57773-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57773-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57773-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57773-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57773-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57773-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57773-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57773-108">DESCRIPTION</span></span>
<span data-ttu-id="57773-109">Обновляет значение пропускной способности базы данных ВайсDB Гремлин.</span><span class="sxs-lookup"><span data-stu-id="57773-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="57773-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57773-110">EXAMPLES</span></span>

### <span data-ttu-id="57773-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57773-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="57773-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57773-112">PARAMETERS</span></span>

### <span data-ttu-id="57773-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57773-113">-AccountName</span></span>
<span data-ttu-id="57773-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="57773-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57773-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="57773-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="57773-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="57773-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="57773-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57773-117">-Confirm</span></span>
<span data-ttu-id="57773-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="57773-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57773-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57773-119">-DefaultProfile</span></span>
<span data-ttu-id="57773-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57773-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57773-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57773-121">-InputObject</span></span>
<span data-ttu-id="57773-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="57773-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57773-123">-Name</span><span class="sxs-lookup"><span data-stu-id="57773-123">-Name</span></span>
<span data-ttu-id="57773-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="57773-124">Database name.</span></span>

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

### <span data-ttu-id="57773-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57773-125">-ParentObject</span></span>
<span data-ttu-id="57773-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="57773-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="57773-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57773-127">-ResourceGroupName</span></span>
<span data-ttu-id="57773-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57773-128">Name of resource group.</span></span>

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

### <span data-ttu-id="57773-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="57773-129">-Throughput</span></span>
<span data-ttu-id="57773-130">Пропускная способность базы данных Гремлин (RU/s).</span><span class="sxs-lookup"><span data-stu-id="57773-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="57773-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="57773-131">Default value is 400.</span></span>

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

### <span data-ttu-id="57773-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57773-132">-WhatIf</span></span>
<span data-ttu-id="57773-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57773-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57773-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57773-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57773-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57773-135">CommonParameters</span></span>
<span data-ttu-id="57773-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57773-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57773-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57773-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57773-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57773-138">INPUTS</span></span>

### <span data-ttu-id="57773-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="57773-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="57773-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57773-140">OUTPUTS</span></span>

### <span data-ttu-id="57773-141">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="57773-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="57773-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57773-142">NOTES</span></span>

## <span data-ttu-id="57773-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57773-143">RELATED LINKS</span></span>