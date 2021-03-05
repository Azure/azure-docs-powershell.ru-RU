---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 65b1cbaebdf4118b5e22a7d1f9672273281ba55b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992830"
---
# <span data-ttu-id="007c5-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="007c5-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="007c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="007c5-102">SYNOPSIS</span></span>
<span data-ttu-id="007c5-103">Используйте этот метод для переноса пропускной способности для автоматической передачи по шкале, которая передается вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="007c5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="007c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="007c5-104">SYNTAX</span></span>

### <span data-ttu-id="007c5-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="007c5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007c5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="007c5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="007c5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007c5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="007c5-108">DESCRIPTION</span></span>
<span data-ttu-id="007c5-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="007c5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="007c5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="007c5-110">EXAMPLES</span></span>

### <span data-ttu-id="007c5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="007c5-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="007c5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="007c5-112">PARAMETERS</span></span>

### <span data-ttu-id="007c5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="007c5-113">-AccountName</span></span>
<span data-ttu-id="007c5-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="007c5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="007c5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="007c5-115">-Confirm</span></span>
<span data-ttu-id="007c5-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="007c5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007c5-117">-DefaultProfile</span></span>
<span data-ttu-id="007c5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="007c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007c5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="007c5-119">-InputObject</span></span>
<span data-ttu-id="007c5-120">Объект "Таблица" Вадима.</span><span class="sxs-lookup"><span data-stu-id="007c5-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007c5-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="007c5-121">-KeyspaceName</span></span>
<span data-ttu-id="007c5-122">Имя клавишНой области Александры.</span><span class="sxs-lookup"><span data-stu-id="007c5-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="007c5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="007c5-123">-Name</span></span>
<span data-ttu-id="007c5-124">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="007c5-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="007c5-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="007c5-125">-ParentObject</span></span>
<span data-ttu-id="007c5-126">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="007c5-126">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007c5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007c5-127">-ResourceGroupName</span></span>
<span data-ttu-id="007c5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="007c5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="007c5-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="007c5-129">-ThroughputType</span></span>
<span data-ttu-id="007c5-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="007c5-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="007c5-131">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="007c5-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="007c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007c5-132">-WhatIf</span></span>
<span data-ttu-id="007c5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="007c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007c5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="007c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007c5-135">CommonParameters</span></span>
<span data-ttu-id="007c5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007c5-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="007c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007c5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="007c5-138">INPUTS</span></span>

### <span data-ttu-id="007c5-139">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="007c5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="007c5-140">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="007c5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="007c5-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="007c5-141">OUTPUTS</span></span>

### <span data-ttu-id="007c5-142">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="007c5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="007c5-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="007c5-143">NOTES</span></span>

## <span data-ttu-id="007c5-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="007c5-144">RELATED LINKS</span></span>
