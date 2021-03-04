---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990338"
---
# <span data-ttu-id="dc0b4-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="dc0b4-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="dc0b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0b4-103">Используйте этот метод для переноса пропускной способности для передачи автоматических по шкале, чтобы перенести ее вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="dc0b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc0b4-104">SYNTAX</span></span>

### <span data-ttu-id="dc0b4-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc0b4-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0b4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0b4-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0b4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0b4-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0b4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc0b4-108">DESCRIPTION</span></span>
<span data-ttu-id="dc0b4-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="dc0b4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc0b4-110">EXAMPLES</span></span>

### <span data-ttu-id="dc0b4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc0b4-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="dc0b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc0b4-112">PARAMETERS</span></span>

### <span data-ttu-id="dc0b4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc0b4-113">-AccountName</span></span>
<span data-ttu-id="dc0b4-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="dc0b4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc0b4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc0b4-115">-Confirm</span></span>
<span data-ttu-id="dc0b4-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0b4-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc0b4-117">-DatabaseName</span></span>
<span data-ttu-id="dc0b4-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-118">Database name.</span></span>

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

### <span data-ttu-id="dc0b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0b4-119">-DefaultProfile</span></span>
<span data-ttu-id="dc0b4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc0b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0b4-121">-InputObject</span></span>
<span data-ttu-id="dc0b4-122">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="dc0b4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dc0b4-123">-Name</span></span>
<span data-ttu-id="dc0b4-124">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="dc0b4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc0b4-125">-ParentObject</span></span>
<span data-ttu-id="dc0b4-126">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="dc0b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc0b4-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dc0b4-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="dc0b4-129">-ThroughputType</span></span>
<span data-ttu-id="dc0b4-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="dc0b4-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="dc0b4-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="dc0b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0b4-132">-WhatIf</span></span>
<span data-ttu-id="dc0b4-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0b4-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0b4-135">CommonParameters</span></span>
<span data-ttu-id="dc0b4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0b4-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc0b4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0b4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc0b4-138">INPUTS</span></span>

### <span data-ttu-id="dc0b4-139">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="dc0b4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="dc0b4-140">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="dc0b4-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="dc0b4-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc0b4-141">OUTPUTS</span></span>

### <span data-ttu-id="dc0b4-142">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dc0b4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc0b4-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc0b4-143">NOTES</span></span>

## <span data-ttu-id="dc0b4-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc0b4-144">RELATED LINKS</span></span>
