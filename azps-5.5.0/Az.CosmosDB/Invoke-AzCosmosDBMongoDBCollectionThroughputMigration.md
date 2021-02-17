---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238543"
---
# <span data-ttu-id="dbfdd-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="dbfdd-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="dbfdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfdd-103">Используйте этот метод для переноса пропускной способности для автоматической передачи с ручной пропускной способностью и наоборот.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="dbfdd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbfdd-104">SYNTAX</span></span>

### <span data-ttu-id="dbfdd-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dbfdd-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfdd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbfdd-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfdd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbfdd-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbfdd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbfdd-108">DESCRIPTION</span></span>
<span data-ttu-id="dbfdd-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="dbfdd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbfdd-110">EXAMPLES</span></span>

### <span data-ttu-id="dbfdd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbfdd-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="dbfdd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbfdd-112">PARAMETERS</span></span>

### <span data-ttu-id="dbfdd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbfdd-113">-AccountName</span></span>
<span data-ttu-id="dbfdd-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="dbfdd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dbfdd-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbfdd-115">-Confirm</span></span>
<span data-ttu-id="dbfdd-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbfdd-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbfdd-117">-DatabaseName</span></span>
<span data-ttu-id="dbfdd-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-118">Database name.</span></span>

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

### <span data-ttu-id="dbfdd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfdd-119">-DefaultProfile</span></span>
<span data-ttu-id="dbfdd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbfdd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbfdd-121">-InputObject</span></span>
<span data-ttu-id="dbfdd-122">Объект Коллекции Mongo.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfdd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dbfdd-123">-Name</span></span>
<span data-ttu-id="dbfdd-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-124">Collection name.</span></span>

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

### <span data-ttu-id="dbfdd-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbfdd-125">-ParentObject</span></span>
<span data-ttu-id="dbfdd-126">Объект базы данных Пнго.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfdd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbfdd-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbfdd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dbfdd-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="dbfdd-129">-ThroughputType</span></span>
<span data-ttu-id="dbfdd-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="dbfdd-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="dbfdd-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="dbfdd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbfdd-132">-WhatIf</span></span>
<span data-ttu-id="dbfdd-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbfdd-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbfdd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfdd-135">CommonParameters</span></span>
<span data-ttu-id="dbfdd-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfdd-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbfdd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfdd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbfdd-138">INPUTS</span></span>

### <span data-ttu-id="dbfdd-139">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="dbfdd-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="dbfdd-140">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="dbfdd-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="dbfdd-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbfdd-141">OUTPUTS</span></span>

### <span data-ttu-id="dbfdd-142">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dbfdd-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dbfdd-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbfdd-143">NOTES</span></span>

## <span data-ttu-id="dbfdd-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbfdd-144">RELATED LINKS</span></span>
