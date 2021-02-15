---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215361"
---
# <span data-ttu-id="46f79-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="46f79-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="46f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f79-102">SYNOPSIS</span></span>
<span data-ttu-id="46f79-103">Обновляет базу данных "ГрадсDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="46f79-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="46f79-104">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="46f79-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="46f79-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46f79-105">SYNTAX</span></span>

### <span data-ttu-id="46f79-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46f79-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f79-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f79-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46f79-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f79-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46f79-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f79-109">DESCRIPTION</span></span>
<span data-ttu-id="46f79-110">Обновляет базу данных "ГрадсDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="46f79-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="46f79-111">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="46f79-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="46f79-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46f79-112">EXAMPLES</span></span>

### <span data-ttu-id="46f79-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46f79-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="46f79-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f79-114">PARAMETERS</span></span>

### <span data-ttu-id="46f79-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46f79-115">-AccountName</span></span>
<span data-ttu-id="46f79-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="46f79-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46f79-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="46f79-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="46f79-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="46f79-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="46f79-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46f79-119">-Confirm</span></span>
<span data-ttu-id="46f79-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46f79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f79-121">-DefaultProfile</span></span>
<span data-ttu-id="46f79-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46f79-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f79-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46f79-123">-InputObject</span></span>
<span data-ttu-id="46f79-124">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="46f79-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="46f79-125">-Name</span><span class="sxs-lookup"><span data-stu-id="46f79-125">-Name</span></span>
<span data-ttu-id="46f79-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="46f79-126">Database name.</span></span>

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

### <span data-ttu-id="46f79-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46f79-127">-ParentObject</span></span>
<span data-ttu-id="46f79-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="46f79-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="46f79-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f79-129">-ResourceGroupName</span></span>
<span data-ttu-id="46f79-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46f79-130">Name of resource group.</span></span>

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

### <span data-ttu-id="46f79-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="46f79-131">-Throughput</span></span>
<span data-ttu-id="46f79-132">Пропускная способность базы данных Гремлин (RU/s).</span><span class="sxs-lookup"><span data-stu-id="46f79-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="46f79-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="46f79-133">Default value is 400.</span></span>

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

### <span data-ttu-id="46f79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f79-134">-WhatIf</span></span>
<span data-ttu-id="46f79-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46f79-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f79-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46f79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f79-137">CommonParameters</span></span>
<span data-ttu-id="46f79-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f79-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46f79-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f79-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46f79-140">INPUTS</span></span>

### <span data-ttu-id="46f79-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="46f79-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="46f79-142">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="46f79-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="46f79-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46f79-143">OUTPUTS</span></span>

### <span data-ttu-id="46f79-144">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="46f79-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="46f79-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="46f79-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="46f79-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46f79-146">NOTES</span></span>

## <span data-ttu-id="46f79-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46f79-147">RELATED LINKS</span></span>
