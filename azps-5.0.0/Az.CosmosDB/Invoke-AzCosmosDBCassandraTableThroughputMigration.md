---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314951"
---
# <span data-ttu-id="97ad4-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="97ad4-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="97ad4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="97ad4-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="97ad4-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="97ad4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97ad4-104">SYNTAX</span></span>

### <span data-ttu-id="97ad4-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97ad4-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ad4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97ad4-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ad4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97ad4-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97ad4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="97ad4-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="97ad4-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="97ad4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="97ad4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97ad4-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="97ad4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97ad4-112">PARAMETERS</span></span>

### <span data-ttu-id="97ad4-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="97ad4-113">-AccountName</span></span>
<span data-ttu-id="97ad4-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="97ad4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="97ad4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97ad4-115">-Confirm</span></span>
<span data-ttu-id="97ad4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97ad4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ad4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ad4-117">-DefaultProfile</span></span>
<span data-ttu-id="97ad4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97ad4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ad4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ad4-119">-InputObject</span></span>
<span data-ttu-id="97ad4-120">Объект таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="97ad4-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="97ad4-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="97ad4-121">-KeyspaceName</span></span>
<span data-ttu-id="97ad4-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="97ad4-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="97ad4-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97ad4-123">-Name</span></span>
<span data-ttu-id="97ad4-124">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="97ad4-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="97ad4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="97ad4-125">-ParentObject</span></span>
<span data-ttu-id="97ad4-126">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="97ad4-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="97ad4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ad4-127">-ResourceGroupName</span></span>
<span data-ttu-id="97ad4-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97ad4-128">Name of resource group.</span></span>

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

### <span data-ttu-id="97ad4-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="97ad4-129">-ThroughputType</span></span>
<span data-ttu-id="97ad4-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="97ad4-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="97ad4-131">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="97ad4-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="97ad4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ad4-132">-WhatIf</span></span>
<span data-ttu-id="97ad4-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97ad4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ad4-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97ad4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ad4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ad4-135">CommonParameters</span></span>
<span data-ttu-id="97ad4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97ad4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ad4-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97ad4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ad4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97ad4-138">INPUTS</span></span>

### <span data-ttu-id="97ad4-139">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="97ad4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="97ad4-140">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="97ad4-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="97ad4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ad4-141">OUTPUTS</span></span>

### <span data-ttu-id="97ad4-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="97ad4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="97ad4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="97ad4-143">NOTES</span></span>

## <span data-ttu-id="97ad4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97ad4-144">RELATED LINKS</span></span>
