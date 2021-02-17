---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 15ee57c32d8eeeca996994900113360adac1c407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211377"
---
# <span data-ttu-id="187ae-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="187ae-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="187ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187ae-102">SYNOPSIS</span></span>
<span data-ttu-id="187ae-103">Используйте этот метод для переноса пропускной способности для автоматической передачи с ручной пропускной способностью и наоборот.</span><span class="sxs-lookup"><span data-stu-id="187ae-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="187ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="187ae-104">SYNTAX</span></span>

### <span data-ttu-id="187ae-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="187ae-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="187ae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187ae-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187ae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187ae-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187ae-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="187ae-108">DESCRIPTION</span></span>
<span data-ttu-id="187ae-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="187ae-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="187ae-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="187ae-110">EXAMPLES</span></span>

### <span data-ttu-id="187ae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="187ae-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="187ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="187ae-112">PARAMETERS</span></span>

### <span data-ttu-id="187ae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="187ae-113">-AccountName</span></span>
<span data-ttu-id="187ae-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="187ae-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="187ae-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="187ae-115">-Confirm</span></span>
<span data-ttu-id="187ae-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187ae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187ae-117">-DefaultProfile</span></span>
<span data-ttu-id="187ae-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="187ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187ae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="187ae-119">-InputObject</span></span>
<span data-ttu-id="187ae-120">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="187ae-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187ae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="187ae-121">-Name</span></span>
<span data-ttu-id="187ae-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="187ae-122">Database name.</span></span>

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

### <span data-ttu-id="187ae-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="187ae-123">-ParentObject</span></span>
<span data-ttu-id="187ae-124">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="187ae-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="187ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="187ae-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="187ae-126">Name of resource group.</span></span>

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

### <span data-ttu-id="187ae-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="187ae-127">-ThroughputType</span></span>
<span data-ttu-id="187ae-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="187ae-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="187ae-129">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="187ae-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="187ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187ae-130">-WhatIf</span></span>
<span data-ttu-id="187ae-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187ae-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="187ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187ae-133">CommonParameters</span></span>
<span data-ttu-id="187ae-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187ae-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="187ae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187ae-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="187ae-136">INPUTS</span></span>

### <span data-ttu-id="187ae-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="187ae-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="187ae-138">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="187ae-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="187ae-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="187ae-139">OUTPUTS</span></span>

### <span data-ttu-id="187ae-140">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="187ae-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="187ae-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="187ae-141">NOTES</span></span>

## <span data-ttu-id="187ae-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="187ae-142">RELATED LINKS</span></span>
