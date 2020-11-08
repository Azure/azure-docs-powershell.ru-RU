---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242554"
---
# <span data-ttu-id="98db8-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="98db8-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="98db8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98db8-102">SYNOPSIS</span></span>
<span data-ttu-id="98db8-103">Обновляет базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="98db8-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="98db8-104">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="98db8-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="98db8-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98db8-105">SYNTAX</span></span>

### <span data-ttu-id="98db8-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98db8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98db8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98db8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98db8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98db8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98db8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98db8-109">DESCRIPTION</span></span>
<span data-ttu-id="98db8-110">Обновляет базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="98db8-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="98db8-111">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="98db8-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="98db8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98db8-112">EXAMPLES</span></span>

### <span data-ttu-id="98db8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98db8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="98db8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98db8-114">PARAMETERS</span></span>

### <span data-ttu-id="98db8-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="98db8-115">-AccountName</span></span>
<span data-ttu-id="98db8-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="98db8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="98db8-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="98db8-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="98db8-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="98db8-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98db8-119">-Confirm</span></span>
<span data-ttu-id="98db8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98db8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98db8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98db8-121">-DefaultProfile</span></span>
<span data-ttu-id="98db8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98db8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98db8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98db8-123">-InputObject</span></span>
<span data-ttu-id="98db8-124">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="98db8-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="98db8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98db8-125">-Name</span></span>
<span data-ttu-id="98db8-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="98db8-126">Database name.</span></span>

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

### <span data-ttu-id="98db8-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="98db8-127">-ParentObject</span></span>
<span data-ttu-id="98db8-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="98db8-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="98db8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98db8-129">-ResourceGroupName</span></span>
<span data-ttu-id="98db8-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98db8-130">Name of resource group.</span></span>

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

### <span data-ttu-id="98db8-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="98db8-131">-Throughput</span></span>
<span data-ttu-id="98db8-132">Пропускная способность Gremlin базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="98db8-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="98db8-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="98db8-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98db8-134">-WhatIf</span></span>
<span data-ttu-id="98db8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98db8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98db8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98db8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98db8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98db8-137">CommonParameters</span></span>
<span data-ttu-id="98db8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98db8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98db8-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98db8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98db8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98db8-140">INPUTS</span></span>

### <span data-ttu-id="98db8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="98db8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="98db8-142">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="98db8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="98db8-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98db8-143">OUTPUTS</span></span>

### <span data-ttu-id="98db8-144">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="98db8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="98db8-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="98db8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="98db8-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="98db8-146">NOTES</span></span>

## <span data-ttu-id="98db8-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98db8-147">RELATED LINKS</span></span>
