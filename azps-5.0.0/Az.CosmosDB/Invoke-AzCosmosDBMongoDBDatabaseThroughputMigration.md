---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314933"
---
# <span data-ttu-id="211e9-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="211e9-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="211e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="211e9-102">SYNOPSIS</span></span>
<span data-ttu-id="211e9-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="211e9-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="211e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="211e9-104">SYNTAX</span></span>

### <span data-ttu-id="211e9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="211e9-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="211e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="211e9-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211e9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="211e9-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211e9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="211e9-108">DESCRIPTION</span></span>
<span data-ttu-id="211e9-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="211e9-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="211e9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="211e9-110">EXAMPLES</span></span>

### <span data-ttu-id="211e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="211e9-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="211e9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="211e9-112">PARAMETERS</span></span>

### <span data-ttu-id="211e9-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="211e9-113">-AccountName</span></span>
<span data-ttu-id="211e9-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="211e9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="211e9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="211e9-115">-Confirm</span></span>
<span data-ttu-id="211e9-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="211e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211e9-117">-DefaultProfile</span></span>
<span data-ttu-id="211e9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="211e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="211e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="211e9-119">-InputObject</span></span>
<span data-ttu-id="211e9-120">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="211e9-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="211e9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="211e9-121">-Name</span></span>
<span data-ttu-id="211e9-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="211e9-122">Database name.</span></span>

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

### <span data-ttu-id="211e9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="211e9-123">-ParentObject</span></span>
<span data-ttu-id="211e9-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="211e9-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="211e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="211e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="211e9-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="211e9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="211e9-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="211e9-127">-ThroughputType</span></span>
<span data-ttu-id="211e9-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="211e9-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="211e9-129">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="211e9-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="211e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211e9-130">-WhatIf</span></span>
<span data-ttu-id="211e9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="211e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="211e9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="211e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211e9-133">CommonParameters</span></span>
<span data-ttu-id="211e9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="211e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211e9-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211e9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="211e9-136">INPUTS</span></span>

### <span data-ttu-id="211e9-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="211e9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="211e9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="211e9-138">OUTPUTS</span></span>

### <span data-ttu-id="211e9-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="211e9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="211e9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="211e9-140">NOTES</span></span>

## <span data-ttu-id="211e9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="211e9-141">RELATED LINKS</span></span>
