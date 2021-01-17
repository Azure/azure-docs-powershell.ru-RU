---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411479"
---
# <span data-ttu-id="d51a1-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d51a1-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="d51a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d51a1-103">Используйте этот метод для переноса пропускной способности для автоматической передачи по шкале, которая передается вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="d51a1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d51a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d51a1-104">SYNTAX</span></span>

### <span data-ttu-id="d51a1-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d51a1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51a1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d51a1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51a1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d51a1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d51a1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d51a1-108">DESCRIPTION</span></span>
<span data-ttu-id="d51a1-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="d51a1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d51a1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d51a1-110">EXAMPLES</span></span>

### <span data-ttu-id="d51a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d51a1-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="d51a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d51a1-112">PARAMETERS</span></span>

### <span data-ttu-id="d51a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d51a1-113">-AccountName</span></span>
<span data-ttu-id="d51a1-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="d51a1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d51a1-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d51a1-115">-Confirm</span></span>
<span data-ttu-id="d51a1-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d51a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51a1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d51a1-117">-DatabaseName</span></span>
<span data-ttu-id="d51a1-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d51a1-118">Database name.</span></span>

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

### <span data-ttu-id="d51a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51a1-119">-DefaultProfile</span></span>
<span data-ttu-id="d51a1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d51a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d51a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d51a1-121">-InputObject</span></span>
<span data-ttu-id="d51a1-122">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="d51a1-122">Sql Container object.</span></span>

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

### <span data-ttu-id="d51a1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d51a1-123">-Name</span></span>
<span data-ttu-id="d51a1-124">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="d51a1-124">Container name.</span></span>

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

### <span data-ttu-id="d51a1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d51a1-125">-ParentObject</span></span>
<span data-ttu-id="d51a1-126">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="d51a1-126">Sql Database object.</span></span>

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

### <span data-ttu-id="d51a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d51a1-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d51a1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d51a1-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d51a1-129">-ThroughputType</span></span>
<span data-ttu-id="d51a1-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="d51a1-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="d51a1-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="d51a1-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d51a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51a1-132">-WhatIf</span></span>
<span data-ttu-id="d51a1-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51a1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51a1-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d51a1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51a1-135">CommonParameters</span></span>
<span data-ttu-id="d51a1-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51a1-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d51a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51a1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d51a1-138">INPUTS</span></span>

### <span data-ttu-id="d51a1-139">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d51a1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d51a1-140">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d51a1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="d51a1-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d51a1-141">OUTPUTS</span></span>

### <span data-ttu-id="d51a1-142">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d51a1-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d51a1-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d51a1-143">NOTES</span></span>

## <span data-ttu-id="d51a1-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d51a1-144">RELATED LINKS</span></span>
