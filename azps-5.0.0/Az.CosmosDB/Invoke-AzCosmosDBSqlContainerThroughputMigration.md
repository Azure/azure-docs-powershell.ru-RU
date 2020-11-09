---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314930"
---
# <span data-ttu-id="efd86-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="efd86-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="efd86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efd86-102">SYNOPSIS</span></span>
<span data-ttu-id="efd86-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="efd86-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="efd86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efd86-104">SYNTAX</span></span>

### <span data-ttu-id="efd86-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efd86-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efd86-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd86-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efd86-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd86-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efd86-108">DESCRIPTION</span></span>
<span data-ttu-id="efd86-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="efd86-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="efd86-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efd86-110">EXAMPLES</span></span>

### <span data-ttu-id="efd86-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="efd86-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="efd86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efd86-112">PARAMETERS</span></span>

### <span data-ttu-id="efd86-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="efd86-113">-AccountName</span></span>
<span data-ttu-id="efd86-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="efd86-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="efd86-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efd86-115">-Confirm</span></span>
<span data-ttu-id="efd86-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="efd86-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd86-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="efd86-117">-DatabaseName</span></span>
<span data-ttu-id="efd86-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="efd86-118">Database name.</span></span>

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

### <span data-ttu-id="efd86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd86-119">-DefaultProfile</span></span>
<span data-ttu-id="efd86-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efd86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efd86-121">-InputObject</span></span>
<span data-ttu-id="efd86-122">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="efd86-122">Sql Container object.</span></span>

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

### <span data-ttu-id="efd86-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efd86-123">-Name</span></span>
<span data-ttu-id="efd86-124">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="efd86-124">Container name.</span></span>

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

### <span data-ttu-id="efd86-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="efd86-125">-ParentObject</span></span>
<span data-ttu-id="efd86-126">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="efd86-126">Sql Database object.</span></span>

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

### <span data-ttu-id="efd86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd86-127">-ResourceGroupName</span></span>
<span data-ttu-id="efd86-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efd86-128">Name of resource group.</span></span>

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

### <span data-ttu-id="efd86-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="efd86-129">-ThroughputType</span></span>
<span data-ttu-id="efd86-130">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="efd86-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="efd86-131">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="efd86-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="efd86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd86-132">-WhatIf</span></span>
<span data-ttu-id="efd86-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="efd86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd86-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="efd86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd86-135">CommonParameters</span></span>
<span data-ttu-id="efd86-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efd86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd86-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efd86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd86-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efd86-138">INPUTS</span></span>

### <span data-ttu-id="efd86-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="efd86-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="efd86-140">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="efd86-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="efd86-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efd86-141">OUTPUTS</span></span>

### <span data-ttu-id="efd86-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="efd86-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="efd86-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="efd86-143">NOTES</span></span>

## <span data-ttu-id="efd86-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efd86-144">RELATED LINKS</span></span>
