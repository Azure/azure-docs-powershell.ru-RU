---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245091"
---
# <span data-ttu-id="01666-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="01666-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="01666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01666-102">SYNOPSIS</span></span>
<span data-ttu-id="01666-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="01666-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="01666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01666-104">SYNTAX</span></span>

### <span data-ttu-id="01666-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01666-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01666-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01666-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01666-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01666-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01666-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01666-108">DESCRIPTION</span></span>
<span data-ttu-id="01666-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="01666-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="01666-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01666-110">EXAMPLES</span></span>

### <span data-ttu-id="01666-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01666-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="01666-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01666-112">PARAMETERS</span></span>

### <span data-ttu-id="01666-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="01666-113">-AccountName</span></span>
<span data-ttu-id="01666-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="01666-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01666-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01666-115">-Confirm</span></span>
<span data-ttu-id="01666-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01666-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01666-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01666-117">-DatabaseName</span></span>
<span data-ttu-id="01666-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="01666-118">Database name.</span></span>

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

### <span data-ttu-id="01666-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01666-119">-DefaultProfile</span></span>
<span data-ttu-id="01666-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01666-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01666-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01666-121">-InputObject</span></span>
<span data-ttu-id="01666-122">Объект Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="01666-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="01666-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01666-123">-Name</span></span>
<span data-ttu-id="01666-124">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="01666-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="01666-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01666-125">-ParentObject</span></span>
<span data-ttu-id="01666-126">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="01666-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="01666-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01666-127">-ResourceGroupName</span></span>
<span data-ttu-id="01666-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01666-128">Name of resource group.</span></span>

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

### <span data-ttu-id="01666-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="01666-129">-ThroughputType</span></span>
<span data-ttu-id="01666-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="01666-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="01666-131">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="01666-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="01666-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01666-132">-WhatIf</span></span>
<span data-ttu-id="01666-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01666-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01666-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01666-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01666-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01666-135">CommonParameters</span></span>
<span data-ttu-id="01666-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01666-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01666-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01666-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01666-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01666-138">INPUTS</span></span>

### <span data-ttu-id="01666-139">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01666-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="01666-140">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="01666-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="01666-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01666-141">OUTPUTS</span></span>

### <span data-ttu-id="01666-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="01666-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="01666-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="01666-143">NOTES</span></span>

## <span data-ttu-id="01666-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01666-144">RELATED LINKS</span></span>
