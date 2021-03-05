---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: bbe2cc26eb5f57e31457023285d8f27a1d326321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972899"
---
# <span data-ttu-id="76763-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="76763-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="76763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76763-102">SYNOPSIS</span></span>
<span data-ttu-id="76763-103">Используйте этот метод для переноса пропускной способности для передачи автоматических по шкале, чтобы перенести ее вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="76763-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="76763-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76763-104">SYNTAX</span></span>

### <span data-ttu-id="76763-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76763-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76763-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76763-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76763-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76763-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76763-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76763-108">DESCRIPTION</span></span>
<span data-ttu-id="76763-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="76763-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="76763-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76763-110">EXAMPLES</span></span>

### <span data-ttu-id="76763-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76763-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="76763-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76763-112">PARAMETERS</span></span>

### <span data-ttu-id="76763-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76763-113">-AccountName</span></span>
<span data-ttu-id="76763-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="76763-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="76763-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76763-115">-Confirm</span></span>
<span data-ttu-id="76763-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76763-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76763-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76763-117">-DefaultProfile</span></span>
<span data-ttu-id="76763-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76763-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76763-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76763-119">-InputObject</span></span>
<span data-ttu-id="76763-120">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="76763-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="76763-121">-Name</span><span class="sxs-lookup"><span data-stu-id="76763-121">-Name</span></span>
<span data-ttu-id="76763-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="76763-122">Database name.</span></span>

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

### <span data-ttu-id="76763-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="76763-123">-ParentObject</span></span>
<span data-ttu-id="76763-124">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="76763-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="76763-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76763-125">-ResourceGroupName</span></span>
<span data-ttu-id="76763-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76763-126">Name of resource group.</span></span>

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

### <span data-ttu-id="76763-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="76763-127">-ThroughputType</span></span>
<span data-ttu-id="76763-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="76763-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="76763-129">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="76763-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="76763-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76763-130">-WhatIf</span></span>
<span data-ttu-id="76763-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76763-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76763-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76763-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76763-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76763-133">CommonParameters</span></span>
<span data-ttu-id="76763-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76763-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76763-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76763-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76763-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76763-136">INPUTS</span></span>

### <span data-ttu-id="76763-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="76763-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="76763-138">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="76763-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="76763-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76763-139">OUTPUTS</span></span>

### <span data-ttu-id="76763-140">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="76763-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="76763-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76763-141">NOTES</span></span>

## <span data-ttu-id="76763-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76763-142">RELATED LINKS</span></span>
