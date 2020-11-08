---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242568"
---
# <span data-ttu-id="52e4c-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="52e4c-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="52e4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="52e4c-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="52e4c-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="52e4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52e4c-104">SYNTAX</span></span>

### <span data-ttu-id="52e4c-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52e4c-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52e4c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52e4c-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e4c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52e4c-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e4c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="52e4c-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="52e4c-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="52e4c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52e4c-110">EXAMPLES</span></span>

### <span data-ttu-id="52e4c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52e4c-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="52e4c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52e4c-112">PARAMETERS</span></span>

### <span data-ttu-id="52e4c-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="52e4c-113">-AccountName</span></span>
<span data-ttu-id="52e4c-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="52e4c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52e4c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52e4c-115">-Confirm</span></span>
<span data-ttu-id="52e4c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52e4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e4c-117">-DefaultProfile</span></span>
<span data-ttu-id="52e4c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52e4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52e4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52e4c-119">-InputObject</span></span>
<span data-ttu-id="52e4c-120">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="52e4c-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="52e4c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52e4c-121">-Name</span></span>
<span data-ttu-id="52e4c-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="52e4c-122">Database name.</span></span>

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

### <span data-ttu-id="52e4c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52e4c-123">-ParentObject</span></span>
<span data-ttu-id="52e4c-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="52e4c-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="52e4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="52e4c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52e4c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="52e4c-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="52e4c-127">-ThroughputType</span></span>
<span data-ttu-id="52e4c-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="52e4c-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="52e4c-129">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="52e4c-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="52e4c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e4c-130">-WhatIf</span></span>
<span data-ttu-id="52e4c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52e4c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52e4c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52e4c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e4c-133">CommonParameters</span></span>
<span data-ttu-id="52e4c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52e4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e4c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52e4c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e4c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52e4c-136">INPUTS</span></span>

### <span data-ttu-id="52e4c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="52e4c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="52e4c-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="52e4c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="52e4c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52e4c-139">OUTPUTS</span></span>

### <span data-ttu-id="52e4c-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="52e4c-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="52e4c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="52e4c-141">NOTES</span></span>

## <span data-ttu-id="52e4c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52e4c-142">RELATED LINKS</span></span>
