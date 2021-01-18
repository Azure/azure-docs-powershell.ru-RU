---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519321"
---
# <span data-ttu-id="bd375-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="bd375-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="bd375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd375-102">SYNOPSIS</span></span>
<span data-ttu-id="bd375-103">Используйте этот метод для переноса пропускной способности для автоматической передачи по шкале, которая передается вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="bd375-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="bd375-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd375-104">SYNTAX</span></span>

### <span data-ttu-id="bd375-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd375-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd375-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd375-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd375-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd375-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd375-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd375-108">DESCRIPTION</span></span>
<span data-ttu-id="bd375-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="bd375-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="bd375-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd375-110">EXAMPLES</span></span>

### <span data-ttu-id="bd375-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd375-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="bd375-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd375-112">PARAMETERS</span></span>

### <span data-ttu-id="bd375-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd375-113">-AccountName</span></span>
<span data-ttu-id="bd375-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="bd375-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd375-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd375-115">-Confirm</span></span>
<span data-ttu-id="bd375-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bd375-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd375-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd375-117">-DatabaseName</span></span>
<span data-ttu-id="bd375-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd375-118">Database name.</span></span>

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

### <span data-ttu-id="bd375-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd375-119">-DefaultProfile</span></span>
<span data-ttu-id="bd375-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd375-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd375-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd375-121">-InputObject</span></span>
<span data-ttu-id="bd375-122">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="bd375-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="bd375-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bd375-123">-Name</span></span>
<span data-ttu-id="bd375-124">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="bd375-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="bd375-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd375-125">-ParentObject</span></span>
<span data-ttu-id="bd375-126">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="bd375-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="bd375-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd375-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd375-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd375-128">Name of resource group.</span></span>

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

### <span data-ttu-id="bd375-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="bd375-129">-ThroughputType</span></span>
<span data-ttu-id="bd375-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="bd375-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="bd375-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="bd375-131">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd375-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd375-132">-WhatIf</span></span>
<span data-ttu-id="bd375-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd375-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd375-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd375-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd375-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd375-135">CommonParameters</span></span>
<span data-ttu-id="bd375-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd375-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd375-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd375-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd375-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd375-138">INPUTS</span></span>

### <span data-ttu-id="bd375-139">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd375-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="bd375-140">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="bd375-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="bd375-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd375-141">OUTPUTS</span></span>

### <span data-ttu-id="bd375-142">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bd375-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bd375-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd375-143">NOTES</span></span>

## <span data-ttu-id="bd375-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd375-144">RELATED LINKS</span></span>
