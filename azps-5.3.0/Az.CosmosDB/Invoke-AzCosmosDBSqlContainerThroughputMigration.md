---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508854"
---
# <span data-ttu-id="585cb-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="585cb-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="585cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="585cb-102">SYNOPSIS</span></span>
<span data-ttu-id="585cb-103">Используйте этот метод для переноса пропускной способности для автоматической передачи с ручной пропускной способностью и наоборот.</span><span class="sxs-lookup"><span data-stu-id="585cb-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="585cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="585cb-104">SYNTAX</span></span>

### <span data-ttu-id="585cb-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="585cb-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="585cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="585cb-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="585cb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="585cb-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="585cb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="585cb-108">DESCRIPTION</span></span>
<span data-ttu-id="585cb-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="585cb-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="585cb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="585cb-110">EXAMPLES</span></span>

### <span data-ttu-id="585cb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="585cb-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="585cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="585cb-112">PARAMETERS</span></span>

### <span data-ttu-id="585cb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="585cb-113">-AccountName</span></span>
<span data-ttu-id="585cb-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="585cb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="585cb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="585cb-115">-Confirm</span></span>
<span data-ttu-id="585cb-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="585cb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585cb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="585cb-117">-DatabaseName</span></span>
<span data-ttu-id="585cb-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="585cb-118">Database name.</span></span>

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

### <span data-ttu-id="585cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585cb-119">-DefaultProfile</span></span>
<span data-ttu-id="585cb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="585cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="585cb-121">-InputObject</span></span>
<span data-ttu-id="585cb-122">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="585cb-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="585cb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="585cb-123">-Name</span></span>
<span data-ttu-id="585cb-124">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="585cb-124">Container name.</span></span>

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

### <span data-ttu-id="585cb-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="585cb-125">-ParentObject</span></span>
<span data-ttu-id="585cb-126">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="585cb-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="585cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="585cb-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="585cb-128">Name of resource group.</span></span>

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

### <span data-ttu-id="585cb-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="585cb-129">-ThroughputType</span></span>
<span data-ttu-id="585cb-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="585cb-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="585cb-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="585cb-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="585cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585cb-132">-WhatIf</span></span>
<span data-ttu-id="585cb-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="585cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="585cb-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="585cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="585cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585cb-135">CommonParameters</span></span>
<span data-ttu-id="585cb-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585cb-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="585cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585cb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="585cb-138">INPUTS</span></span>

### <span data-ttu-id="585cb-139">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="585cb-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="585cb-140">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="585cb-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="585cb-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="585cb-141">OUTPUTS</span></span>

### <span data-ttu-id="585cb-142">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="585cb-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="585cb-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="585cb-143">NOTES</span></span>

## <span data-ttu-id="585cb-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="585cb-144">RELATED LINKS</span></span>
