---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244199"
---
# <span data-ttu-id="5dcc6-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="5dcc6-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="5dcc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dcc6-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcc6-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="5dcc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dcc6-104">SYNTAX</span></span>

### <span data-ttu-id="5dcc6-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5dcc6-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dcc6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dcc6-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dcc6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dcc6-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dcc6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dcc6-108">DESCRIPTION</span></span>
<span data-ttu-id="5dcc6-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="5dcc6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dcc6-110">EXAMPLES</span></span>

### <span data-ttu-id="5dcc6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5dcc6-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="5dcc6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dcc6-112">PARAMETERS</span></span>

### <span data-ttu-id="5dcc6-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5dcc6-113">-AccountName</span></span>
<span data-ttu-id="5dcc6-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5dcc6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dcc6-115">-Confirm</span></span>
<span data-ttu-id="5dcc6-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dcc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcc6-117">-DefaultProfile</span></span>
<span data-ttu-id="5dcc6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dcc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dcc6-119">-InputObject</span></span>
<span data-ttu-id="5dcc6-120">Объект Cassandra keyspace.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcc6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5dcc6-121">-Name</span></span>
<span data-ttu-id="5dcc6-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5dcc6-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5dcc6-123">-ParentObject</span></span>
<span data-ttu-id="5dcc6-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5dcc6-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5dcc6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dcc6-125">-ResourceGroupName</span></span>
<span data-ttu-id="5dcc6-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5dcc6-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="5dcc6-127">-ThroughputType</span></span>
<span data-ttu-id="5dcc6-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="5dcc6-129">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="5dcc6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dcc6-130">-WhatIf</span></span>
<span data-ttu-id="5dcc6-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dcc6-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dcc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcc6-133">CommonParameters</span></span>
<span data-ttu-id="5dcc6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dcc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcc6-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dcc6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcc6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dcc6-136">INPUTS</span></span>

### <span data-ttu-id="5dcc6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="5dcc6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="5dcc6-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5dcc6-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5dcc6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dcc6-139">OUTPUTS</span></span>

### <span data-ttu-id="5dcc6-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5dcc6-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5dcc6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dcc6-141">NOTES</span></span>

## <span data-ttu-id="5dcc6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dcc6-142">RELATED LINKS</span></span>
